---
description: Die folgenden Funktionen werden mit Transaktionen verwendet.
ms.assetid: e9704ea8-e67d-4278-b77e-1d4787224d52
title: Kerneltransaktions-Manager-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce98208b6ac78795be95b7255e9f263971ad6f08237e75ac0ef661c38a0878a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535280"
---
# <a name="kernel-transaction-manager-functions"></a>Kerneltransaktions-Manager-Funktionen

Die folgenden Funktionen werden mit Transaktionen verwendet.



| Funktion                                                            | Beschreibung                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**Committransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | Fordert an, dass für die angegebene Transaktion ein Commit ausgeführt wird.                                           |
| [**CommitTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | Fordert an, dass für die angegebene Transaktion ein Commit ausgeführt wird.                                           |
| [**Createtransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | Erstellt ein neues Transaktionsobjekt.                                                               |
| [**GetTransactionId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionid)                        | Ruft die ID für die angegebene Transaktion ab.                                                   |
| [**GetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | Gibt die angeforderten Informationen zur angegebenen Transaktion zurück.                              |
| [**OpenTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | Öffnet eine vorhandene Transaktion.                                                                  |
| [**RollbackComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)                        | Gibt an, dass der Ressourcen-Manager (RM) das Rollback einer Transaktion erfolgreich abgeschlossen hat. |
| [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | Fordert an, dass für die angegebene Transaktion ein Rollback ausgeführt wird.                                         |
| [**RollbackTransactionAsync**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | Fordert an, dass für die angegebene Transaktion ein Rollback ausgeführt wird. Diese Funktion gibt asynchron zurück.   |
| [**SetTransactionInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | Legt die Transaktionsinformationen für die angegebene Transaktion fest.                                 |



 

Die folgenden Funktionen werden mit Eintragungen verwendet.



| Funktion                                                                          | Beschreibung                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)                                          | Gibt an, dass ein RM den Commit einer Transaktion abgeschlossen hat, die vom Transaktions-Manager (TM) angefordert wurde.                                                                                                                                                                                                                                                                        |
| [**CommitEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-commitenlistment)                                      | Committet die Transaktion für die angegebene Eintragung.                                                                                                                                                                                                                                                                                                                                |
| [**GetEnlistmentId**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentid)                                        | Ruft die ID für die angegebene Eintragung ab.                                                                                                                                                                                                                                                                                                                                         |
| [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)                                      | Erstellt eine Eintragung, legt den Anfangszustand fest und öffnet ein Handle für die Eintragung mit dem angegebenen Zugriff.                                                                                                                                                                                                                                                                       |
| [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) | Ruft eine nicht transparente Struktur von Wiederherstellungsdaten aus DEM -Ausdruck ab. Wiederherstellungsinformationen werden im Namen eines RM in einem Protokoll gespeichert, indem die [**Funktion SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation) aufgerufen wird. Nach einem Fehler kann der RM die [**GetEnlistmentRecoveryInformation-Funktion**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) verwenden, um die Informationen abzurufen. |
| [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)                                          | Öffnet ein vorhandenes Eintragungsobjekt und gibt ein Handle für die Eintragung zurück.                                                                                                                                                                                                                                                                                                         |
| [**PrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-prepareenlistment)                                    | Wird von übergeordnetem TM aufgerufen, um anzugeben, dass die Vorbereitungen abgeschlossen wurden.                                                                                                                                                                                                                                                                                                   |
| [**PrePrepareEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment)                              | Wird von übergeordnetem TM aufgerufen, um anzugeben, dass die Vorbereitungen abgeschlossen wurden.                                                                                                                                                                                                                                                                                                   |
| [**RecoverEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverenlistment)                                    | Wiederherstellung des Zustands einer Eintragung.                                                                                                                                                                                                                                                                                                                                                      |
| [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)                                  | Fordert an, dass die angegebene Eintragung in eine schreibgeschützte Eintragung konvertiert wird. Eine schreibgeschützte Eintragung kann nicht am Ergebnis der Transaktion beteiligt sein und wird nicht dauerhaft für die Wiederherstellung aufgezeichnet.                                                                                                                                                                                 |
| [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)                                  | Führt ein Rollback der angegebenen Transaktion aus, die einer Eintragung zugeordnet ist. Diese Funktion kann nicht für schreibgeschützte Eintragungen aufgerufen werden.                                                                                                                                                                                                                                                |
| [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)      | Legt eine nicht transparente, benutzerdefinierte Struktur von Wiederherstellungsdaten aus DEM BER fest. Wiederherstellungsinformationen werden im Namen eines RM in einem Protokoll gespeichert, indem [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)aufgerufen wird. Nach einem Fehler kann der RM [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) verwenden, um die Informationen abzurufen.                  |
| [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)                                    | Gibt an, dass der RM eine Einphasenanforderung abgibt. Wenn ein TM diesen Aufruf empfängt, initiiert er einen zweistufigen Commit und sendet eine Vorbereitungsanforderung an alle eingetragenen RMs.                                                                                                                                                                                                             |



 

Die folgenden Funktionen werden mit Ressourcen-Managern verwendet.



| Funktion                                                                           | Beschreibung                                                                                                                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager)                             | Erstellt ein neues RM-Objekt und ordnet den RM einem Transaktions-Manager (TM) zu.                                                                                  |
| [**GetNotificationResourceManager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)           | Fordert eine Benachrichtigung für RM an und empfängt sie. Diese Funktion wird vom RM-Register verwendet, um Benachrichtigungen zu empfangen, wenn sich der Status einer Transaktion ändert.                 |
| [**GetNotificationResourceManagerAsync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync) | Fordert asynchrone Benachrichtigungen für einen RM an und empfängt diese. Diese Funktion wird vom RM verwendet, um sich zu registrieren, um Benachrichtigungen zu empfangen, wenn sich der Status einer Transaktion ändert. |
| [**OpenResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager)                                 | Öffnet einen vorhandenen RM.                                                                                                                                            |
| [**PrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)                                         | Gibt an, dass der RM alle erforderlichen Verarbeitungsvorgänge abgeschlossen hat, um sicherzustellen, dass ein Commit- oder Abbruchvorgang für die angegebene Transaktion erfolgreich ist.           |
| [**PrePrepareComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)                                   | Signalisiert, dass dieser RM seine Vorbereitungsvorgänge abgeschlossen hat, sodass andere RMs jetzt mit den Vorbereitungsvorgängen beginnen können.                                                |
| [**RecoverResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverresourcemanager)                           | Stellt den Zustand eines RM aus seiner Protokolldatei wieder her.                                                                                                                         |
| [**SetResourceManagerCompletionPort**](/windows/desktop/api/Ktmw32/nf-ktmw32-setresourcemanagercompletionport)       | Ordnet den angegebenen E/A-Abschlussport dem angegebenen RM zu. Dieser Port empfängt alle Benachrichtigungen für den RM.                                             |



 

Die folgenden Funktionen werden mit Transaktions-Managern verwendet.



| Funktion                                                                            | Beschreibung                                                                 |
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager)                        | Erstellt ein neues TM-Objekt und gibt ein Handle mit dem angegebenen Zugriff zurück.     |
| [**GetCurrentClockTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-getcurrentclocktransactionmanager) | Ruft einen virtuellen Uhrwert von einem TM ab.                                    |
| [**GetTransactionManagerId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionmanagerid)                          | Ruft einen Bezeichner für das angegebene TM ab.                                 |
| [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager)                            | Öffnet ein vorhandenes TM.                                                       |
| [**OpenTransactionManagerById**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanagerbyid)                    | Öffnet ein vorhandenes TM.                                                       |
| [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)                      | Stellt den Zustand eines TM aus seiner Protokolldatei wieder her.                                    |
| [**RenameTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-renametransactionmanager)                        | Benennt einen TM um.                                                               |
| [**RollforwardTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-rollforwardtransactionmanager)              | Stellt den TM-Zustand aus der Protokolldatei auf den angegebenen Wert der virtuellen Uhr wieder auf. |



 

 

 



