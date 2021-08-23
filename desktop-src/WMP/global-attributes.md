---
title: Globale Attribute (Windows Media Player SDK)
description: Globale Attribute
ms.assetid: 2ed09506-990e-4da2-89d6-6ff77dc43eb2
keywords:
- Windows Media Player Skins,globale Attribute
- Skins,globale Attribute
- Referenz für Skins, globale Attribute
- Globale Attribute
- Attribute,global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69c2d52b6489a28eff20e3a7e5c7180fc9e2db9309c0fe42880bfc779a23f563
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648080"
---
# <a name="global-attributes"></a>Globale Attribute

Globale Attribute sind Attribute, die einen einfachen Zugriff auf bestimmte Playerelemente oder -objekte von überall innerhalb einer Skin ermöglichen.

Das **globale Player-Attribut** ist ein Verweis auf das [Player-Objekt](player-object.md) und wird für den Zugriff auf die primäre Funktionalität des Windows Media Player. Im folgenden Beispiel wird der **Player verwendet,** um die Wiedergabe digitaler Medien zu starten.


```C++
<BUTTON
  onclick="jscript:player.controls.play();"
/>

```



Das **globale Designattribut** ist ein Verweis auf das [THEME-Element.](theme-element.md) Dies ist die  richtige Möglichkeit für den Zugriff auf THEME-Attribute, anstatt eine ID innerhalb des **THEME-Elements** anzugeben. Im folgenden Beispiel wird **design verwendet,** um eine neue Ansicht zu öffnen.


```C++
<TEXT 
  value="open" 
  onclick="jscript:theme.openView('newView');"
/>

```



Das **globale View-Attribut** ist ein Verweis auf die aktuelle [VIEW.](view-element.md) Dies kann anstelle der ID verwendet werden, die in den verschiedenen **VIEW-Elementen angegeben** ist. Im folgenden Beispiel wird **die ansicht verwendet,** um die aktuelle Ansicht zu schließen.


```C++
<BUTTON 
  id="quitbutton"
  onclick="jscript:view.close();"
/>

```



Das **globale Ereignisattribut** wird verwendet, um innerhalb von Ereignishandlern auf Ambient-Ereignisattribute zu zugreifen. Im folgenden Beispiel wird das **-Ereignis** verwendet, um zu bestimmen, ob die ALT-TASTE gedrückt wird, wenn auf eine Schaltfläche geklickt wird.


```C++
<BUTTON
  onclick="jscript:if (event.altKey == true) myText.value='ALT';"
/>

```



Das **globale PlayerApplication-Attribut** ist ein Verweis auf das [PlayerApplication-Objekt](playerapplication-object.md) und wird von Skindateien verwendet, die als benutzerdefinierte Benutzeroberflächen für Player-Remotesteuerelemente bereitgestellt werden. Das Player-Steuerelement kann nur in C++-Programme, die die **IWMPRemoteMediaServices-Schnittstelle** implementieren, in den Remotemodus eingebettet werden. Im folgenden Beispiel wird **playerApplication verwendet,** um in den vollständigen Modus des Players zu wechseln.


```C++
<BUTTON
  onclick="jscript:playerApplication.switchToPlayerApplication();"
/>

```



Weitere Informationen finden Sie unter [Ambient Event Attributes](ambient-event-attributes.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**verschiedene gefährliche Stoffe**](miscellaneous.md)
</dt> </dl>

 

 




