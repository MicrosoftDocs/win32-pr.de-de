---
description: Die Eigenschaft AudioStreamsAvailable ruft die Anzahl der audiostreams ab, die im aktuellen Titel verfügbar sind.
ms.assetid: 4359ec30-920a-4b34-8e27-4cf1d9452aa8
title: AudioStreamsAvailable-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07025a3a3bf54ad98d32c54ee3c147bc36489822ef451965e1e0e0da8fe586c8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586730"
---
# <a name="audiostreamsavailable-property"></a>AudioStreamsAvailable-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `AudioStreamsAvailable` -Eigenschaft ruft die Anzahl der Audiostreams ab, die im aktuellen Titel verfügbar sind.

``` syntax
[ iStreams = ] MSWebDVD.AudioStreamsAvailable
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zwischen 1 und 8 zurück, der die Anzahl der im aktuellen Titel verfügbaren Audiostreams darstellt.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist schreibgeschützt und hat keinen Standardwert. Die primäre Verwendung mehrerer Audiostreams besteht darin, Filmvideos in mehr als einer Sprache bereitzustellen. In der Regel sind nicht für jeden Titel auf einem Datenträger alle Audiostreams aktiviert. Der Feature-Film kann z. B. 2017 in drei verschiedenen Sprachen vorliegen, aber die Trailer verfügen möglicherweise nur über einen englischen Englischsprachigen. Bevor ein Benutzer einen Stream auswählen kann, muss die Anwendung bestimmen, welche Streams innerhalb des aktuellen Titels verfügbar sind. Beachten Sie, dass bestimmte Datenströme durch einen Index von 0 bis 7 identifiziert werden.

Datenträger zeigen in der Regel ein Menü mit den verfügbaren Scheiben an, sodass der Benutzer den zu aktivierenden Audiostream auswählen kann.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**GetAudioLanguage**](getaudiolanguage-method.md)
</dt> </dl>

 

 



