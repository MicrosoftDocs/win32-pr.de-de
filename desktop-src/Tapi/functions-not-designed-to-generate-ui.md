---
description: Angenommen, der Dienstanbieter muss ein Dialogfeld (z. b. das Dialogfeld Unimodem oder atsp Talk/hangup) während der Verarbeitung von linemakecall oder linedial anzeigen.
ms.assetid: 46f87947-bfcd-48ad-8c33-7ea4d9caa34c
title: Funktionen, die nicht zum Generieren von Benutzeroberflächen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70bd7ed1395136d1a2d2a31b060127395e8804ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529066"
---
# <a name="functions-not-designed-to-generate-ui"></a>Funktionen, die nicht zum Generieren von Benutzeroberflächen

Angenommen, der Dienstanbieter muss ein Dialogfeld (z. b. das Dialogfeld Unimodem oder atsp **Talk/hangup** ) während der Verarbeitung von [**linemakecall**](/windows/win32/api/tapi/nf-tapi-linemakecall) oder [**linedial**](/windows/win32/api/tapi/nf-tapi-linedial)anzeigen. In diesem Fall ist dies der Dienstanbieter, nicht die Anwendung, der entscheidet, dass die Benutzeroberfläche angezeigt werden muss.

Um die Benutzeroberflächen-DLL im Anwendungsprozess aufzurufen, ruft der Dienstanbieter den TSPI- [*Zeilen \_ Ereignis*](/windows/win32/api/tspi/nc-tspi-lineevent) Rückruf auf und erzeugt dabei eine Zeile mit der Meldung "" mit der Meldung "", dass ein Zeiger auf eine Struktur des Typs " [**tuispikreatedialoginstancepara**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)" übergeben wird. [**\_**](line-createdialoginstance.md) Diese Struktur enthält die **dwrequestid** der Funktion, der die Benutzeroberfläche zugeordnet ist, sodass die Client Anwendung, in der die Benutzeroberfläche generiert werden soll, von tapisrv identifiziert werden kann.

Tapisrv verlangt, dass die Instanz von TAPI der richtigen Anwendung die Benutzeroberflächen-DLL lädt und einen Thread für die Benutzeroberfläche innerhalb des Anwendungsprozesses erstellt. In diesem neuen UI-Thread ruft TAPI die [**tuispi \_ providergenericdialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) -Funktion der UI-dll auf und übergibt dabei Daten, die vom Telefoniedienstanbieter in der Struktur angegeben wurden, die mit der [**Zeile " \_ foratedialoginstance**](line-createdialoginstance.md) " übergeben wurde. die Benutzeroberflächen-DLL zeigt das entsprechende Dialogfeld an Die Benutzeroberflächen-DLL gibt nicht von " **tuispi \_ providergenericdialog** " zurück, bis das Dialogfeld geschlossen wird.

Der Telefoniedienstanbieter kann aktualisierte Daten generieren, um Sie im Dialogfeld anzuzeigen (oder z. b. das Dialogfeld zu schließen, wenn der Rückruf abgebrochen oder andere Ereignisse eintreten), indem eine [**Zeile \_ senddialoginstancedata**](line-senddialoginstancedata.md) -Nachricht gesendet wird. Tapisrv überträgt die Daten an TAPI, das die Funktion " [**tuispi \_ providergenericdialogdata**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) " der UI-DLL aufruft. Dieser Mechanismus stellt ein unidirektionales "Send" an die Benutzeroberflächen-DLL bereit. Wenn die Benutzeroberflächen-DLL den Telefoniedienstanbieter über die Ergebnisse des Dialog Felds informieren oder andere Daten abrufen möchte, kann Sie die [*dllcallbackproc*](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) -Funktion aufrufen (einen Zeiger, den Sie empfangen hat, als " [**tuispi \_ providergenericdialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) " aufgerufen wurde).

Wenn das Dialogfeld verworfen wird, kehrt [**tuispi \_ providergenericdialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) zu TAPI zurück. TAPI ruft [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary) auf, um die UI-DLL freizugeben, und beendet den UI-Thread, den er im Anwendungskontext erstellt hat. Anschließend fordert er tapisrv auf, die [**TSPI \_ providerfredialoginstance**](/windows/win32/api/tspi/nf-tspi-tspi_providerfreedialoginstance) -Funktion des Telefoniedienstanbieters aufzurufen, um die Bindung der Zuordnung aufzuheben, die erstellt wurde, als der Telefoniedienstanbieter ursprünglich die [**Zeile " \_ froatedialoginstance**](line-createdialoginstance.md) " Diese Funktion wird auch aufgerufen, wenn der Anwendungsprozess unerwartet beendet wird, bevor " **tuispi \_ providergenericdialog** " zurückgegeben wird.

 

 
