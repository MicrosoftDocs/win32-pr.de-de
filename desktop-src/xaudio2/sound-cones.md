---
description: Ein Modell, das die Lautstärke des orientierten Sounds beschreibt.
ms.assetid: 15252358-d932-22f4-f13a-8e4b8487dd86
title: Audiokegel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215659ab08c33066abfade2faf206f6360a51051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364228"
---
# <a name="sound-cones"></a><span data-ttu-id="bd803-103">Audiokegel</span><span class="sxs-lookup"><span data-stu-id="bd803-103">Sound Cones</span></span>

<span data-ttu-id="bd803-104">Ein Modell, das die Lautstärke des orientierten Sounds beschreibt.</span><span class="sxs-lookup"><span data-stu-id="bd803-104">A model that describes the loudness of oriented sound.</span></span>

<span data-ttu-id="bd803-105">Ein Sound ohne Ausrichtung hat dieselbe Amplitude in der angegebenen Entfernung in alle Richtungen.</span><span class="sxs-lookup"><span data-stu-id="bd803-105">A sound with no orientation has the same amplitude at a given distance in all directions.</span></span> <span data-ttu-id="bd803-106">Ein Sound mit einer Ausrichtung ist in der Richtung der Ausrichtung laut Loudest.</span><span class="sxs-lookup"><span data-stu-id="bd803-106">A sound with an orientation is loudest in the direction of orientation.</span></span> <span data-ttu-id="bd803-107">Das Modell, das die Lautstärke des orientierten Sounds beschreibt, wird als audiokegel bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="bd803-107">The model that describes the loudness of the oriented sound is called a sound cone.</span></span> <span data-ttu-id="bd803-108">Audiokegel bestehen aus einem inneren (oder inneren) Kegel und einem äußeren (oder äußeren) Kegel.</span><span class="sxs-lookup"><span data-stu-id="bd803-108">Sound cones are made up of an inside (or inner) cone and an outside (or outer) cone.</span></span> <span data-ttu-id="bd803-109">Der äußere Kegelwinkel muss immer größer oder gleich dem inneren Kegelwinkel sein.</span><span class="sxs-lookup"><span data-stu-id="bd803-109">The outside cone angle must always be equal to or greater than the inside cone angle.</span></span>

<span data-ttu-id="bd803-110">In jedem Winkel im Inneren Kegel wird das Volume des Sounds auf das innere Kegel Volume festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bd803-110">At any angle within the inner cone, the volume of the sound is set to the inner cone volume.</span></span> <span data-ttu-id="bd803-111">Dabei wird das Basis Volume des Puffers, die Entfernung vom Listener, die Ausrichtung des Listener, wenn der Listener über einen eigenen Kegel verfügt usw. berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="bd803-111">This takes into account the basic volume of the buffer, the distance from the listener, the listener's orientation if the listener has its own cone, and so on.</span></span>

<span data-ttu-id="bd803-112">In jedem Winkel außerhalb des äußeren Kegel wird das normale Volume durch einen von der Anwendung festgelegten Faktor gedämpft.</span><span class="sxs-lookup"><span data-stu-id="bd803-112">At any angle outside the outer cone, the normal volume is attenuated by a factor set by the application.</span></span> <span data-ttu-id="bd803-113">Die Volumeebene für außen Kegel wird als lineare Amplitude-Scaler ausgedrückt: 1,0 f stellt keine auf das ursprüngliche Signal angewendete Dämpfung dar, 0,5 f bezeichnet eine Dämpfung von 6 dB, und 0,0 f führt zu einer Ruhe Minderung.</span><span class="sxs-lookup"><span data-stu-id="bd803-113">The outside cone volume level is expressed as a linear amplitude scaler: 1.0 f represents no attenuation applied to the original signal, 0.5 f denotes an attenuation of 6 dB, and 0.0 f results in silence.</span></span> <span data-ttu-id="bd803-114">Die Verstärkung (Volume > 1,0 f) ist ebenfalls zulässig und wird nicht geklammert.</span><span class="sxs-lookup"><span data-stu-id="bd803-114">Amplification (volume > 1.0 f) is also allowed, and is not clamped.</span></span> <span data-ttu-id="bd803-115">Der gültige volumebereich ist tatsächlich 0,0 f bis 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="bd803-115">The valid volume range is actually 0.0 f to 2.0 f.</span></span>

