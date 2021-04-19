---
description: Nach jeder Art von Fehler, die die normale Transaktionsverarbeitung stören, müssen KTM und jeder Ressourcen-Manager Wiederherstellungs Vorgänge durchführen. Die Wiederherstellung ist der Prozess, mit dem Transaktions Teilnehmer in einer konsistenten Ansicht jedes Transaktions Zustands eintreffen.
ms.assetid: 5bc9a155-6ba4-41f8-8e12-e87f48d83940
title: Wiederherstellungs Verarbeitung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8e74d4f8bff3e56af03b017522212e7a02e232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106373004"
---
# <a name="recovery-processing"></a>Wiederherstellungs Verarbeitung

Nach jeder Art von Fehler, die die normale Transaktionsverarbeitung stören, müssen KTM und jeder Ressourcen-Manager *Wiederherstellungs* Vorgänge durchführen. Die Wiederherstellung ist der Prozess, mit dem Transaktions Teilnehmer in einer konsistenten Ansicht des Zustands der einzelnen Transaktionen eintreffen.

Ressourcen-Manager sind möglicherweise *unsicher über das* Ergebnis einer Transaktion. Dies bedeutet, dass Sie zum Zeitpunkt des Fehlers eine \_ Benachrichtigung zur Vorbereitung der Transaktion erhalten haben, dass Sie auf permanenten \_ Speicher vorbereitet war, aber nicht empfangen (bzw. empfangen, aber nicht protokolliert). Analog dazu kann KTM eine Transaktion unsicher sein, wenn Sie vorbereitet wurde, aber noch nicht empfangen wurde (oder empfangen, aber nicht protokolliert wurde). Zur Wiederherstellungszeit müssen alle Ergebnisse, die gesendet, aber nicht bestätigt wurden, erneut gesendet werden. Wenn z. b. ein Ressourcen-Manager eine \_ Benachrichtigung über den \_ Commit des Transaktions Benachrichtigungs Diensts empfangen hat und die [**commitcomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) -Funktion aufgerufen hat, erhält der RM möglicherweise immer noch eine doppelte \_ \_ Benachrichtigung zum Benachrichtigen von Transaktionen,

Damit eine Transaktion nach einem Ressourcen-Manager oder Systemausfall ordnungsgemäß wieder hergestellt werden kann, muss jeder Ressourcen-Manager bei jedem Start Folgendes ausführen:

1.  Verwenden Sie die [**openresourcemanager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager) -Funktion, um das zugehörige Resource Manager-Handle mithilfe seines eindeutigen, permanenten namens erneut zu öffnen. Dadurch wird KTM informiert, dass der Ressourcen-Manager erneut ausgeführt wird und für die Wiederherstellung verfügbar ist. Wenn keine Eintragung für die Wiederherstellung vorhanden ist, kann der **openresourcemanager** -Befehl fehlschlagen. Rufen Sie " [**kreateresourcemanager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) " auf, um das RM-Objekt erneut zu erstellen.
2.  [**ResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverresourcemanager)-Rückruf. Der Ressourcen-Manager empfängt für jede Eintragung, für die er Wiederherstellungs Vorgänge ausführen muss, ein Benachrichtigungs Ereignis für die Benachrichtigung zur [**\_ \_ wieder**](notification-mask.md) Herstellung der Transaktion, gefolgt von der \_ \_ letzten Wiederherstellung der Transaktion Benachrichtigen \_ . Das Benachrichtigungs Ereignis schließt eine Globally Unique Identifier für die Transaktion und die Eintragung ein.
3.  Verwenden Sie die [**openenlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) -Funktion, um jedes Registrierungs handle erneut zu öffnen, für das der Ressourcen-Manager eine \_ Benachrichtigung zur Wiederherstellung per Transaktions Benachrichtigung erhalten hat \_ .
4.  Für jede Eintragung, die von [**openeintragung**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)geöffnet wurde, wird die [**Wiederherstellbarkeits Eintragung**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverenlistment)aufgerufen. Dies bewirkt \_ \_ , dass der Commit für die Transaktion benachrichtigen oder die \_ \_ Benachrichtigung über die Benachrichtigung über die Benachrichtigung übermittelt wird.
5.  Wenn für den RM ein \_ Commit für die Transaktions Benachrichtigung empfangen \_ wurde, kann der RM die Transaktion durch Aufrufen von [**commitcomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)vervollständigen.

    Wenn die RM-Transaktion die Transaktion nicht \_ \_ sicher benachrichtigt, sollte der RM auf den Eingang der Ergebnis Benachrichtigung warten.

6.  Für Transaktionen, für die der RM keine Benachrichtigung zur Wiederherstellung per Transaktions Benachrichtigung erhält \_ \_ , aber zuvor eine \_ Transaktion \_ Benachrichtigungs Vorbereitung für empfangen hat, sollte der RM die Transaktion so verarbeiten, als ob ein Rollback ausgeführt würde.

> [!Note]
>
> Ressourcen-Manager können während der Durchführung der Wiederherstellung neue Transaktionen eintragen oder erstellen.

 

KTM verwendet ein *mutmaßliches Abbruch* Transaktionsmodell. Dieses Verhalten wird im folgenden Szenario veranschaulicht. Nehmen Sie an, dass KTM und ein Ressourcen-Manager auf demselben Computer vorhanden sind. Angenommen, KTM gibt eine Vorbereitungs Benachrichtigung für eine Transaktion aus, aber das System stürzt ab, bevor KTM die Vorbereitungs Benachrichtigung protokolliert. Angenommen, der Ressourcen-Manager empfängt und protokolliert die Vorbereitungs Benachrichtigung, kurz bevor das System abstürzt. Nachdem das System wieder hergestellt wurde, kennt KTM die Transaktion nicht, da die Vorbereitungsphase nie protokolliert wurde. Der Ressourcen-Manager hat Kenntnis der Transaktion, weil er die Vorbereitungs Benachrichtigung empfangen, verarbeitet und protokolliert hat. Wenn KTM seine Wiederherstellungs Benachrichtigungen ausgibt, enthält der Ressourcen-Manager keine Wiederherstellungs Benachrichtigung für die betreffende Transaktion. Mit dem mutmaßlichen Abbruch Modell behandelt der Ressourcen-Manager in diesem Fall die vorbereitete Transaktion als abgebrochen, wenn Sie keine Benachrichtigungen empfängt, um die Wiederherstellung für diese Transaktion auszuführen.

 

 



