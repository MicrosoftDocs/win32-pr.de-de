---
title: Trigger.Id-Eigenschaft
description: Ruft für die Skripterstellung den Bezeichner für den Trigger ab oder legt den Bezeichner fest.
ms.assetid: 15dd3aaa-f3ee-459d-a0bd-327c7a4beb03
keywords:
- Id-Eigenschaft Taskplaner
- ID-Eigenschaft Taskplaner , Trigger-Objekt
- Triggerobjekt Taskplaner , ID-Eigenschaft
topic_type:
- apiref
api_name:
- Trigger.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2c9ff851eab7b5e9cfb124bf03c83986d24b391d5ea109865ff2d59e2e33536
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002158"
---
# <a name="triggerid-property"></a>Trigger.Id-Eigenschaft

Ruft für die Skripterstellung den Bezeichner für den Trigger ab oder legt den Bezeichner fest.

## <a name="syntax"></a>Syntax


```VB
Trigger.Id As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Bezeichner für den Trigger. Dieser Bezeichner wird vom Taskplaner zu Protokollierungszwecken verwendet.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird der Triggerbezeichner im Id-Attribut der einzelnen Triggerelemente (z. B. das Id-Attribut des [**BootTrigger-Elements)**](taskschedulerschema-boottrigger-triggergroup-element.md) des Taskplaner Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





