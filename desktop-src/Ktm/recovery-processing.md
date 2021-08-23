---
description: Nach jedem Fehler, der die normale Transaktionsverarbeitung beeinträchtigt, müssen KTM und jeder Ressourcen-Manager Wiederherstellungsvorgänge ausführen. Wiederherstellung ist der Prozess, bei dem Transaktionsteilnehmer eine konsistente Ansicht des jeweiligen Transaktionszustands erhalten.
ms.assetid: 5bc9a155-6ba4-41f8-8e12-e87f48d83940
title: Wiederherstellungsverarbeitung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec99ad63d18c95da3ebb3ad5db6c204301d75336cc1842dd21e1edf79f5f9a38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146493"
---
# <a name="recovery-processing"></a>Wiederherstellungsverarbeitung

Nach jedem Fehler, der die normale Transaktionsverarbeitung beeinträchtigt, müssen KTM und jeder Ressourcen-Manager *Wiederherstellungsvorgänge* ausführen. Wiederherstellung ist der Prozess, bei dem Transaktionsteilnehmer zu einer konsistenten Ansicht des Status jeder Transaktion gelangen.

Ressourcen-Manager  haben möglicherweise keinen Zweifel am Ergebnis einer Transaktion. Dies bedeutet, dass sie zum Zeitpunkt des Fehlers eine TRANSACTION NOTIFY PREPARE-Benachrichtigung erhalten hatten, sich auf dauerhaften Speicher vorbereitet hatten, aber kein Endergebnis für die Transaktion empfangen (oder empfangen, aber nicht protokolliert) \_ \_ hatten. Auf ähnliche Weise kann KTM an einer Transaktion im Zweifelsfall sein, wenn sie vorbereitet, aber kein Ergebnis empfangen (oder nicht protokolliert) wurde. Zur Wiederherstellungszeit müssen alle Ergebnisse, die gesendet, aber nicht bestätigt wurden, erneut gesendet werden. Wenn beispielsweise ein Ressourcen-Manager eine TRANSACTION NOTIFY COMMIT-Benachrichtigung empfangen und die CommitComplete-Funktion aufgerufen hat, erhält der RM möglicherweise zur Wiederherstellungszeit weiterhin eine doppelte \_ \_ TRANSACTION NOTIFY [](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) \_ \_ COMMIT-Benachrichtigung.

Damit eine Transaktion nach einem Ressourcen-Manager- oder Systemfehler ordnungsgemäß wiederhergestellt werden kann, muss jeder Ressourcen-Manager bei jedem Start Folgendes tun:

1.  Rufen Sie die [**OpenResourceManager-Funktion**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager) auf, um das Resource Manager-Handle mit dem eindeutigen, persistenten Namen erneut zu öffnen. Dadurch wird KTM darüber informiert, dass der Ressourcen-Manager erneut ausgeführt wird und für die Wiederherstellung verfügbar ist. Wenn keine Eintragungen wiederhergestellt werden können, kann der Aufruf von **OpenResourceManager** fehlschlagen. Rufen [**Sie CreateResourceManager auf,**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) um das RM-Objekt neu zu erstellen.
2.  Rufen Sie [**RecoverResourceManager auf.**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverresourcemanager) Der Ressourcen-Manager erhält ein [**TRANSACTION \_ NOTIFY RECOVER-Benachrichtigungsereignis \_**](notification-mask.md) für jede Eintragung, für die er Wiederherstellungsvorgänge ausführen muss, gefolgt von TRANSACTION \_ NOTIFY LAST \_ \_ RECOVER. Das Benachrichtigungsereignis enthält einen global eindeutigen Bezeichner für die Transaktion und die Eintragung.
3.  Rufen Sie [**die OpenEnlistment-Funktion**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) auf, um jedes Eintragungshand handle erneut zu öffnen, für das der Ressourcen-Manager eine TRANSACTION \_ NOTIFY \_ RECOVER-Benachrichtigung erhalten hat.
4.  Rufen Sie für jede von [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)geöffnete Eintragung [**RecoverEnlistment auf.**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverenlistment) Dies bewirkt, dass die Benachrichtigung \_ TRANSACTION NOTIFY COMMIT oder TRANSACTION NOTIFY \_ \_ \_ INDOUBT erneut zugestellt wird.
5.  Wenn der RM TRANSACTION NOTIFY COMMIT empfangen hat, kann der RM die Transaktion abschließen, \_ \_ indem er [**CommitComplete aufruft.**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)

    Wenn der RM TRANSACTION \_ NOTIFY \_ INDOUBT empfangen hat, sollte der RM warten, bis die Ergebnisbenachrichtigung eintrifft.

6.  Für alle Transaktionen, für die der RM keine TRANSACTION NOTIFY RECOVER-Benachrichtigung erhält, aber zuvor eine TRANSACTION NOTIFY PREPARE-Benachrichtigung erhalten hat, sollte der RM die Transaktion so verarbeiten, als ob ein Rollback ausgeführt \_ \_ \_ \_ würde.

> [!Note]
>
> Ressourcen-Manager können sich während der Wiederherstellung bei Transaktionen ein- oder neu erstellen.

 

KTM verwendet ein *mutmaßlich abgebrochenes* Transaktionsmodell. Das folgende Szenario veranschaulicht dieses Verhalten. Angenommen, KTM und ein Ressourcen-Manager sind auf demselben Computer vorhanden. Angenommen, KTM gibt eine Vorbereitungsbenachrichtigung für eine Transaktion aus, aber das System stürzt ab, bevor KTM die Vorbereitungsbenachrichtigung protokolliert. Angenommen, der Ressourcen-Manager empfängt und protokolliert die Vorbereitungsbenachrichtigung direkt vor dem Systemabsturz. Nachdem das System wiederhergestellt wurde, kann KTM die Transaktion nicht mehr wissen, da die Vorbereitungsphase nie protokolliert wurde. Der Ressourcen-Manager hat Kenntnis über die Transaktion, da er die Vorbereitungsbenachrichtigung empfangen, verarbeitet und protokolliert hat. Wenn KTM seine Wiederherstellungsbenachrichtigungen aus gibt, enthält der Ressourcen-Manager keine Wiederherstellungsbenachrichtigung für die in Frage kommt. Beim Modell für den vermutlichen Abbruch behandelt der Ressourcen-Manager in diesem Fall die vorbereitete Transaktion als abgebrochen, wenn er keine Benachrichtigungen erhält, um die Wiederherstellung für diese Transaktion durchzuführen.

 

 



