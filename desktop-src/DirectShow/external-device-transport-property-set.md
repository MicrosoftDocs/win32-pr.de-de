---
description: Eigenschaften Satz für externen Geräte Transport
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Eigenschaften Satz für externen Geräte Transport
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e77942157b7cf5f75b883e6953f3a115d1fa9f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125600"
---
# <a name="external-device-transport-property-set"></a>Eigenschaften Satz für externen Geräte Transport

Dieser Eigenschaften Satz steuert den Transport von Daten zu und von einem externen Gerät. In den meisten Fällen sollten diese Eigenschaften nicht direkt von Anwendungen verwendet werden. Verwenden Sie stattdessen die [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) -Schnittstelle.

In der folgenden Tabelle sind die Eigenschaften aufgelistet, die für Benutzermodusanwendungen relevant sind. Eine umfassende Beschreibung dieses Eigenschaften Satzes finden Sie im Microsoft Windows Driver Development Kit-DDK.



|                   |                           |
|-------------------|---------------------------|
| Eigenschaftensatz-GUID | propseetid- \_ Ext- \_ Transport |



 



| Eigenschafts-ID                                                                           | BESCHREIBUNG                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [**ksproperty \_ extxport- \_ Atn- \_ Suche**](ksproperty-extxport-atn-search.md)           | Sucht nach einer absoluten Spur Nummer (ATN). |
| [**ksproperty \_ extxport- \_ \_ timecodesuche**](ksproperty-extxport-timecode-search.md) | Sucht nach einem Zeit Code.                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 



