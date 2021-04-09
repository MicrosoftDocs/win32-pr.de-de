---
title: MicrosoftDNS_StatisticCollection
description: Die MicrosoftDNS \_ statisticcollection-Klasse stellt eine Sammlung verwandter DNS-Server Statistiken dar.
ms.assetid: 74e080e9-a676-4a82-ae8b-ee904622eb9a
keywords:
- MicrosoftDNS_StatisticCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c44f9c65714fb3b1db58b5a6439ade5531792501
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036719"
---
# <a name="microsoftdns_statisticcollection"></a>MicrosoftDNS \_ statisticcollection

Die MicrosoftDNS \_ statisticcollection-Klasse stellt eine Sammlung verwandter DNS-Server Statistiken dar.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

``` syntax
class MicrosoftDNS_StatisticCollection : CIM_LogicalElement
{
  string Name;
  uint32 StatId;
  MicrosoftDNS_Statistic Statistics[];
};
```

## <a name="properties"></a>Eigenschaften

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>**Benennen**
</dt> <dd>

Der Name der Statistik Sammlung.

</dd> <dt>

<span id="StatId"></span><span id="statid"></span><span id="STATID"></span>**Statid**
</dt> <dd>

Numerische Darstellung der Statistik Sammlung.

</dd> <dt>

<span id="MicrosoftDNS_Statistic_Statistics__"></span><span id="microsoftdns_statistic_statistics__"></span><span id="MICROSOFTDNS_STATISTIC_STATISTICS__"></span>**Statistik Statistik zu MicrosoftDNS \_\[\]**
</dt> <dd>

Array von Werten, die der Statistik zugeordnet sind.

</dd> </dl>

## <a name="methods"></a>Methoden

<dl> <dt>

<span id="This_class_has_no_methods."></span><span id="this_class_has_no_methods."></span><span id="THIS_CLASS_HAS_NO_METHODS."></span>Diese Klasse verfügt über keine Methoden.
</dt> <dd></dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**MicrosoftDNS- \_ Statistik**](microsoftdns-statistic.md)
</dt> </dl>

 

 




