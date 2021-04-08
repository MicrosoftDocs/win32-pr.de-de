---
title: Comhandleraction. ClassID (Eigenschaft)
description: Ruft bei der Skripterstellung den Bezeichner der Handlerklasse ab oder legt ihn fest.
ms.assetid: 0b5de9ca-2ce2-4f77-bde9-8b8312753c37
keywords:
- ClassID-Eigenschaft Taskplaner
- ClassID-Eigenschaft Taskplaner, comhandleraction-Objekt
- Comhandleraction-Objekt Taskplaner, ClassID-Eigenschaft
topic_type:
- apiref
api_name:
- ComHandlerAction.ClassId
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30409d5ea8067d1148bf42c88e2a3d1bb6f65ad1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740865"
---
# <a name="comhandleractionclassid-property"></a>Comhandleraction. ClassID (Eigenschaft)

Ruft bei der Skripterstellung den Bezeichner der Handlerklasse ab oder legt ihn fest.

## <a name="syntax"></a>Syntax


```VB
ComHandlerAction.ClassId As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Bezeichner der Klasse, die den auszulösende Handler definiert.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML wird die Klasse eines com-Handlers im [**ClassID-**](taskschedulerschema-classid-comhandlertype-element.md) Element des Taskplaner Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**Comhandleraction**](comhandleraction.md)
</dt> </dl>

 

 





