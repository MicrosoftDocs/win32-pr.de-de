---
description: Ein Transaktions-Manager (TM) ist eine Instanz eines Protokolls. In KTM geben die TM-Objekte das Protokoll und einige Funktionen des TM an. Es gibt in der Regel viele TM-Objekte auf einem bestimmten Knoten. Ressourcen-Manager (RMs) müssen einem bestimmten TM zugeordnet sein.
ms.assetid: 8d43977a-84cf-4109-b7db-f9c94a226c5d
title: Transaktions-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0ea492a3eb10d95002d4e0a61500e7f1e74e87da21bc90daf680a2899e3fa67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119424440"
---
# <a name="transaction-managers"></a>Transaktions-Manager

Ein Transaktions-Manager (TM) ist eine Instanz eines Protokolls. In KTM geben die TM-Objekte das Protokoll und einige Funktionen des TM an. Es gibt in der Regel viele TM-Objekte auf einem bestimmten Knoten. Ressourcen-Manager (RMs) müssen einem bestimmten TM zugeordnet sein. Es gibt drei Arten von TMs:

-   Ein flüchtiger TM, der über kein Protokoll verfügt.
-   Ein reguläres TM, das über ein Protokoll verfügt und zum Koordinieren der Transaktionen von mindestens einem RMs verwendet wird.
-   Ein überlegener Transaktions-Manager.

## <a name="volatile-transaction-managers"></a>Flüchtige Transaktions-Manager

Ein flüchtiges TM ist ein TM für schreibgeschützte oder flüchtige RMs. Es verfügt nicht über ein Protokoll und bleibt den Status von Transaktionen bei Systemneustarts nicht erhalten.

## <a name="transaction-managers"></a>Transaktions-Manager

TMs verfügen über ein Protokoll, mindestens ein dauerhaftes oder flüchtiges RMs oder beides. Der TM wird den Status einer Transaktion über Systemneustarts hinweg beibehalten, bis die Transaktionen abgeschlossen sind. Ein presumed-abort-Modell wird verwendet, sodass ein Rollback für Transaktionen, die aktiv waren, aber nicht vorbereitet wurden, wenn das TM-Objekt heruntergefahren wird. Wenn Sie einen TM zum ersten Mal öffnen, müssen Sie den TM wiederherstellen, indem Sie die [**RecoverTransactionManager-Funktion**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager) aufrufen.

## <a name="superior-transaction-managers"></a>Überlegene Transaktions-Manager

Ein überlegener TM ist ein TM für andere TMs. Er koordiniert Transaktionen. Außerdem werden **TRANSACTION \_ NOTIFY \_ PREPARE-Benachrichtigungen** an den Kerneltransaktions-Manager (KTM) gesendet. Ein Beispiel für ein überlegenes TM ist Microsoft Distributed Transaction Coordinator (DTC). Diese Fähigkeit ist mit einer zusätzlichen Wiederherstellungszeit verantwortlich. Während der Wiederherstellung muss der RM zunächst die [**OpenEnlistment-Funktion**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) aufrufen, um die Eintragung erneut zu öffnen. Sie muss auch das Transaktionsergebnis liefern (oder erneut liefern), wenn für die Transaktion ein Committed ausgeführt wurde. Es ist kostenlos, ein Ergebnis zu liefern, indem entweder die [**CommitTransaction-Funktion**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) oder die [**RollbackTransaction-Funktion aufruft.**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction) Diese Verpflichtung endet erst, wenn sie ein zugeordnetes **TRANSACTION \_ NOTIFY COMMIT \_ \_ COMPLETE-** oder **TRANSACTION NOTIFY \_ \_ ROLLBACK \_ COMPLETE-Benachrichtigungsereignis** empfangen hat. Wenn ein übergeordnetes TM diese Vorgänge zur Wiederherstellungszeit nicht ausführen kann, bereinigt das KTM alle Transaktionen, die bis zum Ende der Wiederherstellungsphase keine Ergebnisse erhalten haben. Dies kann jedoch zu inkonsistenten Transaktionsergebnissen führen.

## <a name="transaction-manager-functions"></a>Transaction Manager-Funktionen

Die folgenden Funktionen werden mit Transaktions-Managern verwendet.



| Funktion                                                                            | Beschreibung                                                                                    |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**CreateTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager)                        | Erstellt ein neues Tm-Objekt (Transaction Manager) und gibt ein Handle mit dem angegebenen Zugriff zurück.  |
| [**GetCurrentClockTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-getcurrentclocktransactionmanager) | Erhält einen Virtuellen Uhrwert von einem Transaktions-Manager.                                      |
| [**GetTransactionManagerId**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionmanagerid)                          | Erhält einen Bezeichner für den angegebenen Transaktions-Manager.                                   |
| [**OpenTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager)                            | Öffnet einen vorhandenen Transaktions-Manager.                                                         |
| [**RecoverTransactionManager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)                      | Stellt den Status eines Transaktions-Managers aus seiner Protokolldatei wieder wieder auf.                                      |
| [**RollforwardTransactionManager**](/windows/desktop/api/KtmW32/nf-ktmw32-rollforwardtransactionmanager)              | Stellt den Status eines Transaktions-Managers aus seiner Protokolldatei auf den angegebenen Wert der virtuellen Uhr wieder wieder auf. |



 

 

 



