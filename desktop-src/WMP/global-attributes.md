---
title: Globale Attribute (Windows Media Player SDK)
description: Globale Attribute
ms.assetid: 2ed09506-990e-4da2-89d6-6ff77dc43eb2
keywords:
- Windows Media Player Skins, globale Attribute
- Skins, globale Attribute
- Referenz für Skins, globale Attribute
- Globale Attribute
- Attribute, Global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19c3f7a605b5c277b3207cefbbeaaa641f81f026
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2019
ms.locfileid: "104389474"
---
# <a name="global-attributes"></a>Globale Attribute

Globale Attribute sind Attribute, die einfachen Zugriff auf bestimmte Player Elemente oder Objekte von jedem beliebigen Ort innerhalb eines Skin ermöglichen.

Das globale Attribut " **Player** " ist ein Verweis auf das [Player](player-object.md) -Objekt und wird für den Zugriff auf die primäre Funktionalität von Windows-Media Player verwendet. Im folgenden Beispiel wird **Player** verwendet, um die Wiedergabe digitaler Medien zu starten.


```C++
<BUTTON
  onclick="jscript:player.controls.play();"
/>

```



Das **Global Attribute** -Attribut ist ein Verweis auf das [Theme](theme-element.md) -Element. Dies ist die richtige Methode für den **Zugriff auf** Design Attribute, anstatt eine ID innerhalb des **Theme** -Elements anzugeben. Im folgenden Beispiel wird das **Design verwendet,** um eine neue Ansicht zu öffnen.


```C++
<TEXT 
  value="open" 
  onclick="jscript:theme.openView('newView');"
/>

```



Das **View** Global-Attribut ist ein Verweis auf die aktuelle [Ansicht](view-element.md). Dies kann anstelle der ID verwendet werden, die in den verschiedenen **Ansichts** Elementen angegeben ist. Im folgenden Beispiel wird die **Ansicht** verwendet, um die aktuelle Ansicht zu schließen.


```C++
<BUTTON 
  id="quitbutton"
  onclick="jscript:view.close();"
/>

```



Das **Ereignis** Global-Attribut wird für den Zugriff auf Ambient-Ereignis Attribute aus Ereignis Handlern verwendet. Im folgenden Beispiel wird das- **Ereignis** verwendet, um zu bestimmen, ob beim Klicken auf eine Schaltfläche die Alt-Taste gedrückt wird.


```C++
<BUTTON
  onclick="jscript:if (event.altKey == true) myText.value='ALT';"
/>

```



Das globale Attribut **playerapplication** ist ein Verweis auf das [playerapplication](playerapplication-object.md) -Objekt und wird von Skin-Dateien verwendet, die als benutzerdefinierte Benutzeroberflächen für Remote Player-Steuerelemente bereitgestellt werden. Das Player-Steuerelement kann nur in C++-Programmen, die die **iwmpremotemediaservices** -Schnittstelle implementieren, in den Remote Modus eingebettet werden. Im folgenden Beispiel wird **playerapplication** verwendet, um in den vollständigen Modus des Players zu wechseln.


```C++
<BUTTON
  onclick="jscript:playerApplication.switchToPlayerApplication();"
/>

```



Weitere Informationen finden Sie unter [Ambient-Ereignis Attribute](ambient-event-attributes.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verschiedenes**](miscellaneous.md)
</dt> </dl>

 

 




