---
description: Transporteigenschaftssatz für externe Geräte
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Transporteigenschaftssatz für externe Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef7db31dfe80fae0178aa329ce7e3c6cd55d3a6acbef7fd5a8ccda07943bef4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685670"
---
# <a name="external-device-transport-property-set"></a>Transporteigenschaftssatz für externe Geräte

Dieser Eigenschaftensatz steuert den Transport von Daten zu und von einem externen Gerät. In den meisten Fällen sollten Anwendungen diesen Eigenschaftensatz nicht direkt verwenden. Verwenden Sie [**stattdessen die IAMExtTransport-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)

In der folgenden Tabelle sind die Eigenschaften aufgeführt, die für Benutzermodusanwendungen relevant sind. Eine vollständige Beschreibung dieses Eigenschaftensatzes finden Sie im Microsoft Windows Driver Development Kit DDK.



| Bezeichnung | Wert |
|-------------------|---------------------------|
| Eigenschaftensatz-GUID | PROPSETID \_ \_ EXT-TRANSPORT |



 



| Eigenschafts-ID                                                                           | BESCHREIBUNG                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [**KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH**](ksproperty-extxport-atn-search.md)           | Sucht nach einer absoluten Tracknummer (ATN). |
| [**KSPROPERTY \_ \_ EXTXPORT-ZEITCODESUCHE \_**](ksproperty-extxport-timecode-search.md) | Sucht nach einem Zeitcode.                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 



