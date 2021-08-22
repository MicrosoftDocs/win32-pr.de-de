---
title: Tasksicherheitshärtung
description: Die Verwendung der Sicherheitshärtungsfunktion "Tasks" ermöglicht Es Taskbesitzern, ihre Aufgaben mit minimal erforderlichen Berechtigungen auszuführen.
ms.assetid: ba03add5-aa05-4bef-baec-684ca17363bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e41117b5317d4cd625ad991db1fdab1428d8748e86f372b2fc5c6e189112a1b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118858741"
---
# <a name="task-security-hardening"></a>Tasksicherheitshärtung

Die Verwendung der Sicherheitshärtungsfunktion "Tasks" ermöglicht Es Taskbesitzern, ihre Aufgaben mit minimal erforderlichen Berechtigungen auszuführen. Beachten Sie, dass diese Funktion standardmäßig aktiviert ist und Taskbesitzer weitere Anpassungen vornehmen können, indem sie den Sicherheitsbezeichnertyp des Taskprozesses und das Array mit den erforderlichen Aufgabenberechtigungen verwenden.

## <a name="task-process-token-sid-type-and-task-required-privileges-array"></a>Taskprozesstoken-SID-Typ und Array der erforderlichen Taskberechtigungen

Wenn **ProcessTokenSidType** auf Taskdefinitionsebene angegeben wird, können Taskbesitzer anfordern, dass ein Taskprozess mit dem SID-Typ "none" oder dem SID-Typ "unrestricted" ausgeführt wird. Wenn das Feld in der Aufgabendefinition vorhanden ist, stellt die Überprüfung sicher, dass die UserId des Tasks den Namen oder die entsprechende SID-Zeichenfolge für eines dieser integrierten Betriebssystemdienstkonten enthält: "NETWORK SERVICE" oder "LOCAL SERVICE".

Der SID-Typ "none" bedeutet, dass der Task in einem Prozess ausgeführt wird, der keine Prozesstoken-SID enthält (an der Liste der Prozesstokengruppen werden keine Änderungen vorgenommen). Die Sid des Aufgabenprinzipalkontos (LocalService/NetworkService) hat in diesem Fall Vollzugriff auf das Prozesstoken.

Der SID-Typ "unrestricted" bedeutet, dass eine Task-SID vom vollständigen Aufgabenpfad abgeleitet und der Liste der Prozesstokengruppen hinzugefügt wird. Beispielsweise wird die \\ Microsoft \\ Windows \\ \\ RAC-RACTask, die im lokalen Dienstkonto ausgeführt wird, die Task-SID vom Namen Microsoft-Windows-RAC-RACTask abgeleitet, wobei ein "-" durch "" ersetzt \\ wird, da " ein \\ ungültiges Benutzernamenzeichen ist. Der bekannte Gruppenname für die Task-SID lautet "NT \\ <modified full task path> TASK" \\ (Domänenname-Benutzernamenformat). Die standardmäßige DACL (Discretionary Access Control List) des Prozesstokens wird ebenfalls geändert, um die vollständige Kontrolle nur für die Task-SID und die lokale System-SID zu ermöglichen und die Steuerung auf die SID des Aufgabenprinzipalkontos zu lesen. "schtasks.exe /showsid /tn" <full task path> zeigt die Task-SID an, die der Aufgabe entspricht.

Wenn eine Nicht-COM-Taskaktion gestartet wird, protokolliert die Planungs-Engine das Aufgabenprinzipalkonto, ruft das Prozesstoken ab und fragt die Liste der Berechtigungen ab, über die das Token verfügt, und vergleicht diese dann mit der unter RequiredPrivileges angegebenen Berechtigungsliste. Wenn in letzterem keine Berechtigung angegeben ist, wird dies als SE \_ PRIVILEGE \_ REMOVED markiert. Die ausführbare Aktion wird dann mit dem resultierenden Tokenhandle mithilfe der CreateProcessAsUser-API gestartet.

Wenn eine COM-Taskaktion gestartet wird, muss sie vom taskhost.exe Prozess aktiviert werden. Die Planungs-Engine fragt den Kontextblock jedes ausgeführten taskhost.exe mit demselben Konto wie die Startaufgabe ab. Wenn festgestellt wird, dass ein Hostprozess mit einer Übermenge von Berechtigungen gestartet wurde, die der Starttask benötigt, wird dieser Task in diesem Prozess gehostet. Wenn ein solcher Prozess nicht gefunden wird, kombiniert er die Härtungsinformationen aller Aufgaben, die in den taskhosts unter dem Aufgabenprinzipalkonto ausgeführt werden, mit der angegebenen RequiredPrivileges-Maske und startet dann eine neue Instanz von taskhost.exe.

Wenn RequiredPrivileges in der Aufgabendefinition nicht vorhanden ist, werden die Standardberechtigungen des Aufgabenprinzipalkontos ohne SeImpersonatePrivilege für den Taskprozess verwendet. Wenn **ProcessTokenSidType** in der Taskdefinition nicht vorhanden ist, wird "unrestricted" als Standard verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Aufgabenregistrierung](task-registration-information.md)
</dt> <dt>

[Informationen zum Taskplaner](about-the-task-scheduler.md)
</dt> <dt>

[Sicherheitskontexte für Aufgaben](security-contexts-for-running-tasks.md)
</dt> </dl>

 

 




