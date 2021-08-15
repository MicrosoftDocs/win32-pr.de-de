---
title: IResultProperty-Schnittstelle (WdsSharedIDL.h)
description: Macht Ergebniseigenschaften verfügbar.
ms.assetid: 58d8c516-47c6-4cae-b46c-5127baf3054d
keywords:
- Legacy-Windows-Umgebungsfeatures der IResultProperty-Schnittstelle
- IResultProperty-Schnittstelle Legacy Windows Umgebungsfeatures , beschrieben
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
ms.openlocfilehash: efba214aaaadec2cfad52db02f9f4f18d289b0b3ee9df37ee60295d5499241e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118754583"
---
# <a name="iresultproperty-interface"></a>IResultProperty-Schnittstelle

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API.](../search/-search-reference-entry-page.md) 

Macht Ergebniseigenschaften verfügbar.

## <a name="members"></a>Member

Die **IResultProperty-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IResultProperty** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IResultProperty-Schnittstelle** verfügt über diese Methoden.



| Methode                                                    | BESCHREIBUNG                 |
|:----------------------------------------------------------|:----------------------------|
| [**GoBack**](-search-2x-iresultproperty-goback.md)       | Nicht implementiert.<br/> |
| [**Goforward**](-search-2x-iresultproperty-goforward.md) | Nicht implementiert.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **IResultProperty-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                   | Zugriffstyp          | BESCHREIBUNG                                           |
|:---------------------------------------------------------------------------|:---------------------|:------------------------------------------------------|
| [**Datatype**](-search-2x-iresultproperty-datatype.md)<br/>         | Schreibgeschützt<br/> | Ein Properties-Datentyp. <br/>                   |
| [**DisplayName**](-search-2x-iresultproperty-displayname.md)<br/>   | Schreibgeschützt<br/> | Lokalisierter Anzeigename der Eigenschaft. <br/>   |
| [**DisplayState**](-search-2x-iresultproperty-displaystate.md)<br/> | Schreibgeschützt<br/> | Sichtbarkeit der Eigenschaft. <br/>               |
| [**Hinweis**](-search-2x-iresultproperty-hint.md)<br/>                 | Schreibgeschützt<br/> | Ein spezieller Wert, der zum Abrufen von Daten verwendet wird. <br/> |
| [**IndexColumn**](-search-2x-iresultproperty-indexcolumn.md)<br/>   | Schreibgeschützt<br/> | Eigenschaftenspaltenname im Index. <br/>      |
| [**UID**](-search-2x-iresultproperty-uid.md)<br/>                   | Schreibgeschützt<br/> | Eindeutiger Bezeichner für die Eigenschaft. <br/>       |



 

## <a name="remarks"></a>Hinweise

Dies sind die Elemente, die Eigenschaften zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur XP mit \[ SP2-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 nur mit \[ SP1-Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows Desktopsuche (WDS) 3.0<br/>                                               |
| Header<br/>                   | <dl> <dt>WdsSharedIDL.h</dt> </dl> |



 

