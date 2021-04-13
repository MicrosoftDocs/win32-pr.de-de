---
title: Runningtask-Objekt
description: Skript Objekt, das die Methoden bereitstellt, um Informationen aus einer laufenden Aufgabe zu erhalten und zu steuern.
ms.assetid: 335e69d8-affa-4845-a067-641184e0f7df
keywords:
- Runningtask-Objekt Taskplaner
- Runningtask-Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- RunningTask
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 261be07f71d0d35f5d3140de1b39574b635a531e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518209"
---
# <a name="runningtask-object"></a>Runningtask-Objekt

Skript Objekt, das die Methoden bereitstellt, um Informationen aus einer laufenden Aufgabe zu erhalten und zu steuern.

## <a name="members"></a>Member

Das **runningtask** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **runningtask** -Objekt verfügt über diese Methoden.



| Methode                                 | BESCHREIBUNG                                                           |
|:---------------------------------------|:----------------------------------------------------------------------|
| [**Aktualisieren**](runningtask-refresh.md) | Aktualisiert alle lokalen Instanzvariablen der Aufgabe.<br/> |
| [**Stop**](runningtask-stop.md)       | Beendet diese Instanz der Aufgabe.<br/>                           |



 

### <a name="properties"></a>Eigenschaften

Das **runningtask** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                      | Zugriffstyp          | BESCHREIBUNG                                                                         |
|:--------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**Currentaction**](runningtask-currentaction.md)<br/> | Schreibgeschützt<br/> | Ruft den Namen der aktuellen Aktion ab, die der laufende Task ausführt.<br/> |
| [**Enginepid**](runningtask-enginepid.md)<br/>         | Schreibgeschützt<br/> | Ruft die Prozess-ID für die Engine (Prozess) ab, in der die Aufgabe ausgeführt wird.<br/>  |
| [**GUID**](runningtask-instanceguid.md)<br/>   | Schreibgeschützt<br/> | Ruft den GUID-Bezeichner für diese Instanz der Aufgabe ab.<br/>                  |
| [**Name**](runningtask-name.md)<br/>                   | Schreibgeschützt<br/> | Ruft den Namen des Tasks ab.<br/>                                               |
| [**ADS**](runningtask-path.md)<br/>                   | Schreibgeschützt<br/> | Ruft den Pfad zum Speicherort der Aufgabe ab.<br/>                               |
| [**State**](runningtask-state.md)<br/>                 | Schreibgeschützt<br/> | Ruft den Zustand der aktuell laufenden Aufgabe ab. <br/>                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner Objekte](task-scheduler-objects.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**Runningtaskcollection**](runningtaskcollection.md)
</dt> <dt>

[**Registeredtask. Run**](registeredtask-run.md)
</dt> <dt>

[**Registeredtask. RunEx**](registeredtask-runex.md)
</dt> </dl>

 

 





