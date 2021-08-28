---
title: MicrosoftDNS_StatisticCollection
description: Die MicrosoftDNS \_ StatisticCollection-Klasse stellt eine Sammlung verwandter DNS-Serverstatistiken dar.
ms.assetid: 74e080e9-a676-4a82-ae8b-ee904622eb9a
keywords:
- MicrosoftDNS_StatisticCollection
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42fda276433290ab2b151b4b6a34abae7a0113ee3db75054f6c66c0536009dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109090"
---
# <a name="microsoftdns_statisticcollection"></a>MicrosoftDNS \_ StatisticCollection

Die MicrosoftDNS \_ StatisticCollection-Klasse stellt eine Sammlung verwandter DNS-Serverstatistiken dar.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

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

<span id="Name"></span><span id="name"></span><span id="NAME"></span>**Namen**
</dt> <dd>

Name der Statistiksammlung.

</dd> <dt>

<span id="StatId"></span><span id="statid"></span><span id="STATID"></span>**StatId**
</dt> <dd>

Numerische Darstellung der Statistiksammlung.

</dd> <dt>

<span id="MicrosoftDNS_Statistic_Statistics__"></span><span id="microsoftdns_statistic_statistics__"></span><span id="MICROSOFTDNS_STATISTIC_STATISTICS__"></span>**Statistik der \_ MicrosoftDNS-Statistik\[\]**
</dt> <dd>

Array von Werten, die der Statistik zugeordnet sind.

</dd> </dl>

## <a name="methods"></a>Methoden

<dl> <dt>

<span id="This_class_has_no_methods."></span><span id="this_class_has_no_methods."></span><span id="THIS_CLASS_HAS_NO_METHODS."></span>Diese Klasse verfügt über keine Methoden.
</dt> <dd></dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**MicrosoftDNS-Statistik \_**](microsoftdns-statistic.md)
</dt> </dl>

 

 




