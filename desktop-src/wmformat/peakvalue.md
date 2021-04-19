---
title: Peer Value
description: Das peakvalue-Attribut enthält einen 16-Bit-Amplitude-Wert, der die maximale Volumeebene von Audioinhalten festlegt.
ms.assetid: 885f6d4c-661a-4681-96b6-c1a282c8bf18
keywords:
- Windows Media-Format von "Peer Value"
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ef933ec1b10555aa4c88a24261313abb261163
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106341895"
---
# <a name="peakvalue"></a>Peer Value

Das **peakvalue** -Attribut enthält einen 16-Bit-Amplitude-Wert, der die maximale Volumeebene von Audioinhalten festlegt. Bei [**averagelevel**](averagelevel.md)wird dieses Attribut für die Normalisierung verwendet. Normalisierung ist der Prozess, bei dem die Wiedergabe Volume-Ebene von Audiodateien angepasst wird, sodass die laugsten Teile von Dateien, die auf derselben Ebene wiedergegeben werden, und das durchschnittliche Volume für die beiden identisch sind.

## <a name="global-constant"></a>Globale Konstante

g \_ wszpeer Value

## <a name="data-type"></a>Datentyp

**WMT- \_ Typ \_ DWORD**

## <a name="remarks"></a>Bemerkungen

Dieses Attribut wird durch das Writer-Objekt auf der Grundlage von Informationen aus dem Codec festgelegt. Nur mit einem der Windows Media Audio Codecs komprimierte Streams haben einen automatisch festgelegten Wert.

" **Peer Value** " ist nicht schreibgeschützt. Wenn die Datei jedoch vom Windows-Media Player abgespielt wird, sollten Sie diesen Wert nicht ändern. Der Windows-Media Player verwendet diese, um die Ebenen von Dateien in einer Wiedergabeliste zu normalisieren.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




