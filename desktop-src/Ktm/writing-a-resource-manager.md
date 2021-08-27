---
description: Wenn Sie einen Dienst oder eine Komponente schreiben und Transaktionsdienste verwenden müssen oder den Status einer Kerneltransaktion überwachen müssen, müssen Sie einen Ressourcen-Manager (RM) erstellen.
ms.assetid: 9b62ef58-9897-4573-bda4-8c3ec952b6d2
title: Schreiben eines Resource Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b1443bef61f56a14779612a6275aacbd65e344d7294325bd87b953795f0f8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086450"
---
# <a name="writing-a-resource-manager"></a>Schreiben eines Resource Manager

Wenn Sie einen Dienst oder eine Komponente schreiben und Transaktionsdienste verwenden müssen oder den Status einer Kerneltransaktion überwachen müssen, müssen Sie einen Ressourcen-Manager (RM) erstellen.

Um einen Ressourcen-Manager zu schreiben, müssen Sie mehrere Kernelobjekte erstellen. Die von einem RM verwendeten Objekte sind:

-   Transaktions-Manager-Objekte (TM)
-   Resource Manager-Objekten
-   Eintragungsobjekte

Erstellen Sie zunächst ein TM-Objekt. Es gibt zwei Arten von TMs:

-   Flüchtig: Diese TMs verfügen nicht über ein Protokoll und können ihren Zustand nicht wiederherstellen.
-   Durable : Diese TMs verfügen über ein Protokoll.

Um ein dauerhaftes TM zu erstellen, müssen Sie entweder ein CLFS-Protokoll erstellen und [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager) aufrufen, oder SIE müssen IHN für Sie erstellen lassen. Nachdem ein dauerhaftes TM erstellt wurde, müssen Sie zuerst das TM wiederherstellen, indem Sie [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)aufrufen. Nachdem das TM wiederhergestellt wurde, kann es verwendet werden.

Wenn Sie ein vorhandenes TM wiederhergestellt haben, empfangen alle RMs, die diesem TM zugeordnet sind, Wiederherstellungsmeldungen. Weitere Informationen finden Sie unter [Wiederherstellungsverarbeitung.](recovery-processing.md)

Als Nächstes erstellen Sie einen Ressourcen-Manager, indem [**Sie CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager) mit dem TM-Handle aufrufen. Der RM kann flüchtig oder dauerhaft sein. Nur dauerhafte TMs können mit permanenten RMs verwendet werden.

Wenn Sie transaktional arbeiten, werden Sie in die Transaktion eintragen, indem [**Sie CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)aufrufen und angeben, welche Benachrichtigungen empfangen werden sollen.

**Hinweis**  Sie können Benachrichtigungen empfangen, bevor der Aufruf von [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment) abgeschlossen ist.

Wenn Sie eine Benachrichtigung erhalten, rufen Sie die entsprechende \* Funktion "Complete" auf, wenn alle mit der Verarbeitung der Benachrichtigung verbundenen Aufgaben abgeschlossen sind. Die vollständigen Funktionen sind:

-   [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)
-   [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)
-   [**PreprepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)

Wenn ein Ressourcen-Manager die Transaktion zu einem beliebigen Zeitpunkt nicht abschließen kann oder wenn das Fortsetzen der Transaktion dazu führen würde, dass ihre Anwendung die innerhalb der Transaktion ausgeführte Arbeit nicht rückgängig machen kann, müssen Sie ein Rollback für die Transaktion ausführen, indem Sie [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)aufrufen.

 

 



