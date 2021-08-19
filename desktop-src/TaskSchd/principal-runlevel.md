---
title: Principal.RunLevel-Eigenschaft
description: Ruft für die Skripterstellung den Bezeichner ab, der zum Angeben der Berechtigungsstufe verwendet wird, die zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind, oder legt diesen fest.
ms.assetid: 2ec3d93e-9eef-4590-842c-edfc9232bcdf
keywords:
- Taskplaner der RunLevel-Eigenschaft
- RunLevel-Eigenschaft Taskplaner , Principal-Objekt
- Prinzipalobjekt Taskplaner , RunLevel-Eigenschaft
topic_type:
- apiref
api_name:
- Principal.RunLevel
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be2bc9552ac8650bb2cf9ca40944a480683f2ef6dc6cccecfc5ed34eb544ca6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126130"
---
# <a name="principalrunlevel-property"></a>Principal.RunLevel-Eigenschaft

Ruft für die Skripterstellung den Bezeichner ab, der zum Angeben der Berechtigungsstufe verwendet wird, die zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind, oder legt diesen fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Principal.RunLevel As Integer
```



## <a name="property-value"></a>Eigenschaftswert

Der Bezeichner, der verwendet wird, um die Berechtigungsstufe anzugeben, die zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.



| Wert                                                                                                                                                                                                                                         | Bedeutung                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="TASK_RUNLEVEL_LUA"></span><span id="task_runlevel_lua"></span><dl> <dt>**TASK \_ RUNLEVEL \_ LUA**</dt> <dt>0</dt> </dl>             | Tasks werden mit den geringsten Berechtigungen (LUA) ausgeführt.<br/> |
| <span id="TASK_RUNLEVEL_HIGHEST"></span><span id="task_runlevel_highest"></span><dl> <dt>**TASK \_ RUNLEVEL \_ HIGHEST**</dt> <dt>1</dt> </dl> | Tasks werden mit den höchsten Berechtigungen ausgeführt.<br/>     |



 

## <a name="remarks"></a>Hinweise

Wenn eine Aufgabe mithilfe des integrierten \\ Administratorkontos oder des lokalen Systems oder des lokalen Dienstkontos registriert wird, wird die **RunLevel-Eigenschaft** ignoriert. Der Eigenschaftswert wird auch ignoriert, wenn die Benutzerkontensteuerung (User Account Control, UAC) deaktiviert ist.

Wenn eine Aufgabe mithilfe der Gruppe Administratoren für den Sicherheitskontext der Aufgabe registriert wird, müssen Sie auch die [**RunLevel-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) auf **TASK \_ RUNLEVEL \_ HIGHEST** festlegen, wenn Sie den Task ausführen möchten. Weitere Informationen finden Sie unter [Sicherheitskontexte für Tasks.](security-contexts-for-running-tasks.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Prinzipal**](principal.md)
</dt> </dl>

 

 





