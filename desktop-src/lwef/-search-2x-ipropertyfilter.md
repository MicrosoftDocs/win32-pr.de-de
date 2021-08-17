---
title: IPropertyFilter-Schnittstelle (WdsSharedIDL.h)
description: Macht Eigenschaften verfügbar, die zum Filtern der Abfrage verwendet werden.
ms.assetid: 3760c413-931c-44f2-adaf-eb17df4015c3
keywords:
- IPropertyFilter-Schnittstelle – Legacy Windows Umgebungsfeatures
- IPropertyFilter-Schnittstelle Legacy Windows Umgebungsfeatures , beschrieben
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
ms.openlocfilehash: 3e5bc406661492702e4a012cab58a2e0a3e08507aeaa13d10b010f14ce31e6fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481094"
---
# <a name="ipropertyfilter-interface"></a>IPropertyFilter-Schnittstelle

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen [die Windows Search-API.](../search/-search-reference-entry-page.md) 

Macht Eigenschaften verfügbar, die zum Filtern der Abfrage verwendet werden.

## <a name="members"></a>Member

Die **IPropertyFilter-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IPropertyFilter** verfügt auch über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IPropertyFilter-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                      | Zugriffstyp           | BESCHREIBUNG                                                   |
|:----------------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------|
| [**IPropertyFilter::IndexColumn**](-search-2x-ipropertyfilter-indexcolumn.md)<br/>     | Lesen/Schreiben<br/> | Indizierter Spaltenname der Eigenschaft, nach der gefiltert werden soll. <br/> |
| [**IPropertyFilter::LogicOperator**](-search-2x-ipropertyfilter-logicoperator.md)<br/> | Lesen/Schreiben<br/> | Logikoperator, der beim Anwenden des Filters verwendet werden soll. <br/>       |
| [**IPropertyFilter::NestingDepth**](-search-2x-ipropertyfilter-nestingdepth.md)<br/>   | Lesen/Schreiben<br/> | Filtert die Tiefe in einem geschachtelten Satz von Klammern. <br/> |
| [**IPropertyFilter::Text**](-search-2x-ipropertyfilter-text.md)<br/>                   | Lesen/Schreiben<br/> | Text des Filters. <br/>                               |
| [**IPropertyFilter::UID**](-search-2x-ipropertyfilter-uid.md)<br/>                     | Lesen/Schreiben<br/> | UID für die Eigenschaft, nach der gefiltert werden soll. <br/>                 |



 

## <a name="remarks"></a>Hinweise

Diese Eigenschaften werden verwendet, um die Abfrage zu filtern.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2003 mit \[ SP1-Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 3.0<br/>                                               |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

