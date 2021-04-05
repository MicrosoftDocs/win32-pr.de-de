---
title: Task Aktionen
description: Die Arbeitselemente, die von einer Aufgabe ausgeführt werden, werden als Aktionen bezeichnet. Eine Aufgabe kann eine einzelne Aktion oder maximal 32 Aktionen aufweisen. Beachten Sie, dass beim Angeben mehrerer Aktionen sequenziell ausgeführt wird.
ms.assetid: 4cbe739d-4c4e-4469-8289-4be41b93950c
keywords:
- Aktionen Taskplaner
- Aktionen Taskplaner, beschrieben
- Aktionen Taskplaner, Aktion ausführen
- Aktionen Taskplaner, com-handleraktion
- Aktion Taskplaner ausführen
- Aktionen des com-Handlers Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71003e2cea5febfab61617451f3b6ebef4a244a3
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/11/2020
ms.locfileid: "103722058"
---
# <a name="task-actions"></a>Task Aktionen

Die Arbeitselemente, die von einer Aufgabe ausgeführt werden, werden als Aktionen bezeichnet. Eine Aufgabe kann eine einzelne Aktion oder maximal 32 Aktionen aufweisen. Beachten Sie, dass beim Angeben mehrerer Aktionen sequenziell ausgeführt wird.

## <a name="types-of-actions"></a>Aktionstypen

In der folgenden Tabelle von Aktionen werden der Typ der Arbeit oder Aktionen beschrieben, die von einer Aufgabe ausgeführt werden können.

| Aktionstyp      | BESCHREIBUNG                                                             |
|---------------------|-------------------------------------------------------------------------|
| Comhandleraktion   | Diese Aktion löst einen com-Handler aus.                                        |
| Exec-Aktion         | Diese Aktion führt einen Befehlszeilen Vorgang aus, z. b. das Starten von Notepad. |
| E-Mail-Aktion       | Diese Aktion sendet eine e-Mail, wenn ein Task ausgelöst wird.                    |
| Nachricht anzeigen (Aktion) | Diese Aktion zeigt ein Meldungs Feld mit einer angegebenen Meldung und einem angegebenen Titel an.     |



 

## <a name="specifying-actions"></a>Festlegen von Aktionen

Die Aktionen einer Aufgabe werden angegeben, wenn der Task definiert und in einer Auflistung von Aktionen gespeichert wird, die vom Taskplaner Dienst verwendet werden. In der folgenden Tabelle sind Links zu Referenz Themen für die APIs und XML-Elemente aufgelistet, die Aktionen zugeordnet sind.

Weitere Informationen und Beispiele zur Verwendung der Taskplaner Schnittstellen, Skript Objekte und XML finden [Sie unter Verwenden der Taskplaner](using-the-task-scheduler.md).

### <a name="interface-apis-for-c-development"></a>Interface-APIs für die C++-Entwicklung



| API                                                                    | BESCHREIBUNG                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**Actions-Eigenschaft von itaskdefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) | Ruft die von der Aufgabe ausgeführten Aktionen ab oder legt Sie fest.              |
| [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection)                         | Enthält die Aktionen, die vom Task ausgeführt werden.                  |
| [**Icomhandleraction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)                         | Stellt eine Aktion dar, die einen Handler auslöst.                   |
| [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction)                                     | Stellt eine Aktion dar, die einen Befehlszeilen Vorgang ausführt. |
| [**Iemailaction**](/windows/desktop/api/taskschd/nn-taskschd-iemailaction)                                   | Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.            |
| [**Ishowmessageaction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction)                       | Stellt eine Aktion dar, die ein Meldungs Feld anzeigt.               |



 

### <a name="scripting-object-apis-for-scripting-development"></a>Skript Objekt-APIs für die Skript Entwicklung



| API                                                      | BESCHREIBUNG                                                  |
|----------------------------------------------------------|--------------------------------------------------------------|
| [**Task Definition. Actions**](taskdefinition-actions.md) | Ruft die von der Aufgabe ausgeführten Aktionen ab oder legt Sie fest.              |
| [**ActionCollection**](actioncollection.md)             | Enthält die Aktionen, die vom Task ausgeführt werden.                  |
| [**Comhandleraction**](comhandleraction.md)             | Stellt eine Aktion dar, die einen Handler auslöst.                   |
| [**Execaction**](execaction.md)                         | Stellt eine Aktion dar, die einen Befehlszeilen Vorgang ausführt. |
| [**Emailaction**](emailaction.md)                       | Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.            |
| [**Showmessageaction**](showmessageaction.md)           | Stellt eine Aktion dar, die ein Meldungs Feld anzeigt.               |



 

