---
description: Geräte Rollen
ms.assetid: aa787004-0d3e-448b-80dd-92055f841aee
title: Geräte Rollen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b7182e3af6bf76af500588546a1b7c0db9eea97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126901"
---
# <a name="device-roles"></a><span data-ttu-id="9d0cf-103">Geräte Rollen</span><span class="sxs-lookup"><span data-stu-id="9d0cf-103">Device Roles</span></span>

<span data-ttu-id="9d0cf-104">Wenn ein System mindestens zwei audiorendering-Endpunkt Geräte enthält, kann ein Gerät am besten für die Wiedergabe eines audioinhaltstyp geeignet sein, und ein anderes Gerät eignet sich möglicherweise am besten für die Wiedergabe eines anderen Inhaltstyps.</span><span class="sxs-lookup"><span data-stu-id="9d0cf-104">If a system contains two or more audio-rendering endpoint devices, then one device might be best for playing one type of audio content, and another device might be best for playing another type of content.</span></span> <span data-ttu-id="9d0cf-105">Wenn ein System z. b. über zwei renderinggeräte verfügt, kann der Benutzer auf einem Gerät Musik abspielen und System Benachrichtigungs Sounds auf dem anderen Gerät abspielen.</span><span class="sxs-lookup"><span data-stu-id="9d0cf-105">For example, if a system has two rendering devices, the user might choose to play music on one device and to play system notification sounds on the other.</span></span>

<span data-ttu-id="9d0cf-106">Wenn ein System mindestens zwei audioerfassungs-Endpunkt Geräte enthält, kann ein Gerät am besten zum Erfassen eines Audioinhalts Typs geeignet sein, und ein anderes Gerät eignet sich möglicherweise am besten zum Erfassen eines anderen Inhaltstyps.</span><span class="sxs-lookup"><span data-stu-id="9d0cf-106">Similarly, if a system contains two or more audio-capture endpoint devices, then one device might be best for capturing one type of audio content, and another device might be best for capturing another type of content.</span></span> <span data-ttu-id="9d0cf-107">Wenn ein System beispielsweise über zwei Erfassungsgeräte verfügt, kann der Benutzer Live Musik auf einem Gerät aufzeichnen und das andere Gerät für Sprachbefehle verwenden.</span><span class="sxs-lookup"><span data-stu-id="9d0cf-107">For example, if a system has two capture devices, the user might choose to record live music on one device and to use the other device for voice commands.</span></span>

<span data-ttu-id="9d0cf-108">Geräte können über drei Rollen verfügen: Console, Communications und Multimedia. in der folgenden Tabelle werden die Geräte Rollen beschrieben, die von den drei Konstanten – econsole, eCommunications und emultimedia – in der [**erole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) -Enumeration identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="9d0cf-108">Devices can have three roles: Console, Communications, and Multimedia.The following table describes the device roles identified by the three constants—eConsole, eCommunications, and eMultimedia—in the [**ERole**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-erole) enumeration.</span></span>



| <span data-ttu-id="9d0cf-109">Erole-Konstante</span><span class="sxs-lookup"><span data-stu-id="9d0cf-109">ERole constant</span></span>  | <span data-ttu-id="9d0cf-110">Geräte Rolle</span><span class="sxs-lookup"><span data-stu-id="9d0cf-110">Device role</span></span>                              | <span data-ttu-id="9d0cf-111">Renderingbeispiele</span><span class="sxs-lookup"><span data-stu-id="9d0cf-111">Rendering examples</span></span>             | <span data-ttu-id="9d0cf-112">Beispiele für die Erfassung</span><span class="sxs-lookup"><span data-stu-id="9d0cf-112">Capture examples</span></span>                   |
|-----------------|------------------------------------------|--------------------------------|------------------------------------|
| <span data-ttu-id="9d0cf-113">econsole</span><span class="sxs-lookup"><span data-stu-id="9d0cf-113">eConsole</span></span>        | <span data-ttu-id="9d0cf-114">Interaktion mit dem Computer</span><span class="sxs-lookup"><span data-stu-id="9d0cf-114">Interaction with the computer</span></span>            | <span data-ttu-id="9d0cf-115">Spiele und System Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="9d0cf-115">Games and system notifications</span></span> | <span data-ttu-id="9d0cf-116">Sprachbefehle</span><span class="sxs-lookup"><span data-stu-id="9d0cf-116">Voice commands</span></span>                     |
| <span data-ttu-id="9d0cf-117">eCommunications</span><span class="sxs-lookup"><span data-stu-id="9d0cf-117">eCommunications</span></span> | <span data-ttu-id="9d0cf-118">Sprachkommunikation mit einer anderen Person</span><span class="sxs-lookup"><span data-stu-id="9d0cf-118">Voice communications with another person</span></span> | <span data-ttu-id="9d0cf-119">Chat und VoIP</span><span class="sxs-lookup"><span data-stu-id="9d0cf-119">Chat and VoIP</span></span>                  | <span data-ttu-id="9d0cf-120">Chat und VoIP</span><span class="sxs-lookup"><span data-stu-id="9d0cf-120">Chat and VoIP</span></span>                      |
| <span data-ttu-id="9d0cf-121">emultimedia</span><span class="sxs-lookup"><span data-stu-id="9d0cf-121">eMultimedia</span></span>     | <span data-ttu-id="9d0cf-122">Abspielen oder Aufzeichnen von Audioinhalten</span><span class="sxs-lookup"><span data-stu-id="9d0cf-122">Playing or recording audio content</span></span>       | <span data-ttu-id="9d0cf-123">Musik und Filme</span><span class="sxs-lookup"><span data-stu-id="9d0cf-123">Music and movies</span></span>               | <span data-ttu-id="9d0cf-124">Erzählung und Live Musik Aufzeichnung</span><span class="sxs-lookup"><span data-stu-id="9d0cf-124">Narration and live music recording</span></span> |



 

