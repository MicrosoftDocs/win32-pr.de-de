---
title: Funktionen für die Anwendungs Wiederherstellung und Neustart
description: 'Anwendungs Wiederherstellung und Neustart definiert die folgenden Funktionen:'
ms.assetid: 17de24d1-32fe-4b2d-a224-3730af73c892
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f9f5fb41f2ef694b4d99044a8756ff0bb66c3f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102035"
---
# <a name="application-recovery-and-restart-functions"></a><span data-ttu-id="d8570-103">Funktionen für die Anwendungs Wiederherstellung und Neustart</span><span class="sxs-lookup"><span data-stu-id="d8570-103">Application Recovery and Restart Functions</span></span>

<span data-ttu-id="d8570-104">Anwendungs Wiederherstellung und Neustart definiert die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="d8570-104">Application Recovery and Restart defines the following functions:</span></span>



| <span data-ttu-id="d8570-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="d8570-105">Function</span></span>                                                                               | <span data-ttu-id="d8570-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d8570-106">Description</span></span>                                                                                |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d8570-107">**Applicationwiederherstellungsfertig**</span><span class="sxs-lookup"><span data-stu-id="d8570-107">**ApplicationRecoveryFinished**</span></span>](/windows/win32/api/winbase/nf-winbase-applicationrecoveryfinished)                     | <span data-ttu-id="d8570-108">Gibt an, dass die aufrufenden Anwendung die Datenwiederherstellung abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="d8570-108">Indicates that the calling application has completed its data recovery.</span></span>                    |
| [<span data-ttu-id="d8570-109">**Applicationwiederherstellungsinprogress**</span><span class="sxs-lookup"><span data-stu-id="d8570-109">**ApplicationRecoveryInProgress**</span></span>](/windows/win32/api/winbase/nf-winbase-applicationrecoveryinprogress)                 | <span data-ttu-id="d8570-110">Gibt an, dass die aufrufende Anwendung weiterhin Daten wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="d8570-110">Indicates that the calling application is continuing to recover data.</span></span>                      |
| [<span data-ttu-id="d8570-111">**Getapplicationwiederherstellungsrückruf**</span><span class="sxs-lookup"><span data-stu-id="d8570-111">**GetApplicationRecoveryCallback**</span></span>](/windows/win32/api/winbase/nf-winbase-getapplicationrecoverycallback)               | <span data-ttu-id="d8570-112">Ruft einen Zeiger auf die Wiederherstellungs Rückruf Routine ab, die für den angegebenen Prozess registriert ist.</span><span class="sxs-lookup"><span data-stu-id="d8570-112">Retrieves a pointer to the recovery callback routine registered for the specified process.</span></span> |
| [<span data-ttu-id="d8570-113">**Getapplicationrestartsettings**</span><span class="sxs-lookup"><span data-stu-id="d8570-113">**GetApplicationRestartSettings**</span></span>](/windows/win32/api/winbase/nf-winbase-getapplicationrestartsettings)                 | <span data-ttu-id="d8570-114">Ruft die für den angegebenen Prozess registrierten Neustart Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="d8570-114">Retrieves the restart information registered for the specified process.</span></span>                    |
| [<span data-ttu-id="d8570-115">**Registerapplicationwiederherstellungsrückruf**</span><span class="sxs-lookup"><span data-stu-id="d8570-115">**RegisterApplicationRecoveryCallback**</span></span>](/windows/win32/api/winbase/nf-winbase-registerapplicationrecoverycallback)     | <span data-ttu-id="d8570-116">Registriert die aktive Instanz einer Anwendung für die Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="d8570-116">Registers the active instance of an application for recovery.</span></span>                              |
| [<span data-ttu-id="d8570-117">**RegisterApplicationRestart**</span><span class="sxs-lookup"><span data-stu-id="d8570-117">**RegisterApplicationRestart**</span></span>](/windows/win32/api/winbase/nf-winbase-registerapplicationrestart)                       | <span data-ttu-id="d8570-118">Registriert die aktive Instanz einer Anwendung für den Neustart.</span><span class="sxs-lookup"><span data-stu-id="d8570-118">Registers the active instance of an application for restart.</span></span>                               |
| [<span data-ttu-id="d8570-119">**Unregisterapplicationwiederherstellungsrückruf**</span><span class="sxs-lookup"><span data-stu-id="d8570-119">**UnregisterApplicationRecoveryCallback**</span></span>](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrecoverycallback) | <span data-ttu-id="d8570-120">Entfernt die aktive Instanz einer Anwendung aus der Wiederherstellungs Liste.</span><span class="sxs-lookup"><span data-stu-id="d8570-120">Removes the active instance of an application from the recovery list.</span></span>                      |
| [<span data-ttu-id="d8570-121">**Unregisterapplicationrestart**</span><span class="sxs-lookup"><span data-stu-id="d8570-121">**UnregisterApplicationRestart**</span></span>](/windows/win32/api/winbase/nf-winbase-unregisterapplicationrestart)                   | <span data-ttu-id="d8570-122">Entfernt die aktive Instanz einer Anwendung aus der Neustart Liste.</span><span class="sxs-lookup"><span data-stu-id="d8570-122">Removes the active instance of an application from the restart list.</span></span>                       |



 

 

 