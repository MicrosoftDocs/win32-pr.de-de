---
description: Wenn ein Dienst Steuerungsprogramm anfordert, dass ein neuer Dienst ausgeführt wird, startet der Dienststeuerungs-Manager (SCM) den Dienst und sendet eine Start Anforderung an den Steuerelement Verteiler.
ms.assetid: e55e056f-7628-4e3d-9aea-b55c371b4287
title: ServiceMain-Dienstfunktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed50f0f378f348415e56827a09fcf17eea7fc330
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960631"
---
# <a name="service-servicemain-function"></a>ServiceMain-Dienstfunktion

Wenn ein Dienst Steuerungsprogramm anfordert, dass ein neuer Dienst ausgeführt wird, startet der Dienststeuerungs-Manager (SCM) den Dienst und sendet eine Start Anforderung an den Steuerelement Verteiler. Der Steuerelement Verteiler erstellt einen neuen Thread, um die [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) -Funktion für den Dienst auszuführen. Ein Beispiel finden Sie unter [Schreiben einer ServiceMain-Funktion](writing-a-servicemain-function.md).

Die [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona) -Funktion sollte die folgenden Aufgaben ausführen:

1.  Initialisieren Sie alle globalen Variablen.
2.  Wenn Sie die [**registerservicectrlhandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) -Funktion sofort aufrufen, um eine [**Handlerfunktion**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function) zum Verarbeiten von Steuerungsanforderungen für den Dienst zu registrieren. Der Rückgabewert von **registerservicectrlhandler** ist ein *Dienststatus handle* , das in Aufrufen verwendet wird, um den SCM über den Dienststatus zu benachrichtigen.
3.  Initialisierung ausführen. Wenn die Ausführungszeit des Initialisierungs Codes sehr kurz sein soll (weniger als eine Sekunde), kann die Initialisierung direkt in [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona)ausgeführt werden.

    Wenn die Initialisierungs Zeit voraussichtlich länger als eine Sekunde ist, sollte der Dienst eine der folgenden Initialisierungs Verfahren verwenden:

    -   Aufrufen der [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) -Funktion für den Berichts Dienst, der \_ ausgeführt wird, aber keine Steuerelemente akzeptieren, bis die Initialisierung abgeschlossen ist Der Dienst führt dies durch Aufrufen von **SetServiceStatus** , wobei **dwcurrentstate** auf Dienst wird \_ ausgeführt und **dwcontrolsaccepted** in der [**Dienst \_ Status**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) Struktur auf 0 festgelegt ist. Dadurch wird sichergestellt, dass der SCM keine Steuerungsanforderungen an den Dienst sendet, bevor er bereit ist, und den SCM zum Verwalten anderer Dienste freigibt. Dieser Ansatz für die Initialisierung wird für die Leistung empfohlen, insbesondere für Autostart-Dienste.
    -   Der Berichts \_ Dienst \_ steht aus, es werden keine Steuerelemente akzeptiert, und Sie können einen Wait-Hinweis angeben. Wenn der Initialisierungs Code des Diensts Tasks ausführt, die voraussichtlich länger als der anfängliche Wait-Hinweis Wert dauern, muss der Code die Funktion [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) regelmäßig aufrufen (möglicherweise mit einem überarbeiteten warte Hinweis), um anzugeben, dass der Fortschritt ausgeführt wird. Stellen Sie sicher, dass **SetServiceStatus** nur aufgerufen wird, wenn die Initialisierung fortgesetzt wird. Andernfalls kann der SCM warten, bis der Dienst \_ ausgeführt wird, wenn der Dienst ausgeführt wird, vorausgesetzt, der Dienst wird fortgesetzt, und der Start anderer Dienste wird blockiert. Wenn Sie nicht sicher sind, dass der Thread, der die Initialisierung ausführt, tatsächlich Fortschritte macht, sollten Sie **SetServiceStatus** nicht in einem separaten Thread aufrufen.

        Ein Dienst, der diesen Ansatz verwendet, kann auch einen Prüf Punkt Wert angeben und den Wert in regelmäßigen Abständen während einer langwierigen Initialisierung erhöhen. Das Programm, mit dem der Dienst gestartet wurde, kann [**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus) oder [**queryservicestatusex**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) aufrufen, um den letzten Prüf Punkt Wert aus dem SCM abzurufen und den Wert zu verwenden, um dem Benutzer den inkrementellen Fortschritt zu melden.

4.  Wenn die Initialisierung abgeschlossen ist, müssen Sie [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) aufrufen, um den Dienststatus auf Dienst Ausführung festzulegen, \_ und die Steuerelemente angeben, die der Dienst akzeptieren soll. Eine Liste der Steuerelemente finden Sie in der [**Dienst \_ Status**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) Struktur.
5.  Führen Sie die Dienst Tasks aus, oder geben Sie, falls keine ausstehenden Aufgaben vorhanden sind, die Steuerung an den Aufrufer zurück. Jede Änderung des Dienst Zustands erfordert einen Aufrufen von [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) , um neue Statusinformationen zu melden.
6.  Wenn ein Fehler auftritt, während der Dienst initialisiert wird oder ausgeführt wird, sollte der Dienst [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus) aufrufen, um den Dienststatus auf \_ Beenden ausstehend festzulegen, wenn die \_ Bereinigung langwierig ist. Nachdem die Bereinigung abgeschlossen ist, können Sie **SetServiceStatus** aufrufen, um den Dienststatus auf den Dienst festzulegen, der \_ vom letzten zu beendenden Thread beendet wurde. Stellen Sie sicher, dass Sie die Member " **dwservicespecificexitcode** " und " **dwWin32ExitCode** " der [**Dienst \_ Status**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) Struktur festlegen, um den Fehler zu identifizieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schreiben einer ServiceMain-Funktion](writing-a-servicemain-function.md)
</dt> </dl>

 

 
