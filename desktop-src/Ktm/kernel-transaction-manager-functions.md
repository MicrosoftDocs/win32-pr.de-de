---
description: Die folgenden Funktionen werden mit Transaktionen verwendet.
ms.assetid: e9704ea8-e67d-4278-b77e-1d4787224d52
title: Kerneltransaktions-Manager-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 221bcc13bb1cfb1f8cc67eb4d16f40a27799b921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868476"
---
# <a name="kernel-transaction-manager-functions"></a>Kerneltransaktions-Manager-Funktionen

Die folgenden Funktionen werden mit Transaktionen verwendet.



| Funktion                                                            | BESCHREIBUNG                                                                                     |
|---------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction)                      | Fordert an, dass die angegebene Transaktion ein Commit ausgeführt wird.                                           |
| [**Committransaktionasync**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransactionasync)            | Fordert an, dass die angegebene Transaktion ein Commit ausgeführt wird.                                           |
| [**CreateTransaction**](/windows/desktop/api/KtmW32/nf-ktmw32-createtransaction)                      | Erstellt ein neues Transaktions Objekt.                                                               |
| [**Gettransaktionid**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionid)                        | Ruft die ID für die angegebene Transaktion ab.                                                   |
| [**Gettransaktioninformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactioninformation) | Gibt die angeforderten Informationen zur angegebenen Transaktion zurück.                              |
| [**Opentransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransaction)                          | Öffnet eine vorhandene Transaktion.                                                                  |
| [**Rollbackcomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackcomplete)                        | Gibt an, dass der Ressourcen-Manager (RM) das Rollback einer Transaktion erfolgreich abgeschlossen hat. |
| [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction)                  | Fordert an, dass für die angegebene Transaktion ein Rollback ausgeführt wird.                                         |
| [**Rollbacktransaktionasync**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransactionasync)        | Fordert an, dass für die angegebene Transaktion ein Rollback ausgeführt wird. Diese Funktion gibt asynchron zurück.   |
| [**Settransaktioninformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-settransactioninformation)      | Legt die Transaktionsinformationen für die angegebene Transaktion fest.                                 |



 

Die folgenden Funktionen werden bei Eintragung verwendet.



| Funktion                                                                          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Commitcomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)                                          | Gibt an, dass ein RM den Commit einer Transaktion abgeschlossen hat, die vom Transaktions-Manager (TM) angefordert wurde.                                                                                                                                                                                                                                                                        |
| [**Commitenlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-commitenlistment)                                      | Führt für die angegebene Eintragung einen Commit für die Transaktion aus.                                                                                                                                                                                                                                                                                                                                |
| [**Getenlistmentid**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentid)                                        | Ruft die ID für die angegebene Eintragung ab.                                                                                                                                                                                                                                                                                                                                         |
| [**"Kreateeintragung"**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)                                      | Erstellt eine Eintragung, legt ihren Anfangszustand fest und öffnet ein Handle für die Eintragung mit dem angegebenen Zugriff.                                                                                                                                                                                                                                                                       |
| [**Getenlistmentherstellungsinformationen**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) | Ruft eine nicht transparente Struktur der Wiederherstellungsdaten von KTM ab. Wiederherstellungs Informationen werden in einem Protokoll im Auftrag eines RM gespeichert, indem die Funktion " [**settenlistmentherstellungsinformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation) " aufgerufen wird. Nach einem Fehler kann der RM die [**getenlistmentherstellyinformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) -Funktion verwenden, um die Informationen abzurufen. |
| [**Openeintragung**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)                                          | Öffnet ein vorhandenes Eintragung-Objekt und gibt ein Handle für die Eintragung zurück.                                                                                                                                                                                                                                                                                                         |
| [**Prepareeintragung**](/windows/desktop/api/KtmW32/nf-ktmw32-prepareenlistment)                                    | Wird von der übergeordneten TM-Funktion aufgerufen, um anzugeben, dass die Vorbereitung der Vorbereitung abgeschlossen ist.                                                                                                                                                                                                                                                                                                   |
| [**Vorprepareeintragung**](/windows/desktop/api/KtmW32/nf-ktmw32-preprepareenlistment)                              | Wird von der übergeordneten TM-Funktion aufgerufen, um anzugeben, dass die Vorbereitung der Vorbereitung abgeschlossen ist.                                                                                                                                                                                                                                                                                                   |
| [**Wiederherstellung**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverenlistment)                                    | Stellt den Status einer Eintragung wieder her.                                                                                                                                                                                                                                                                                                                                                      |
| [**Read onlyeintragung**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)                                  | Fordert an, dass die angegebene Eintragung in eine schreibgeschützte Eintragung konvertiert wird. Eine schreibgeschützte Eintragung kann nicht an das Ergebnis der Transaktion teilnehmen und wird nicht dauerhaft für die Wiederherstellung aufgezeichnet.                                                                                                                                                                                 |
| [**Rollbackeintragung**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)                                  | Führt einen Rollback für die angegebene Transaktion aus, die einer Eintragung zugeordnet ist. Diese Funktion kann nicht für schreibgeschützte Eintragung aufgerufen werden.                                                                                                                                                                                                                                                |
| [**"Tenlistmentwiederherstellungsinformationen"**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)      | Legt eine nicht transparente, benutzerdefinierte Struktur von Wiederherstellungsdaten von KTM fest. Wiederherstellungs [**Informationen werden**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)in einem Protokoll im Namen eines RM gespeichert, indem "" "" Nach einem Fehler kann das RM die Informationen mithilfe von [**getenlistmentherstellungsinformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) abrufen.                  |
| [**Singlephasereject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)                                    | Gibt an, dass der RM eine einphasenanforderung ablehnt. Wenn eine TM diesen Befehl empfängt, initiiert Sie einen Zweiphasencommit und sendet eine Prepare-Anforderung an alle eingetragenen RMS.                                                                                                                                                                                                             |



 

