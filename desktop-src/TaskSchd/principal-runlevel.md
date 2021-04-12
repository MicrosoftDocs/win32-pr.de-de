---
title: Principal. Runlevel-Eigenschaft
description: Ruft bei der Skripterstellung den Bezeichner ab, der zum Ausführen der dem Prinzipal zugeordneten Aufgaben verwendet wird, oder legt ihn fest.
ms.assetid: 2ec3d93e-9eef-4590-842c-edfc9232bcdf
keywords:
- Taskplaner der Runlevel-Eigenschaft
- Runlevel-Eigenschaften Taskplaner, Prinzipal Objekt
- Principal-Objekt Taskplaner, Runlevel-Eigenschaft
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
ms.openlocfilehash: 9acb6c4c86215312b2df73f7bf85847ef61a4b96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517906"
---
# <a name="principalrunlevel-property"></a>Principal. Runlevel-Eigenschaft

Ruft bei der Skripterstellung den Bezeichner ab, der zum Ausführen der dem Prinzipal zugeordneten Aufgaben verwendet wird, oder legt ihn fest.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="syntax"></a>Syntax


```VB
Principal.RunLevel As Integer
```



## <a name="property-value"></a>Eigenschaftswert

Der Bezeichner, der verwendet wird, um die Berechtigungsebene anzugeben, die zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.



| Wert                                                                                                                                                                                                                                         | Bedeutung                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="TASK_RUNLEVEL_LUA"></span><span id="task_runlevel_lua"></span><dl> <dt>**Aufgabe \_ Runlevel \_ Lua**</dt> <dt>0</dt> </dl>             | Tasks werden mit den geringsten Berechtigungen (LUA) ausgeführt.<br/> |
| <span id="TASK_RUNLEVEL_HIGHEST"></span><span id="task_runlevel_highest"></span><dl> <dt>**Aufgabe \_ \_Höchste Runlevel**</dt> <dt>1</dt> </dl> | Tasks werden mit den höchsten Berechtigungen ausgeführt.<br/>     |



 

## <a name="remarks"></a>Bemerkungen

Wenn ein Task mit dem integrierten \\ Administrator Konto oder dem lokalen System Konto oder dem lokalen Dienst Konto registriert wird, wird die **Runlevel** -Eigenschaft ignoriert. Der Eigenschafts Wert wird auch ignoriert, wenn die Benutzerkontensteuerung (User Account Control, UAC) ausgeschaltet ist.

Wenn eine Aufgabe mithilfe der Gruppe "Administratoren" für den Sicherheitskontext der Aufgabe registriert wird, müssen Sie die [**Runlevel**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_runlevel) -Eigenschaft auch auf " **Task \_ Runlevel \_** " festlegen, wenn Sie die Aufgabe ausführen möchten. Weitere Informationen finden Sie unter [Sicherheits Kontexte für Aufgaben](security-contexts-for-running-tasks.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Prinzipal**](principal.md)
</dt> </dl>

 

 





