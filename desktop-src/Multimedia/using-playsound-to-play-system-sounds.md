---
title: Verwenden von PlaySound zum Wiedergeben von Systemsounds
description: Verwenden von PlaySound zum Wiedergeben von Systemsounds
ms.assetid: b645c488-8b76-4886-8909-75f0342263db
keywords:
- Waveform-Audio, PlaySound-Funktion
- Waveformaudio, Wiedergeben von Systemsounds
- Waveformaudio, Soundereignisse
- PlaySound-Funktion,Wiedergeben von Systemsounds
- PlaySound-Funktion, Soundereignisse
- Wiedergeben von Waveform-Audio-Systemsounds
- Soundereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf9978e9e33c049db82a033b2379ac9f52b5e2959fd9d8425deac180ba7a81e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804570"
---
# <a name="using-playsound-to-play-system-sounds"></a>Verwenden von PlaySound zum Wiedergeben von Systemsounds

Die [**PlaySound-Funktion**](/previous-versions//dd743680(v=vs.85)) gibt auch Sounds wieder, auf die durch einen Schlüsselnamen in der Registrierung verwiesen wird. Benutzer können Systemwarnungen und Warnungen oder Benutzeraktionen, z. B. einem Mausklick, eigene Sounds zuweisen. Sounds, die Systemwarnungen und Warnungen zugeordnet sind, werden als *Soundereignisse* bezeichnet.

Um ein Soundereignis wiederzuspielen, rufen **Sie PlaySound** mit dem *Parameter pszSound* auf, der auf eine Zeichenfolge verweist, die den Namen des Registrierungseintrags enthält, der den Sound identifiziert. Verwenden Sie beispielsweise die folgende Anweisung, um den Sound wiederzugeben, der dem Eintrag "MouseClick" zugeordnet ist, und um auf den Abschluss des Sounds zu warten, bevor er zurückgegeben wird:


```C++
PlaySound("MouseClick", NULL, SND_SYNC); 
```



Wenn der angegebene Registrierungseintrag oder die von ihm identifizierte Waveform-Audiodatei nicht vorhanden ist oder die Datei nicht in den verfügbaren Arbeitsspeicher passt, gibt **PlaySound** den Standardsystemsound wieder.

Die vom System vordefinierten Soundereignisse können je nach Plattform variieren. Die folgende Liste enthält die Soundereignisse, die für alle Implementierungen der Win32-API definiert sind:

-   SystemAsterisk
-   SystemExclamation
-   SystemExit
-   SystemHand
-   SystemQuestion
-   SystemStart

Wenn eine Anwendung eigene Soundereignisse registriert, kann der Benutzer das Soundereignis mithilfe der Systemsteuerung Standardschnittstelle konfigurieren. Die Anwendung sollte das Soundereignis mithilfe der Standardregistrierungsfunktionen registrieren. Weitere Informationen finden Sie unter [Registrierung.](../sysinfo/registry.md) Die Einträge gehören an derselben Position in der Registrierungshierarchie wie die restlichen Soundereignisse. Diese Position variiert je nach Win32-Implementierung. Der entsprechende Datenwert variiert auch je nach Implementierung.

Die [**sndPlaySound-Funktion**](/previous-versions//dd798676(v=vs.85)) durchsucht die Registrierung immer nach einem Schlüsselnamen, der *lpszSound entspricht,* bevor versucht wird, eine Datei mit diesem Namen zu laden. Die [**PlaySound-Funktion**](/previous-versions//dd743680(v=vs.85)) akzeptiert Flags, die die Position des Sounds angeben.

 

 