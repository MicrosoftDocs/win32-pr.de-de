---
title: Die PlaySound-Funktion
description: Die PlaySound-Funktion
ms.assetid: ce405a13-c4ab-4c9a-bcfe-8d4427b3d2d8
keywords:
- Multimedia-Audio, PlaySound-Funktion
- Audio, PlaySound-Funktion
- Wellenform-Audio, PlaySound-Funktion
- PlaySound-Funktion, Informationen zu
- SndPlaySound-Funktion
- PlaySound-Funktion im Vergleich zur SndPlaySound-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5723b1937c974e6c622c1f2010e8d2129e787cdd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104208866"
---
# <a name="the-playsound-function"></a>Die PlaySound-Funktion

Sie können die [**PlaySound**](/previous-versions//dd743680(v=vs.85)) -Funktion verwenden, um Wellenform-Audio wiederzugeben, wenn der Sound in den verfügbaren Arbeitsspeicher passt. (Die Funktion [**sndPlaySound**](/previous-versions//dd798676(v=vs.85)) bietet eine Teilmenge der Funktionen von PlaySound. Verwenden Sie " **PlaySound**", nicht " **sndPlaySound**", um die Portabilität Ihrer Win32-basierten Anwendung zu maximieren.)

Mit der Funktion " **PlaySound** " können Sie einen Sound auf eine von drei Arten angeben:

-   Als Systemwarnung mit dem Alias, der in der WIN.INI-Datei oder der Registrierung gespeichert ist
-   Als Dateiname
-   Als Ressourcen Bezeichner

Mit der Funktion " [**PlaySound**](/previous-versions//dd743680(v=vs.85)) " können Sie einen Sound in einer kontinuierlichen Schleife wiedergeben. Dies wird nur beendet, wenn Sie " **PlaySound** " erneut aufrufen, indem Sie entweder **null** oder den Sound Bezeichner eines anderen Sounds für den *pszsound* -Parameter angeben.

Mit **PlaySound** können Sie den Sound synchron oder asynchron abspielen und das Verhalten der Funktion auf andere Weise steuern, wenn Sie Systemressourcen freigeben muss.

Weitere Informationen zur Verwendung von PlaySound finden Sie in den folgenden Themen:

-   [Verwenden von PlaySound zum Abspielen von Waveform-Audio Dateien](using-playsound-to-play-waveform-audio-files.md)
-   [Verwenden von PlaySound für Schleifen Klänge](using-playsound-to-loop-sounds.md)
-   [Verwenden von PlaySound zum Abspielen von System Sounds](using-playsound-to-play-system-sounds.md)

Weitere Beispiele für die Verwendung von **PlaySound** in ihren Win32-basierten Anwendungen finden Sie unter [spielen von Wave-Ressourcen](playing-wave-resources.md).

 

 