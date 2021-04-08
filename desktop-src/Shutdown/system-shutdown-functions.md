---
description: Die folgenden Funktionen werden mit dem Herunterfahren des Systems verwendet.
ms.assetid: 6a08a769-1acf-49eb-ba95-beaf56a374bf
title: SystemShutdown-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd457c86129b3e5f80d6359018c1474f837b9e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959856"
---
# <a name="system-shutdown-functions"></a><span data-ttu-id="5fb4d-103">SystemShutdown-Funktionen</span><span class="sxs-lookup"><span data-stu-id="5fb4d-103">System Shutdown Functions</span></span>

<span data-ttu-id="5fb4d-104">Die folgenden Funktionen werden mit dem Herunterfahren des Systems verwendet.</span><span class="sxs-lookup"><span data-stu-id="5fb4d-104">The following functions are used with system shutdown.</span></span>



| <span data-ttu-id="5fb4d-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="5fb4d-105">Function</span></span>                                                         | <span data-ttu-id="5fb4d-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fb4d-106">Description</span></span>                                                                                                                         |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5fb4d-107">**Abortsystemshutdown**</span><span class="sxs-lookup"><span data-stu-id="5fb4d-107">**AbortSystemShutdown**</span></span>](/windows/desktop/api/Winreg/nf-winreg-abortsystemshutdowna)               | <span data-ttu-id="5fb4d-108">Beendet das Herunterfahren eines Systems, das initiiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5fb4d-108">Stops a system shutdown that has been initiated.</span></span>                                                                                    |
| [<span data-ttu-id="5fb4d-109">**Exitwindows**</span><span class="sxs-lookup"><span data-stu-id="5fb4d-109">**ExitWindows**</span></span>](/windows/desktop/api/Winuser/nf-winuser-exitwindows)                               | <span data-ttu-id="5fb4d-110">Protokolliert den interaktiven Benutzer.</span><span class="sxs-lookup"><span data-stu-id="5fb4d-110">Logs off the interactive user.</span></span>                                                                                                      |
| [<span data-ttu-id="5fb4d-111">**ExitWindowsEx**</span><span class="sxs-lookup"><span data-stu-id="5fb4d-111">**ExitWindowsEx**</span></span>](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex)                           | <span data-ttu-id="5fb4d-112">Hiermit wird der interaktive Benutzer protokolliert, das System heruntergefahren oder das System heruntergefahren und neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="5fb4d-112">Logs off the interactive user, shuts down the system, or shuts down and restarts the system.</span></span>                                        |
| [<span data-ttu-id="5fb4d-113">**InitiateShutdown**</span><span class="sxs-lookup"><span data-stu-id="5fb4d-113">**InitiateShutdown**</span></span>](/windows/desktop/api/Winreg/nf-winreg-initiateshutdowna)                     | <span data-ttu-id="5fb4d-114">Initiiert das Herunterfahren und Neustarten des angegebenen Computers und startet alle Anwendungen neu, die für den Neustart registriert wurden.</span><span class="sxs-lookup"><span data-stu-id="5fb4d-114">Initiates a shutdown and restart of the specified computer, and restarts any applications that have been registered for restart.</span></span>    |
| [<span data-ttu-id="5fb4d-115">**InitiateSystemShutdown**</span><span class="sxs-lookup"><span data-stu-id="5fb4d-115">**InitiateSystemShutdown**</span></span>](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdowna)         | <span data-ttu-id="5fb4d-116">Initiiert ein Herunterfahren und einen optionalen Neustart des angegebenen Computers.</span><span class="sxs-lookup"><span data-stu-id="5fb4d-116">Initiates a shutdown and optional restart of the specified computer.</span></span>                                                                |
| [<span data-ttu-id="5fb4d-117">**Initiatesystemshutdownetx**</span><span class="sxs-lookup"><span data-stu-id="5fb4d-117">**InitiateSystemShutdownEx**</span></span>](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa)     | <span data-ttu-id="5fb4d-118">Initiiert ein Herunterfahren und einen optionalen Neustart des angegebenen Computers und zeichnet optional den Grund für das Herunterfahren auf.</span><span class="sxs-lookup"><span data-stu-id="5fb4d-118">Initiates a shutdown and optional restart of the specified computer, and optionally records the reason for the shutdown.</span></span>            |
| [<span data-ttu-id="5fb4d-119">**Lock Workstation**</span><span class="sxs-lookup"><span data-stu-id="5fb4d-119">**LockWorkStation**</span></span>](/windows/desktop/api/Winuser/nf-winuser-lockworkstation)                       | <span data-ttu-id="5fb4d-120">Sperrt die Anzeige der Arbeitsstation.</span><span class="sxs-lookup"><span data-stu-id="5fb4d-120">Locks the workstation's display.</span></span>                                                                                                    |
| [<span data-ttu-id="5fb4d-121">**Shutdownblockreasoncreate**</span><span class="sxs-lookup"><span data-stu-id="5fb4d-121">**ShutdownBlockReasonCreate**</span></span>](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate)   | <span data-ttu-id="5fb4d-122">Gibt an, dass das System nicht heruntergefahren werden kann, und legt eine Grund Zeichenfolge fest, die dem Benutzer angezeigt wird, wenn das System heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="5fb4d-122">Indicates that the system cannot be shut down and sets a reason string to be displayed to the user if system shutdown is initiated.</span></span> |
| [<span data-ttu-id="5fb4d-123">**Shutdownblockreasondestroy**</span><span class="sxs-lookup"><span data-stu-id="5fb4d-123">**ShutdownBlockReasonDestroy**</span></span>](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasondestroy) | <span data-ttu-id="5fb4d-124">Gibt an, dass das System heruntergefahren werden kann, und gibt die Grund Zeichenfolge frei.</span><span class="sxs-lookup"><span data-stu-id="5fb4d-124">Indicates that the system can be shut down and frees the reason string.</span></span>                                                             |
| [<span data-ttu-id="5fb4d-125">**Shutdownblockreasonquery**</span><span class="sxs-lookup"><span data-stu-id="5fb4d-125">**ShutdownBlockReasonQuery**</span></span>](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasonquery)     | <span data-ttu-id="5fb4d-126">Ruft die von der [**shutdownblockreasoncreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) -Funktion festgelegte Grund Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="5fb4d-126">Retrieves the reason string set by the [**ShutdownBlockReasonCreate**](/windows/desktop/api/Winuser/nf-winuser-shutdownblockreasoncreate) function.</span></span>                     |



 

 

 



