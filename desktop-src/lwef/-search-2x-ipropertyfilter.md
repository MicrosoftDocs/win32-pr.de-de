---
title: Ipropertyfilter-Schnittstelle (wdssharedidl. h)
description: Macht Eigenschaften verfügbar, die zum Filtern der Abfrage verwendet werden.
ms.assetid: 3760c413-931c-44f2-adaf-eb17df4015c3
keywords:
- Ipropertyfilter Interface, ältere Windows-Umgebungs Features
- Ipropertyfilter Interface Legacy Windows-Umgebungs Features, beschrieben
topic_type:
- apiref
api_name:
- IPropertyFilter
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4358ca7e111fd68beb68391ba7f08a9b8095d7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518311"
---
# <a name="ipropertyfilter-interface"></a>Ipropertyfilter-Schnittstelle

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) . 

Macht Eigenschaften verfügbar, die zum Filtern der Abfrage verwendet werden.

## <a name="members"></a>Member

Die **ipropertyfilter** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Ipropertyfilter** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ipropertyfilter** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                                      | Zugriffstyp           | BESCHREIBUNG                                                   |
|:----------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------|
| [**Ipropertyfilter:: indexcolumn**](-search-2x-ipropertyfilter-indexcolumn.md)<br/>     | Lesen/Schreiben<br/> | Der Name der indizierten Spalte der Eigenschaft, nach der gefiltert werden soll. <br/> |
| [**Ipropertyfilter:: logicoperator**](-search-2x-ipropertyfilter-logicoperator.md)<br/> | Lesen/Schreiben<br/> | Der zum Anwenden des Filters zu verwendende Logik Operator. <br/>       |
| [**Ipropertyfilter:: nestingtiefe**](-search-2x-ipropertyfilter-nestingdepth.md)<br/>   | Lesen/Schreiben<br/> | Filtert die Tiefe innerhalb eines geschachtelten Satzes von Klammern. <br/> |
| [**Ipropertyfilter:: Text**](-search-2x-ipropertyfilter-text.md)<br/>                   | Lesen/Schreiben<br/> | Text des Filters. <br/>                               |
| [**Ipropertyfilter:: UID**](-search-2x-ipropertyfilter-uid.md)<br/>                     | Lesen/Schreiben<br/> | UID: die Eigenschaft, nach der gefiltert werden soll. <br/>                 |



 

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaften werden verwendet, um die Abfrage zu filtern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 mit SP1 \[ Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 3,0<br/>                                               |
| Header<br/>                   | <dl> <dt>Wdssharedidl. h</dt> </dl> |



 

