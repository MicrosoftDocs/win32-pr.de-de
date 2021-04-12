---
description: Bei der herkömmlichen Installations Technologie ist es erforderlich, eine Anwendung zu beenden und Setup erneut auszuführen, um eine Installationsaufgabe auszuführen.
ms.assetid: 94c3d5a8-a560-4a1d-b40e-7ebc92d659f3
title: Installation bei Bedarf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f25c83135a0497d09aa0a7800a1272105d0db1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216366"
---
# <a name="installation-on-demand"></a>Installation bei Bedarf

Bei der herkömmlichen Installations Technologie ist es erforderlich, eine Anwendung zu beenden und Setup erneut auszuführen, um eine Installationsaufgabe auszuführen. Dies ist häufig der Fall, wenn ein Benutzer eine Funktion oder ein Produkt gewünscht hätte, die während der ersten Installation nicht ausgewählt wurden. Dadurch wurde der Prozess der Produktkonfiguration häufig ineffizient, da der Benutzer die erforderliche Funktionalität vor der Verwendung des Produkts vorhersehen musste.

Bei der bedarfsgesteuerten Installation ist es möglich, Benutzern und Anwendungen Funktionalität zur Verfügung zu stellen, wenn die Dateien nicht selbst vorhanden sind. Dieses Konzept wird als Ankündigung bezeichnet. Der Windows Installer verfügt über die Möglichkeit, Funktionen zu bewerben und die Installation auf Anfrage von Anwendungs Features oder gesamten Produkten zu ermöglichen. Wenn ein Benutzer oder eine Anwendung eine angekündigte Funktion oder ein angekündigtes Produkt aktiviert, fährt das Installationsprogramm mit der Installation der erforderlichen Komponenten fort. Dadurch wird der Konfigurations Vorgang verkürzt, da auf zusätzliche Funktionen zugegriffen werden kann, ohne dass ein weiteres Setup Verfahren beendet und erneut ausgeführt werden muss.

Wenn ein Produkt das Installationsprogramm verwendet, kann ein Benutzer zum Zeitpunkt des Setups auswählen, welche Features oder Anwendungen installiert und welche angekündigt werden sollen. Wenn der Benutzer während der Ausführung einer Anwendung ein angekündigtes Feature anfordert, das noch nicht installiert wurde, ruft die Anwendung den Installer auf, um eine Just-in-Time-Funktionsebene der erforderlichen Dateien zu implementieren. Wenn der Benutzer ein angekündigtes Produkt aktiviert, das noch nicht installiert wurde, ruft das Betriebssystem den Installer auf, um eine Just-in-Time-Installation auf Produktebene durchzusetzen.

Durch [Ankündigung und Installation](advertisement.md) bei Bedarf kann die Systemverwaltung auch vereinfacht werden, indem Administratoren für verschiedene Gruppen von Benutzern Anwendungen als erforderlich oder optional festlegen können. Es gibt zwei Arten von Ankündigungen, die als "zuweisen" und "veröffentlichen" bezeichnet werden. Wenn ein Administrator einer Gruppe eine Anwendung zuweist, können diese Benutzer die Anwendung bei Bedarf installieren. Wenn der Administrator die Anwendung jedoch in der Gruppe veröffentlicht, werden diesen Benutzern keine Einstiegspunkte angezeigt, und die Installation bei Bedarf wird nur aktiviert, wenn die veröffentlichte Anwendung von einer anderen Anwendung aktiviert wird.

 

 



