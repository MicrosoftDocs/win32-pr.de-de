---
title: Iresultproperty-Schnittstelle (wdssharedidl. h)
description: Macht Ergebnis Eigenschaften verfügbar.
ms.assetid: 58d8c516-47c6-4cae-b46c-5127baf3054d
keywords:
- Iresultproperty-Schnittstelle ältere Windows-Umgebungs Features
- Iresultproperty-Schnittstelle ältere Windows-Umgebungs Features, beschrieben
topic_type:
- apiref
api_name:
- IResultProperty
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 716c0b3998171731dea5f976afc266fe81b2c613
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345313"
---
# <a name="iresultproperty-interface"></a>Iresultproperty-Schnittstelle

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) . 

Macht Ergebnis Eigenschaften verfügbar.

## <a name="members"></a>Member

Die **iresultproperty** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iresultproperty** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **iresultproperty** -Schnittstelle verfügt über diese Methoden.



| Methode                                                    | BESCHREIBUNG                 |
|:----------------------------------------------------------|:----------------------------|
| [**GoBack**](-search-2x-iresultproperty-goback.md)       | Nicht implementiert.<br/> |
| [**GoForward**](-search-2x-iresultproperty-goforward.md) | Nicht implementiert.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **iresultproperty** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                   | Zugriffstyp          | BESCHREIBUNG                                           |
|:---------------------------------------------------------------------------|:---------------------|:------------------------------------------------------|
| [**Datentyp**](-search-2x-iresultproperty-datatype.md)<br/>         | Schreibgeschützt<br/> | Ein Properties-Datentyp. <br/>                   |
| [**DisplayName**](-search-2x-iresultproperty-displayname.md)<br/>   | Schreibgeschützt<br/> | Lokalisierter Anzeige Name der Eigenschaft. <br/>   |
| [**DisplayState**](-search-2x-iresultproperty-displaystate.md)<br/> | Schreibgeschützt<br/> | Die Fähigkeit der Eigenschaft. <br/>               |
| [**Deuteten**](-search-2x-iresultproperty-hint.md)<br/>                 | Schreibgeschützt<br/> | Spezieller Wert, der für das Abrufen von Daten verwendet wird. <br/> |
| [**Indexcolumn**](-search-2x-iresultproperty-indexcolumn.md)<br/>   | Schreibgeschützt<br/> | Eigenschaften Spaltenname im Index. <br/>      |
| [**UID**](-search-2x-iresultproperty-uid.md)<br/>                   | Schreibgeschützt<br/> | Eindeutiger Bezeichner für die Eigenschaft. <br/>       |



 

## <a name="remarks"></a>Bemerkungen

Dies sind die Rückgabe Eigenschaften von Elementen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 mit SP1 \[ Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 3,0<br/>                                               |
| Header<br/>                   | <dl> <dt>Wdssharedidl. h</dt> </dl> |



 

