---
title: Principal-Objekt
description: Skript Objekt, das die Sicherheits Anmelde Informationen für einen Prinzipal bereitstellt.
ms.assetid: 9589f3c2-2709-4e71-8986-2347be049f6b
keywords:
- Prinzipal Objekt Taskplaner
- Prinzipal Objekt Taskplaner, beschrieben
topic_type:
- apiref
api_name:
- Principal
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6dc9ff69973fb340bf3b140462c4012499680ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858770"
---
# <a name="principal-object"></a>Principal-Objekt

Skript Objekt, das die Sicherheits Anmelde Informationen für einen Prinzipal bereitstellt. Diese Sicherheits Anmelde Informationen definieren den Sicherheitskontext für die Tasks, die dem Prinzipal zugeordnet sind.

## <a name="members"></a>Member

Das **Prinzipal** Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **Prinzipal** Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                  |
|:--------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DisplayName**](principal-displayname.md)<br/> | Lesen/Schreiben<br/> | Ruft den Namen des Prinzipals ab, der in der Taskplaner Benutzeroberfläche angezeigt wird, oder legt diesen fest.<br/>                                                                |
| [**GroupID**](principal-groupid.md)<br/>         | Lesen/Schreiben<br/> | Ruft den Bezeichner der Benutzergruppe ab, die zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind, oder legt ihn fest.<br/>                           |
| [**Name**](principal-id.md)<br/>                   | Lesen/Schreiben<br/> | Ruft den Bezeichner des Prinzipals ab oder legt ihn fest.<br/>                                                                                                     |
| [**LogonType**](principal-logontype.md)<br/>     | Lesen/Schreiben<br/> | Dient zum Abrufen oder Festlegen der Sicherheits Anmelde Methode, die zum Ausführen der Tasks erforderlich ist, die dem Prinzipal zugeordnet sind.<br/>                                  |
| [**Ausführungs Ebene**](principal-runlevel.md)<br/>       | Lesen/Schreiben<br/> | Ruft den Bezeichner ab oder legt ihn fest, der die Berechtigungsstufe angibt, die zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind.<br/> |
| [**UserID**](principal-userid.md)<br/>           | Lesen/Schreiben<br/> | Ruft die Benutzer-ID ab, die zum Ausführen der Aufgaben erforderlich ist, die dem Prinzipal zugeordnet sind, oder legt Sie fest.<br/>                                        |



 

## <a name="remarks"></a>Bemerkungen

Beachten Sie beim Angeben eines Kontos, dass Sie den doppelten umgekehrten Schrägstrich im Code verwenden, um die Domäne und den Benutzernamen anzugeben. Verwenden Sie z. b \\ \\ . den Domänen Benutzernamen, um einen Wert für die [**UserID**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid) -Eigenschaft anzugeben.

Beim Lesen oder Schreiben von XML für eine Aufgabe werden die Sicherheits Anmelde Informationen für einen Prinzipal im [**Principal**](taskschedulerschema-principal-principaltype-element.md) -Element des Taskplaner-Schemas angegeben.

Wenn eine Aufgabe mit dem at.exe-Befehlszeilen Tool registriert wird und dieses Objekt zum Abrufen von Informationen über den Task verwendet wird, gibt die [**logontype**](principal-logontype.md) -Eigenschaft den Wert 0 zurück, die [**Runlevel**](principal-runlevel.md) -Eigenschaft gibt 0 zurück, und die [**UserID**](principal-userid.md) -Eigenschaft gibt nichts zurück.

## <a name="examples"></a>Beispiele

Weitere Informationen und Beispielcode für dieses Skript Objekt finden Sie unter [time-auslöserbeispiel (Skripterstellung)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                    |
| Typbibliothek<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





