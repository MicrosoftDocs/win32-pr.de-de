---
description: Die getkaraokechannelcontent-Methode ruft einen Wert ab, der den Inhaltstyp im angegebenen Datenstrom im angegebenen Karaoke-Channel angibt.
ms.assetid: e36a88b8-7184-44a4-8e02-204440f651bc
title: Getkaraokechannelcontent-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd35705f1fba65eaf5c6f7c67ea55078c68e5036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346599"
---
# <a name="getkaraokechannelcontent-method"></a>Getkaraokechannelcontent-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `GetKaraokeChannelContent` Methode ruft einen Wert ab, der den Inhaltstyp im angegebenen Datenstrom im angegebenen Karaoke-Channel angibt.

``` syntax
[ iContent = ] MSWebDVD.GetKaraokeChannelContent(iStream, iChannel)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*IStream*
</dt> <dd>

Gibt den Audiodatenstrom als Ganzzahl an.

</dd> <dt>

<span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*IChannel*
</dt> <dd>

Gibt den Kanal als Ganzzahl an. Die möglichen Werte für jeden Kanal lauten:



| Wert  | BESCHREIBUNG    |
|--------|----------------|
| 0x0001 | Leitfaden 1  |
| 0x0002 | Leitfaden für Gesang 2  |
| 0x0004 | Hand Buch-Melodie 1 |
| 0x0008 | Führungslinie 2 |
| 0x0010 | Leitfaden für die Anleitung A |
| 0x0020 | Führungslinie B |
| 0x0040 | Sound Effekt A |
| 0x0080 | Sound Effekt B |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, dessen einzelne Bits den Inhalt des Karaoke-Kanals angeben.

## <a name="remarks"></a>Bemerkungen

Die Nummerierung des DVD-Audiokanals ist NULL basiert, sodass die Kanäle 2, 3 und 4 die zusätzlichen Karaoke-Kanäle sind. Führen Sie nach dem Zurückgeben der Methode eine bitweise AND-Operation für *icontent* aus, um den Inhalt der einzelnen Kanäle zu ermitteln. Da in einem einzelnen Kanal möglicherweise mehr als ein Inhaltstyp aufgezeichnet wurde, sollten Sie alle möglichen Werte testen, auch nachdem eine Entsprechung gefunden wurde.

Nachdem der Benutzer die Inhalte der einzelnen Kanäle kennt, muss er das Volume anpassen oder die einzelnen Kanäle bei Bedarf ein-oder ausschalten können. Implementieren Sie diese Funktionalität in Ihrer Anwendung, indem Sie die Eigenschaft " [**karaokeaudiopresentationmode**](karaokeaudiopresentationmode-property.md) " verwenden.

> [!Note]  
> Zum Wiedergeben von Karaoke-Festplatten muss der Audiodecoder im System des Benutzers mit der "DirectShow 8"-Karaoke-Implementierung kompatibel sein.

 

 

 



