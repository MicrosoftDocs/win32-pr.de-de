---
description: Die folgenden Funktionen werden von Zeit Anbietern verwendet.
ms.assetid: 05687a67-4e0b-4a44-9c2d-7e097be9008c
title: Zeit Anbieter Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a24f15bd67751dc09a689078a8a518224267c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352621"
---
# <a name="time-provider-functions"></a><span data-ttu-id="559dd-103">Zeit Anbieter Funktionen</span><span class="sxs-lookup"><span data-stu-id="559dd-103">Time Provider Functions</span></span>

<span data-ttu-id="559dd-104">Die folgenden Funktionen werden von Zeit Anbietern verwendet.</span><span class="sxs-lookup"><span data-stu-id="559dd-104">The following functions are used by time providers.</span></span>



| <span data-ttu-id="559dd-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="559dd-105">Function</span></span>                                                               | <span data-ttu-id="559dd-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="559dd-106">Description</span></span>                                                                                            |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="559dd-107">**Alertsamplesavailfunc**</span><span class="sxs-lookup"><span data-stu-id="559dd-107">**AlertSamplesAvailFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)                     | <span data-ttu-id="559dd-108">Benachrichtigt das System, dass neue Beispiele vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="559dd-108">Notifies the system that there are new samples available.</span></span>                                              |
| [<span data-ttu-id="559dd-109">**Gettimesysinfofunc**</span><span class="sxs-lookup"><span data-stu-id="559dd-109">**GetTimeSysInfoFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)                           | <span data-ttu-id="559dd-110">Ruft die Systemzeit Zustandsinformationen ab.</span><span class="sxs-lookup"><span data-stu-id="559dd-110">Retrieves the system time state information.</span></span>                                                           |
| [<span data-ttu-id="559dd-111">**Logtimeproveventfunc**</span><span class="sxs-lookup"><span data-stu-id="559dd-111">**LogTimeProvEventFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)                       | <span data-ttu-id="559dd-112">Protokolliert ein Zeit Anbieter Ereignis im Ereignisprotokoll.</span><span class="sxs-lookup"><span data-stu-id="559dd-112">Logs a time provider event in the event log.</span></span>                                                           |
| [<span data-ttu-id="559dd-113">**Setproviderstatus-Func**</span><span class="sxs-lookup"><span data-stu-id="559dd-113">**SetProviderStatusFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusfunc)                 | <span data-ttu-id="559dd-114">Legt die Statusinformationen des Zeit Anbieters fest.</span><span class="sxs-lookup"><span data-stu-id="559dd-114">Sets the time provider's status information.</span></span>                                                           |
| [<span data-ttu-id="559dd-115">**Setproviderstatusinfofreifunc**</span><span class="sxs-lookup"><span data-stu-id="559dd-115">**SetProviderStatusInfoFreeFunc**</span></span>](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusinfofreefunc) | <span data-ttu-id="559dd-116">Gibt eine [**setproviderstatusinfo**](/windows/desktop/api/Timeprov/ns-timeprov-setproviderstatusinfo) -Struktur frei.</span><span class="sxs-lookup"><span data-stu-id="559dd-116">Frees a [**SetProviderStatusInfo**](/windows/desktop/api/Timeprov/ns-timeprov-setproviderstatusinfo) structure.</span></span>                          |
| [<span data-ttu-id="559dd-117">**Timeprovclose**</span><span class="sxs-lookup"><span data-stu-id="559dd-117">**TimeProvClose**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)                                 | <span data-ttu-id="559dd-118">Eine Rückruffunktion, die vom Zeit Anbieter-Manager zum Herunterfahren des Zeit Anbieters aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="559dd-118">A callback function that is called by the time provider manager to shut down the time provider.</span></span>        |
| [<span data-ttu-id="559dd-119">**Timeprovcommand**</span><span class="sxs-lookup"><span data-stu-id="559dd-119">**TimeProvCommand**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)                             | <span data-ttu-id="559dd-120">Eine Rückruffunktion, die vom Zeit Anbieter-Manager zum Senden von Befehlen an den Zeit Anbieter aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="559dd-120">A callback function that is called by the time provider manager to send commands to the time provider.</span></span> |
| [<span data-ttu-id="559dd-121">**Timeprovopen**</span><span class="sxs-lookup"><span data-stu-id="559dd-121">**TimeProvOpen**</span></span>](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)                                   | <span data-ttu-id="559dd-122">Eine Rückruffunktion, die vom Zeit Anbieter-Manager aufgerufen wird, wenn die Zeit Anbieter-DLL geladen wird.</span><span class="sxs-lookup"><span data-stu-id="559dd-122">A callback function that is called by the time provider manager when the time provider DLL is loaded.</span></span>  |



 

 

 



