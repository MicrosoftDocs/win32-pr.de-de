---
title: Gerätenamen
description: Gerätenamen
ms.assetid: 0ba06439-cc33-43e1-a094-09bcc5e2f6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85183a1b23817352ba9e45e8dbb2aaa70493430cd092f357e1eaa8e9bf179d65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497270"
---
# <a name="device-names"></a>Gerätenamen

Für jeden Gerätetyp gibt es möglicherweise mehrere MCI-Treiber, die den Befehlssatz gemeinsam nutzen, aber mit unterschiedlichen Datenformaten arbeiten. Um einen MCI-Treiber eindeutig zu identifizieren, verwendet MCI *Gerätenamen.*

Gerätenamen werden entweder im \[ \] mci-Abschnitt der SYSTEM.INI-Datei oder im entsprechenden Teil der Registrierung identifiziert. Diese Informationen identifizieren alle MCI-Treiber, die Windows werden sollen. Die Einträge im \[ \] mci-Abschnitt verwenden das folgende Format:

*Device \_ Name*  =  *Driver \_ filename.extension*

Das folgende Beispiel zeigt einen typischen \[ mci-Abschnitt \] aus SYSTEM.INI:


```C++
[mci]
cdaudio=mcicda.drv 
sequencer=mciseq.drv 
waveaudio=mciwave.drv 
avivideo=mciavi.drv
```



Wenn ein MCI-Treiber mit einem Gerätenamen installiert wird, der bereits in SYSTEM.INI oder der Registrierung vorhanden ist, fügt das System eine ganze Zahl an den Gerätenamen des neuen Treibers an und erstellt einen eindeutigen Gerätenamen. Im vorherigen Beispiel wurde einem zusätzlichen Treiber, der mit dem Gerätenamen "cdaudio" installiert wurde, der Gerätename "cdaudio1" zugewiesen.

 

 




