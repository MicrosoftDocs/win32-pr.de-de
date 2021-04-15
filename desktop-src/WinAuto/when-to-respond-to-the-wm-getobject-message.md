---
title: Zeitpunkt der Reaktion auf die WM_GETOBJECT Nachricht
description: Wenn eine Anwendung Microsoft Active Accessibility oder Benutzeroberflächen Automatisierung für ein UI-Element unterstützt, darf die Anwendung nicht auf die WM- \_ GetObject-Nachricht reagieren, bevor das Objekt, das das UI-Element darstellt, vollständig initialisiert ist oder nachdem die Anwendung geschlossen wurde.
ms.assetid: cc99f7ef-1eb6-40c4-9ec0-8fb18cb4a3e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18cfa8d6604a13e84ffa89bf1fcf93d5d13e66e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473949"
---
# <a name="when-to-respond-to-the-wm_getobject-message"></a><span data-ttu-id="aefda-103">Antworten auf die WM- \_ GetObject-Nachricht</span><span class="sxs-lookup"><span data-stu-id="aefda-103">When to Respond to the WM\_GETOBJECT Message</span></span>

<span data-ttu-id="aefda-104">Wenn eine Anwendung Microsoft Active Accessibility oder Benutzeroberflächen Automatisierung für ein UI-Element unterstützt, darf die Anwendung nicht auf die [**WM- \_ GetObject**](wm-getobject.md) -Nachricht reagieren, bevor das Objekt, das das UI-Element darstellt, vollständig initialisiert ist oder nachdem die Anwendung geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="aefda-104">If an application supports Microsoft Active Accessibility or UI Automation for a UI element, the application must not respond to the [**WM\_GETOBJECT**](wm-getobject.md) message before the object that represents the UI element is fully initialized, or after the application has begun to close.</span></span> <span data-ttu-id="aefda-105">Wenn eine Anwendung ein neues Fenster erstellt, löst das System das [**Ereignis \_ Objekt \_ Create**](event-constants.md) WinEvent aus, um Clients zu benachrichtigen, bevor die [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Nachricht an die Fenster Prozedur der Anwendung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="aefda-105">When an application creates a new window, the system raises the [**EVENT\_OBJECT\_CREATE**](event-constants.md) WinEvent to notify clients before sending the [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message to the application's window procedure.</span></span> <span data-ttu-id="aefda-106">Da viele Anwendungen **WM \_ Create** verwenden, um den Initialisierungs Prozess zu starten, antwortet jede Barrierefreiheits Implementierung eines UI-Elements erst, nachdem die Anwendung die Verarbeitung der **WM \_ Create** [**-Nachricht abgeschlossen \_**](wm-getobject.md) hat.</span><span class="sxs-lookup"><span data-stu-id="aefda-106">Because many applications use **WM\_CREATE** to start the initialization process, any accessibility implementation of a UI element does not respond to the [**WM\_GETOBJECT**](wm-getobject.md) message until after the application has finished processing the **WM\_CREATE** message.</span></span>

 

 