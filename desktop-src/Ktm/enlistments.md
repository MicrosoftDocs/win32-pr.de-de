---
description: Ein Ressourcen-Manager trägt eine Transaktion in eine Transaktion ein, wenn er mit der Teilnahme an dieser bestimmten Transaktion beginnt.
ms.assetid: 9c201699-c00b-4efe-9f30-8d4e182de785
title: Eintragungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52820af2a7b280bc4740d0309fb627725e648685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218208"
---
# <a name="enlistments"></a>Eintragungen

Ein Ressourcen-Manager trägt eine Transaktion in eine Transaktion ein, wenn er mit der Teilnahme an dieser bestimmten Transaktion beginnt. Die Eintragung definiert, welche Benachrichtigungen der Ressourcen-Manager akzeptiert. Ein Ressourcen-Manager erstellt ein Eintragung-Objekt, wenn es in eine Transaktion eingetragen wird. Dieses Objekt signalisiert KTM, dass der Ressourcen-Manager (RM) Benachrichtigungen über die angegebene Transaktion anfordert.

Der RM stellt eine [**Benachrichtigungs \_ Masken**](notification-mask.md) Struktur bereit, die detailliert erläutert, welche Benachrichtigungen angefordert werden.

## <a name="enlistment-functions"></a>Eintragung-Funktionen

Die folgenden Funktionen werden bei Eintragung verwendet.



| Funktion                                                                          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Commitcomplete**](/windows/desktop/api/Ktmw32/nf-ktmw32-commitcomplete)                                          | Gibt an, dass ein Ressourcen-Manager (RM) einen Commit für eine Transaktion abgeschlossen hat, die vom Transaktions-Manager angefordert wurde.                                                                                                                                                                                                                                                                        |
| [**"Kreateeintragung"**](/windows/desktop/api/KtmW32/nf-ktmw32-createenlistment)                                      | Erstellt eine Eintragung, legt ihren Anfangszustand fest und öffnet ein Handle für die Eintragung mit dem angegebenen Zugriff.                                                                                                                                                                                                                                                                                          |
| [**Getenlistmentherstellungsinformationen**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) | Ruft eine nicht transparente Struktur der Wiederherstellungsdaten von KTM ab. Wiederherstellungs Informationen werden in einem Protokoll im Namen eines Ressourcen-Managers (RM) gespeichert, indem die Funktion " [**settenlistmentherstellungsinformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation) " aufgerufen wird. Nach einem Fehler kann der RM die [**getenlistmentherstellyinformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) -Funktion verwenden, um die Informationen abzurufen. |
| [**Openeintragung**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment)                                          | Öffnet ein vorhandenes Eintragung-Objekt und gibt ein Handle für die Eintragung zurück.                                                                                                                                                                                                                                                                                                                            |
| [**Read onlyeintragung**](/windows/desktop/api/Ktmw32/nf-ktmw32-readonlyenlistment)                                  | Fordert an, dass die angegebene Eintragung in eine schreibgeschützte Eintragung konvertiert wird. Eine schreibgeschützte Eintragung kann nicht an das Ergebnis der Transaktion teilnehmen und wird nicht dauerhaft für die Wiederherstellung aufgezeichnet.                                                                                                                                                                                                    |
| [**Rollbackeintragung**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbackenlistment)                                  | Führt einen Rollback für die angegebene Transaktion aus, die einer Eintragung zugeordnet ist. Diese Funktion kann nicht für schreibgeschützte Eintragung aufgerufen werden.                                                                                                                                                                                                                                                                   |
| [**"Tenlistmentwiederherstellungsinformationen"**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)      | Legt eine nicht transparente, benutzerdefinierte Struktur von Wiederherstellungsdaten von KTM fest. Die Wiederherstellungs Informationen werden in einem Protokoll im Namen eines Ressourcen-Managers (RM) gespeichert, indem " [**sstenlistmentherstellungsinformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-setenlistmentrecoveryinformation)" aufgerufen wird. Nach einem Fehler kann das RM die Informationen mithilfe von [**getenlistmentherstellungsinformation**](/windows/desktop/api/Ktmw32/nf-ktmw32-getenlistmentrecoveryinformation) abrufen.                  |
| [**Singlephasereject**](/windows/desktop/api/Ktmw32/nf-ktmw32-singlephasereject)                                    | Gibt an, dass der Ressourcen-Manager (RM) eine einphasenanforderung ablehnt. Wenn ein Transaktions-Manager (TM) diesen Befehl empfängt, initiiert er einen Zweiphasencommit und sendet eine Prepare-Anforderung an alle eingetragenen RMS.                                                                                                                                                                                       |



 

 

 



