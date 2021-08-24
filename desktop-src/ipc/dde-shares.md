---
description: DDE-Freigaben sind eine Computerressource.
ms.assetid: 98d24300-52cc-4f0d-b74f-c58b823ac5f3
title: DDE-Freigaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5e3416235f78e48c68b7d2e35c7ac042f8ff5d6eac79cc2471efa5ea12d82b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602120"
---
# <a name="dde-shares"></a>DDE-Freigaben

\[Netzwerk-DDE wird nicht mehr unterstützt. Nddeapi.dll ist auf Windows Vista vorhanden, aber alle Funktionsaufrufe geben NDDE \_ NOT \_ IMPLEMENTED zurück.\]

DDE-Freigaben sind eine Computerressource. Sie ähneln Dateifreigaben, da sie zum Steuern des Zugriffs auf eine Ressource verwendet werden. Bei Dateifreigaben ist die Ressource eine Datei. Bei DDE-Freigaben werden daten dynamisch ausgetauscht. Der Typ der ausgetauschten Daten wird von der Serveranwendung bestimmt, die die Daten liefert, und von der Clientanwendung, die die Daten anfordert.

Der Server ruft die [**NDdeShareAdd-Funktion**](nddeshareadd.md) auf, um die DDE-Freigabe zu erstellen, die im DDE-Freigabedatenbank-Manager (DSDM) gespeichert ist.

Der Client startet die DDE-Konversation, indem er eine Verbindung mit der DDE-Freigabe herstellt. Der Client muss die [**DdeInitialize-Funktion**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) aufrufen, um DDEML zu initialisieren, und die [**DdeConnect-Funktion**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) aufrufen, um eine Verbindung mit der DDE-Freigabe herzustellen. Im **DdeConnect-Aufruf** gibt der Client den Dienstnamen wie folgt an:

\\\\*ComputerName* \\ NDDE$

Wobei *ComputerName* der Name des Computers ist, auf dem die Serveranwendung ausgeführt wird. NDDE$ gibt an, dass das für [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) bereitgestellte Thema der DDE-Freigabename auf dem Remotecomputer mit dem Namen *ComputerName* ist.

Es gibt drei Arten von DDE-Freigaben: alter Stil, neuer Stil und statisch. Es ist üblich, nur den statischen Typ zu unterstützen. Die Namen statischer Freigaben verwenden die folgende Konvention: *ShareName*$.

 

 
