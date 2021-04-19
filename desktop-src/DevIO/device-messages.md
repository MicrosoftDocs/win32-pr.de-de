---
description: Geräte Nachrichten sind Systemmeldungen, die Anwendungen und andere Features von Geräte Änderungs Ereignissen benachrichtigen.
ms.assetid: 4d1ace87-2d02-4ba4-9bcc-da86cf3481db
title: Gerätemeldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e22fe5b9f8b3f9fcc2a075767aa684bd92962f32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343000"
---
# <a name="device-messages"></a><span data-ttu-id="3c2aa-103">Gerätemeldungen</span><span class="sxs-lookup"><span data-stu-id="3c2aa-103">Device Messages</span></span>

<span data-ttu-id="3c2aa-104">Geräte Nachrichten sind Systemmeldungen, die Anwendungen und andere Features von Geräte Änderungs Ereignissen benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-104">Device messages are system messages that notify applications and other features of device change events.</span></span> <span data-ttu-id="3c2aa-105">Diese Ereignisse treten immer dann auf, wenn das System eine Änderung an der System Hardware erkennt, z. b. wenn der Benutzer einen Laptop andockt und ihn abdockt oder ein Gerät wie eine PCMCIA-Karte einfügt oder entfernt.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-105">These events occur whenever the system detects a change to the system hardware, such as when the user docks and undocks a laptop computer, or inserts or removes a device such as a PCMCIA card.</span></span> <span data-ttu-id="3c2aa-106">Geräte Ereignisse können auftreten, während das System ausgeführt wird, oder wenn der Vorgang fortgesetzt wird, nachdem das System vorübergehend angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-106">Device events can occur while the system is running or when the system resumes operation after temporarily being suspended.</span></span>

<span data-ttu-id="3c2aa-107">Um sicherzustellen, dass Anwendungen keine Daten verlieren, wenn Geräte nicht mehr verfügbar sind, überwacht das System die Hardwarekonfiguration und sendet Geräte Nachrichten an die Anwendungen, um Sie über die Änderungen zu informieren und Ihnen die Möglichkeit zu geben, die Änderungen vorzubereiten, bevor Sie auftreten.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-107">To help ensure that applications do not lose data when devices become unavailable, the system monitors the hardware configuration and sends device messages to the applications to notify them of the changes and to give them the opportunity to prepare for the changes before they occur.</span></span>

<span data-ttu-id="3c2aa-108">Das System überträgt für jedes Geräte Ereignis eine [**WM- \_ devicechange**](wm-devicechange.md) -Nachricht an alle Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-108">For each device event, the system broadcasts a [**WM\_DEVICECHANGE**](wm-devicechange.md) message to all applications.</span></span> <span data-ttu-id="3c2aa-109">In dieser Meldung identifiziert der *wParam* -Parameter den [Geräte Ereignistyp](device-event-types.md) , und der *LPARAM* -Parameter ist ein Zeiger auf ereignisspezifische Daten.</span><span class="sxs-lookup"><span data-stu-id="3c2aa-109">In this message, the *wParam* parameter identifies the [device event type](device-event-types.md) and the *lParam* parameter is a pointer to event-specific data.</span></span>

 

 



