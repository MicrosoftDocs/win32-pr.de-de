---
title: Installier bares Laufwerk Module-Definition Datei
description: Installier bares Laufwerk Module-Definition Datei
ms.assetid: d8d8d32e-18ac-47a5-a923-48b94b75e11d
keywords:
- installierbare Treiber, Modul Definitions Dateien
- installierbare Treiber, DEF-Dateien
- ninstallable Drivers, driverproc-Funktion
- Driverproc-Funktion
- Modul Definitions Dateien
- DEF-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 700931c91bfb3c17a36a1e3a1bbc4833097b4b38
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038879"
---
# <a name="installable-drive-module-definition-file"></a>Installier bares Laufwerk Module-Definition Datei

Die Modul Definition (. DEF) die Datei eines installierbaren Treibers benennt den Treiber, exportiert die [driverproc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) -Funktion und definiert eine Treiber Beschreibung. Das folgende Beispiel zeigt eine typische Modul Definitionsdatei für einen installierbaren Treiber:


```C++
LIBRARY OSCI 
DESCRIPTION 'FREQ,AMPL:Oscilloscope frequency and amplitude drivers.'
EXPORTS
    DriverProc
 
```



Einige Installationsanwendungen können den Treiber öffnen und die Beschreibungs Zeile abrufen, die bei der Installation des Treibers verwendet werden soll. Um mit diesen Installationsanwendungen kompatibel zu bleiben, sollte die Beschreibungs Zeile folgendes Format aufweisen:

**Beschreibungs**  *Alias* \[ ,*Alias* \] ... **:* * * Text*

Der *Alias* gibt einen eindeutigen Namen für den Treiber an, der von Anwendungen zum Öffnen des Treibers verwendet werden kann. Der Alias fungiert auch als Wertname, der dem Treiber in der Registrierung zugeordnet ist. Mehrere Aliase werden durch Kommas getrennt. Der *Text* beschreibt den Zweck des Treibers.

 

 