---
title: RunningTask-Objekt
description: Skripterstellungsobjekt, das die Methoden zum Abrufen von Informationen aus einer ausgeführten Aufgabe und zum Steuern einer ausgeführten Aufgabe bereitstellt.
ms.assetid: 335e69d8-affa-4845-a067-641184e0f7df
keywords:
- RunningTask-Objekt Taskplaner
- RunningTask-Objekt Taskplaner beschrieben
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
ms.openlocfilehash: b0dea9d0810c12af383092e4cad7f77be601927f2a440efbbbb424f822159a31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866870"
---
# <a name="runningtask-object"></a>RunningTask-Objekt

Skripterstellungsobjekt, das die Methoden zum Abrufen von Informationen aus einer ausgeführten Aufgabe und zum Steuern einer ausgeführten Aufgabe bereitstellt.

## <a name="members"></a>Member

Das **RunningTask-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **RunningTask-Objekt** verfügt über diese Methoden.



| Methode                                 | BESCHREIBUNG                                                           |
|:---------------------------------------|:----------------------------------------------------------------------|
| [**Aktualisieren**](runningtask-refresh.md) | Aktualisiert alle lokalen Instanzvariablen der Aufgabe.<br/> |
| [**Beenden**](runningtask-stop.md)       | Beendet diese Instanz des Tasks.<br/>                           |



 

### <a name="properties"></a>Eigenschaften

Das **RunningTask-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                      | Zugriffstyp          | BESCHREIBUNG                                                                         |
|:--------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------|
| [**CurrentAction**](runningtask-currentaction.md)<br/> | Schreibgeschützt<br/> | Ruft den Namen der aktuellen Aktion ab, die der ausgeführte Task ausführt.<br/> |
| [**EnginePID**](runningtask-enginepid.md)<br/>         | Schreibgeschützt<br/> | Ruft die Prozess-ID für die Engine (Prozess) ab, die den Task ausführt.<br/>  |
| [**InstanceGuid**](runningtask-instanceguid.md)<br/>   | Schreibgeschützt<br/> | Ruft den GUID-Bezeichner für diese Instanz der Aufgabe ab.<br/>                  |
| [**Name**](runningtask-name.md)<br/>                   | Schreibgeschützt<br/> | Ruft den Namen des Tasks ab.<br/>                                               |
| [**Pfad**](runningtask-path.md)<br/>                   | Schreibgeschützt<br/> | Ruft den Pfad zum Ort ab, an dem die Aufgabe gespeichert wird.<br/>                               |
| [**State**](runningtask-state.md)<br/>                 | Schreibgeschützt<br/> | Ruft den Status des ausgeführten Tasks ab. <br/>                                     |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Taskplaner-Objekte](task-scheduler-objects.md)
</dt> <dt>

[Aufgabenplanung](task-scheduler-start-page.md)
</dt> <dt>

[**RunningTaskCollection**](runningtaskcollection.md)
</dt> <dt>

[**RegisteredTask.Run**](registeredtask-run.md)
</dt> <dt>

[**RegisteredTask.RunEx**](registeredtask-runex.md)
</dt> </dl>

 

 





