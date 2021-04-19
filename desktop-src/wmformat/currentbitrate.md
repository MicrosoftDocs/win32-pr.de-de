---
title: Currentbitrate
description: Das currentbitrate-Attribut enthält die aktuelle gesamte Bitrate der aktiven Datenströme in der Datei.
ms.assetid: 961f36d5-a408-40d9-9ca1-0ed7c484858f
keywords:
- Currentbitrate Windows Media-Format
topic_type:
- apiref
api_name:
- CurrentBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdcd8db7d60c65bcb7ceedcac4498ac650f90d9a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106339031"
---
# <a name="currentbitrate"></a>Currentbitrate

Das currentbitrate-Attribut enthält die aktuelle gesamte Bitrate der aktiven Datenströme in der Datei.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmcurrentbitrate

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ \_ DWORD**

## <a name="remarks"></a>Bemerkungen

Dies ist ein codiertes Attribut.

Der Wert, der für **currentbitrate** abgerufen wird, unterscheidet sich je nach verwendetem Objekt. Im Reader-oder synchronen Reader-Objekt ist der Wert die tatsächliche Bitrate zum Zeitpunkt des Aufrufes. Im Metadateneditor-Objekt ist der Wert die durchschnittliche Bitrate der Datei.

Die tatsächliche Bitrate einer Datei entspricht den Bitraten aller aktiven Streams plus einem gewissen Verwaltungsaufwand. Dies ist der Wert, der beispielsweise angezeigt wird, wenn eine Datei mit dem Windows-Media Player wiedergegeben wird.

Dieses Attribut kann nicht auf Dateiebene dupliziert werden. Wenn dieses Attribut für einen einzelnen Stream verwendet wird, wird es als benutzerdefinierte Metadaten behandelt und gibt seine normale Bedeutung nicht an die Objekte des Windows Media Format SDK aus.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




