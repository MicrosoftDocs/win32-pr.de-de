---
title: IPropertyFilterCollection-Schnittstelle (WdsSharedIDL.h)
description: Macht Eigenschaften der zurückgegebenen Auflistung basierend auf der übermittelten Abfrage verfügbar.
ms.assetid: 9ed4217f-54b0-4d69-bf44-2547320a9681
keywords:
- Legacy-Windows-Umgebungsfeatures der IPropertyFilterCollection-Schnittstelle
- IPropertyFilterCollection-Schnittstelle Legacy Windows Umgebungsfeatures , beschrieben
topic_type:
- apiref
api_name:
- IPropertyFilterCollection
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69fb2f7ce6e100c74046f3402eee3385108723202fbaa6dce01e888bffef4b93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349980"
---
# <a name="ipropertyfiltercollection-interface"></a>IPropertyFilterCollection-Schnittstelle

> [!NOTE]
> Windows DesktopSuche 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows-Suche-API.](../search/-search-reference-entry-page.md) 

Macht Eigenschaften der zurückgegebenen Auflistung basierend auf der übermittelten Abfrage verfügbar.

## <a name="members"></a>Member

Die **IPropertyFilterCollection-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPropertyFilterCollection** verfügt auch über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IPropertyFilterCollection-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                         | Zugriffstyp           | Beschreibung                                                  |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------|
| [**AddItem**](-search-2x-ipropertyfiltercollection-additem.md)<br/>       | Schreibgeschützt<br/>  | Fügt der Auflistung einen neuen Filter hinzu. <br/>             |
| [**Klar**](-search-2x-ipropertyfiltercollection-clear.md)<br/>           | Lesegeschützt<br/> | Löscht die Auflistung. <br/>                           |
| [**Anzahl**](-search-2x-ipropertyfiltercollection-count.md)<br/>           | Schreibgeschützt<br/>  | Anzahl der Filter in der Auflistung. <br/>             |
| [**Getitem**](-search-2x-ipropertyfiltercollection-getitem.md)<br/>       | Lesen/Schreiben<br/> | Gibt einen bestimmten Filter innerhalb der Auflistung zurück. <br/> |
| [**RemoveItem**](-search-2x-ipropertyfiltercollection-removeitem.md)<br/> | Lesegeschützt<br/> | Entfernt einen bestimmten Filter für die Auflistung. <br/>     |



 

## <a name="remarks"></a>Hinweise

Diese Eigenschaften werden verwendet, um die von der Abfrage zurückgegebene Sammlung zu filtern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 nur mit \[ SP1-Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 3.0<br/>                                               |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

