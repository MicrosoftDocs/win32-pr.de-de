---
description: Eigenschaftensatz für den Transport externer Geräte
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Eigenschaftensatz für den Transport externer Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e38217af21ea1839d7c9207a4922bcff00d63a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909218"
---
# <a name="external-device-transport-property-set"></a>Eigenschaftensatz für den Transport externer Geräte

Dieser Eigenschaftensatz steuert den Transport von Daten zu und von einem externen Gerät. In den meisten Fällen sollten Anwendungen diesen Eigenschaftensatz nicht direkt verwenden. Verwenden Sie stattdessen die [**IAMExtTransport-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)

In der folgenden Tabelle sind die Eigenschaften aufgeführt, die für Benutzermodusanwendungen relevant sind. Eine vollständige Beschreibung dieses Eigenschaftensatzes finden Sie im Microsoft Windows Driver Development Kit DDK.



| Bezeichnung | Wert |
|-------------------|---------------------------|
| Eigenschaftensatz-GUID | PROPSETID \_ EXT \_ TRANSPORT |



 



| Eigenschafts-ID                                                                           | BESCHREIBUNG                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [**KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH**](ksproperty-extxport-atn-search.md)           | Sucht nach einer absoluten Tracknummer (ATN). |
| [**KSPROPERTY \_ EXTXPORT \_ TIMECODE \_ SEARCH**](ksproperty-extxport-timecode-search.md) | Sucht nach einem Zeitcode.                    |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 



