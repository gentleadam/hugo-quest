+++
title = 'Velit veniam in officia nulla'
date = 2023-02-15T10:00:00-07:00
draft = false
tags = ['red','green']
description = "Velit veniam in officia nulla adipisicing ut duis officia."
emoji = "👑"
+++

Anim eiusmod irure incididunt sint cupidatat. Incididunt irure irure irure nisi ipsum do ut quis fugiat consectetur proident cupidatat incididunt cillum. Dolore voluptate occaecat qui mollit laborum ullamco et. Ipsum laboris officia anim laboris culpa eiusmod ex magna ex cupidatat anim ipsum aute. Mollit aliquip occaecat qui sunt velit ut cupidatat reprehenderit enim sunt laborum. Velit veniam in officia nulla adipisicing ut duis officia.

Exercitation voluptate irure in irure tempor mollit Lorem nostrud ad officia. Velit id fugiat occaecat do tempor. Sit officia Lorem aliquip eu deserunt consectetur. Aute proident deserunt in nulla aliquip dolore ipsum Lorem ut cupidatat consectetur sit sint laborum. Esse cupidatat sit sint sunt tempor exercitation deserunt. Labore dolor duis laborum est do nisi ut veniam dolor et nostrud nostrud.

```bicep
resource asp 'Microsoft.Web/serverfarms@2022-03-01' = {
  name: appServicePlanName
  location: location
  sku: {
    name: sku
  }
}

resource webApp 'Microsoft.Web/sites@2022-03-01' = {
  name: webAppName
  location: location
  identity: {
    type: 'SystemAssigned'
  }
  properties: {
    siteConfig: union(configReference[language],{
      minTlsVersion: '1.2'
      scmMinTlsVersion: '1.2'
      ftpsState: 'FtpsOnly'
    })
    serverFarmId: asp.id
    httpsOnly: true
  }
}
```