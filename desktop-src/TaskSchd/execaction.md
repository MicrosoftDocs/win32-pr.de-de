---
title: Execaction-Objekt
description: Skript Objekt, das eine Aktion darstellt, die einen Befehlszeilen Vorgang ausführt.
ms.assetid: 51d2746d-3a90-4e8b-ac2b-d73193b3aa74
keywords:
- Aktion Taskplaner ausführen, Schnittstelle
- Execaction-Objekt Taskplaner
- Taskplaner des execaction-Objekts, beschrieben
topic_type:
- apiref
api_name:
- ExecAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cddd1b9b44612b4ce896fb3ceb99a6deeaa5e3a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105692"
---
# <a name="execaction-object"></a>Execaction-Objekt

Skript Objekt, das eine Aktion darstellt, die einen Befehlszeilen Vorgang ausführt.

## <a name="members"></a>Member

Das **execaction** -Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **execaction** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp           | BESCHREIBUNG                                                                                                                       |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**Argumente**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)<br/>               | Lesen/Schreiben<br/> | Ruft die Argumente ab, die dem Befehlszeilen Vorgang zugeordnet sind, oder legt Sie fest.<br/>                                                 |
| [**Name**](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_id)<br/>                                 | Lesen/Schreiben<br/> | Wird vom [**Action**](action.md) -Objekt geerbt. Ruft den Bezeichner der Aktion ab oder legt ihn fest.<br/>                         |
| [**ADS**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path)<br/>                         | Lesen/Schreiben<br/> | Ruft den Pfad zu einer ausführbaren Datei ab oder legt diesen fest.<br/>                                                                           |
| [**type**](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_type)<br/>                             | Schreibgeschützt<br/>  | Wird vom [**Action**](action.md) -Objekt geerbt. Ruft den Typ der Aktion ab.<br/>                                       |
| [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory)<br/> | Lesen/Schreiben<br/> | Ruft das Verzeichnis ab, das entweder die ausführbare Datei oder die Dateien enthält, die von der ausführbaren Datei verwendet werden, oder legt dieses fest.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Wenn Umgebungsvariablen in den [**path**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path)-, [**Arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)-oder [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) -Eigenschaften verwendet werden, werden die Werte der Umgebungsvariablen zwischengespeichert und verwendet, wenn die Taskeng.exe (Task-Engine) gestartet wird. Änderungen an den Umgebungsvariablen, die nach dem Start der Task-Engine auftreten, werden von der Task-Engine nicht verwendet.

Diese Aktion führt einen Befehlszeilen Vorgang aus. Beispielsweise könnte die Aktion ein Skript ausführen oder eine ausführbare Datei starten.

Beim Lesen oder Schreiben von XML wird im [**exec**](taskschedulerschema-exec-actiongroup-element.md) -Element des Taskplaner Schemas eine Ausführungs Aktion angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





