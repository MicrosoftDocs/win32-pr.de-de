---
title: ExecAction-Objekt
description: Skripterstellungsobjekt, das eine Aktion darstellt, die einen Befehlszeilenvorgang ausgeführt.
ms.assetid: 51d2746d-3a90-4e8b-ac2b-d73193b3aa74
keywords:
- Aktion ausführen Taskplaner , Schnittstelle
- ExecAction-Taskplaner
- ExecAction-Objekt Taskplaner , beschrieben
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
ms.openlocfilehash: 140ff991bd26f779beee7407666572d8649bd9f1a2718b719713770745157656
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072660"
---
# <a name="execaction-object"></a>ExecAction-Objekt

Skripterstellungsobjekt, das eine Aktion darstellt, die einen Befehlszeilenvorgang ausgeführt.

## <a name="members"></a>Member

Das **ExecAction-Objekt** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **ExecAction-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp           | BESCHREIBUNG                                                                                                                       |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [**Argumente**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)<br/>               | Lesen/Schreiben<br/> | Ruft die Argumente ab, die dem Befehlszeilenvorgang zugeordnet sind, oder legt sie fest.<br/>                                                 |
| [**Id**](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_id)<br/>                                 | Lesen/Schreiben<br/> | Geerbt vom [**Action-Objekt.**](action.md) Ruft den Bezeichner der Aktion ab oder legt den Bezeichner fest.<br/>                         |
| [**Pfad**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path)<br/>                         | Lesen/Schreiben<br/> | Ruft den Pfad zu einer ausführbaren Datei ab oder legt diesen fest.<br/>                                                                           |
| [**type**](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_type)<br/>                             | Schreibgeschützt<br/>  | Geerbt vom [**Action-Objekt.**](action.md) Ruft den Typ der Aktion ab.<br/>                                       |
| [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory)<br/> | Lesen/Schreiben<br/> | Ruft das Verzeichnis ab, das entweder die ausführbare Datei oder die von der ausführbaren Datei verwendeten Dateien enthält, oder legt dieses fest.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn Umgebungsvariablen in den Eigenschaften [**Path,**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path) [**Arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)oder [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) verwendet werden, werden die Werte der Umgebungsvariablen zwischengespeichert und verwendet, wenn der Taskeng.exe (die Task-Engine) gestartet wird. Änderungen an den Umgebungsvariablen, die nach dem Start der Task-Engine auftreten, werden von der Task-Engine nicht verwendet.

Diese Aktion führt einen Befehlszeilenvorgang aus. Die Aktion kann z. B. ein Skript ausführen oder eine ausführbare Datei starten.

Beim Lesen oder Schreiben von XML wird eine Ausführungsaktion im [**Exec-Element**](taskschedulerschema-exec-actiongroup-element.md) des Taskplaner angegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skriptobjekt finden Sie unter [Time Trigger Example (Scripting) .](time-trigger-example--scripting-.md)

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





