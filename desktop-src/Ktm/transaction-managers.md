---
description: Ein Transaktions-Manager (TM) ist eine Instanz eines Protokolls. In KTM geben die TM-Objekte das Protokoll und einige Funktionen der TM-Funktionalität an. Es gibt in der Regel viele TM-Objekte auf einem bestimmten Knoten. Ressourcen-Manager (RMS) müssen mit einem bestimmten TM verknüpft werden.
ms.assetid: 8d43977a-84cf-4109-b7db-f9c94a226c5d
title: Transaktions-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 313215816642201c75ae5f0facae3bf98799c8d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358856"
---
# <a name="transaction-managers"></a>Transaktions-Manager

Ein Transaktions-Manager (TM) ist eine Instanz eines Protokolls. In KTM geben die TM-Objekte das Protokoll und einige Funktionen der TM-Funktionalität an. Es gibt in der Regel viele TM-Objekte auf einem bestimmten Knoten. Ressourcen-Manager (RMS) müssen mit einem bestimmten TM verknüpft werden. Es gibt drei Arten von TMS:

-   Ein flüchtiges TM ohne Protokoll.
-   Ein reguläres TM, das über ein Protokoll verfügt und zum Koordinieren der Transaktionen von einem oder mehreren RMS verwendet wird.
-   Ein übergeordneter Transaktions-Manager.

## <a name="volatile-transaction-managers"></a>Flüchtige Transaktions-Manager

Ein flüchtiges TM ist ein TM für Schreib geschütztes oder flüchtiges RMS. Sie verfügt nicht über ein Protokoll und speichert den Status von Transaktionen nicht über Systemneustarts hinweg.

## <a name="transaction-managers"></a>Transaktions-Manager

TMS verfügen über ein Protokoll, mindestens ein dauerhaftes oder flüchtiges RMS oder beides. Der TM speichert den Status einer Transaktion über Systemneustarts hinweg, bis die Transaktionen abgeschlossen sind. Ein mutmaßliches Abbruch Modell wird verwendet, sodass Transaktionen, die aktiv sind, aber nicht vorbereitet sind, wenn das TM-Objekt heruntergefahren wird, ein Rollback ausgeführt werden. Wenn Sie ein TM zum ersten Mal öffnen, müssen Sie das TM durch Aufrufen der Funktion " [**Recover transaktionmanager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager) " wiederherstellen.

## <a name="superior-transaction-managers"></a>Übergeordnete Transaktions-Manager

Ein überlegenes TM ist eine TM-Datei für andere TMS. Es koordiniert Transaktionen. Außerdem werden Benachrichtigungs Benachrichtigungen für **Transaktionen \_ \_** an den Kerneltransaktions-Manager (KTM) ausgegeben. Ein Beispiel für einen übergeordneten TM ist die Microsoft Distributed Transaction Coordinator (DTC). Diese Möglichkeit ist mit einer zusätzlichen Wiederherstellungszeit verantwortlich. Während der Wiederherstellung muss der RM zuerst die [**openenlistment**](/windows/desktop/api/Ktmw32/nf-ktmw32-openenlistment) -Funktion zum erneuten Öffnen der Eintragung aufzurufen. Außerdem muss das Ergebnis der Transaktion bereitgestellt (oder erneut übertragen) werden, wenn für die Transaktion ein Commit ausgeführt wurde. Es ist kostenlos, ein Ergebnis durch Aufrufen der [**CommitTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-committransaction) -Funktion oder der [**RollbackTransaction**](/windows/desktop/api/Ktmw32/nf-ktmw32-rollbacktransaction) -Funktion bereitzustellen. Diese Verpflichtung endet nicht, bis Sie ein zugeordnetes Transaktions Benachrichtigungs- **\_ \_ Commit \_ abgeschlossen** oder ein **\_ \_ Rollback \_** für eine Transaktions Benachrichtigung abgeschlossen hat. Wenn ein übergeordnetes TM diese Vorgänge nicht zur Wiederherstellungszeit ausführt, bereinigt KTM alle Transaktionen, die nach Ende der Wiederherstellungs Phase keine Ergebnisse empfangen haben. Dies kann jedoch zu inkonsistenten Transaktions Ergebnissen führen.

## <a name="transaction-manager-functions"></a>Transaktions-Manager-Funktionen

Die folgenden Funktionen werden mit dem Transaktions-Manager verwendet.



| Funktion                                                                            | BESCHREIBUNG                                                                                    |
|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**"Kreatetransaktionmanager"**](/windows/desktop/api/Ktmw32/nf-ktmw32-createtransactionmanager)                        | Erstellt ein neues Transaktions-Manager-Objekt (TM) und gibt ein Handle mit dem angegebenen Zugriff zurück.  |
| [**Getcurrentclocktransaktionmanager**](/windows/desktop/api/Ktmw32/nf-ktmw32-getcurrentclocktransactionmanager) | Erhält einen virtuellen Uhrzeitwert von einem Transaktions-Manager.                                      |
| [**Gettransaktionmanagerid**](/windows/desktop/api/Ktmw32/nf-ktmw32-gettransactionmanagerid)                          | Ruft einen Bezeichner für den angegebenen Transaktions-Manager ab.                                   |
| [**Opentransactionmanager**](/windows/desktop/api/Ktmw32/nf-ktmw32-opentransactionmanager)                            | Öffnet einen vorhandenen Transaktions-Manager.                                                         |
| [**Wiederherstellbarkeits-Manager**](/windows/desktop/api/Ktmw32/nf-ktmw32-recovertransactionmanager)                      | Stellt den Status eines Transaktions-Managers aus seiner Protokolldatei wieder her.                                      |
| [**Rollforwardtransaktionmanager**](/windows/desktop/api/KtmW32/nf-ktmw32-rollforwardtransactionmanager)              | Stellt den Status eines Transaktions-Managers aus seiner Protokolldatei in den angegebenen virtuellen Uhrzeitwert wieder her. |



 

 

 



