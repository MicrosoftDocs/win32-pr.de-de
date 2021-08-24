---
description: Ein Ressourcen-Manager nimmt eine Transaktion auf, wenn er mit der Teilnahme an dieser bestimmten Transaktion beginnt.
ms.assetid: 9c201699-c00b-4efe-9f30-8d4e182de785
title: Eintragungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c19fea9c19da9bb16f81bd417e22c943876997ac224e3823020e5660218dfa5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146583"
---
# <a name="enlistments"></a>Eintragungen

Ein Ressourcen-Manager nimmt eine Transaktion auf, wenn er mit der Teilnahme an dieser bestimmten Transaktion beginnt. Die Eintragung definiert, welche Benachrichtigungen der Ressourcen-Manager akzeptiert. Ein Ressourcen-Manager erstellt ein Eintragungsobjekt, wenn er in eine Transaktion einträgt. Dieses Objekt signalisiert KTM, dass der Ressourcen-Manager (RM) Benachrichtigungen über die angegebene Transaktion an fordert.

Der RM stellt eine [**\_ BENACHRICHTIGUNGSMASKEnstruktur**](notification-mask.md) zur Verfügung, die die Benachrichtigungen anfing, die er anfing.

## <a name="enlistment-functions"></a>Eintragungsfunktionen

Die folgenden Funktionen werden mit Eintragungen verwendet.



| Funktion                                                                          | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommitComplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)                                          | Gibt an, dass ein Ressourcen-Manager (RM) das Committen einer Transaktion abgeschlossen hat, die vom Transaktions-Manager (TM) angefordert wurde.                                                                                                                                                                                                                                                                        |
| [**CreateEnlistment**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)                                      | Erstellt eine Eintragung, legt ihren Anfangszustand fest und öffnet ein Handle für die Eintragung mit dem angegebenen Zugriff.                                                                                                                                                                                                                                                                                          |
| [**GetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) | Ruft eine nicht transparente Struktur von Wiederherstellungsdaten aus KTM ab. Wiederherstellungsinformationen werden im Namen eines Ressourcen-Managers (RM) in einem Protokoll gespeichert, indem die [**SetEnlistmentRecoveryInformation-Funktion aufruft.**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation) Nach einem Fehler kann der RM die [**GetEnlistmentRecoveryInformation-Funktion**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) verwenden, um die Informationen abzurufen. |
| [**OpenEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)                                          | Öffnet ein vorhandenes Eintragungsobjekt und gibt ein Handle an die Eintragung zurück.                                                                                                                                                                                                                                                                                                                            |
| [**ReadOnlyEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)                                  | Fordert an, dass die angegebene Eintragung in eine schreibgeschützte Eintragung konvertiert wird. Eine schreibgeschützte Eintragung kann nicht am Ergebnis der Transaktion teilnehmen und wird nicht dauerhaft für die Wiederherstellung aufgezeichnet.                                                                                                                                                                                                    |
| [**RollbackEnlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)                                  | Führt ein Rollback für die angegebene Transaktion aus, die einer Eintragung zugeordnet ist. Diese Funktion kann nicht für schreibgeschützte Eintragungen aufgerufen werden.                                                                                                                                                                                                                                                                   |
| [**SetEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)      | Legt eine nicht transparente, benutzerdefinierte Struktur von Wiederherstellungsdaten aus KTM fest. Wiederherstellungsinformationen werden im Namen eines Ressourcen-Managers (RM) in einem Protokoll gespeichert, indem [**SetEnlistmentRecoveryInformation aufruft.**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation) Nach einem Fehler kann der RM [**getEnlistmentRecoveryInformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) verwenden, um die Informationen abzurufen.                  |
| [**SinglePhaseReject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)                                    | Gibt an, dass der Ressourcen-Manager (RM) eine einphasenbasierte Anforderung ablehnt. Wenn ein Transaktions-Manager (TM) diesen Aufruf empfängt, initiiert er einen zweiphasenbasierten Commit und sendet eine Vorbereitungsanforderung an alle eingetragenen RMs.                                                                                                                                                                                       |



 

 

 



