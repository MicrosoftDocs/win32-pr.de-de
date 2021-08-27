---
title: Aufgabenaktionen
description: Die von einer Aufgabe ausgeführten Arbeitselemente werden als Aktionen bezeichnet. Eine Aufgabe kann eine einzelne Aktion oder maximal 32 Aktionen haben. Beachten Sie, dass mehrere Aktionen sequenziell ausgeführt werden, wenn mehrere Aktionen angegeben werden.
ms.assetid: 4cbe739d-4c4e-4469-8289-4be41b93950c
keywords:
- Aktionen Taskplaner
- Aktionen Taskplaner , beschrieben
- Aktionen Taskplaner , Aktion ausführen
- Aktionen Taskplaner , COM-Handleraktion
- Aktions-Taskplaner
- COM-Handleraktions Taskplaner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a7cc4a0e3ecbd4d55e4731379287f2cf4fd660
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470495"
---
# <a name="task-actions"></a>Aufgabenaktionen

Die von einer Aufgabe ausgeführten Arbeitselemente werden als Aktionen bezeichnet. Eine Aufgabe kann eine einzelne Aktion oder maximal 32 Aktionen haben. Beachten Sie, dass mehrere Aktionen sequenziell ausgeführt werden, wenn mehrere Aktionen angegeben werden.

## <a name="types-of-actions"></a>Aktionstypen

In der folgenden Tabelle mit Aktionen wird der Typ der Arbeit oder Aktionen beschrieben, die von einer Aufgabe ausgeführt werden können.

| Aktionstyp      | BESCHREIBUNG                                                             |
|---------------------|-------------------------------------------------------------------------|
| ComHandler-Aktion   | Diese Aktion gibt einen COM-Handler aus.                                        |
| Exec-Aktion         | Diese Aktion führt einen Befehlszeilenvorgang aus, z. B. das Starten Editor. |
| E-Mail-Aktion       | Diese Aktion sendet eine E-Mail, wenn eine Aufgabe ausgelöst wird.                    |
| Meldungsaktion anzeigen | Diese Aktion zeigt ein Meldungsfeld mit einer angegebenen Meldung und einem angegebenen Titel an.     |



 

## <a name="specifying-actions"></a>Festlegen von Aktionen

Die Aktionen einer Aufgabe werden angegeben, wenn der Task definiert und in einer Auflistung von Aktionen gespeichert wird, die vom Taskplaner werden. Die folgende Tabelle enthält Links zu Referenzthemen für die APIs und XML-Elemente, die Aktionen zugeordnet sind.

Weitere Informationen und Beispiele zur Verwendung der Taskplaner, Skriptobjekten und XML finden Sie unter [Verwenden der Taskplaner.](using-the-task-scheduler.md)

### <a name="interface-apis-for-c-development"></a>Schnittstellen-APIs für die C++-Entwicklung



| API                                                                    | BESCHREIBUNG                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**Actions-Eigenschaft von ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) | Ruft die aktionen ab, die von der Aufgabe ausgeführt werden, oder legt sie fest.              |
| [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection)                         | Enthält die aktionen, die von der Aufgabe ausgeführt werden.                  |
| [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)                         | Stellt eine Aktion dar, die einen Handler ausspricht.                   |
| [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction)                                     | Stellt eine Aktion dar, die einen Befehlszeilenvorgang ausgeführt. |
| [**IEmailAction**](/windows/desktop/api/taskschd/nn-taskschd-iemailaction)                                   | Stellt eine Aktion dar, die eine E-Mail sendet.            |
| [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction)                       | Stellt eine Aktion dar, die ein Meldungsfeld zeigt.               |



 

### <a name="scripting-object-apis-for-scripting-development"></a>Skriptobjekt-APIs für die Skriptentwicklung



| API                                                      | BESCHREIBUNG                                                  |
|----------------------------------------------------------|--------------------------------------------------------------|
| [**TaskDefinition.Actions**](taskdefinition-actions.md) | Ruft die aktionen ab, die von der Aufgabe ausgeführt werden, oder legt sie fest.              |
| [**ActionCollection**](actioncollection.md)             | Enthält die aktionen, die von der Aufgabe ausgeführt werden.                  |
| [**ComHandlerAction**](comhandleraction.md)             | Stellt eine Aktion dar, die einen Handler ausspricht.                   |
| [**ExecAction**](execaction.md)                         | Stellt eine Aktion dar, die einen Befehlszeilenvorgang ausgeführt. |
| [**EmailAction**](emailaction.md)                       | Stellt eine Aktion dar, die eine E-Mail sendet.            |
| [**ShowMessageAction**](showmessageaction.md)           | Stellt eine Aktion dar, die ein Meldungsfeld zeigt.               |



 