<span data-ttu-id="bd803-116">Zwischen dem inneren und äußeren Kegel besteht eine Übergangszone zwischen dem inneren Volume und dem externen Volume.</span><span class="sxs-lookup"><span data-stu-id="bd803-116">Between the inner and outer cones is a zone of transition from the inside volume to the outside volume.</span></span> <span data-ttu-id="bd803-117">Das Volume nähert sich dem äußeren Volume des Cone, wenn sich der Winkel vergrößert.</span><span class="sxs-lookup"><span data-stu-id="bd803-117">The volume approaches the cone's outer volume as the angle increases.</span></span>

<span data-ttu-id="bd803-118">Kegel können andere Parameter als das Volume beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="bd803-118">Cones can affect parameters other than volume.</span></span> <span data-ttu-id="bd803-119">Der niedrige Durchlauf Filter und die sendersendeebene können ebenfalls beeinträchtigt werden, sodass die Technik noch dramatischer wird.</span><span class="sxs-lookup"><span data-stu-id="bd803-119">Low pass filter and reverb send level may also be affected, making the technique even more dramatic.</span></span> <span data-ttu-id="bd803-120">Beispielsweise kann mit einem Kegel auf dem Listener alle Klänge hinter dem Listener angegeben werden, um einen wenig gedämpften Wert zu erhalten, und einen geringfügig höheren Inhalt für das Direct-Verhältnis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="bd803-120">For example, with a cone on the listener, one can specify all sounds behind the listener get a bit muffled, and have slightly higher reverb-to-direct ratio content.</span></span> <span data-ttu-id="bd803-121">Diese stellen weitere Hinweise bereit, dass der Sound hinter dem Benutzer liegt.</span><span class="sxs-lookup"><span data-stu-id="bd803-121">These provide more cues that the sound is behind the user.</span></span> <span data-ttu-id="bd803-122">Dadurch wird der Realismus verbessert.</span><span class="sxs-lookup"><span data-stu-id="bd803-122">This enhances realism.</span></span>

<span data-ttu-id="bd803-123">In der folgenden Abbildung ist das Konzept der Sound Kegel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="bd803-123">The following illustration shows the concept of sound cones.</span></span>

![audiokegel](images/common-audio-concepts-sound-cones.png)

<span data-ttu-id="bd803-125">Wenn Sie audiokegel ordnungsgemäß entwerfen, können Sie Ihre Anwendung mit dramatischen Effekten versehen.</span><span class="sxs-lookup"><span data-stu-id="bd803-125">Designing sound cones properly can add dramatic effects to your application.</span></span> <span data-ttu-id="bd803-126">Sie können z. b. eine Audioquelle in der Mitte eines Raums positionieren und deren Ausrichtung auf eine öffnende Tür in einem Gang festlegen.</span><span class="sxs-lookup"><span data-stu-id="bd803-126">For example, you could position a sound source in the center of a room, setting its orientation toward an open door in a hallway.</span></span> <span data-ttu-id="bd803-127">Legen Sie dann den Winkel des inneren Kegel so fest, dass er sich auf die Breite der Tür erstreckt, den äußeren Kegel etwas breiter macht und schließlich das äußere Kegel Volume als nicht hörbar festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bd803-127">Then set the angle of the inside cone so that it extends to the width of the doorway, make the outside cone a bit wider, and finally set the outside cone volume to inaudible.</span></span> <span data-ttu-id="bd803-128">Ein Listener, der sich entlang des Flurs bewegt, wird den Sound nur dann hören, wenn er sich in der Nähe der</span><span class="sxs-lookup"><span data-stu-id="bd803-128">A listener moving along the hallway will begin to hear the sound only when near the doorway.</span></span> <span data-ttu-id="bd803-129">Der Sound ist laut laudest, wenn der Listener vor dem öffnenden Tor übergibt.</span><span class="sxs-lookup"><span data-stu-id="bd803-129">The sound will be loudest as the listener passes in front of the open door.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bd803-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bd803-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd803-131">Allgemeine audiokonzepte</span><span class="sxs-lookup"><span data-stu-id="bd803-131">Common Audio Concepts</span></span>](common-audio-concepts.md)
</dt> <dt>

[<span data-ttu-id="bd803-132">X3DAudio</span><span class="sxs-lookup"><span data-stu-id="bd803-132">X3DAudio</span></span>](x3daudio-overview.md)
</dt> <dt>

[<span data-ttu-id="bd803-133">**X3DAUDIO- \_ Kegel**</span><span class="sxs-lookup"><span data-stu-id="bd803-133">**X3DAUDIO\_CONE**</span></span>](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)
</dt> </dl>

 

 



