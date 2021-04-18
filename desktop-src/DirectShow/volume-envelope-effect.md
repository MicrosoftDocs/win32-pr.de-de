---
description: Volumeumschlags Effekt
ms.assetid: 17b6d842-e79c-49b0-baa4-1535b4a2c6ae
title: Volumeumschlags Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9364b88b1928e533a031f0700cb8a2c44bc9822d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357876"
---
# <a name="volume-envelope-effect"></a><span data-ttu-id="22528-103">Volumeumschlags Effekt</span><span class="sxs-lookup"><span data-stu-id="22528-103">Volume Envelope Effect</span></span>

> [!Note]  
> <span data-ttu-id="22528-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="22528-104">\[Deprecated.</span></span> <span data-ttu-id="22528-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="22528-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="22528-106">Der volumeumschlags Effekt legt das Volume in einem Audiostream fest.</span><span class="sxs-lookup"><span data-stu-id="22528-106">The Volume Envelope effect sets the volume on an audio stream.</span></span>

<span data-ttu-id="22528-107">Klassen-ID (CLSID): {036a9790-C153-11d2-9ef7-006008039e37}</span><span class="sxs-lookup"><span data-stu-id="22528-107">Class ID (CLSID): {036A9790-C153-11D2-9EF7-006008039E37}</span></span>

<span data-ttu-id="22528-108">CLSID-Variablen Name: CLSID- \_ audmixer</span><span class="sxs-lookup"><span data-stu-id="22528-108">CLSID Variable Name: CLSID\_AudMixer</span></span>

<span data-ttu-id="22528-109">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="22528-109">Properties</span></span>



| <span data-ttu-id="22528-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="22528-110">Property</span></span> | <span data-ttu-id="22528-111">type</span><span class="sxs-lookup"><span data-stu-id="22528-111">Type</span></span>   | <span data-ttu-id="22528-112">Standard</span><span class="sxs-lookup"><span data-stu-id="22528-112">Default</span></span> | <span data-ttu-id="22528-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="22528-113">Description</span></span>                                                                                                           |
|----------|--------|---------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22528-114">Volumen</span><span class="sxs-lookup"><span data-stu-id="22528-114">Vol</span></span>      | <span data-ttu-id="22528-115">double</span><span class="sxs-lookup"><span data-stu-id="22528-115">double</span></span> | <span data-ttu-id="22528-116">1.0</span><span class="sxs-lookup"><span data-stu-id="22528-116">1.0</span></span>     | <span data-ttu-id="22528-117">Volume als Prozentsatz des erstellten Volumes.</span><span class="sxs-lookup"><span data-stu-id="22528-117">Volume, as a percentage of the authored volume.</span></span> <span data-ttu-id="22528-118">Sie können Audioüberblendungen entwickeln, indem Sie diesen Eigenschafts Wert im Zeitverlauf variieren</span><span class="sxs-lookup"><span data-stu-id="22528-118">You can produce audio fades by varying this property value over time.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="22528-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22528-119">Remarks</span></span>

<span data-ttu-id="22528-120">Jedes Objekt in einer Zeitachse kann höchstens einen volumeumschlags Effekt haben.</span><span class="sxs-lookup"><span data-stu-id="22528-120">Each object in a timeline can have at most one volume envelope effect.</span></span> <span data-ttu-id="22528-121">In einer Komposition oder einer Gruppe wird der volumeumschlag vor allen anderen Audioeffekten unabhängig von seiner Priorität zuerst angewendet.</span><span class="sxs-lookup"><span data-stu-id="22528-121">In a composition or a group, the volume envelope is applied first, before any other audio effects, regardless of its priority.</span></span> <span data-ttu-id="22528-122">In einer Quelle oder einer Spur wird der volumeeffekt entsprechend seiner Priorität angewendet.</span><span class="sxs-lookup"><span data-stu-id="22528-122">In a source or a track, the volume effect is applied according to its priority.</span></span>

 

 



