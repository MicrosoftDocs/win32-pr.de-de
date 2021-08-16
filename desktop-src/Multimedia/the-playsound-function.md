---
title: Die PlaySound-Funktion
description: Die PlaySound-Funktion
ms.assetid: ce405a13-c4ab-4c9a-bcfe-8d4427b3d2d8
keywords:
- Multimediaaudio, PlaySound-Funktion
- audio,PlaySound-Funktion
- Waveform-Audio, PlaySound-Funktion
- PlaySound-Funktion,About
- sndPlaySound-Funktion
- PlaySound-Funktion im Vergleich zur sndPlaySound-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1921ec4ef91f6266b48ee80d7f42be4540124c0b5c98dc18438ce0d16c398c2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370850"
---
# <a name="the-playsound-function"></a>Die PlaySound-Funktion

Sie können die [**PlaySound-Funktion**](/previous-versions//dd743680(v=vs.85)) verwenden, um Wellenformaudio wieder zu geben, wenn der Sound in den verfügbaren Arbeitsspeicher passt. (Die [**sndPlaySound-Funktion**](/previous-versions//dd798676(v=vs.85)) bietet eine Teilmenge der Funktionen von PlaySound. Um die Portabilität Ihrer Win32-basierten Anwendung zu maximieren, verwenden Sie **PlaySound,** nicht **sndPlaySound**.)

Mit **der PlaySound-Funktion** können Sie einen Sound auf eine von drei Arten angeben:

-   Als Systemwarnung mithilfe des alias, der in der WIN.INI oder registrierung gespeichert ist
-   Als Dateiname
-   Als Ressourcenbezeichner

Mit [**der PlaySound-Funktion**](/previous-versions//dd743680(v=vs.85)) können Sie einen Sound in einer kontinuierlichen Schleife wiedergibt, der nur endet, wenn **Sie PlaySound** erneut aufrufen und entweder **NULL** oder den Soundbezeichner eines anderen Sounds für den *pszSound-Parameter* angeben.

Sie können **PlaySound verwenden,** um den Sound synchron oder asynchron wieder zu spielen und das Verhalten der Funktion auf andere Weise zu steuern, wenn systemressourcen gemeinsam verwendet werden müssen.

Weitere Informationen zur Verwendung von PlaySound finden Sie in den folgenden Themen:

-   [Verwenden von PlaySound zum Wiederspielen Waveform-Audio Dateien](using-playsound-to-play-waveform-audio-files.md)
-   [Verwenden von PlaySound zum Schleifen von Sounds](using-playsound-to-loop-sounds.md)
-   [Verwenden von PlaySound zum Wiederspielen von Systemsounds](using-playsound-to-play-system-sounds.md)

Weitere Beispiele für die Verwendung von **PlaySound** in Win32-basierten Anwendungen finden Sie unter [Wiedergabe von WAVE-Ressourcen.](playing-wave-resources.md)

 

 