### <a name="xml-elements"></a>XML-Elemente



| Element                                                                    | BESCHREIBUNG                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [**Aktionen**](taskschedulerschema-actions-tasktype-element.md)            | Definiert die Aktionen, die von der Aufgabe ausgeführt werden.                   |
| [**Comhandler**](taskschedulerschema-comhandler-actiongroup-element.md)   | Stellt eine Aktion dar, die einen Handler auslöst.                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | Stellt eine Aktion dar, die einen Befehlszeilen Vorgang ausführt. |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | Stellt eine Aktion dar, die eine e-Mail-Nachricht sendet.            |
| [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) | Stellt eine Aktion dar, die ein Meldungs Feld anzeigt.               |



 

## <a name="using-variables-in-action-properties"></a>Verwenden von Variablen in Aktions Eigenschaften

Einige Aktions Eigenschaften vom Typ **BSTR** können die Variablen $ (Arg0), $ (arg1),..., $ (Arg32) in ihren Zeichen folgen Werten enthalten. Diese Variablen werden durch die Werte ersetzt, die im Parameter *para* meters der [**IRegisteredTask:: Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) -Methode und der [**IRegisteredTask:: RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) -Methode angegeben sind oder im Ereignis--Fehler für die Aufgabe enthalten sind. In der folgenden Tabelle sind die Aktions Eigenschaften aufgeführt, die Variablen in ihren Zeichen folgen Werten verwenden können.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Aktion</th>
<th>Eigenschaften</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>COM-handleraktion</td>
<td>C++:
<ul>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>ClassID-Eigenschaft von icomhandleraction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>Dateneigenschaft von icomhandleraction</strong></a></li>
</ul>
<br/> Skripterstellung:
<ul>
<li><a href="comhandleraction-classid.md"><strong>Comhandleraction. ClassID</strong></a></li>
<li><a href="comhandleraction-data.md"><strong>Comhandleraction. Data</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>E-Mail-Aktion</td>
<td>C++:
<ul>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>Body-Eigenschaft von iemailaction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>Server-Eigenschaft von iemailaction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>Subject-Eigenschaft von iemailaction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>To-Eigenschaft von iemailaction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>CC-Eigenschaft von iemailaction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>BCC-Eigenschaft von iemailaction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>ReplyTo-Eigenschaft von iemailaction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>From-Eigenschaft von iemailaction</strong></a></li>
</ul>
<br/> Skripterstellung:
<ul>
<li><a href="emailaction-body.md"><strong>Emailaction. Body</strong></a></li>
<li><a href="emailaction-server.md"><strong>Emailaction. Server</strong></a></li>
<li><a href="emailaction-subject.md"><strong>Emailaction. Subject</strong></a></li>
<li><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></li>
<li><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></li>
<li><a href="emailaction-bcc.md"><strong>Emailaction. BCC</strong></a></li>
<li><a href="emailaction-replyto.md"><strong>Emailaction. ReplyTo</strong></a></li>
<li><a href="emailaction-from.md"><strong>Emailaction. from</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td>Exec-Aktion</td>
<td>C++:
<ul>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>Arguments-Eigenschaft von IExecAction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>WorkingDirectory-Eigenschaft von IExecAction</strong></a></li>
</ul>
<br/> Skripterstellung:
<ul>
<li><a href="execaction-arguments.md"><strong>Execaction. Arguments</strong></a></li>
<li><a href="execaction-workingdirectory.md"><strong>Execaction. WorkingDirectory</strong></a></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>Nachricht anzeigen (Aktion)</td>
<td>C++:
<ul>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>Title-Eigenschaft von ishowmessageaction</strong></a></li>
<li><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>MessageBody-Eigenschaft von ishowmessageaction</strong></a></li>
</ul>
<br/> Skripterstellung:
<ul>
<li><a href="showmessageaction-title.md"><strong>Showmessageaction. Title</strong></a></li>
<li><a href="showmessageaction-messagebody.md"><strong>Showmessageaction. MessageBody</strong></a></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Taskplaner](about-the-task-scheduler.md)
</dt> </dl>

 

 





