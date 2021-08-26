---
title: ISearchResult-Schnittstelle (WdsSharedIDL.h)
description: Macht Informationen und Eigenschaften in Bezug auf das Resultset verfügbar.
ms.assetid: 2f50b9d7-f6fd-481c-a5db-d622a7b02017
keywords:
- ISearchResult-Schnittstelle – Legacy Windows Umgebungsfeatures
- ISearchResult-Schnittstelle Legacy Windows Umgebungsfeatures , beschrieben
topic_type:
- apiref
api_name:
- ISearchResult
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd15db1340b28c8ac273746a64a5aee8c4b3235155d948692ffcc16582ac4549
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963520"
---
# <a name="isearchresult-interface"></a>ISearchResult-Schnittstelle

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen [die Windows Search-API.](../search/-search-reference-entry-page.md) 

Macht Informationen und Eigenschaften in Bezug auf das Resultset verfügbar.

## <a name="members"></a>Member

Die **ISearchResult-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ISearchResult** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **ISearchResult-Schnittstelle** verfügt über diese Methoden.



| Methode                                                            | BESCHREIBUNG                 |
|:------------------------------------------------------------------|:----------------------------|
| [**Verfügbarkeit**](-search-2x-isearchresult-availability.md)     | Nicht implementiert.<br/> |
| [**DoVerb**](-search-2x-isearchresult-doverb.md)                 | Nicht implementiert.<br/> |
| [**GetIcon**](-search-2x-isearchresult-geticon.md)               | Nicht implementiert.<br/> |
| [**GetThumbnail**](-search-2x-isearchresult-getthumbnail.md)     | Nicht implementiert.<br/> |
| [**GetValue**](-search-2x-isearchresult-getvalue.md)             | Nicht implementiert.<br/> |
| [**GetVerb**](-search-2x-isearchresult-getverb.md)               | Nicht implementiert.<br/> |
| [**IconCount**](-search-2x-isearchresult-iconcount.md)           | Nicht implementiert.<br/> |
| [**Index**](-search-2x-isearchresult-index.md)                   | Nicht implementiert.<br/> |
| [**Loadstate**](-search-2x-isearchresult-loadstate.md)           | Nicht implementiert.<br/> |
| [**Vorschau**](-search-2x-isearchresult-previewer.md)           | Nicht implementiert.<br/> |
| [**PutValue**](-search-2x-isearchresult-putvalue.md)             | Nicht implementiert.<br/> |
| [**ThumbnailState**](-search-2x-isearchresult-thumbnailstate.md) | Nicht implementiert.<br/> |
| [**type**](-search-2x-isearchresult-type.md)                     | Nicht implementiert.<br/> |
| [**VerbCount**](-search-2x-isearchresult-verbcount.md)           | Nicht implementiert.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methoden machen Eigenschaften und Aktionen verfügbar, die für das Resultset gelten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2003 mit \[ SP1-Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 3.0<br/>                                               |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

