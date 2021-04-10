---
description: Die audiostreamsavailable-Eigenschaft ruft die Anzahl der Audiostreams ab, die im aktuellen Titel verfügbar sind.
ms.assetid: 4359ec30-920a-4b34-8e27-4cf1d9452aa8
title: Audiostreamsavailable (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb68020b30f4349fcbbb464150624d75250a0dbf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860198"
---
# <a name="audiostreamsavailable-property"></a>Audiostreamsavailable (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `AudioStreamsAvailable` -Eigenschaft ruft die Anzahl der Audiostreams ab, die im aktuellen Titel verfügbar sind.

``` syntax
[ iStreams = ] MSWebDVD.AudioStreamsAvailable
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zwischen 1 und 8 zurück, der die Anzahl der im aktuellen Titel verfügbaren Audiostreams darstellt.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf. Die primäre Verwendung mehrerer Audiodatenströme besteht darin, Movie Soundtracks in mehr als einer Sprache bereitzustellen. In der Regel sind nicht für alle Titel auf einem Datenträger alle Audiostreams aktiviert. Beispielsweise kann der Feature Movie Soundtracks in drei verschiedenen Sprachen enthalten, aber die nach spannenden enthalten möglicherweise nur einen englischen Sound. Bevor ein Benutzer einen Stream auswählen kann, muss die Anwendung bestimmen, welche Streams innerhalb des aktuellen Titels verfügbar sind. Beachten Sie, dass bestimmte Streams durch einen Index von 0 bis 7 identifiziert werden.

Auf den Datenträgern wird in der Regel ein Menü mit den verfügbaren Sound Spuren angezeigt, sodass der Benutzer den Audiostream auswählen kann.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Getaudiolanguage**](getaudiolanguage-method.md)
</dt> </dl>

 

 