Die folgenden Funktionen werden für Ressourcen-Manager verwendet.



| Funktion                                                                           | BESCHREIBUNG                                                                                                                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateResourceManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createresourcemanager)                             | Erstellt ein neues RM-Objekt und ordnet das RM einem Transaktions-Manager (TM) zu.                                                                                  |
| [**Getnotificationresourcemanager**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanager)           | Fordert eine Benachrichtigung für RM an und empfängt diese. Diese Funktion wird vom RM-Register verwendet, um Benachrichtigungen zu empfangen, wenn sich der Zustand einer Transaktion ändert.                 |
| [**Getnotificationresourcemanagerasync**](/windows/desktop/api/KtmW32/nf-ktmw32-getnotificationresourcemanagerasync) | Fordert die asynchrone Benachrichtigung für einen RM an und empfängt diese. Diese Funktion wird vom RM zum Registrieren für den Empfang von Benachrichtigungen verwendet, wenn sich der Status einer Transaktion ändert. |
| [**Openresourcemanager**](/windows/desktop/api/Ktmw32/nf-ktmw32-openresourcemanager)                                 | Öffnet ein vorhandenes RM.                                                                                                                                            |
| [**Preparecomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-preparecomplete)                                         | Gibt an, dass der RM alle erforderlichen Verarbeitungsschritte abgeschlossen hat, um sicherzustellen, dass ein Commit-oder Abbruch Vorgang für die angegebene Transaktion erfolgreich ausgeführt wird.           |
| [**Prepreparecomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-prepreparecomplete)                                   | Signalisiert, dass dieser RM seine vorvorbereitungs Arbeit abgeschlossen hat, sodass andere RMS nun mit dem Vorbereiten von Vorgängen beginnen können.                                                |
| [**Wiederherstellbarkeits Manager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recoverresourcemanager)                           | Stellt den Status eines RM aus seiner Protokolldatei wieder her.                                                                                                                         |
| [**Setresourcemanagercompletionport**](/windows/desktop/api/Ktmw32/nf-ktmw32-setresourcemanagercompletionport)       | Ordnet den angegebenen e/a-Abschlussport dem angegebenen RM zu. Dieser Port empfängt alle Benachrichtigungen für den RM.                                             |



 

Die folgenden Funktionen werden mit dem Transaktions-Manager verwendet.



| Funktion                                                                            | BESCHREIBUNG                                                                 |
|-------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [**"Kreatetransaktionmanager"**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager)                        | Erstellt ein neues TM-Objekt und gibt ein Handle mit dem angegebenen Zugriff zurück.     |
| [**Getcurrentclocktransaktionmanager**](/windows/desktop/api/Ktmw32/nf-ktmw32-getcurrentclocktransactionmanager) | Erhält einen virtuellen Uhrzeitwert aus einem TM.                                    |
| [**Gettransaktionmanagerid**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionmanagerid)                          | Ruft einen Bezeichner für die angegebene TM-ab.                                 |
| [**Opentransactionmanager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager)                            | Öffnet ein vorhandenes TM.                                                       |
| [**Opentransactionmanagerbyid**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanagerbyid)                    | Öffnet ein vorhandenes TM.                                                       |
| [**Wiederherstellbarkeits-Manager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)                      | Stellt den Status einer TM-Datei aus der zugehörigen Protokolldatei wieder her.                                    |
| [**Renametransaktionmanager**](/windows/desktop/api/KtmW32/nf-ktmw32-renametransactionmanager)                        | Benennt eine TM-Datei um.                                                               |
| [**Rollforwardtransaktionmanager**](/windows/desktop/api/KtmW32/nf-ktmw32-rollforwardtransactionmanager)              | Stellt den Status von TM aus seiner Protokolldatei in den angegebenen virtuellen Uhrzeitwert wieder her. |



 

 

 