<span data-ttu-id="9d0cf-125">Einem bestimmten Rendering-oder Aufzeichnungsgerät können keine, eine, einige oder alle Rollen in der vorangehenden Tabelle zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="9d0cf-125">A particular rendering or capture device might be assigned none, one, some, or all of the roles in the preceding table.</span></span> <span data-ttu-id="9d0cf-126">Jede Rolle in der Tabelle wird immer einem (und nur einem) renderinggerät und einem (und nur einem) Erfassungsgerät zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="9d0cf-126">At any time, each role in the table is assigned to one (and only one) rendering device and to one (and only one) capture device.</span></span> <span data-ttu-id="9d0cf-127">Das heißt, die Zuweisung von Rollen zum Rendern von Geräten ist unabhängig von der Zuweisung von Rollen zum Erfassen von Geräten.</span><span class="sxs-lookup"><span data-stu-id="9d0cf-127">That is, the assignment of roles to rendering devices is independent of the assignment of roles to capture devices.</span></span>

<span data-ttu-id="9d0cf-128">Eine Anwendung kann Ihre gesamten Ausgabedaten Ströme über ein einzelnes renderingendpunkt-Gerät wiedergeben und alle Eingabedaten Ströme von einem einzelnen Erfassungs Endpunkt-Gerät aufzeichnen.</span><span class="sxs-lookup"><span data-stu-id="9d0cf-128">An application might choose to play all of its output streams through a single rendering endpoint device, and to record all of its input streams from a single capture endpoint device.</span></span> <span data-ttu-id="9d0cf-129">Alternativ kann eine Anwendung ihre Ausgabedaten Ströme über ein renderinggerät wiedergeben und andere Ausgabedaten Ströme über ein anderes renderinggerät wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="9d0cf-129">Alternatively, an application might choose to play some of its output streams through one rendering device and to play other output streams through another rendering device.</span></span> <span data-ttu-id="9d0cf-130">Entsprechend kann es auch sein, dass einige der Eingabedaten Ströme über ein Erfassungsgerät aufgezeichnet werden und andere Eingabedaten Ströme über ein anderes Erfassungsgerät aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="9d0cf-130">Similarly, it might choose to record some of its input streams through one capture device and to record other input streams through another capture device.</span></span> <span data-ttu-id="9d0cf-131">In allen Fällen kann die Anwendung jeden Stream dem Gerät zuweisen, dessen Rolle für diesen Stream am besten geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="9d0cf-131">In all cases, the application can assign each stream to the device whose role is most appropriate for that stream.</span></span>

<span data-ttu-id="9d0cf-132">Beispielsweise kann eine VoIP-Anwendung den Ausgabestream, der die Benachrichtigung über den Ring enthält, dem renderingendpunktgerät mit der econsole-Rolle zuweisen.</span><span class="sxs-lookup"><span data-stu-id="9d0cf-132">For example, a VoIP application might assign the output stream that contains the ring-in notification to the rendering endpoint device with the eConsole role.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d0cf-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9d0cf-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d0cf-134">Audioendpunktgeräte</span><span class="sxs-lookup"><span data-stu-id="9d0cf-134">Audio Endpoint Devices</span></span>](audio-endpoint-devices.md)
</dt> <dt>

[<span data-ttu-id="9d0cf-135">Arbeiten mit Geräte Rollen</span><span class="sxs-lookup"><span data-stu-id="9d0cf-135">Working with Device Roles</span></span>](device-roles-in-windows-vista.md)
</dt> <dt>

[<span data-ttu-id="9d0cf-136">Interoperabilität mit Legacy-audioapis</span><span class="sxs-lookup"><span data-stu-id="9d0cf-136">Interoperability with Legacy Audio APIs</span></span>](interoperability-with-legacy-audio-apis.md)
</dt> </dl>

 

 



