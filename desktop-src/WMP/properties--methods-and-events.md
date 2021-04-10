---
title: Eigenschaften, Methoden und Ereignisse
description: Eigenschaften, Methoden und Ereignisse
ms.assetid: 9426d13b-42db-4a20-81f2-7a849a6e1f33
keywords:
- Windows Media Player, Eigenschaften für das Objektmodell
- Windows Media Player, Methoden für das Objektmodell
- Windows Media Player, Ereignisse für das Objektmodell
- Windows Media Player-Objektmodell, Eigenschaften
- Windows Media Player-Objektmodell, Methoden
- Windows Media Player-Objektmodell, Ereignisse
- Objektmodell, Eigenschaften
- Objektmodell, Methoden
- Objektmodell, Ereignisse
- Windows Media Player ActiveX-Steuerelement, Eigenschaften für das Objektmodell
- ActiveX-Steuerelement, Eigenschaften für das Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Eigenschaften für das Objektmodell
- Windows Media Player Mobile, Eigenschaften für das Objektmodell
- Windows Media Player ActiveX-Steuerelement, Methoden für das Objektmodell
- ActiveX-Steuerelement, Methoden für das Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Methoden für das Objektmodell
- Windows Media Player Mobile, Methoden für das Objektmodell
- Windows Media Player ActiveX-Steuerelement, Ereignisse für das Objektmodell
- ActiveX-Steuerelement, Ereignisse für das Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement, Ereignisse für das Objektmodell
- Windows Media Player Mobile, Ereignisse für das Objektmodell
- Eigenschaften, Windows Media Player-Objektmodell
- Methoden, Windows Media Player-Objektmodell
- Ereignisse, Windows Media Player-Objektmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e06a860d04bfc1a5ccd5b33c0604a0ef818a0127
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100730"
---
# <a name="properties-methods-and-events"></a>Eigenschaften, Methoden und Ereignisse

Jedes-Objekt verfügt über Methoden und Eigenschaften, über die Sie das Windows Media Player-Steuerelement programmieren können. Eine Methode ist eine Aktion, die das Objekt ausführen kann. Eine Eigenschaft ist ein Datenwert, den Sie lesen oder ändern können. Die **Play** -Methode startet z. b. die Wiedergabe des Inhalts, und die Framerate-Eigenschaft gibt die aktuelle **Framerate** der wiedergegebenen Inhalte an.

Außerdem löst das **Player** -Objekt Ereignisse aus, die Ihnen die Möglichkeit bieten, Aktionen zu bestimmten Zeiten auszuführen. Sie schreiben Code in einem Ereignishandler, der ausgeführt wird, wenn Windows Media Player das entsprechende Ereignis auslöst. Sie können z. b. Code in einem **PlayStateChange** -Ereignishandler schreiben, der bestimmt, ob die Änderung des Zustands lautet, dass das Medium beendet wurde. wenn dies der Fall ist, wird ein Dialogfeld mit der Frage angezeigt, ob die Medien wiedergegeben werden sollen.

> [!Note]  
> Alle Methoden im Windows Media Player-Objektmodell sind asynchron. Wenn Sie zwei Methoden in derselben Prozedur aufrufen, kann die zweite Methode nicht darauf basieren, dass die erste Methode ihre Aktion abgeschlossen hat.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Player-Objektmodell**](about-the-player-object-model.md)
</dt> </dl>

 

 




