---
title: Color-Element
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Color-Element
ms.assetid: 36fafe16-b708-4dc1-9325-d4f39265069a
keywords:
- Farb Element Fenster Media Player
topic_type:
- apiref
api_name:
- Color Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6c73aa9fe2c7f731e872c4a2e235bf9c0e29ce05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362071"
---
# <a name="color-element"></a>Color-Element

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Das Color-Element gibt die Hintergrundfarbe für die Navigations Schaltflächen des Online Stores, den Schaltflächen Text und die Features-Taskleiste an.

``` syntax
<Color
    MediaPlayer = "#FFFFFF"
    MediaPlayerText = "#FFFFFF"
/>
```

## <a name="attributes"></a>Attribute

<dl> <dt>

<span id="MediaPlayer__required_"></span><span id="mediaplayer__required_"></span><span id="MEDIAPLAYER__REQUIRED_"></span>**Media Player** (erforderlich)
</dt> <dd>

Hexadezimal-RGB-Farbwert. Gibt die Hintergrundfarbe für Schaltflächen und die Taskleiste an.

</dd> <dt>

<span id="MediaPlayerText__required_"></span><span id="mediaplayertext__required_"></span><span id="MEDIAPLAYERTEXT__REQUIRED_"></span>**Mediaplayertext** (erforderlich)
</dt> <dd>

Hexadezimal-RGB-Farbwert. Gibt die Farbe für den Schaltflächen Text an.

</dd> </dl>

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Element         |
|-----------------|-----------------|
| Übergeordnete Elemente | **ServiceInfo** |
| Untergeordnete Elemente  | Keine            |



 

## <a name="remarks"></a>Bemerkungen

Der Standardwert für **Media Player** ist \# 7c9ad6. Der Standardwert für **mediaplayertext** ist \# FFFFFF.

Achten Sie darauf, Farben zu verwenden, die es dem Benutzer erleichtern, den Schaltflächen Text zu lesen. Sie sollten z. b. die Verwendung von weißem Schaltflächen Text auf hellfarbigen Schaltflächen vermeiden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Servicinfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 





