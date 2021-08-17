---
description: Nehmen wir für ein Beispiel an, dass die Anwendung die TAPI lineConfigDialog-Funktion aufruft, die zum Öffnen eines Dialogfelds entwickelt wurde, um die Konfiguration von Dienstanbieteroptionen im Zusammenhang mit dem angegebenen Liniengerät zu ermöglichen.
ms.assetid: a388d192-a327-4e67-968b-344d80c19fb1
title: Funktionen zum Generieren der Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e7aeda54d4c04a144b2786b56f32d13c51ab39c5274204485151caecc2db1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140613"
---
# <a name="functions-designed-to-generate-ui"></a>Funktionen zum Generieren der Benutzeroberfläche

Nehmen wir für ein Beispiel an, dass die Anwendung die TAPI [**lineConfigDialog-Funktion**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog) aufruft, die zum Öffnen eines Dialogfelds entwickelt wurde, um die Konfiguration von Dienstanbieteroptionen im Zusammenhang mit dem angegebenen Liniengerät zu ermöglichen. Als Reaktion auf diesen Aufruf fordert TAPISRV auf, [**den TSPI-AnbieterUIIdentify \_**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify) im Telefoniedienstanbieter aufrufen und den Namen der TSP-UI-DLL zu erhalten.

Im Kontext der Anwendung lädt TAPI die TSP-BENUTZEROBERFLÄCHEn-DLL und ruft die [**\_ LINECONFIGDialog-Funktion mit den**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog) parametern auf, die von der Anwendung bereitgestellt werden, und enthält einen Zeiger auf die TAPI-Funktion [*DllCallbackProc.*](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) Die TSP-UI-DLL zeigt das Konfigurationsdialogfeld an und ruft die *DllCallbackProc-Funktion* nach Bedarf auf, um vom Telefoniedienstanbieter die anzuzeigenden Informationen zu erhalten. Jedes Mal, wenn die *DllCallbackProc-Funktion* aufgerufen wird, fordert TAPISRV auf, die [**TSPI-AnbietergenericDialogData-Funktion \_**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata) des Telefoniedienstanbieters aufzurufen, den Parameterblock aus der UI-DLL zu übergeben und den Parameterblock an die UI-DLL zurückgibt. Die BENUTZEROBERFLÄCHEN-DLL übermittelt alle Konfigurationsänderungen an den Telefoniedienstanbieter, indem *dllCallbackProc aufruft.*

Wenn die Funktion abgeschlossen ist, gibt die BENUTZEROBERFLÄCHEN-DLL von (in diesem Fall) [**ZURÜCK: CODSPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog). TAPI ruft die [**FreeLibrary-Funktion**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary) auf, um die UI-DLL frei zu geben, und kehrt zur Anwendung zurück.

 

 
