---
title: Iresulttype-Schnittstelle (wdssharedidl. h)
description: Macht Eigenschaftentyp Informationen verfügbar.
ms.assetid: 68abd470-2505-4836-a17f-f1c14157f8e7
keywords:
- Iresulttype-Schnittstelle Legacy Windows-Umgebungs Features
- Iresulttype-Schnittstelle Legacy Windows-Umgebungs Features, beschrieben
topic_type:
- apiref
api_name:
- IResultType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88451739a6ca2eb600838ea137ebc1ddba98f3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476128"
---
# <a name="iresulttype-interface"></a>Iresulttype-Schnittstelle

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen die [Windows Search-API](../search/-search-reference-entry-page.md) . 

Macht Eigenschaftentyp Informationen verfügbar.

## <a name="members"></a>Member

Die **iresulttype** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iresulttype** verfügt auch über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **iresulttype** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                 | Zugriffstyp           | BESCHREIBUNG                                                                           |
|:-------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------|
| [**DisplayName**](-search-2x-iresulttype-displayname.md)<br/>     | Schreibgeschützt<br/>  | Lokalisierter Anzeige Name des Typs:<br/>                                        |
| [**GetProperty**](-search-2x-iresulttype-getproperty.md)<br/>     | Lesen/Schreiben<br/> | Diese Eigenschaft enthält angegebene Eigenschafts Informationen. <br/>                    |
| [**Preceivedtype**](-search-2x-iresulttype-preceivedtype.md)<br/> | Schreibgeschützt<br/>  | Diese Eigenschaft enthält die Zeichenfolge, mit der der Typ im Index identifiziert wird. <br/> |
| [**PropertyCount**](-search-2x-iresulttype-propertycount.md)<br/> | Schreibgeschützt<br/>  | Diese Eigenschaft enthält die Anzahl der Eigenschaften, die vom-Typ verfügbar gemacht werden. <br/>      |
| [**UID**](-search-2x-iresulttype-uid.md)<br/>                     | Schreibgeschützt<br/>  | Diese Eigenschaft enthält den eindeutigen Bezeichner für den Typ. <br/>                |



 

## <a name="remarks"></a>Bemerkungen

Diese Methoden machen die Typen der zurückgegebenen Informationen verfügbar.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP mit SP2 \[ Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2003 mit SP1 \[ Desktop-Apps\]<br/>                             |
| Verteilbare Komponente<br/>          | Windows-Desktop Suche (WDS) 3,0<br/>                                               |
| Header<br/>                   | <dl> <dt>Wdssharedidl. h</dt> </dl> |



 

