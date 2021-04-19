---
description: Nachdem ein Gerätetreiber eine gesamte Journal Datei in unformatierte Geräte Befehle konvertiert hat, wird die Datei der konvertierten Befehle an den Spooler zurückgegeben.
ms.assetid: 149e44d0-052a-48ba-8f65-59eab193c785
title: Port Monitore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4b00e4171b3fd6e366a66deae8f5e70578ca92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364050"
---
# <a name="port-monitors"></a>Port Monitore

Nachdem ein Gerätetreiber eine gesamte Journal Datei in unformatierte Geräte Befehle konvertiert hat, wird die Datei der konvertierten Befehle an den Spooler zurückgegeben. Der Spooler sendet diese Befehle auf niedriger Ebene an einen Monitor. Bei einem Port Monitor handelt es sich um eine DLL, die die unformatierten Geräte Befehle über das Netzwerk, über einen parallelen Port oder über einen seriellen Anschluss an das Druckergerät übergibt. Benutzerdefinierte Port Monitore können installiert werden, um die Übergabe von Gerätedaten über andere Kommunikationsports zu unterstützen.

Verwenden Sie die folgenden Funktionen, um mit Port Monitoren zu arbeiten.



| Funktion                               | BESCHREIBUNG                                                                         |
|----------------------------------------|-------------------------------------------------------------------------------------|
| [**Addmonitor**](addmonitor.md)       | Installiert einen lokalen Port Monitor und verknüpft die Konfigurations-, Daten-und Überwachungs Dateien. |
| [**Deletemonitor**](deletemonitor.md) | Entfernt einen von der [**addmonitor**](addmonitor.md) -Funktion hinzugefügten Port Monitor.      |
| [**Enumüberwachungen**](enummonitors.md)   | Listet die auf einem angegebenen Server installierten Port Monitore auf.                       |



 

 

 



