---
title: Playerapplication-Objekt
description: Das playerapplication-Objekt bietet eine Möglichkeit, den Wechsel zwischen einem remoten Windows Media Player-Steuerelement und dem vollständigen Modus von Windows Media Player zu koordinieren.
ms.assetid: 904bb30c-939d-4aeb-ba4b-c27afee471ea
keywords:
- Playerapplication-Objekt Windows-Media Player
topic_type:
- apiref
api_name:
- PlayerApplication Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 950efeb0a84f43dec904b3ffd21f715061e50d4d
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "104313242"
---
# <a name="playerapplication-object"></a><span data-ttu-id="95c86-104">Playerapplication-Objekt</span><span class="sxs-lookup"><span data-stu-id="95c86-104">PlayerApplication Object</span></span>

<span data-ttu-id="95c86-105">Das **playerapplication** -Objekt bietet eine Möglichkeit, den Wechsel zwischen einem remoten Windows Media Player-Steuerelement und dem vollständigen Modus von Windows Media Player zu koordinieren.</span><span class="sxs-lookup"><span data-stu-id="95c86-105">The **PlayerApplication** object provides a way to coordinate switching between a remoted Windows Media Player control and the full mode of Windows Media Player.</span></span> <span data-ttu-id="95c86-106">Dieses Objekt wird nur in C++-Programmen verwendet, die die **iwmpremotemediaservices** -Schnittstelle implementieren und das Player-Steuerelement in den Remote Modus einbetten.</span><span class="sxs-lookup"><span data-stu-id="95c86-106">This object is used only with C++ programs that implement the **IWMPRemoteMediaServices** interface and embed the Player control in remote mode.</span></span> <span data-ttu-id="95c86-107">Skin-Dateien, die als benutzerdefinierte Schnittstellen für die Remote-Windows-Media Player Steuerung verwendet werden, greifen in Skriptcode über das globale Attribut **playerapplication** auf dieses Objekt zu</span><span class="sxs-lookup"><span data-stu-id="95c86-107">Skin files used as custom interfaces for the remoted Windows Media Player control access this object in script code through the **playerApplication** global attribute.</span></span>

<span data-ttu-id="95c86-108">Das **playerapplication** -Objekt unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="95c86-108">The **PlayerApplication** object supports the following properties.</span></span>



| <span data-ttu-id="95c86-109">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="95c86-109">Property</span></span>                                           | <span data-ttu-id="95c86-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95c86-110">Description</span></span>                                                                                              |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="95c86-111">hasdisplay</span><span class="sxs-lookup"><span data-stu-id="95c86-111">hasDisplay</span></span>](playerapplication-hasdisplay.md)     | <span data-ttu-id="95c86-112">Ruft einen Wert ab, der angibt, ob Videos über das Remote Fenster Media Player-Steuerelement angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="95c86-112">Retrieves a value indicating whether video can display through the remoted Windows Media Player control.</span></span> |
| [<span data-ttu-id="95c86-113">playerdocked</span><span class="sxs-lookup"><span data-stu-id="95c86-113">playerDocked</span></span>](playerapplication-playerdocked.md) | <span data-ttu-id="95c86-114">Ruft einen Wert ab, der angibt, ob sich Windows Media Player in einem angedockten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="95c86-114">Retrieves a value indicating whether Windows Media Player is in a docked state.</span></span>                          |



 

<span data-ttu-id="95c86-115">Das **playerapplication** -Objekt unterstützt die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="95c86-115">The **PlayerApplication** object supports the following methods.</span></span>



| <span data-ttu-id="95c86-116">Methode</span><span class="sxs-lookup"><span data-stu-id="95c86-116">Method</span></span>                                                                       | <span data-ttu-id="95c86-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="95c86-117">Description</span></span>                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="95c86-118">SwitchTo-Control</span><span class="sxs-lookup"><span data-stu-id="95c86-118">switchToControl</span></span>](playerapplication-switchtocontrol.md)                     | <span data-ttu-id="95c86-119">Schaltet ein Remotes Windows Media Player-Steuerelement in den angedockten Zustand.</span><span class="sxs-lookup"><span data-stu-id="95c86-119">Switches a remoted Windows Media Player control to the docked state.</span></span>            |
| [<span data-ttu-id="95c86-120">switchtoplayerapplication</span><span class="sxs-lookup"><span data-stu-id="95c86-120">switchToPlayerApplication</span></span>](playerapplication-switchtoplayerapplication.md) | <span data-ttu-id="95c86-121">Schaltet ein Remotes Windows Media Player-Steuerelement in den vollständigen Modus des Players.</span><span class="sxs-lookup"><span data-stu-id="95c86-121">Switches a remoted Windows Media Player control to the full mode of the Player.</span></span> |



 

<span data-ttu-id="95c86-122">Der Zugriff auf das **playerapplication** -Objekt erfolgt über die folgende Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="95c86-122">The **PlayerApplication** object is accessed through the following property.</span></span>



| <span data-ttu-id="95c86-123">Object</span><span class="sxs-lookup"><span data-stu-id="95c86-123">Object</span></span>                      | <span data-ttu-id="95c86-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="95c86-124">Property</span></span>                                          |
|-----------------------------|---------------------------------------------------|
| [<span data-ttu-id="95c86-125">Player</span><span class="sxs-lookup"><span data-stu-id="95c86-125">Player</span></span>](player-object.md) | [<span data-ttu-id="95c86-126">playerapplication</span><span class="sxs-lookup"><span data-stu-id="95c86-126">playerApplication</span></span>](player-playerapplication.md) |



 

## <a name="see-also"></a><span data-ttu-id="95c86-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95c86-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95c86-128">**Objektmodell Referenz für die Skripterstellung**</span><span class="sxs-lookup"><span data-stu-id="95c86-128">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> <dt>

[<span data-ttu-id="95c86-129">**Remoting des Windows Media Player-Steuerelements**</span><span class="sxs-lookup"><span data-stu-id="95c86-129">**Remoting the Windows Media Player Control**</span></span>](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




