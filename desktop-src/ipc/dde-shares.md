---
description: DDE-Freigaben sind eine Computer Ressource.
ms.assetid: 98d24300-52cc-4f0d-b74f-c58b823ac5f3
title: DDE-Freigaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 012c219897187c9e68b5b9e662b93678b77974c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865591"
---
# <a name="dde-shares"></a>DDE-Freigaben

\[Network DDE wird nicht mehr unterstützt. Nddeapi.dll ist unter Windows Vista vorhanden, aber alle Funktionsaufrufe geben "ndde" \_ nicht \_ implementiert zurück.\]

DDE-Freigaben sind eine Computer Ressource. Sie ähneln Dateifreigaben, da Sie verwendet werden, um den Zugriff auf eine Ressource zu steuern. Bei Dateifreigaben ist die Ressource eine Datei. Bei DDE-Freigaben werden die Daten dynamisch ausgetauscht. Der Typ der ausgetauschten Daten wird von der Serveranwendung bestimmt, die die Daten bereitstellt, und der Client Anwendung, die die Daten anfordert.

Der Server Ruft die [**nddeshareadd**](nddeshareadd.md) -Funktion auf, um die DDE-Freigabe zu erstellen, die im DDE Share Database Manager (DSDM) gespeichert ist.

Der Client startet die DDE-Konversation durch Herstellen einer Verbindung mit der DDE-Freigabe. Der Client muss die [**DDEInitialize**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) -Funktion zum Initialisieren von Ddeml und zum Abrufen der [**ddeconnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) -Funktion zum Herstellen einer Verbindung mit der DDE-Freigabe aufruft. Im **ddeconnect** -Befehl gibt der Client den Dienstnamen wie folgt an:

\\\\*Computername* \\ Ndde $

Dabei steht *Computername* für den Namen des Computers, auf dem die Serveranwendung ausgeführt wird. Der ndde $-Wert gibt an, dass das für [**ddeconnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) bereitgestellte Thema der DDE-Freigabe Name auf dem Remote Computer namens *Computername* ist.

Es gibt drei Typen von DDE-Freigaben: Alter Stil, neue Formatvorlage und statisch. Es ist typisch, nur den statischen Typ zu unterstützen. Die Namen von statischen Freigaben verwenden die folgende Konvention: *ShareName*$.

 

 
