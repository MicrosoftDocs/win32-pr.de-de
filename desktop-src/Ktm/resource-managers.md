---
description: Ressourcen-Manager
ms.assetid: c717b731-cf0b-45cb-bbff-695410fcf6ce
title: Ressourcen-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b2ea9b1cd834daf3bfbca49bf37d3f2c0956344
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348946"
---
# <a name="resource-managers"></a>Ressourcen-Manager

Ein Ressourcen-Manager verwendet das Transaktions-Manager-Protokoll, um den Transaktionsstatus zu verfolgen. Die Aktion des Ressourcen-Managers bei der Verarbeitung einer Transaktion lautet wie folgt:

-   Der Client übergibt eine Transaktion explizit an den RM.
-   Der RM trägt in der [**Transaktion mithilfe von**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)"" "".
-   Der Benutzer kann dann mit dem Ausführen eines beliebigen Vorgangs fortfahren.
-   Wenn der Benutzer CommitTransaction aufruft, sendet KTM eine Prepare \_ Transaction-Benachrichtigung an den RM. An diesem Punkt werden alle Änderungen, die zum Ausführen eines Commits für die Transaktion erforderlich wären, von der RM auf den Datenträger geleert. Wenn diese Vorgänge erfolgreich ausgeführt werden, signalisiert der RM, dass er den Vorbereitungs Vorgang durch Aufrufen von [**preparecomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)abgeschlossen hat. Wenn diese Vorgänge fehlschlagen, antwortet der RM durch Aufrufen von [**rollbackeintragung**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment).
-   Der Ressourcen-Manager empfängt eine Vorbereitungs Benachrichtigung.
-   Der Ressourcen-Manager Leert alle Daten, die der Transaktion zugeordnet sind, in die allgemeine Protokolldienst-Protokolldatei.
-   Der Ressourcen-Manager ruft die [**preparecomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete) -Funktion auf und wartet darauf, das Ergebnis der Transaktion von KTM zu empfangen.
-   Abhängig vom Ergebnis der Transaktion empfängt der Ressourcen-Manager ein Commit-oder Rollback-Benachrichtigungs Ereignis. Wenn der Ressourcen-Manager eine Commit-Benachrichtigung empfängt, werden die Änderungen permanent gemacht, und der KTM wird durch Aufrufen der [**commitcomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete) -Funktion informiert. Wenn der Ressourcen-Manager eine Rollback-Benachrichtigung empfängt, werden alle Änderungen verworfen und der Status vor den Transaktions Änderungen zurückgesetzt, und der KTM wird durch Aufrufen von [**rollbackcomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)informiert.

## <a name="resource-manager-functions"></a>Ressourcen-Manager Funktionen

Die folgenden Funktionen werden für Ressourcen-Manager verwendet.



| Funktion                                                                           | BESCHREIBUNG                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager)                             | Erstellt ein neues Resource Manager-Objekt (RM) und ordnet das RM einem Transaktions-Manager (TM) zu.                                                                               |
| [**Getnotificationresourcemanager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)           | Fordert und empfängt eine Benachrichtigung für einen Ressourcen-Manager (RM). Diese Funktion wird vom RM-Register verwendet, um Benachrichtigungen zu empfangen, wenn sich der Zustand einer Transaktion ändert.            |
| [**Getnotificationresourcemanagerasync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync) | Fordert und empfängt asynchrone Benachrichtigungen für einen Ressourcen-Manager (RM). Diese Funktion wird vom RM-Register verwendet, um Benachrichtigungen zu empfangen, wenn sich der Zustand einer Transaktion ändert. |
| [**Openresourcemanager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager)                                 | Öffnet einen vorhandenen Ressourcen-Manager (RM).                                                                                                                                         |
| [**Preparecomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)                                         | Gibt an, dass der Ressourcen-Manager (RM) alle erforderlichen Verarbeitungsschritte abgeschlossen hat, um sicherzustellen, dass ein Commit-oder Abbruch Vorgang für die angegebene Transaktion erfolgreich ausgeführt wird.        |
| [**Prepreparecomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)                                   | Signalisiert, dass dieser Ressourcen-Manager seine Vorbereitung abgeschlossen hat, sodass andere Ressourcen-Manager jetzt mit der Vorbereitung beginnen können.                                    |
| [**Setresourcemanagercompletionport**](/windows/desktop/api/Ktmw32/nf-ktmw32-setresourcemanagercompletionport)       | Verknüpft den angegebenen e/a-Abschlussport mit dem angegebenen Ressourcen-Manager (RM). Dieser Port empfängt alle Benachrichtigungen für den RM.                                          |



 

 

 



