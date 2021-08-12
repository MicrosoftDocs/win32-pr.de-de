---
title: Eigenschaften, Methoden und Ereignisse
description: Eigenschaften, Methoden und Ereignisse
ms.assetid: 9426d13b-42db-4a20-81f2-7a849a6e1f33
keywords:
- Windows Media Player,Eigenschaften für das Objektmodell
- Windows Media Player,Methoden für das Objektmodell
- Windows Media Player,Ereignisse für das Objektmodell
- Windows Media Player Objektmodell,Eigenschaften
- Windows Media Player Objektmodell,Methoden
- Windows Media Player Objektmodell,Ereignisse
- Objektmodell,Eigenschaften
- Objektmodell,Methoden
- Objektmodell,Ereignisse
- Windows Media Player ActiveX,Eigenschaften für das Objektmodell
- ActiveX-Steuerelement,Eigenschaften für das Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement,Eigenschaften für das Objektmodell
- Windows Media Player Mobil,Eigenschaften für Objektmodell
- Windows Media Player ActiveX,Methoden für das Objektmodell
- ActiveX,Methoden für das Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement,Methoden für das Objektmodell
- Windows Media Player Mobil,Methoden für Objektmodell
- Windows Media Player ActiveX-Steuerelement,Ereignisse für das Objektmodell
- ActiveX-Steuerelement,Ereignisse für das Objektmodell
- Windows Media Player Mobile ActiveX-Steuerelement,Ereignisse für Objektmodell
- Windows Media Player Mobil,Ereignisse für Objektmodell
- Properties,Windows Media Player-Objektmodell
- Methoden,Windows Media Player Objektmodell
- events,Windows Media Player-Objektmodell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbcc07977bc7ddcd2dd162600d4fa3d2822a3f52f38983ea8427f89d9403ecf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118571084"
---
# <a name="properties-methods-and-events"></a>Eigenschaften, Methoden und Ereignisse

Jedes Objekt verfügt über Methoden und Eigenschaften, mit denen Sie das Steuerelement Windows Media Player programmieren können. Eine Methode ist eine Aktion, die das -Objekt übernehmen kann. Eine Eigenschaft ist ein Datenwert, den Sie lesen oder ändern können. Beispielsweise startet die **Play-Methode** die Wiedergabe des Inhalts, und die **frameRate-Eigenschaft** gibt die aktuelle Framerate des Inhalts an, der abspielt.

Darüber hinaus löst das **Player-Objekt** Ereignisse aus, die Ihnen die Möglichkeit geben, Aktionen zu bestimmten Zeiten durchzuführen. Sie schreiben Code in einen Ereignishandler, der ausgeführt wird, wenn Windows Media Player das entsprechende Ereignis löst. Sie können z. B. Code in einen **PlayStateChange-Ereignishandler** schreiben, der bestimmt, ob die Änderung des Zustands das Ende des Mediums ist. Wenn dies der Fall ist, wird ein Dialogfeld angezeigt, in dem Benutzer gefragt werden, ob sie die Medien wieder verwenden möchten.

> [!Note]  
> Alle Methoden im Windows Media Player sind asynchron. Wenn Sie zwei Methoden in derselben Prozedur aufrufen, kann sich die zweite Methode nicht darauf verlassen, dass die erste Methode ihre Aktion abgeschlossen hat.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Player-Objektmodell**](about-the-player-object-model.md)
</dt> </dl>

 

 




