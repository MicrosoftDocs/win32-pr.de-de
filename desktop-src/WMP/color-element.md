---
title: Color-Element
description: Hinweis In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. | Color-Element
ms.assetid: 36fafe16-b708-4dc1-9325-d4f39265069a
keywords:
- Farbelement-Windows Media Player
topic_type:
- apiref
api_name:
- Color Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8b8576f94c2d1aa88608f8f40cbfe32c2d1dc315e0e4578ca6554fa5fcde82c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118580755"
---
# <a name="color-element"></a>Color-Element

> [!Note]  
> In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Das Color-Element gibt die Hintergrundfarbe für Die Navigationsschaltflächen des Onlineshops, den Text der Schaltfläche und die Taskleiste Features an.

``` syntax
<Color
    MediaPlayer = "#FFFFFF"
    MediaPlayerText = "#FFFFFF"
/>
```

## <a name="attributes"></a>Attribute

<dl> <dt>

<span id="MediaPlayer__required_"></span><span id="mediaplayer__required_"></span><span id="MEDIAPLAYER__REQUIRED_"></span>**MediaPlayer** (erforderlich)
</dt> <dd>

Hexadezimaler RGB-Farbwert. Gibt die Hintergrundfarbe für Schaltflächen und die Taskleiste an.

</dd> <dt>

<span id="MediaPlayerText__required_"></span><span id="mediaplayertext__required_"></span><span id="MEDIAPLAYERTEXT__REQUIRED_"></span>**MediaPlayerText** (erforderlich)
</dt> <dd>

Hexadezimaler RGB-Farbwert. Gibt die Farbe für den Schaltflächentext an.

</dd> </dl>

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Element         |
|-----------------|-----------------|
| Übergeordnete Elemente | **ServiceInfo** |
| Untergeordnete Elemente  | Keine            |



 

## <a name="remarks"></a>Bemerkungen

Der Standardwert für **MediaPlayer** ist \# 7C9AD6. Der Standardwert für **MediaPlayerText** ist \# FFFFFF.

Achten Sie darauf, Farben zu verwenden, die dem Benutzer das Lesen des Schaltflächentexts leicht machen. Sie sollten z. B. die Verwendung von weißem Schaltflächentext auf hellfarbenen Schaltflächen vermeiden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ServiceInfo-Beispieldokument für eine Online-Store**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**ServiceInfo-Beispieldokument für eine Online-Store**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 





