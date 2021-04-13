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
# <a name="global-attributes"></a><span data-ttu-id="e8a11-108">Globale Attribute</span><span class="sxs-lookup"><span data-stu-id="e8a11-108">Global Attributes</span></span>

<span data-ttu-id="e8a11-109">Globale Attribute sind Attribute, die einfachen Zugriff auf bestimmte Player Elemente oder Objekte von jedem beliebigen Ort innerhalb eines Skin ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="e8a11-109">Global attributes are attributes that provide easy access to certain player elements or objects from anywhere within a skin.</span></span>

<span data-ttu-id="e8a11-110">Das globale Attribut " **Player** " ist ein Verweis auf das [Player](player-object.md) -Objekt und wird für den Zugriff auf die primäre Funktionalität von Windows-Media Player verwendet.</span><span class="sxs-lookup"><span data-stu-id="e8a11-110">The **player** global attribute is a reference to the [Player](player-object.md) object, and is used to access the primary functionality of Windows Media Player.</span></span> <span data-ttu-id="e8a11-111">Im folgenden Beispiel wird **Player** verwendet, um die Wiedergabe digitaler Medien zu starten.</span><span class="sxs-lookup"><span data-stu-id="e8a11-111">The following example uses **player** to begin digital media playback.</span></span>


```C++
<BUTTON
  onclick="jscript:player.controls.play();"
/>

```



<span data-ttu-id="e8a11-112">Das **Global Attribute** -Attribut ist ein Verweis auf das [Theme](theme-element.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="e8a11-112">The **theme** global attribute is a reference to the [THEME](theme-element.md) element.</span></span> <span data-ttu-id="e8a11-113">Dies ist die richtige Methode für den **Zugriff auf** Design Attribute, anstatt eine ID innerhalb des **Theme** -Elements anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e8a11-113">This is the proper way to access **THEME** attributes, rather than by specifying an ID within the **THEME** element.</span></span> <span data-ttu-id="e8a11-114">Im folgenden Beispiel wird das **Design verwendet,** um eine neue Ansicht zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e8a11-114">The following example uses **theme** to open a new view.</span></span>


```C++
<TEXT 
  value="open" 
  onclick="jscript:theme.openView('newView');"
/>

```



<span data-ttu-id="e8a11-115">Das **View** Global-Attribut ist ein Verweis auf die aktuelle [Ansicht](view-element.md).</span><span class="sxs-lookup"><span data-stu-id="e8a11-115">The **view** global attribute is a reference to the current [VIEW](view-element.md).</span></span> <span data-ttu-id="e8a11-116">Dies kann anstelle der ID verwendet werden, die in den verschiedenen **Ansichts** Elementen angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="e8a11-116">This can be used instead of the ID specified within the various **VIEW** elements.</span></span> <span data-ttu-id="e8a11-117">Im folgenden Beispiel wird die **Ansicht** verwendet, um die aktuelle Ansicht zu schließen.</span><span class="sxs-lookup"><span data-stu-id="e8a11-117">The following example uses **view** to close the current view.</span></span>


```C++
<BUTTON 
  id="quitbutton"
  onclick="jscript:view.close();"
/>

```



<span data-ttu-id="e8a11-118">Das **Ereignis** Global-Attribut wird für den Zugriff auf Ambient-Ereignis Attribute aus Ereignis Handlern verwendet.</span><span class="sxs-lookup"><span data-stu-id="e8a11-118">The **event** global attribute is used to access ambient event attributes from within event handlers.</span></span> <span data-ttu-id="e8a11-119">Im folgenden Beispiel wird das- **Ereignis** verwendet, um zu bestimmen, ob beim Klicken auf eine Schaltfläche die Alt-Taste gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="e8a11-119">The following example uses **event** to determine whether the ALT key is pressed when a button is clicked.</span></span>


```C++
<BUTTON
  onclick="jscript:if (event.altKey == true) myText.value='ALT';"
/>

```



<span data-ttu-id="e8a11-120">Das globale Attribut **playerapplication** ist ein Verweis auf das [playerapplication](playerapplication-object.md) -Objekt und wird von Skin-Dateien verwendet, die als benutzerdefinierte Benutzeroberflächen für Remote Player-Steuerelemente bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e8a11-120">The **playerApplication** global attribute is a reference to the [PlayerApplication](playerapplication-object.md) object, and is used by skin files provided as custom user interfaces for remoted Player controls.</span></span> <span data-ttu-id="e8a11-121">Das Player-Steuerelement kann nur in C++-Programmen, die die **iwmpremotemediaservices** -Schnittstelle implementieren, in den Remote Modus eingebettet werden.</span><span class="sxs-lookup"><span data-stu-id="e8a11-121">The Player control can be embedded in remote mode only in C++ programs that implement the **IWMPRemoteMediaServices** interface.</span></span> <span data-ttu-id="e8a11-122">Im folgenden Beispiel wird **playerapplication** verwendet, um in den vollständigen Modus des Players zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="e8a11-122">The following example uses **playerApplication** to switch to the full mode of the Player.</span></span>


```C++
<BUTTON
  onclick="jscript:playerApplication.switchToPlayerApplication();"
/>

```



<span data-ttu-id="e8a11-123">Weitere Informationen finden Sie unter [Ambient-Ereignis Attribute](ambient-event-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="e8a11-123">For more information, see [Ambient Event Attributes](ambient-event-attributes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e8a11-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e8a11-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8a11-125">**Verschiedenes**</span><span class="sxs-lookup"><span data-stu-id="e8a11-125">**Miscellaneous**</span></span>](miscellaneous.md)
</dt> </dl>

 

 




