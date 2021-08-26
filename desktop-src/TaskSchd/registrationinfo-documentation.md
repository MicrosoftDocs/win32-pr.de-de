---
title: RegistrationInfo.Documentation-Eigenschaft
description: Für die Skripterstellung ruft eine zusätzliche Dokumentation für die Aufgabe ab oder legt diese fest.
ms.assetid: 12ce9461-0cc7-49d0-8c57-7ff3ca32850a
keywords:
- Dokumentationseigenschaft Taskplaner
- Dokumentationseigenschaft Taskplaner , RegistrationInfo-Objekt
- RegistrationInfo-Taskplaner , Dokumentationseigenschaft
topic_type:
- apiref
api_name:
- RegistrationInfo.Documentation
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31878417d6a225c5fa7c67569d557a4c6d7a716a24bffd94dfe58a84e3809a37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100180"
---
# <a name="registrationinfodocumentation-property"></a>RegistrationInfo.Documentation-Eigenschaft

Für die Skripterstellung ruft eine zusätzliche Dokumentation für die Aufgabe ab oder legt diese fest.

## <a name="syntax"></a>Syntax


```VB
RegistrationInfo.Documentation As String
```



## <a name="property-value"></a>Eigenschaftswert

Jede zusätzliche Dokumentation, die der Aufgabe zugeordnet ist.

## <a name="remarks"></a>Hinweise

Beim Lesen oder Schreiben von XML für eine Aufgabe wird die zusätzliche Dokumentation für die Aufgabe mithilfe des [**Documentation-Elements**](taskschedulerschema-documentation-registrationinfotype-element.md) des Taskplaner angegeben.

Beim Festlegen dieses Eigenschaftswerts kann der Wert Text sein, der aus einer Ressourcendatei .dll wird. Eine spezialisierte Zeichenfolge wird verwendet, um auf den Text aus der Ressourcendatei zu verweisen. Das Format der Zeichenfolge ist $(@ Dll , ResourceID ), wobei DLL der Pfad zur .dll-Datei ist, die die Ressource enthält, und ResourceID der Bezeichner für den \[ \] \[ \] \[ \] \[ \] Ressourcentext ist. Wenn Sie diesen Eigenschaftswert beispielsweise auf $(@ %SystemRoot% System32ResourceName.dll, -101) festlegen, wird die -Eigenschaft auf den Wert des Ressourcentexts mit einem Bezeichner gleich \\ \\ -101 in der Datei %SystemRoot% \\ System32 \\ResourceName.dll festgelegt.

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
</dt> </dl>

 

 





