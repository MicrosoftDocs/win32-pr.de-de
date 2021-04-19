---
title: Optimalbitrate
description: Das optimalbitrate-Attribut enthält die Bitrate, in der die Datei am besten wiedergegeben wird.
ms.assetid: cd13b9b5-34d2-4ebb-9f10-3bf42dd9de81
keywords:
- Optimalbitrate Windows Media-Format
topic_type:
- apiref
api_name:
- OptimalBitrate
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff71c6b64cbc4bf4ccc4f346e62a5eae066e78ce
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106341898"
---
# <a name="optimalbitrate"></a>Optimalbitrate

Das **optimalbitrate** -Attribut enthält die Bitrate, in der die Datei am besten wiedergegeben wird.

## <a name="global-constant"></a>Globale Konstante

g \_ wszwmoptimalbitrate

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ \_ DWORD**

## <a name="remarks"></a>Bemerkungen

Dies ist ein codiertes Attribut.

Bei Dateien, die VBR-Streams (Variable Bitrate) enthalten, ist dieser Wert die Spitzen Bitrate für die Datenströme in der Datei. Bei Dateien ohne VBR ist dieser Wert mit der [**Bitrate**](bit-rate.md)identisch.

Dieses Attribut kann nicht auf Dateiebene dupliziert werden. Wenn dieses Attribut für einen einzelnen Stream verwendet wird, wird es als benutzerdefinierte Metadaten behandelt und gibt seine normale Bedeutung nicht an die Objekte des Windows Media Format SDK aus.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




