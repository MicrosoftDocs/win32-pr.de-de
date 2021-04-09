---
title: Verwenden von PlaySound zum Abspielen von System Sounds
description: Verwenden von PlaySound zum Abspielen von System Sounds
ms.assetid: b645c488-8b76-4886-8909-75f0342263db
keywords:
- Wellenform-Audio, PlaySound-Funktion
- Wellenform-Audio, Abspielen von Systemsounds
- Wellenform-Audio, Sound Ereignisse
- PlaySound-Funktion, Abspielen von Systemsounds
- PlaySound-Funktion, Sound Ereignisse
- Wiedergabe von Waveform-audiosystemsounds
- Sound Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1940ee9f207213c4337c9b6bb0a0d58b0f471000
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858250"
---
# <a name="using-playsound-to-play-system-sounds"></a>Verwenden von PlaySound zum Abspielen von System Sounds

Die [**PlaySound**](/previous-versions//dd743680(v=vs.85)) -Funktion gibt auch Sounds wieder, auf die in der Registrierung durch einen keyName verwiesen wird. Benutzer können Ihren eigenen Soundsystem Warnungen und-Warnungen oder Benutzeraktionen zuweisen, z. b. durch Klicken auf die Maustaste. Sounds, die Systemwarnungen und Warnungen zugeordnet sind, werden als *Sound Ereignisse* bezeichnet.

Um ein Sound Ereignis wiederzugeben, müssen Sie **PlaySound** mit dem *pszsound* -Parameter aufrufen, der auf eine Zeichenfolge verweist, die den Namen des Registrierungs Eintrags enthält, der den Sound identifiziert. Verwenden Sie die folgende Anweisung, um beispielsweise den dem "moukliclick"-Eintrag zugeordneten Sound wiederzugeben und vor der Rückgabe auf den Abschluss des Sounds zu warten:


```C++
PlaySound("MouseClick", NULL, SND_SYNC); 
```



Wenn der angegebene Registrierungs Eintrag oder die anzuzeigende Waveform-Audiodatei nicht vorhanden ist, oder wenn die Datei nicht in den verfügbaren Arbeitsspeicher passt, gibt **PlaySound** den Standardsystem Sound wieder.

Die vom System vordefinierten Audioereignisse können von der Plattform abweichen. Die folgende Liste enthält die Audioereignisse, die für alle Implementierungen der Win32-API definiert sind:

-   Systemasterisk
-   SystemExclamation
-   System Exit
-   Systemhand
-   Systemfrage
-   Systemstart

Wenn eine Anwendung eigene Audioereignisse registriert, kann der Benutzer das Audioereignis mithilfe der standardmäßigen System Steuerungs Schnittstelle konfigurieren. Die Anwendung sollte das Sound Ereignis mithilfe der Standard Registrierungsfunktionen registrieren. Weitere Informationen finden Sie unter [Registry](../sysinfo/registry.md). Die Einträge gehören zur gleichen Position in der Registrierungs Hierarchie wie die restlichen Sound Ereignisse. Diese Position variiert bei der Win32-Implementierung. Der entsprechende Datenwert variiert auch mit der-Implementierung.

Die Funktion " [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) " durchsucht die Registrierung stets nach einem keyName, der mit *lpszsound* übereinstimmt, bevor versucht wird, eine Datei mit diesem Namen zu laden. Die [**PlaySound**](/previous-versions//dd743680(v=vs.85)) -Funktion akzeptiert Flags, die den Speicherort des Sounds angeben.

 

 