---
title: Execaction. Path-Eigenschaft
description: Bei der Skripterstellung wird der Pfad zu einer ausführbaren Datei abgerufen oder festgelegt.
ms.assetid: 00fea05f-4f57-47ac-9812-8cd352fe02a8
keywords:
- Pfadeigenschaft Taskplaner
- Pfadeigenschaft Taskplaner, execaction-Objekt
- Execaction-Objekt Taskplaner, Path-Eigenschaft
topic_type:
- apiref
api_name:
- ExecAction.Path
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b20e1dcd8cd9700f961eb944c7be3168582b8c55
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740857"
---
# <a name="execactionpath-property"></a>Execaction. Path-Eigenschaft

Bei der Skripterstellung wird der Pfad zu einer ausführbaren Datei abgerufen oder festgelegt.

## <a name="syntax"></a>Syntax


```VB
ExecAction.Path As String
```



## <a name="property-value"></a>Eigenschaftswert

Der Pfad zu der ausführbaren Datei, die von der Aktion ausgeführt werden soll.

## <a name="remarks"></a>Bemerkungen

Diese Aktion führt einen Befehlszeilen Vorgang aus. Beispielsweise könnte die Aktion ein Skript ausführen oder eine ausführbare Datei starten.

Beim Lesen oder Schreiben von XML wird der Befehlszeilen-Vorgangs Pfad im [**Command**](taskschedulerschema-command-exectype-element.md) -Element des Taskplaner-Schemas angegeben.

Der Pfad wird geprüft, um sicherzustellen, dass er gültig ist, wenn die Aufgabe registriert wird, und nicht, wenn diese Eigenschaft festgelegt ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Execaction**](execaction.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> </dl>

 

 





