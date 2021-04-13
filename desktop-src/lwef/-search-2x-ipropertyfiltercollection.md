---
title: Ipropertyfiltercollection-Schnittstelle (wdssharedidl. h)
description: Macht Eigenschaften der zurückgegebenen Auflistung auf der Grundlage der übermittelten Abfrage verfügbar.
ms.assetid: 9ed4217f-54b0-4d69-bf44-2547320a9681
keywords:
- Ipropertyfiltercollection-Schnittstelle ältere Windows-Umgebungs Features
- Ipropertyfiltercollection-Schnittstelle ältere Windows-Umgebungs Features, beschrieben
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
ms.openlocfilehash: 9be9fe01bacf24c852b49538beae16b4ecbc97b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340857"
---
# <a name="ipropertyfiltercollection-interface"></a>Ipropertyfiltercollection-Schnittstelle

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) . 

Macht Eigenschaften der zurückgegebenen Auflistung auf der Grundlage der übermittelten Abfrage verfügbar.

## <a name="members"></a>Member

Die **ipropertyfiltercollection** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ipropertyfiltercollection** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ipropertyfiltercollection** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                         | Zugriffstyp           | BESCHREIBUNG                                                  |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------|
| [**AddItem**](-search-2x-ipropertyfiltercollection-additem.md)<br/>       | Schreibgeschützt<br/>  | Fügt der Auflistung einen neuen Filter hinzu. <br/>             |
| [**Klartext**](-search-2x-ipropertyfiltercollection-clear.md)<br/>           | Lesegeschützt<br/> | Löscht die Auflistung. <br/>                           |
| [**Countdown**](-search-2x-ipropertyfiltercollection-count.md)<br/>           | Schreibgeschützt<br/>  | Anzahl der Filter in der Auflistung. <br/>             |
| [**GetITem**](-search-2x-ipropertyfiltercollection-getitem.md)<br/>       | Lesen/Schreiben<br/> | Gibt einen bestimmten Filter in der Auflistung zurück. <br/> |
| [**RemoveItem**](-search-2x-ipropertyfiltercollection-removeitem.md)<br/> | Lesegeschützt<br/> | Entfernt einen bestimmten Filter für die Auflistung. <br/>     |



 

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften werden verwendet, um die von der Abfrage zurückgegebene Auflistung zu filtern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 mit SP1 \[ Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 3,0<br/>                                               |
| Header<br/>                   | <dl> <dt>Wdssharedidl. h</dt> </dl> |



 

