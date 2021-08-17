---
description: Nachdem ein Gerätetreiber eine gesamte Journaldatei in unformatierte Gerätebefehle konvertiert hat, wird die Datei mit den konvertierten Befehlen an den Spooler übergeben.
ms.assetid: 149e44d0-052a-48ba-8f65-59eab193c785
title: Portmonitore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8334da48fb147a41924be2cf090f55d7955cb1d7913c43b302a312fd4447602f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470930"
---
# <a name="port-monitors"></a>Portmonitore

Nachdem ein Gerätetreiber eine gesamte Journaldatei in unformatierte Gerätebefehle konvertiert hat, wird die Datei mit den konvertierten Befehlen an den Spooler übergeben. Der Spooler sendet diese Befehle auf niedriger Ebene an einen Monitor. Ein Portmonitor ist ein .dll, der die unformatierten Gerätebefehle über das Netzwerk, über einen parallelen Port oder über einen seriellen Anschluss an das Druckergerät übergibt. Benutzerdefinierte Portmonitore können installiert werden, um die Übergabe von Gerätedaten über andere Kommunikationsports zu unterstützen.

Verwenden Sie die folgenden Funktionen, um mit Portmonitoren zu arbeiten.



| Funktion                               | BESCHREIBUNG                                                                         |
|----------------------------------------|-------------------------------------------------------------------------------------|
| [**AddMonitor**](addmonitor.md)       | Installiert einen lokalen Portmonitor und verknüpft die Konfigurations-, Daten- und Überwachungsdateien. |
| [**DeleteMonitor**](deletemonitor.md) | Entfernt einen Portmonitor, der von der [**AddMonitor-Funktion**](addmonitor.md) hinzugefügt wurde.      |
| [**EnumMonitors**](enummonitors.md)   | Listet die Portmonitore auf, die auf einem angegebenen Server installiert sind.                       |



 

 

 



