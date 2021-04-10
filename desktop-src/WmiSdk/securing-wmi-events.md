---
description: WMI-Ereignisse werden vom Ereignis Anbieter an einen temporären oder permanenten Consumer übermittelt. Das WMI-Ereignis System verwendet den Vergleich der Sicherheits Deskriptoren für Ereignisse und Benutzerkonten-SIDs, um den Zugriff auf das Ereignis zu steuern.
ms.assetid: 86eaeb5c-c27e-4794-88e2-e0ffbb885290
ms.tgt_platform: multiple
title: Sichern von WMI-Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31280a4be25e358e28477bf6be060637f3f96bad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215327"
---
# <a name="securing-wmi-events"></a><span data-ttu-id="be624-104">Sichern von WMI-Ereignissen</span><span class="sxs-lookup"><span data-stu-id="be624-104">Securing WMI Events</span></span>

<span data-ttu-id="be624-105">WMI-Ereignisse werden vom [*Ereignis Anbieter*](gloss-e.md) an einen [*temporären*](gloss-t.md) oder [*permanenten*](gloss-p.md) Consumer übermittelt.</span><span class="sxs-lookup"><span data-stu-id="be624-105">WMI events are delivered by the [*event provider*](gloss-e.md) to a [*temporary*](gloss-t.md) or [*permanent*](gloss-p.md) consumer.</span></span> <span data-ttu-id="be624-106">Das WMI-Ereignis System verwendet den Vergleich der [*Sicherheits Deskriptoren*](gloss-s.md) für Ereignisse und Benutzerkonten- [*SIDs*](gloss-s.md) , um den Zugriff auf das Ereignis zu steuern.</span><span class="sxs-lookup"><span data-stu-id="be624-106">The WMI event system uses the comparison of [*security descriptors*](gloss-s.md) on events and user account [*SIDs*](gloss-s.md) to control event access.</span></span>

<span data-ttu-id="be624-107">Ereignisse werden normalerweise in Form einer Instanz einer Ereignisklasse übermittelt, aber nicht notwendigerweise vom [**\_ \_ Ereignis**](--event.md)abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="be624-107">Events are delivered in the form of an instance of an event class usually, but not necessarily, derived ultimately from [**\_\_Event**](--event.md).</span></span> <span data-ttu-id="be624-108">WMI bietet mehrere allgemeine Ereignis Klassen in den [WMI-System Klassen](wmi-system-classes.md), z. b. [**\_ \_ instancemodificationevent**](--instancemodificationevent.md).</span><span class="sxs-lookup"><span data-stu-id="be624-108">WMI supplies several general event classes in the [WMI System Classes](wmi-system-classes.md), such as [**\_\_InstanceModificationEvent**](--instancemodificationevent.md).</span></span> <span data-ttu-id="be624-109">Anbieter können auch Ihre eigenen Ereignis Klassen angeben.</span><span class="sxs-lookup"><span data-stu-id="be624-109">Providers may also supply their own event classes.</span></span> <span data-ttu-id="be624-110">Der [System Registrierungs Anbieter](/previous-versions/windows/desktop/regprov/system-registry-provider) verfügt z. b. über Ereignis Klassen, die die Änderung eines Registrierungsschlüssels oder-Werts melden, z. b. [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span><span class="sxs-lookup"><span data-stu-id="be624-110">For example, the [System Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider) has event classes that report the change of a registry key or value, such as [**RegistryKeyChangeEvent**](/previous-versions/windows/desktop/regprov/registrykeychangeevent).</span></span>

<span data-ttu-id="be624-111">In den folgenden Themen finden Sie Informationen zur sicheren Übermittlung von Ereignissen für Anbieter und zum sicheren empfangen von Ereignissen für Client Skripts und Anwendungen:</span><span class="sxs-lookup"><span data-stu-id="be624-111">The following topics supply information about securing delivery of events for providers and receiving events securely for client scripts and applications:</span></span>

-   [<span data-ttu-id="be624-112">Sicheres Bereitstellen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="be624-112">Providing Events Securely</span></span>](providing-events-securely.md)
-   [<span data-ttu-id="be624-113">Sicheres empfangen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="be624-113">Receiving Events Securely</span></span>](receiving-events-securely.md)

## <a name="related-topics"></a><span data-ttu-id="be624-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="be624-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be624-115">Verwalten der WMI-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="be624-115">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> </dl>

 

 
