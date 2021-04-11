---
description: Angenommen, das Beispiel zeigt, dass die Anwendung die TAPI lineconfigdialog-Funktion aufruft, die zum Öffnen eines Dialog Felds entworfen wurde, um die Konfiguration von Dienstanbieter Optionen zu ermöglichen, die mit dem angegebenen Zeilen Gerät verknüpft sind.
ms.assetid: a388d192-a327-4e67-968b-344d80c19fb1
title: Funktionen zum Generieren der Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa360effd2a1504d2325be2131c430664f1e7a5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958941"
---
# <a name="functions-designed-to-generate-ui"></a>Funktionen zum Generieren der Benutzeroberfläche

Angenommen, das Beispiel zeigt, dass die Anwendung die TAPI [**lineconfigdialog**](/windows/win32/api/tapi/nf-tapi-lineconfigdialog) -Funktion aufruft, die zum Öffnen eines Dialog Felds entworfen wurde, um die Konfiguration von Dienstanbieter Optionen zu ermöglichen, die mit dem angegebenen Zeilen Gerät verknüpft sind. Als Reaktion auf diesen-Befehl fordert TAPI tapisrv an, [**TSPI \_ provideruiidentifiim**](/windows/win32/api/tspi/nf-tspi-tspi_provideruiidentify) Telefoniedienstanbieter aufzurufen, wobei der Name der TSP-UI-dll abgerufen wird.

Im Kontext der Anwendung lädt TAPI die TSP-UI-dll und ruft die Funktion " [**tuispi \_ lineconfigdialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog) " mit den von der Anwendung bereitgestellten Parametern und dem Einschließen eines Zeigers auf die TAPI- [*dllcallbackproc*](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) -Funktion auf. Die TSP-Benutzeroberflächen-DLL zeigt das Dialogfeld Konfiguration an und ruft die *dllcallbackproc* -Funktion nach Bedarf auf, um die anzuzeigenden Informationen vom Telefoniedienstanbieter abzurufen. Jedes Mal, wenn die *dllcallbackproc* -Funktion aufgerufen wird, fordert TAPI tapisrv an, die [**TSPI \_ providergenericdialogdata**](/windows/win32/api/tspi/nf-tspi-tspi_providergenericdialogdata) -Funktion des Telefoniedienstanbieters aufzurufen, den Parameter Block von der Benutzeroberflächen-DLL zu übergeben und den Parameter Block an die UI-DLL zurückzugeben. Die UI-DLL überträgt alle Konfigurationsänderungen an den Telefoniedienstanbieter durch Aufrufen von *dllcallbackproc*.

Wenn die Funktion fertig ist, gibt die Benutzeroberflächen-DLL von (in diesem Fall) " [**tuispi \_ lineconfigdialog**](/windows/win32/api/tspi/nf-tspi-tuispi_lineconfigdialog)" zurück. TAPI Ruft die [**FreeLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-freelibrary) -Funktion auf, um die UI-DLL freizugeben, und kehrt zur Anwendung zurück.

 

 