### <a name="xml-elements"></a>XML-Elemente



| Element                                                                    | BESCHREIBUNG                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [**Aktionen**](taskschedulerschema-actions-tasktype-element.md)            | Definiert die aktionen, die von der Aufgabe ausgeführt werden.                   |
| [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md)   | Stellt eine Aktion dar, die einen Handler ausspricht.                   |
| [**Exec**](taskschedulerschema-exec-actiongroup-element.md)               | Stellt eine Aktion dar, die einen Befehlszeilenvorgang ausgeführt. |
| [**Sendemail**](taskschedulerschema-sendemail-actiongroup-element.md)     | Stellt eine Aktion dar, die eine E-Mail sendet.            |
| [**Showmessage**](taskschedulerschema-showmessage-actiongroup-element.md) | Stellt eine Aktion dar, die ein Meldungsfeld zeigt.               |



 

## <a name="using-variables-in-action-properties"></a>Verwenden von Variablen in Aktionseigenschaften

Einige Aktionseigenschaften vom Typ **BSTR** können $(Arg0),$(Arg1), ..., $(Arg32)-Variablen in ihren Zeichenfolgenwerten enthalten. Diese Variablen werden durch die Werte ersetzt, die im *parameterms-Parameter* der [**Methoden IRegisteredTask::Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) und [**IRegisteredTask::RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) angegeben sind oder im Ereignistrigger für die Aufgabe enthalten sind. In der folgenden Tabelle sind die Aktionseigenschaften aufgeführt, die Variablen in ihren Zeichenfolgenwerten verwenden können.


| Aktion | Eigenschaften | 
|--------|------------|
| COM-Handleraktion | C++:<ul><li><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>ClassId-Eigenschaft von IComHandlerAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>Data-Eigenschaft von IComHandlerAction</strong></a></li></ul><br /> Skripterstellung:<ul><li><a href="comhandleraction-classid.md"><strong>ComHandlerAction.ClassId</strong></a></li><li><a href="comhandleraction-data.md"><strong>ComHandlerAction.Data</strong></a></li></ul><br /> | 
| E-Mail-Aktion | C++:<ul><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>Body-Eigenschaft von IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>Servereigenschaft von IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>Subject-Eigenschaft von IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>To-Eigenschaft von IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>Cc-Eigenschaft von IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>Bcc-Eigenschaft von IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>ReplyTo-Eigenschaft von IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>From-Eigenschaft von IEmailAction</strong></a></li></ul><br /> Skripterstellung:<ul><li><a href="emailaction-body.md"><strong>EmailAction.Body</strong></a></li><li><a href="emailaction-server.md"><strong>EmailAction.Server</strong></a></li><li><a href="emailaction-subject.md"><strong>EmailAction.Subject</strong></a></li><li><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></li><li><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></li><li><a href="emailaction-bcc.md"><strong>EmailAction.Bcc</strong></a></li><li><a href="emailaction-replyto.md"><strong>EmailAction.ReplyTo</strong></a></li><li><a href="emailaction-from.md"><strong>EmailAction.From</strong></a></li></ul><br /> | 
| Exec-Aktion | C++:<ul><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>Arguments-Eigenschaft von IExecAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>WorkingDirectory-Eigenschaft von IExecAction</strong></a></li></ul><br /> Skripterstellung:<ul><li><a href="execaction-arguments.md"><strong>ExecAction.Arguments</strong></a></li><li><a href="execaction-workingdirectory.md"><strong>ExecAction.WorkingDirectory</strong></a></li></ul><br /> | 
| Aktion "Nachricht anzeigen" | C++:<ul><li><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>Title-Eigenschaft von IShowMessageAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>MessageBody-Eigenschaft von IShowMessageAction</strong></a></li></ul><br /> Skripterstellung:<ul><li><a href="showmessageaction-title.md"><strong>ShowMessageAction.Title</strong></a></li><li><a href="showmessageaction-messagebody.md"><strong>ShowMessageAction.MessageBody</strong></a></li></ul><br /> | 




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Taskplaner](about-the-task-scheduler.md)
</dt> </dl>

 

 





