---
title: Downloadstatus-Element (msfeeds. h)
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Downloadstatus-Element (msfeeds. h)
ms.assetid: 08d9719a-390d-454a-935e-27812c0f3599
keywords:
- Download Status-Element Fenster Media Player
topic_type:
- apiref
api_name:
- DownloadStatus Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 431da810a9591d891fca914a9ecb6d3146a651d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370171"
---
# <a name="downloadstatus-element"></a>Downloadstatus-Element

> [!Note]  
> In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.

 

Das **Downloadstatus** -Element gibt eine URL an, die der Windows-Media Player als Link anzeigt, damit Benutzer den Download Status anzeigen können.

``` syntax
<DownloadStatus
    URL = "URL"
/>
```

## <a name="attributes"></a>Attribute

<dl> <dt>

<span id="URL"></span><span id="url"></span>Urne
</dt> <dd>

Die URL für die Webseite, die im Online Store angezeigt wird, um den Download Status für den Benutzer anzuzeigen.

</dd> </dl>

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Element         |
|-----------------|-----------------|
| Übergeordnete Elemente | **ServiceInfo** |
| Untergeordnete Elemente  | Keine            |



 

## <a name="remarks"></a>Bemerkungen

Windows Media Player zeigt Benutzern eine Meldung an, wenn ein Download ausgeführt wird. Wenn die aktuellen aktiven Dienste eine Download Status-URL definieren, kann der Benutzer auf den Meldungs Text klicken. Wenn der Benutzer auf die Meldung klickt, navigiert der Spieler zu der URL, die vom **Downloadstatus** -Element angegeben wird, sodass der aktuelle aktive Speicher Details zu den zurzeit ausgeführten Downloads bereitstellen kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher<br/>                                          |
| Header<br/>  | <dl> <dt>Msfeeds. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**Servicinfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 





