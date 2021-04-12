---
description: Ein Auftragsobjekt ermöglicht es, Gruppen von Prozessen als Einheit zu verwalten. Auftrags Objekte sind namable-, Securable-und freigegeben-Objekte, die Attribute der zugeordneten Prozesse steuern.
ms.assetid: 59296384-5e78-44dd-8019-f1df6668928b
title: Auftrags Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e6d9758faf2b66f047ca60dbba91601b202b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345469"
---
# <a name="job-objects"></a>Auftrags Objekte

Ein *Auftrags Objekt* ermöglicht das Verwalten von Gruppen von Prozessen als Einheit. Auftrags Objekte sind namable-, Securable-und freigegeben-Objekte, die Attribute der zugeordneten Prozesse steuern. Vorgänge für ein Auftragsobjekt wirken sich auf alle Prozesse aus, die dem Auftragsobjekt zugeordnet sind. Beispiele hierfür sind die Erzwingung von Grenzwerten, wie z. b. Workingsetgröße und Prozesspriorität, oder das Beenden aller Prozesse

-   [Erstellen von Aufträgen](#creating-jobs)
-   [Verwalten von Prozessen in Aufträgen](#managing-processes-in-jobs)
-   [Auftrags Limits und-Benachrichtigungen](#job-limits-and-notifications)
-   [Ressourcen Führung für Aufträge](#resource-accounting-for-jobs)
-   [Verwalten von Auftrags Objekten](#managing-job-objects)
-   [Verwalten einer Prozess Struktur, die Auftrags Objekte verwendet](#managing-a-process-tree-that-uses-job-objects)

## <a name="creating-jobs"></a>Erstellen von Aufträgen

Um ein Auftrags Objekt zu erstellen, verwenden Sie die Funktion " [**kreatejobobject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) ". Beim Erstellen des Auftrags werden dem Auftrag keine Prozesse zugeordnet.

Um einen Prozess einem [**Auftrag zuzuordnen, verwenden Sie die Funktion**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) "Zuordnungs Funktion". Nachdem ein Prozess einem Auftrag zugeordnet ist, kann die Zuordnung nicht mehr unterbrechen. Ein Prozess kann mehr als einem Auftrag in einer Hierarchie von verknüpften Aufträgen zugeordnet werden. Weitere Informationen finden Sie unter "in der Liste mit den [Daten.](nested-jobs.md)

**Windows 7, Windows Server 2008 R2, Windows XP mit SP3, Windows Server 2008, Windows Vista und Windows Server 2003:** Ein Prozess kann nur einem Auftrag zugeordnet werden. Aufträge können nicht eingefügt werden. Die Möglichkeit zum Schachteln von Aufträgen wurde in Windows 8 und Windows Server 2012 hinzugefügt.

Sie können eine Sicherheits Beschreibung für ein Auftrags Objekt angeben, wenn Sie die Funktion "up- [**JobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) " aufrufen. Weitere Informationen finden Sie unter [Auftrags Objektsicherheit und Zugriffsrechte](job-object-security-and-access-rights.md).

## <a name="managing-processes-in-jobs"></a>Verwalten von Prozessen in Aufträgen

Nachdem ein Prozess einem Auftrag zugeordnet ist, werden standardmäßig alle untergeordneten Prozesse, die er mithilfe von " [**deateprocess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) " erstellt, dem Auftrag zugeordnet. (Untergeordnete Prozesse, die mit [**Win32 \_ Process. Create**](../cimwin32prov/create-method-in-class-win32-process.md) erstellt wurden, sind nicht mit dem Auftrag verknüpft.) Dieses Standardverhalten kann geändert werden, indem Sie für den Auftrag die Einstellung für das Limit für erweiterte Aufträge des Auftrags \_ Objekts \_ \_ \_ auf OK oder das Auftrags \_ \_ Limit \_ \_ für das Auftrags Limit festlegen \_ .

-   Wenn für den Auftrag das Limit für erweiterte Aufträge der Auftrags \_ \_ Grenze \_ \_ OK und der übergeordnete Prozess mit dem Flag zum Erstellen \_ \_ von break from Job erstellt wurde, sind die unter \_ geordneten Prozesse des übergeordneten Prozesses dem Auftrag nicht zugeordnet.
-   Wenn für den Auftrag das Limit für erweiterte Aufträge für das Auftrags \_ \_ Limit in Ordnung ist, werden die unter \_ \_ \_ geordneten Prozesse eines beliebigen übergeordneten Prozesses, der dem Auftrag zugeordnet ist, nicht dem Auftrag zugeordnet. Es ist nicht erforderlich, dass übergeordnete Prozesse mit dem Flag Create \_ Breakaway \_ from \_ Job erstellt werden.

Wenn der Auftrag mit einem anderen Auftrag verknüpft ist, beeinflussen die Unterbrechungs Einstellungen der übergeordneten Aufträge in der Hierarchie, ob untergeordnete Prozesse einem anderen Auftrag in der Hierarchie zugeordnet sind. Weitere Informationen finden Sie unter "in der Liste mit den [Daten.](nested-jobs.md)

Verwenden Sie die [**isprocessinjob**](/windows/win32/api/jobapi/nf-jobapi-isprocessinjob) -Funktion, um zu bestimmen, ob ein Prozess in einem Auftrag ausgeführt wird.

Verwenden Sie die [**terminatejobobject**](/windows/win32/api/jobapi2/nf-jobapi2-terminatejobobject) -Funktion, um alle Prozesse zu beenden, die derzeit einem Auftrags Objekt zugeordnet sind.

## <a name="job-limits-and-notifications"></a>Auftrags Limits und-Benachrichtigungen

Ein Auftrag kann Grenzwerte wie Workingsetgröße, Prozesspriorität und Zeitlimit für das Ende des Auftrags für jeden Prozess erzwingen, der dem Auftrag zugeordnet ist. Wenn ein Prozess, der einem Auftrag zugeordnet ist, versucht, die Workingsetgröße oder die Prozesspriorität von dem durch den Auftrag festgelegten Grenzwert zu erhöhen, werden die Funktionsaufrufe erfolgreich ausgeführt, werden jedoch ignoriert. Ein Auftrag kann auch Grenzwerte festlegen, die eine Benachrichtigung auslöst, wenn Sie überschritten werden, die Ausführung des Auftrags jedoch fortgesetzt werden kann.

Verwenden Sie die Funktion [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) , um Grenzwerte für einen Auftrag festzulegen. Eine Liste möglicher Beschränkungen, die für einen Auftrag festgelegt werden können, finden Sie in den folgenden Themen:

-   [**\_Informationen zu grundlegenden \_ \_ Informationen zu JobObject**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [**\_grundlegende Einschränkungen der \_ Benutzeroberfläche von JobObject \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [**\_Informationen zur CPU- \_ Raten \_ Kontrolle \_ für JobObject**](/windows/desktop/api/Winnt/ns-winnt-jobobject_cpu_rate_control_information)
-   [**\_Informationen zu erweiterten \_ \_ Informationen zu JobObject**](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [**Informationen zu JobObject- \_ Benachrichtigungs \_ Limit \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_notification_limit_information)

Sicherheitsgrenzwerte müssen für jeden Prozess, der einem Auftrags Objekt zugeordnet ist, einzeln festgelegt werden. Weitere Informationen finden Sie unter [Prozesssicherheit und Zugriffsrechte](process-security-and-access-rights.md).

**Windows XP mit SP3 und Windows Server 2003:** Die [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) -Funktion kann verwendet werden, um Sicherheitseinschränkungen für alle Prozesse festzulegen, die einem Auftrags Objekt zugeordnet sind. Ab Windows Vista müssen die Sicherheitsgrenzwerte für jeden Prozess, der einem Auftrags Objekt zugeordnet ist, einzeln festgelegt werden.

Wenn der Auftrag eingebettet ist, beeinflussen übergeordnete Aufträge in der Hierarchie den Grenzwert, der für den Auftrag erzwungen wird. Weitere Informationen finden Sie unter "in der Liste mit den [Daten.](nested-jobs.md)

Wenn dem Auftrag ein e/a-Abschlussport zugeordnet ist, kann er Benachrichtigungen empfangen, wenn bestimmte Auftrags Limits überschritten werden. Das System sendet Nachrichten an den Abschlussport, wenn ein Grenzwert überschritten wird oder bestimmte andere Ereignisse eintreten. Um einen Abschlussport einem Auftrag zuzuordnen, verwenden Sie die [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) -Funktion mit der Auftrags Objekt Informations Klasse **jobobjectassociatecompletionportinformation** und einen Zeiger auf eine [**JobObject-Zuordnungs \_ \_ Vervollständigungs- \_ Port**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port) Struktur. Es ist am besten, dies zu tun, wenn der Auftrag inaktiv ist, um die Wahrscheinlichkeit zu vermeiden, dass Benachrichtigungen für Prozesse fehlen, deren Zustände sich während der Zuordnung des Abschlussports ändern.

Alle Nachrichten werden direkt vom Auftrag gesendet, als ob der Auftrag die [**PostQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-postqueuedcompletionstatus) -Funktion aufgerufen hätte. Ein Thread muss den Abschlussport mithilfe der [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) -Funktion überwachen, um die Nachrichten zu überwachen. Beachten Sie, dass die Übermittlung von Nachrichten an den Abschlussport nicht garantiert wird, mit Ausnahme der Limits, die mit der **jobobjectnotificationlimitinformation** -Klasse festgelegt wurden. Wenn eine Nachricht nicht eintreffen kann, bedeutet das nicht unbedingt, dass das Ereignis nicht aufgetreten ist. Benachrichtigungen für Grenzwerte, die mit **jobobjectnotificationlimitinformation** festgelegt wurden, werden am Abschlussport garantiert. Eine Liste der möglichen Meldungen finden Sie unter [**JobObject \_ Zuordnen des \_ Vervollständigungs \_ Ports**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port).

## <a name="resource-accounting-for-jobs"></a>Ressourcen Führung für Aufträge

Das Job-Objekt zeichnet grundlegende Buchhaltungsinformationen für alle zugehörigen Prozesse auf, einschließlich derjenigen, die beendet wurden. Um diese Buchhaltungsinformationen abzurufen, verwenden Sie die Funktion [**queryinformationjobobject**](/windows/win32/api/jobapi2/nf-jobapi2-queryinformationjobobject) . Eine Liste der für einen Auftrag verwalteten Buchhaltungsinformationen finden Sie in den folgenden Themen:

-   [**\_grundlegende Informationen zur \_ Buchhaltung von JobObject \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [**\_grundlegende Informationen und e/a \_ - \_ \_ Buchhaltungs \_ Informationen**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)

Wenn das Auftrags Objekt eingebettet ist, werden Buchhaltungsinformationen für jeden untergeordneten Auftrag in seinem übergeordneten Auftrag aggregiert. Weitere Informationen finden Sie unter "in der Liste mit den [Daten.](nested-jobs.md)

## <a name="managing-job-objects"></a>Verwalten von Auftrags Objekten

Der Status eines Auftrags Objekts wird auf "signalisiert" festgelegt, wenn alle Prozesse beendet werden, da das angegebene Zeitlimit für das Zeitlimit überschritten wurde. Verwenden Sie " [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) " oder " [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) ", um das Auftrags Objekt für dieses Ereignis zu überwachen.

Verwenden Sie zum Abrufen eines Handles für ein vorhandenes Auftrags Objekt die [**openjobobject**](/windows/desktop/api/WinBase/nf-winbase-openjobobjecta) -Funktion, und geben Sie den Namen an, der dem Objekt bei der Erstellung angegeben wurde. Nur benannte Auftrags Objekte können geöffnet werden.

Verwenden Sie die [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) -Funktion, um ein Auftrags Objekt Handle zu schließen. Der Auftrag wird zerstört, wenn sein letztes Handle geschlossen wurde und alle zugehörigen Prozesse beendet wurden. Wenn für den Auftrag jedoch das Flag "Job \_ Object \_ Limit \_ Kill \_ on \_ Job Close" angegeben ist \_ , werden beim Schließen des letzten Auftrags Objekt Handles alle zugeordneten Prozesse beendet und das Auftrags Objekt selbst zerstört. Wenn ein geänderter Auftrag das Flag "Job \_ Object \_ Limit \_ Kill \_ on \_ Job \_ Close" angegeben hat, werden durch das Schließen des letzten Auftrags Objekt Handles alle Prozesse beendet, die dem Auftrag und seinen untergeordneten Aufträgen in der Hierarchie zugeordnet sind.

## <a name="managing-a-process-tree-that-uses-job-objects"></a>Verwalten einer Prozess Struktur, die Auftrags Objekte verwendet

Ab Windows 8 und Windows Server 2012 kann eine Anwendung mithilfe von mit einem Auftrag verwalteten [Aufträgen](nested-jobs.md) eine Prozess Struktur verwalten, die mehrere Auftrags Objekte verwendet. Eine Anwendung, die unter Windows 7, Windows Server 2008 R2 oder früheren Versionen von Windows ausgeführt werden muss, die keine Unterstützung für die Prozess Struktur benötigen, muss jedoch auf andere Weise verwaltet werden.

Wenn ein Tool eine Prozess Struktur verwalten muss, die Auftrags Objekte verwendet, und es nicht möglich ist, die Verwendung von nicht-Netz Aufträgen zu ermöglichen, müssen sowohl das Tool als auch die Elemente der Prozess Struktur zusammenarbeiten. Nutzen Sie eine der folgenden Optionen:

-   Verwenden Sie das Limit für das automatische brechen von "Job \_ Object \_ Limit" \_ \_ \_ . Wenn das Tool dieses Limit verwendet, kann es eine gesamte Prozess Struktur nicht überwachen. Das Tool kann nur die Prozesse überwachen, die dem Auftrag hinzugefügt werden. Wenn diese Prozesse untergeordnete Prozesse erstellen, sind Sie nicht dem Auftrag zugeordnet. Bei dieser Option können untergeordnete Prozesse anderen Auftrags Objekten zugeordnet werden.
-   Verwenden Sie das Limit für die Beschränkung des Limits für den Arbeitsplatz \_ \_ \_ \_ . Wenn das Tool dieses Limit verwendet, kann es die gesamte Prozess Struktur überwachen, mit Ausnahme der Prozesse, die ein beliebiges Mitglied der Struktur explizit aus der Struktur entfernt. Ein Member der-Struktur kann einen untergeordneten Prozess in einem neuen Job-Objekt erstellen, indem er die [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) -Funktion mit dem \_ Flag Create breakoff \_ from Job aufruft \_ und dann die Funktion "zuordnungsprozesstojobobject" aufruft. [](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) Andernfalls muss der Member Fälle **behandeln, in denen "** zuordnet" einen Fehler verursacht.

    Das \_ Flag "Breakaway \_ aus Auftrag erstellen" \_ hat keine Auswirkung, wenn die Struktur nicht vom Tool überwacht wird. Daher ist dies die bevorzugte Option, erfordert jedoch vorab Kenntnisse über die überwachten Prozesse.

-   Vermeiden Sie halte Abbrüche beliebiger Art, indem Sie weder das Auftrags \_ Objekt \_ Limit \_ Break Away \_ OK noch das Limit für den automatischen Abbruch des Auftrags \_ Objekts \_ Limit \_ OK festlegen \_ \_ . Bei dieser Option kann das Tool die gesamte Prozess Struktur überwachen. Wenn jedoch ein untergeordneter Prozess versucht, sich selbst oder einen anderen untergeordneten Prozess durch Aufrufen von [**zuordnungsesstojobobject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject)einem Auftrag zuzuordnen, schlägt der Aufruf fehl. Wenn der Prozess für die Zuordnung zu einem bestimmten Auftrag konzipiert wurde, kann dieser Fehler die ordnungsgemäße Ausführung des Prozesses verhindern.

 

 
