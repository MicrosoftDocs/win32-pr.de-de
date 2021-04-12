---
title: Gerätenamen
description: Gerätenamen
ms.assetid: 0ba06439-cc33-43e1-a094-09bcc5e2f6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e516f7f8eed338067dc373f8509f46598e198c71
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471765"
---
# <a name="device-names"></a>Gerätenamen

Für jeden Gerätetyp gibt es möglicherweise mehrere MCI-Treiber, die den Befehlssatz gemeinsam nutzen, aber unterschiedlichen Datenformaten arbeiten. Zum eindeutigen Identifizieren eines MCI-Treibers verwendet MCI *Gerätenamen*.

Gerätenamen werden entweder im \[ MCI- \] Abschnitt der SYSTEM.INI Datei oder im entsprechenden Teil der Registrierung identifiziert. Diese Informationen identifizieren alle MCI-Treiber für Windows. Die Einträge im \[ MCI- \] Abschnitt verwenden die folgende Form:

*Geräte \_ Namen*  =  *Treiber \_ Dateiname. Erweiterung*

Das folgende Beispiel zeigt einen typischen \[ MCI- \] Abschnitt aus SYSTEM.INI:


```C++
[mci]
cdaudio=mcicda.drv 
sequencer=mciseq.drv 
waveaudio=mciwave.drv 
avivideo=mciavi.drv
```



Wenn ein MCI-Treiber mit einem Gerätenamen installiert wird, der bereits in SYSTEM.INI oder der Registrierung vorhanden ist, fügt das System eine ganze Zahl an den Gerätenamen des neuen Treibers an und erstellt dabei einen eindeutigen Gerätenamen. Im vorherigen Beispiel würde ein zusätzlicher Treiber, der mit dem Gerätenamen "CDAudio" installiert wird, dem Gerätenamen "cdaudio1" zugewiesen werden.

 

 




