---
description: Geräteklassen ermöglichen die Angabe der Eigenschaften "Symbole", "Bezeichnung" und "devicehandlers" für jedes Gerät dieser Klasse.
ms.assetid: E32C1BA6-B520-4809-A9E9-48813C7EBAA4
title: Angeben eines Symbols, einer Bezeichnung oder eines Geräte Handlers für ein Gerät mithilfe einer Geräteklasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f81ee6fa469a6bec13abbc1d8a088f5fb334ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994654"
---
# <a name="how-to-specify-an-icon-label-or-device-handler-for-a-device-using-a-device-class"></a><span data-ttu-id="5ca93-103">Angeben eines Symbols, einer Bezeichnung oder eines Geräte Handlers für ein Gerät mithilfe einer Geräteklasse</span><span class="sxs-lookup"><span data-stu-id="5ca93-103">How to Specify an Icon, Label, or Device Handler for a Device Using a Device Class</span></span>

<span data-ttu-id="5ca93-104">Geräteklassen ermöglichen die Angabe der Eigenschaften "Symbole", "Bezeichnung" und "devicehandlers" für jedes Gerät dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="5ca93-104">Device classes allow the specification of the Icons, Label, and DeviceHandlers properties for any device of that class.</span></span> <span data-ttu-id="5ca93-105">Dies ähnelt der Verwendung von Gerätegruppen, aber Geräteklassen und ihre Mitgliedschaften werden von der Hardware bestimmt, anstatt erstellt oder zugewiesen zu werden.</span><span class="sxs-lookup"><span data-stu-id="5ca93-105">This is similar to the use of device groups, but device classes and their memberships are determined by the hardware rather than being created or assigned.</span></span> <span data-ttu-id="5ca93-106">Jeder Klassen Schlüssel Name, der die GUID der Plug & Play Geräteschnittstelle ist, befindet sich unter dem **deviceclasses** -Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="5ca93-106">Each class key name, which is the Plug and Play device interface GUID, is found under the **DeviceClasses** key.</span></span> <span data-ttu-id="5ca93-107">Weisen Sie unter dem Schlüssel der einzelnen Klasse die Werte für Symbole, Bezeichnung und devicehandlers zu.</span><span class="sxs-lookup"><span data-stu-id="5ca93-107">Under the individual class key, assign the values for Icons, Label, and DeviceHandlers.</span></span>

## <a name="instructions"></a><span data-ttu-id="5ca93-108">Instructions</span><span class="sxs-lookup"><span data-stu-id="5ca93-108">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="5ca93-109">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="5ca93-109">Step 1:</span></span>

<span data-ttu-id="5ca93-110">Das folgende Beispiel zeigt die Werte Class Key und devicehandlers für die Volume-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5ca93-110">The following example shows the class key and DeviceHandlers values for the volume interface.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceClasses
                        {53f5630d-b6bf-11d0-94f2-00a0c91efb8b}
                           DeviceHandlers [REG_SZ] = GenericVolumeHandler
```

<span data-ttu-id="5ca93-111">Sie können auch benutzerdefinierte Geräteeigenschaften unter dem Geräteklassen Schlüssel hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5ca93-111">You can also add custom device properties under the device class key.</span></span> <span data-ttu-id="5ca93-112">Die benutzerdefinierten Geräteeigenschaften gelten dann für alle Geräte in dieser Klasse.</span><span class="sxs-lookup"><span data-stu-id="5ca93-112">The custom device properties then apply to all devices in that class.</span></span> <span data-ttu-id="5ca93-113">Geräten und Geräte Handlern sollten immer Symbole und Bezeichnungen zugeordnet sein, um die Mindestanforderungen an die Nutzbarkeit zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="5ca93-113">Devices and device handlers should always have associated icons and labels to meet minimum usability requirements.</span></span>

> [!Note]  
> <span data-ttu-id="5ca93-114">Eigenschaften, die auf der Geräte Instanzebene definiert werden, haben Vorrang vor den auf Gerätegruppen Ebene definierten Eigenschaften, die wiederum Vorrang vor den Eigenschaften haben, die auf Geräteklassen Ebene definiert sind.</span><span class="sxs-lookup"><span data-stu-id="5ca93-114">Properties that are defined at the device instance level take precedence over properties defined at the device group level, which in turn take precedence over properties defined at the device class level.</span></span>

 

 

 



