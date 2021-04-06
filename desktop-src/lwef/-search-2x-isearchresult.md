---
title: Isearchresult-Schnittstelle (wdssharedidl. h)
description: Macht Informationen und Eigenschaften für das Resultset verfügbar.
ms.assetid: 2f50b9d7-f6fd-481c-a5db-d622a7b02017
keywords:
- Isearchresult Interface, ältere Windows-Umgebungs Features
- Isearchresult Interface, ältere Windows-Umgebungs Features, beschrieben
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
ms.openlocfilehash: 89387ebe02c87ca6a5c5ac663a67ea060bd78948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742312"
---
# <a name="isearchresult-interface"></a>Isearchresult-Schnittstelle

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) . 

Macht Informationen und Eigenschaften für das Resultset verfügbar.

## <a name="members"></a>Member

Die **isearchresult** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Isearchresult** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **isearchresult** -Schnittstelle verfügt über diese Methoden.



| Methode                                                            | BESCHREIBUNG                 |
|:------------------------------------------------------------------|:----------------------------|
| [**Verfügbarkeit**](-search-2x-isearchresult-availability.md)     | Nicht implementiert.<br/> |
| [**DoVerb**](-search-2x-isearchresult-doverb.md)                 | Nicht implementiert.<br/> |
| [**GetIcon**](-search-2x-isearchresult-geticon.md)               | Nicht implementiert.<br/> |
| [**GetThumbnail**](-search-2x-isearchresult-getthumbnail.md)     | Nicht implementiert.<br/> |
| [**GetValue**](-search-2x-isearchresult-getvalue.md)             | Nicht implementiert.<br/> |
| [**Getverb**](-search-2x-isearchresult-getverb.md)               | Nicht implementiert.<br/> |
| [**Iconcount**](-search-2x-isearchresult-iconcount.md)           | Nicht implementiert.<br/> |
| [**Sin**](-search-2x-isearchresult-index.md)                   | Nicht implementiert.<br/> |
| [**LoadState**](-search-2x-isearchresult-loadstate.md)           | Nicht implementiert.<br/> |
| [**Vorschau**](-search-2x-isearchresult-previewer.md)           | Nicht implementiert.<br/> |
| [**PutValue**](-search-2x-isearchresult-putvalue.md)             | Nicht implementiert.<br/> |
| [**Thumbnailstate**](-search-2x-isearchresult-thumbnailstate.md) | Nicht implementiert.<br/> |
| [**type**](-search-2x-isearchresult-type.md)                     | Nicht implementiert.<br/> |
| [**Verbcount**](-search-2x-isearchresult-verbcount.md)           | Nicht implementiert.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methoden machen Eigenschaften und Aktionen verfügbar, die für das Resultset gelten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 mit SP1 \[ Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 3,0<br/>                                               |
| Header<br/>                   | <dl> <dt>Wdssharedidl. h</dt> </dl> |



 

