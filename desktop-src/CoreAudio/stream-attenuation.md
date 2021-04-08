---
description: Standardmäßiges ducken
ms.assetid: 2ad9482f-1888-4f19-bc41-9d47a8e0ed15
title: Standardmäßiges ducken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d81aa22254ab33ee7396fd4a22d83cc7f5a58041
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748529"
---
# <a name="default-ducking-experience"></a><span data-ttu-id="c170f-103">Standardmäßiges ducken</span><span class="sxs-lookup"><span data-stu-id="c170f-103">Default Ducking Experience</span></span>

<span data-ttu-id="c170f-104">Stellen Sie sich ein Szenario vor, in dem ein Benutzer einen Telefonanruf erhält, während er die Musik auf dem Computer hört.</span><span class="sxs-lookup"><span data-stu-id="c170f-104">Consider a scenario where a user receives a phone call while listening to music on the computer.</span></span> <span data-ttu-id="c170f-105">Während des Telefonanrufs möchte der Benutzer die Lautstärke der Musik reduzieren, während er an den Telefonanruf teilnimmt, und das ursprüngliche Volume fortsetzen, nachdem der Telefonanruf beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="c170f-105">During the phone call, the user wants to reduce the volume level of the music while attending to the phone call, and resume the original volume after the phone call has ended.</span></span> <span data-ttu-id="c170f-106">Abhängig von den Optionen, die vom Benutzer in der **Sounds** -Systemsteuerung angegeben werden, stellt das Betriebssystem diese Funktion automatisch durch *Ducking* -oder *streamdämpfung* bereit – Verringerung der Intensität eines Audiostreams.</span><span class="sxs-lookup"><span data-stu-id="c170f-106">Depending on the options specified by the user in the **Sounds** control panel, the operating system automatically provides this functionality through *ducking* or *stream attenuation*—reduction in the intensity of an audio stream.</span></span>

<span data-ttu-id="c170f-107">Die standardmäßige Dämpfung ist abhängig von der Benutzereinstellung, wie in der **Sound** Option der Systemsteuerung angegeben.</span><span class="sxs-lookup"><span data-stu-id="c170f-107">The default attenuation experience depends on the user's preference, as specified in the control panel's **Sound** option.</span></span> <span data-ttu-id="c170f-108">Auf der Registerkarte **Kommunikation** kann der Benutzer eine Dämpfung auswählen (der Standardwert ist 80%), alle nicht-Kommunikationsstreams stumm schalten oder die standardmäßige Datenstrom Dämpfung deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="c170f-108">On the **Communications** tab, the user can choose an attenuation level (default value is 80%), mute all non-communication streams, or disable the default stream attenuation experience.</span></span> <span data-ttu-id="c170f-109">Das System ermöglicht das Öffnen neuer nicht-Kommunikationsstreams (außer bei neuen Systemsounds) während der Kommunikationssitzung, die neuen Streams werden jedoch nicht automatisch abgeschwächt.</span><span class="sxs-lookup"><span data-stu-id="c170f-109">The system allows new non-communication streams (except for new system sounds) to be opened during the communication session but the new streams are not automatically attenuated.</span></span> <span data-ttu-id="c170f-110">Wenn alle Kommunikationsstreams geschlossen sind, beendet das System die Kommunikationssitzung und stellt die Menge der Datenströme wieder her, die während der Kommunikationssitzung gedämpft wurden.</span><span class="sxs-lookup"><span data-stu-id="c170f-110">When all of the communication streams are closed, the system ends the communication session and restores the volume of the streams that were attenuated during the communication session.</span></span>

<span data-ttu-id="c170f-111">Um die streamdämpfung visuell anzugeben, ändert das System die volumemixer-Einstellungen abhängig von der Benutzereinstellung.</span><span class="sxs-lookup"><span data-stu-id="c170f-111">To indicate stream attenuation visually, the system changes the volume mixer settings depending on the user's preference.</span></span> <span data-ttu-id="c170f-112">Wenn der Benutzer z. b. eine Dämpfungs Ebene angibt, wird der Schieberegler vom volumemixer gesenkt, das neue abgedämpfte Volume wird angezeigt, und die ursprüngliche Volumeebene wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c170f-112">For example, if the user specifies an attenuation level, the volume mixer lowers the slider, displays the new attenuated volume, and displays the original volume level.</span></span> <span data-ttu-id="c170f-113">Dieses Verfahren wird in der folgenden Abbildung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c170f-113">The following image illustrates this process.</span></span>

![Diagramm des standardmäßigen streamdedäsierungsverhaltens in Windows 7](images/stream-aatenuation.jpg)

<span data-ttu-id="c170f-115">Eine Anwendung kann die Datenstrom Dämpfung überschreiben und eine benutzerdefinierte Ducking-Funktion implementieren, wenn Sie weiß, wann die Kommunikationssitzung beginnt und endet.</span><span class="sxs-lookup"><span data-stu-id="c170f-115">An application can override stream attenuation and implement a custom ducking experience if it knows when the communication session starts and ends.</span></span> <span data-ttu-id="c170f-116">Weitere Informationen finden Sie unter [Bereitstellen eines benutzerdefinierten Ducking-Verhaltens](providing-a-custom-ducking-experience.md).</span><span class="sxs-lookup"><span data-stu-id="c170f-116">For more information, see [Providing a Custom Ducking Behavior](providing-a-custom-ducking-experience.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c170f-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c170f-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c170f-118">Verwenden eines kommunikationsgeräts</span><span class="sxs-lookup"><span data-stu-id="c170f-118">Using a Communication Device</span></span>](using-the-communication-device.md)
</dt> <dt>

[<span data-ttu-id="c170f-119">Deaktivieren der Standardeinstellung für das ducken</span><span class="sxs-lookup"><span data-stu-id="c170f-119">Disabling the Default Ducking Experience</span></span>](disabling-the-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="c170f-120">Bereitstellen eines benutzerdefinierten Ducking-Verhaltens</span><span class="sxs-lookup"><span data-stu-id="c170f-120">Providing a Custom Ducking Behavior</span></span>](providing-a-custom-ducking-experience.md)
</dt> <dt>

[<span data-ttu-id="c170f-121">Implementierungs Überlegungen für Ducking-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="c170f-121">Implementation Considerations for Ducking Notifications</span></span>](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[<span data-ttu-id="c170f-122">Erhalten von Ducking-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="c170f-122">Getting Ducking Events</span></span>](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



