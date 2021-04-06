---
title: Informationen zu iwmppluginenable
description: Informationen zu iwmppluginenable
ms.assetid: 7611a197-f404-4cfb-88b0-05348a41ac42
keywords:
- Windows Media Player-Plug-ins, Schnittstellen
- Plug-ins, Schnittstellen
- Plug-Ins für die digitale Signalverarbeitung, Schnittstellen
- DSP-Plug-ins, Schnittstellen
- Schnittstellen, DSP-Plug-ins
- Windows Media Player-Plug-ins, iwmppluginenable-Schnittstelle
- Plug-ins, iwmppluginenable-Schnittstelle
- Plug-Ins für die digitale Signalverarbeitung, iwmppluginenable-Schnittstelle
- DSP-Plug-ins, iwmppluginenable-Schnittstelle
- Iwmppluginenable-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7bf0f58be1d2623539cc5ac1329838246c8697
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947441"
---
# <a name="about-iwmppluginenable"></a>Informationen zu iwmppluginenable

Die **iwmppluginenable** -Schnittstelle ist für Windows Media Player DSP-Plug-Ins erforderlich. **Iwmppluginenable** enthält zwei Methoden, mit denen gespeichert wird, ob Windows Media Player das DSP-Plug-in aktiviert hat. Windows Media Player ruft **iwmppluginenable:: abtenable** auf, wenn eine Instanz des DSP-Plug-Ins erstellt wird. dabei wird der Wert **true** übergeben, wenn das Plug-in aktiviert wurde, andernfalls **false** .

DSP-Plug-ins bleiben möglicherweise auch dann geladen, wenn der Benutzer Sie deaktiviert. Wenn diese Option deaktiviert ist, muss ein Plug-in Daten aus dem Eingabepuffer in den Ausgabepuffer kopieren und damit nur die Formatierung der Formatierungs Verarbeitung durchführen.

Außerdem ruft Windows Media Player diese Methode auf, bevor Sie eine Instanz des DSP-Plug-ins freigibt. Dies ist hilfreich, damit Clients des Plug-ins überprüfen können, ob das Plug-in derzeit aktiviert ist. Beispielsweise kann ein Benutzeroberflächen-Plug-in die Darstellung der Steuerelemente ändern, um den Benutzer darüber zu benachrichtigen, dass das DSP-Plug-in nicht verbunden ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erforderliche Schnittstellen**](required-interfaces.md)
</dt> </dl>

 

 




