---
title: Execaction. WorkingDirectory-Eigenschaft
description: Ruft bei der Skripterstellung das Verzeichnis ab, das entweder die ausführbare Datei oder die Dateien enthält, die von der ausführbaren Datei verwendet werden, oder legt dieses fest.
ms.assetid: 7b1e3c9d-ba08-4812-b50e-f97b6c12f8bd
keywords:
- WorkingDirectory-Eigenschaft Taskplaner
- WorkingDirectory-Eigenschaft Taskplaner, execaction-Objekt
- Execaction-Objekt Taskplaner, WorkingDirectory-Eigenschaft
topic_type:
- apiref
api_name:
- ExecAction.WorkingDirectory
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28d4755b6f760ed1af75c676ecb70074c3ea7c92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337309"
---
# <a name="execactionworkingdirectory-property"></a>Execaction. WorkingDirectory-Eigenschaft

Ruft bei der Skripterstellung das Verzeichnis ab, das entweder die ausführbare Datei oder die Dateien enthält, die von der ausführbaren Datei verwendet werden, oder legt dieses fest.

## <a name="syntax"></a>Syntax


```VB
ExecAction.WorkingDirectory As String
```



## <a name="property-value"></a>Eigenschaftswert

Das Verzeichnis, das entweder die ausführbare Datei oder die Dateien enthält, die von der ausführbaren Datei verwendet werden.

## <a name="remarks"></a>Bemerkungen

Beim Lesen oder Schreiben von XML wird das Arbeitsverzeichnis der Anwendung im [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) -Element des Taskplaner-Schemas angegeben.

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

 

 





