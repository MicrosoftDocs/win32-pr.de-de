---
title: ComHandlerAction.ClassId (Eigenschaft)
description: Für die Skripterstellung ruft den Bezeichner der Handlerklasse ab oder legt diesen fest.
ms.assetid: 0b5de9ca-2ce2-4f77-bde9-8b8312753c37
keywords:
- ClassId-Taskplaner
- ClassId-Eigenschaft Taskplaner , ComHandlerAction-Objekt
- ComHandlerAction-Objekt Taskplaner , ClassId-Eigenschaft
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
ms.openlocfilehash: 72338d4fe15936fcfe8f158098a798c4a3630cbd0587f46dc2f9346405477a59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100460"
---
# <a name="comhandleractionclassid-property"></a>ComHandlerAction.ClassId (Eigenschaft)

Für die Skripterstellung ruft den Bezeichner der Handlerklasse ab oder legt diesen fest.

## <a name="syntax"></a>Syntax


```VB
ComHandlerAction.ClassId As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Bezeichner der Klasse, die den zu ausgelösten Handler definiert.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML wird die Klasse eines COM-Handlers im [**ClassId-Element**](taskschedulerschema-classid-comhandlertype-element.md) des Taskplaner angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**ComHandlerAction**](comhandleraction.md)
</dt> </dl>

 

 





