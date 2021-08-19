---
title: CurrentBitrate
description: Das CurrentBitrate-Attribut enthält die aktuelle Bitrate der aktiven Streams in der Datei.
ms.assetid: 961f36d5-a408-40d9-9ca1-0ed7c484858f
keywords:
- CurrentBitrate-Windows-Medienformat
topic_type:
- apiref
api_name:
- CurrentBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 028207ee152acac289da6608c682f5fc14a4fde69603a2aae05b841d0cfb46ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027948"
---
# <a name="currentbitrate"></a>CurrentBitrate

Das CurrentBitrate-Attribut enthält die aktuelle Bitrate der aktiven Streams in der Datei.

## <a name="global-constant"></a>Globale Konstante

g \_ wszWMCurrentBitrate

## <a name="data-type"></a>Datentyp

**WMT \_ TYPE \_ DWORD**

## <a name="remarks"></a>Hinweise

Dies ist ein codiertes Attribut.

Der für **CurrentBitrate abgerufene** Wert ist abhängig vom verwendeten Objekt unterschiedlich. Im Reader- oder synchronen Readerobjekt ist der Wert die tatsächliche Bitrate zum Zeitpunkt des Aufrufs. Im Metadaten-Editor-Objekt ist der Wert die durchschnittliche Bitrate der Datei.

Die tatsächliche Bitrate einer Datei entspricht den Bitraten aller aktiven Streams plus etwas Mehraufwand. Dies ist der Wert, der z. B. angezeigt wird, wenn eine Datei mit dem -Windows Media Player.

Dieses Attribut kann nicht auf Dateiebene dupliziert werden. Wenn dieses Attribut für einen einzelnen Stream verwendet wird, wird es als benutzerdefinierte Metadaten behandelt und vermittelt den Objekten des Windows Media Format SDK nicht seine normale Bedeutung.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




