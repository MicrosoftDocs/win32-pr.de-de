---
title: Sicherheitshärtung der Aufgabe
description: Mithilfe der Funktion zum Sichern von Tasks können Aufgaben Besitzer ihre Aufgaben mit mindestens erforderlichen Berechtigungen ausführen.
ms.assetid: ba03add5-aa05-4bef-baec-684ca17363bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ab70679d605a9ad56c6d26116245ae17d41a7a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206778"
---
# <a name="task-security-hardening"></a>Sicherheitshärtung der Aufgabe

Mithilfe der Funktion zum Sichern von Tasks können Aufgaben Besitzer ihre Aufgaben mit mindestens erforderlichen Berechtigungen ausführen. Beachten Sie, dass diese Funktion standardmäßig aktiviert ist und die Aufgaben Besitzer weitere Anpassungen vornehmen können, indem Sie das Array Task Process Token Security Identifier Type und Task required-Berechtigungen verwenden.

## <a name="task-process-token-sid-type-and-task-required-privileges-array"></a>Task Prozess Token SID-Typ und Task erforderliches Berechtigungs Array

Durch die Angabe von **processtokensidtype** auf der Aufgaben Definitions Ebene können Aufgaben Besitzer einen Task Prozess anfordern, der mit dem SID-Typ "None" oder dem "uneingeschränkten" SID-Typ ausgeführt werden soll. Wenn das Feld in der Aufgabendefinition vorhanden ist, stellt die Überprüfung sicher, dass die Aufgabe UserID den Namen oder die entsprechende SID-Zeichenfolge für eines der integrierten Dienst Konten des Betriebssystems enthält: "Netzwerkdienst" oder "lokaler Dienst".

Der SID-Typ "None" bedeutet, dass der Task in einem Prozess ausgeführt wird, der keine Prozess Token-sid enthält (es werden keine Änderungen an der Liste der prozesstokengruppen vorgenommen). Die Task Prinzipal Konto-sid (LocalService/NetworkService) in diesem Fall hat vollen Zugriff auf das Prozess Token.

Der "uneingeschränkte" SID-Typ bedeutet, dass eine Task-sid vom vollständigen Aufgaben Pfad abgeleitet wird und der Liste der prozesstokengruppen hinzugefügt wird. Beispiel: \\ Microsoft \\ Windows \\ RAC \\ RacTask, das im lokalen Dienst Konto ausgeführt wird, wird die Task-sid von dem Namen Microsoft-Windows-RAC-RACTask abgeleitet, wobei ein "-" ein \\ \\ Ungültiges Benutzernamens Zeichen ist. Der bekannte Gruppenname für die Task-sid wäre "NT Task \\ <modified full task path> " (Domain Name \\ username Format). Die standardmäßige Zugriffs Steuerungs Liste (DACL) des Prozess Tokens wird ebenfalls geändert, um die vollständige Kontrolle über die Task-sid und die SID des lokalen Systems zu ermöglichen, und die Lese Steuerung für die Task Prinzipal Konto-SID. "schtasks.exe/showsid/TN <full task path> " zeigt die Task-SID an, die dem Task entspricht.

Wenn eine nicht-com-Task Aktion gestartet wird, protokolliert die Planungs-Engine das Aufgaben Prinzipal Konto, ruft das Prozess Token ab und fragt die Liste der Berechtigungen ab, die das Token besitzt, und vergleicht dann mit der in "Requirements dprivileges" angegebenen Berechtigungs Liste. Wenn keine Berechtigung in der letzteren angegeben ist, wird diese als "SE- \_ Berechtigung entfernt" markiert \_ . Die ausführbare Aktion wird dann mit dem sich ergebenden Tokenhandle mithilfe der-API von "API" gestartet.

Wenn eine com-Task Aktion gestartet wird, muss Sie durch den taskhost.exe Prozess aktiviert werden. Die Planungs-Engine fragt den Kontext Block der einzelnen laufenden taskhost.exe mit demselben Konto wie die Startaufgabe ab. Wenn festgestellt wird, dass ein Host Prozess mit einer übergeordneten Menge von Berechtigungen gestartet wurde, die der Start Task benötigt, wird dieser Task in diesem Prozess gehostet. Wenn ein solcher Prozess nicht gefunden wird, werden die Härtungs Informationen aller Aufgaben, die in den TasksHosts unter dem Aufgaben Prinzipal Konto ausgeführt werden, mit der angegebenen "Requirements dprivileges"-Maske kombiniert und eine neue Instanz von taskhost.exe gestartet.

Wenn "Requirements dprivileges" in der Aufgabendefinition nicht vorhanden ist, werden die Standard Berechtigungen des Aufgaben Prinzipal Kontos ohne die "SeImpersonatePrivilege"-Berechtigung für den Task Prozess verwendet. Wenn **processtokensidtype** in der Aufgabendefinition nicht vorhanden ist, wird "uneingeschränkt" als Standard verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufgaben Registrierungsinformationen](task-registration-information.md)
</dt> <dt>

[Informationen zum Taskplaner](about-the-task-scheduler.md)
</dt> <dt>

[Sicherheits Kontexte für Tasks](security-contexts-for-running-tasks.md)
</dt> </dl>

 

 




