---
description: Wenn Sie einen Dienst oder eine Komponente schreiben und transaktionale Dienste verwenden müssen, oder wenn Sie den Status einer Kernel Transaktion überwachen müssen, müssen Sie einen Ressourcen-Manager (RM) erstellen.
ms.assetid: 9b62ef58-9897-4573-bda4-8c3ec952b6d2
title: Schreiben einer Ressourcen-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2c47f9a0704f6edaea02d752fe39f01fce61c0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347966"
---
# <a name="writing-a-resource-manager"></a>Schreiben einer Ressourcen-Manager

Wenn Sie einen Dienst oder eine Komponente schreiben und transaktionale Dienste verwenden müssen, oder wenn Sie den Status einer Kernel Transaktion überwachen müssen, müssen Sie einen Ressourcen-Manager (RM) erstellen.

Zum Schreiben eines Ressourcen-Managers müssen Sie mehrere Kernel Objekte erstellen. Die von einem RM verwendeten Objekte lauten wie folgt:

-   Transaktions-Manager-Objekte (TM)
-   Ressourcen-Manager Objekte
-   Eintragung von Objekten

Erstellen Sie zunächst ein TM-Objekt. Es gibt zwei Arten von TMS:

-   Flüchtig – diese TMS verfügen nicht über ein Protokoll und können Ihren Zustand nicht wiederherstellen.
-   Permanent – diese TMS verfügen über ein Protokoll.

Um ein dauerhaftes TM zu erstellen, müssen Sie entweder ein CLFS-Protokoll erstellen und den Befehl " [**kreatetransaktionsmanager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) " aufrufen, oder Sie müssen von KTM für Sie erstellen. Nachdem ein dauerhaftes TM erstellt wurde, müssen Sie das TM zuerst wiederherstellen, indem Sie den [**wiederherstellbaren Transaktions-Manager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)aufrufen. Nachdem die TM-Datei wieder hergestellt wurde, kann Sie verwendet werden.

Wenn Sie ein vorhandenes TM wieder hergestellt haben, empfangen alle diesem TM zugeordneten RMS Wiederherstellungs Nachrichten. Weitere Informationen finden Sie unter [Wiederherstellungs Verarbeitung](recovery-processing.md).

Als Nächstes erstellen Sie einen Ressourcen-Manager, indem Sie [**createresourcemanager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) mit dem TM-handle aufrufen. Der RM kann flüchtig oder dauerhaft sein. Nur dauerhafte TMS können mit Durable RMS verwendet werden.

Wenn Sie transaktional arbeiten, tragen Sie in die Transaktion ein, indem Sie [**createenlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)aufrufen und angeben, welche Benachrichtigungen empfangen werden sollen.

**Hinweis**  Sie können Benachrichtigungen empfangen, bevor der aufzurufende [**Auflistungs**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment) Vorgang abgeschlossen ist.

Wenn Sie eine Benachrichtigung erhalten, wenden Sie die entsprechende "Complete \* "-Funktion an, wenn die Arbeit, die mit der Verarbeitung der Benachrichtigung verknüpft ist, abgeschlossen ist. Die kompletten Funktionen sind:

-   [**Commitcomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [**Preparecomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [**Prepreparecomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)

Wenn ein Ressourcen-Manager zu einem beliebigen Zeitpunkt nicht in der Lage ist, die Transaktion abzuschließen, oder wenn die Anwendung fortgesetzt wird, kann die in der Transaktion ausgeführte Aufgabe nicht rückgängig gemacht werden, müssen Sie die Transaktion durch Aufrufen von [**rollbackenlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)zurücksetzen.

 

 



