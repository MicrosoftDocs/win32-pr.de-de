---
description: Die GetKaraokeChannelContent-Methode ruft einen Wert ab, der den Inhaltstyp im angegebenenlaufoke-Kanal im angegebenen Stream angibt.
ms.assetid: e36a88b8-7184-44a4-8e02-204440f651bc
title: GetKaraokeChannelContent-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ef0353ebda6469627b5f41209b780fc1403c51940705be72d6acaa139d8320f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812490"
---
# <a name="getkaraokechannelcontent-method"></a>GetKaraokeChannelContent-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `GetKaraokeChannelContent` -Methode ruft einen Wert ab, der den Typ des Inhalts im angegebenenlaufoke-Kanal im angegebenen Stream angibt.

``` syntax
[ iContent = ] MSWebDVD.GetKaraokeChannelContent(iStream, iChannel)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*Istream*
</dt> <dd>

Gibt den Audiostream als ganze Zahl an.

</dd> <dt>

<span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*Ichannel*
</dt> <dd>

Gibt den Kanal als ganze Zahl an. Die möglichen Werte für jeden Kanal sind:



| Wert  | Beschreibung    |
|--------|----------------|
| 0x0001 | Guide Guides 1  |
| 0x0002 | Guide Guides 2  |
| 0x0004 | Leitfaden 1 |
| 0x0008 | Leitfaden 2 |
| 0x0010 | Guide Melody A |
| 0x0020 | Leitfaden B |
| 0x0040 | Sound Effect A |
| 0x0080 | Soundeffekt B |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, dessen einzelne Bits den Inhalt des sendeoke-Kanals angeben.

## <a name="remarks"></a>Hinweise

Da die Nummerierung von DVD-Audiokanälen nullbasiert ist, sind die Kanäle 2, 3 und 4 die hilfsfreien Kanäle. Nachdem die Methode zurückgegeben wurde, führen Sie eine bitweise AND-Operation für *iContent* aus, um den Inhalt jedes Kanals zu bestimmen. Da für einen einzelnen Kanal möglicherweise mehr als ein Inhaltstyp aufgezeichnet wird, sollten Sie auch nach der Suche nach einer Übereinstimmung alle möglichen Werte testen.

Nachdem der Benutzer die Inhalte der einzelnen Kanäle kennt, muss er in der Lage sein, das Volume anzupassen oder die einzelnen Kanäle bei Bedarf zu aktivieren oder zu deaktivieren. Implementieren Sie diese Funktionalität in Ihrer Anwendung, indem Sie die [**EigenschaftQualokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md) verwenden.

> [!Note]  
> Zum Wiedergeben von Datenträgern muss der Audiodecoder auf dem System des Benutzers mit der DirectShow 8-Implementierung kompatibel sein.

 

 

 



