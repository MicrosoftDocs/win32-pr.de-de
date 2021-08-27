---
title: ExecAction.Arguments-Eigenschaft
description: Ruft für die Skripterstellung die Argumente ab, die dem Befehlszeilenvorgang zugeordnet sind, oder legt sie fest.
ms.assetid: 911e720f-ea7b-474d-ac75-4cd4f9adee55
keywords:
- Arguments-Eigenschaft Taskplaner
- Arguments-Eigenschaft Taskplaner , ExecAction-Objekt
- ExecAction-Objekt Taskplaner , Arguments-Eigenschaft
topic_type:
- apiref
api_name:
- ExecAction.Arguments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 899e4ceaaf3a0d04dc678592add18184401d54569fea71f0570a0acbf2a33027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011490"
---
# <a name="execactionarguments-property"></a>ExecAction.Arguments-Eigenschaft

Ruft für die Skripterstellung die Argumente ab, die dem Befehlszeilenvorgang zugeordnet sind, oder legt sie fest.

## <a name="syntax"></a>Syntax


```VB
ExecAction.Arguments As String
```



## <a name="property-value"></a>Eigenschaftswert

Die Argumente, die für den Befehlszeilenvorgang erforderlich sind.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML werden die Befehlszeilenvorgangsargumente im [**Arguments-Element**](taskschedulerschema-arguments-exectype-element.md) des Taskplaner Schemas angegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





