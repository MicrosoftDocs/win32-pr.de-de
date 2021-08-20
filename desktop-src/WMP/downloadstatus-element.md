---
title: DownloadStatus-Element (Msfeeds.h)
description: Hinweis In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. | DownloadStatus-Element (Msfeeds.h)
ms.assetid: 08d9719a-390d-454a-935e-27812c0f3599
keywords:
- DownloadStatus-Windows Media Player
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
ms.openlocfilehash: f445152e6df2aaffbd3a508942fd4f86838e28671737995c069fac51bc3b0f21
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117935758"
---
# <a name="downloadstatus-element"></a>DownloadStatus-Element

> [!Note]  
> In diesem Abschnitt werden Funktionen beschrieben, die für die Verwendung durch Onlineshops entwickelt wurden. Die Verwendung dieser Funktionalität außerhalb des Kontexts eines Onlineshops wird nicht unterstützt.

 

Das **DownloadStatus-Element** gibt eine URL an, Windows Media Player als Link angezeigt wird, damit Benutzer den Downloadstatus anzeigen können.

``` syntax
<DownloadStatus
    URL = "URL"
/>
```

## <a name="attributes"></a>Attribute

<dl> <dt>

<span id="URL"></span><span id="url"></span>Url
</dt> <dd>

URL für die Webseite, die im Onlineshop angezeigt wird, um dem Benutzer den Downloadstatus anzuzeigen.

</dd> </dl>

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Element         |
|-----------------|-----------------|
| Übergeordnete Elemente | **ServiceInfo** |
| Untergeordnete Elemente  | Keine            |



 

## <a name="remarks"></a>Bemerkungen

Windows Media Player zeigt benutzern eine Meldung an, wenn ein Download läuft. Wenn die aktuellen aktiven Dienste eine Downloadstatus-URL definieren, kann der Benutzer auf den Meldungstext klicken. Wenn der Benutzer auf die Nachricht klickt, navigiert der Player zu der URL, die durch das **DownloadStatus-Element** angegeben wird, damit der aktuelle aktive Store Details zu downloads in Bearbeitung bereitstellen kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player 10 oder höher<br/>                                          |
| Header<br/>  | <dl> <dt>Msfeeds.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ServiceInfo-Beispieldokument für eine Online-Store**](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[**ServiceInfo-Beispieldokument für eine Online-Store**](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[**ServiceInfo-Dokument**](serviceinfo-document.md)
</dt> </dl>

 

 





