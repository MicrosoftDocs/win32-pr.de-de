---
description: Ressourcen-Manager
ms.assetid: c717b731-cf0b-45cb-bbff-695410fcf6ce
title: Ressourcen-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33d32d697d58705760002065d005f5927717055f235358c12fd0629de86e14b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870020"
---
# <a name="resource-managers"></a>Ressourcen-Manager

Ein Ressourcen-Manager verwendet das Transaktion-Manager-Protokoll, um den Transaktionsstatus nachzuverfolgen. Die Aktion des Ressourcen-Managers beim Verarbeiten einer Transaktion sieht wie folgt aus:

-   Der Client übergibt eine Transaktion explizit an den RM.
-   Der RM wird mit [**createEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)in die Transaktion eintragen.
-   Der Benutzer kann dann mit dem Ausführen eines beliebigen Vorgangs fortfahren.
-   Wenn der Benutzer CommitTransaction aufruft, sendet DER EINE PREPARE \_ TRANSACTION-Benachrichtigung an den RM. An diesem Punkt leert der RM alle Änderungen, die zum Committen der Transaktion erforderlich wären, auf den Datenträger, kann aber fehlschlagen. Wenn diese Vorgänge erfolgreich sind, signalisiert der RM, dass der Vorbereitungsvorgang abgeschlossen ist, indem [**er PrepareComplete aufruft.**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) Wenn diese Vorgänge fehlschlagen, antwortet der RM durch Aufrufen von [**RollBackEnlistment.**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)
-   Der Ressourcen-Manager empfängt eine Vorbereitungsbenachrichtigung.
-   Der Ressourcen-Manager leert alle daten, die der Transaktion zugeordnet sind, in die Common Log Services-Protokolldatei.
-   Der Ressourcen-Manager ruft die [**PrepareComplete-Funktion**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) auf und wartet darauf, das Transaktionsergebnis von DER TRANSAKTION zu empfangen.
-   Abhängig vom Ergebnis der Transaktion empfängt der Ressourcen-Manager ein Commit- oder Rollbackbenachrichtigungsereignis. Wenn der Ressourcen-Manager eine Commitbenachrichtigung empfängt, macht er die Änderungen dauerhaft und informiert den AUFTRAG durch Aufrufen der [**CommitComplete-Funktion.**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) Wenn der Ressourcen-Manager eine Rollbackbenachrichtigung empfängt, verwirft er alle Änderungen und stellt den Zustand wieder her, der vor einer der transaktiven Änderungen vorhanden war, und informiert den ENTF durch Aufrufen von [**RollbackComplete.**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)

## <a name="resource-manager-functions"></a>Resource Manager Functions

Die folgenden Funktionen werden mit Ressourcen-Managern verwendet.



| Funktion                                                                           | BESCHREIBUNG                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager)                             | Erstellt ein neues Resource Manager-Objekt (RM) und ordnet den RM einem Transaktions-Manager (TM) zu.                                                                               |
| [**GetNotificationResourceManager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)           | Fordert eine Benachrichtigung für einen Ressourcen-Manager (RM) an und empfängt sie. Diese Funktion wird vom RM-Register verwendet, um Benachrichtigungen zu empfangen, wenn sich der Status einer Transaktion ändert.            |
| [**GetNotificationResourceManagerAsync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync) | Fordert asynchrone Benachrichtigungen für einen Ressourcen-Manager (RM) an und empfängt sie. Diese Funktion wird vom RM-Register verwendet, um Benachrichtigungen zu empfangen, wenn sich der Status einer Transaktion ändert. |
| [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager)                                 | Öffnet einen vorhandenen Ressourcen-Manager (RM).                                                                                                                                         |
| [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)                                         | Gibt an, dass der Ressourcen-Manager (RM) alle Verarbeitungsvorgänge abgeschlossen hat, die erforderlich sind, um sicherzustellen, dass ein Commit- oder Abbruchvorgang für die angegebene Transaktion erfolgreich ist.        |
| [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)                                   | Signalisiert, dass dieser Ressourcen-Manager seine Vorbereitungsvorgänge abgeschlossen hat, sodass andere Ressourcen-Manager nun mit den Vorbereitungsvorgängen beginnen können.                                    |
| [**SetResourceManagerCompletionPort**](/windows/desktop/api/Ktmw32/nf-ktmw32-setresourcemanagercompletionport)       | Ordnet den angegebenen E/A-Abschlussport dem angegebenen Ressourcen-Manager (RM) zu. Dieser Port empfängt alle Benachrichtigungen für den RM.                                          |



 

 

 



