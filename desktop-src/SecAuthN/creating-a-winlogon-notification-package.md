---
description: Ein Winlogon-Benachrichtigungs Paket ist eine DLL, die Funktionen exportiert, die Winlogon-Ereignisse verarbeiten. Wenn sich ein Benutzer beispielsweise beim System anmeldet, ruft Winlogon die Anmelde Ereignishandler-Funktion jedes Benachrichtigungs Pakets auf, um Informationen zum Ereignis bereitzustellen.
ms.assetid: a2a26bac-93b6-4d94-94fc-42c9821935a0
title: Erstellen eines Winlogon-Benachrichtigungs Pakets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0127674967ee3155d42e143a1b142d8c83137c56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359032"
---
# <a name="creating-a-winlogon-notification-package"></a><span data-ttu-id="ace43-104">Erstellen eines Winlogon-Benachrichtigungs Pakets</span><span class="sxs-lookup"><span data-stu-id="ace43-104">Creating a Winlogon Notification Package</span></span>

<span data-ttu-id="ace43-105">Ein [*Winlogon*](/windows/desktop/SecGloss/w-gly) -Benachrichtigungs Paket ist eine DLL, die Funktionen exportiert, die Winlogon-Ereignisse verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="ace43-105">A [*Winlogon*](/windows/desktop/SecGloss/w-gly) notification package is a DLL that exports functions that handle Winlogon events.</span></span> <span data-ttu-id="ace43-106">Wenn sich ein Benutzer beispielsweise beim System anmeldet, ruft Winlogon die Anmelde Ereignishandler-Funktion jedes Benachrichtigungs Pakets auf, um Informationen zum Ereignis bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ace43-106">For example, when a user logs onto the system, Winlogon calls each notification package's logon event handler function to provide information about the event.</span></span>

<span data-ttu-id="ace43-107">Die Namen der in einem Benachrichtigungs Paket implementierten Ereignishandlerfunktionen werden dem Entwickler überlassen. Winlogon überprüft die Registrierung, um die Namen der Ereignishandlerfunktionen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="ace43-107">The names of the event handler functions implemented in a notification package are left up to the developer; Winlogon checks the registry to obtain the names of the event handler functions.</span></span> <span data-ttu-id="ace43-108">Beispielsweise kann ein Benachrichtigungs Paket die LOGON-Ereignishandlerfunktion so implementieren, als `WLEventLogon` wäre andere möglicherweise verwendende `HandleLogonEvent` .</span><span class="sxs-lookup"><span data-stu-id="ace43-108">For example, one notification package might implement the logon event handler function as `WLEventLogon` whereas another might use `HandleLogonEvent`.</span></span>

<span data-ttu-id="ace43-109">Sie müssen für jedes Winlogon-Ereignis keine Ereignishandler implementieren und registrieren, sondern nur für Ereignisse, die für Ihre Anwendung nützlich sind.</span><span class="sxs-lookup"><span data-stu-id="ace43-109">You do not have to implement and register event handlers for every Winlogon event, only for events that are useful to your application.</span></span> <span data-ttu-id="ace43-110">Jede Ereignishandlerfunktion muss den Funktionsprototyp verwenden, der im [Prototyp der Ereignishandler-Funktion](event-handler-function-prototype.md)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="ace43-110">Each event handler function must use the function prototype described in [Event Handler Function Prototype](event-handler-function-prototype.md).</span></span> <span data-ttu-id="ace43-111">Dieser Prototyp verfügt über einen einzelnen Parameter: eine [**wlx- \_ Benachrichtigungs \_ Informations**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) Struktur, die Details zum Ereignis enthält.</span><span class="sxs-lookup"><span data-stu-id="ace43-111">This prototype has a single parameter: a [**WLX\_NOTIFICATION\_INFO**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) structure that contains details about the event.</span></span>

<span data-ttu-id="ace43-112">Winlogon ignoriert die Ausgabe von Ereignishandlerfunktionen.</span><span class="sxs-lookup"><span data-stu-id="ace43-112">Winlogon ignores the output of event handler functions.</span></span> <span data-ttu-id="ace43-113">Wenn die Behandlung eines Ereignisses eine Interaktion mit Winlogon erfordert, verwenden Sie die [Winlogon-Unterstützungsfunktionen](authentication-functions.md).</span><span class="sxs-lookup"><span data-stu-id="ace43-113">If handling an event requires interacting with Winlogon, use the [Winlogon Support Functions](authentication-functions.md).</span></span>

<span data-ttu-id="ace43-114">Um das Winlogon-Benachrichtigungs Paket zu verwenden, muss die dll in den Ordner% SystemRoot% System32 kopiert werden \\ , und für das Benachrichtigungs Paket muss ein Registrierungs Update durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ace43-114">To use your Winlogon notification package, the DLL must be copied to the %SystemRoot%\\system32 folder, and a registry update must be made for the notification package.</span></span> <span data-ttu-id="ace43-115">Weitere Informationen zum Registrierungs Update finden Sie unter [Registrieren eines Winlogon-Benachrichtigungs Pakets](registering-a-winlogon-notification-package.md).</span><span class="sxs-lookup"><span data-stu-id="ace43-115">For information about the registry update, see [Registering a Winlogon Notification Package](registering-a-winlogon-notification-package.md).</span></span>

 

 
