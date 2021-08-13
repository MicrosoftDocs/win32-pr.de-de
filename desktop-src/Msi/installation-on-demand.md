---
description: Bei herkömmlicher Installationstechnologie ist es erforderlich, eine Anwendung zu beenden und das Setup erneut auszuführen, um eine Installationsaufgabe auszuführen.
ms.assetid: 94c3d5a8-a560-4a1d-b40e-7ebc92d659f3
title: Installation bei Bedarf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd20f83465fa110c4f749c6f11ba5ece1c6797a521174a8caebb9d152740aaba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633869"
---
# <a name="installation-on-demand"></a>Installation bei Bedarf

Bei herkömmlicher Installationstechnologie ist es erforderlich, eine Anwendung zu beenden und das Setup erneut auszuführen, um eine Installationsaufgabe auszuführen. Dies ist häufig der Fall, wenn ein Benutzer ein Feature oder Produkt nicht während der ersten Ausführung des Setups ausgewählt haben wollte. Dies hat den Prozess der Produktkonfiguration oft ineffizient gemacht, da der Benutzer die erforderliche Funktionalität vorhersehen musste, bevor er das Produkt verwendet hat.

Bei Bedarf ist es möglich, Benutzern und Anwendungen Funktionen zur Verfügung zu stellen, wenn die Dateien selbst fehlen. Dieses Konzept wird als Ankündigung bezeichnet. Der Windows Installer verfügt über die Funktion zur Werbung und ermöglicht die Bedarfsbasierte Installation von Anwendungsfeatures oder ganzen Produkten. Wenn ein Benutzer oder eine Anwendung ein angekündigtes Feature oder Produkt aktiviert, wird die Installation der erforderlichen Komponenten fortgesetzt. Dadurch wird der Konfigurationsprozess verkürzt, da auf zusätzliche Funktionen zugegriffen werden kann, ohne ein anderes Setupverfahren beenden und erneut ausführen zu müssen.

Wenn ein Produkt das Installationsprogramm verwendet, kann ein Benutzer beim Setup auswählen, welche Features oder Anwendungen installiert und welche angekündigt werden. Wenn der Benutzer dann während der Ausführung einer Anwendung ein angekündigtes Feature an fordert, das noch nicht installiert wurde, ruft die Anwendung das Installationsprogramm auf, um eine Just-In-Time-Installation der erforderlichen Dateien auf Featureebene in Kraft zu stellen. Wenn der Benutzer ein angekündigtes Produkt aktiviert, das noch nicht installiert wurde, ruft das Betriebssystem das Installationsprogramm auf, um eine Just-In-Time-Installation auf Produktebene zu starten.

[Ankündigung](advertisement.md) und Installation bei Bedarf können auch die Systemverwaltung vereinfachen, indem Administratoren Anwendungen für verschiedene Benutzergruppen als erforderlich oder optional festlegen können. Es gibt zwei Arten von Werbung, die als "Zuweisen" und "Veröffentlichen" bezeichnet werden. Wenn ein Administrator einer Gruppe eine Anwendung zu weist, können diese Benutzer die Anwendung bei Bedarf installieren. Wenn der Administrator die Anwendung jedoch in der Gruppe veröffentlicht, werden diesen Benutzern keine Einstiegspunkte angezeigt, und installation-on-demand wird nur aktiviert, wenn eine andere Anwendung die veröffentlichte Anwendung aktiviert.

 

 



