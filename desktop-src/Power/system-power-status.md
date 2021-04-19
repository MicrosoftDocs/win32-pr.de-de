---
description: Der System Energiestatus gibt an, ob die Stromversorgung eines Computers eine System Batterie oder eine Stromversorgung ist. Bei Computern, die Akkus verwenden, gibt der System Energiestatus auch an, wie viel Akku Lebensdauer verbleiben und ob der Akku belastet wird.
ms.assetid: b9a5e7de-a603-4bd9-b854-1e58572c3b2b
title: System Energie Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e221142b5d39a4cb5bc49dbe85271c99837d0a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356160"
---
# <a name="system-power-status"></a><span data-ttu-id="94493-104">System Energie Status</span><span class="sxs-lookup"><span data-stu-id="94493-104">System Power Status</span></span>

<span data-ttu-id="94493-105">Der System Energiestatus gibt an, ob die Stromversorgung eines Computers eine System Batterie oder eine Stromversorgung ist.</span><span class="sxs-lookup"><span data-stu-id="94493-105">The system power status indicates whether the source of power for a computer is a system battery or AC power.</span></span> <span data-ttu-id="94493-106">Bei Computern, die Akkus verwenden, gibt der System Energiestatus auch an, wie viel Akku Lebensdauer verbleiben und ob der Akku belastet wird.</span><span class="sxs-lookup"><span data-stu-id="94493-106">For computers that use batteries, the system power status also indicates how much battery life remains and whether the battery is charging.</span></span>

<span data-ttu-id="94493-107">Energieinformationen werden abgerufen, indem Sie über die [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) -Funktion für Energie Einstellungs Benachrichtigungen registriert werden.</span><span class="sxs-lookup"><span data-stu-id="94493-107">Power information is retrieved by registering for power setting notifications through the [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) function.</span></span> <span data-ttu-id="94493-108">Diese Funktion ermöglicht es Anwendungen, sich für bestimmte Energie Einstellungen zu registrieren und benachrichtigt zu werden, wenn Sie sich ändern.</span><span class="sxs-lookup"><span data-stu-id="94493-108">This function allows applications to register for specific power settings and be notified when they change.</span></span>

> [!Note]  
> <span data-ttu-id="94493-109">Verwenden Sie [**callntpowerinformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation), um Energiestatus Informationen ohne Benachrichtigungen abzufragen.</span><span class="sxs-lookup"><span data-stu-id="94493-109">To query for power status information without notifications, use [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation).</span></span>

 

<span data-ttu-id="94493-110">Anwendungen und installierbare Treiber verwenden normalerweise den System Energiestatus, um zu bestimmen, ob ein fortgesetzter Vorgang möglich ist.</span><span class="sxs-lookup"><span data-stu-id="94493-110">Applications and installable drivers typically use the system power status to determine whether continued operation is feasible.</span></span> <span data-ttu-id="94493-111">Bevor eine Anwendung z. b. Hintergrund Vorgänge durchführt, z. b. das komprimieren oder Paginieren einer Datei, sollte überprüft werden, ob es sich um ein System mit Batterien handelt.</span><span class="sxs-lookup"><span data-stu-id="94493-111">For example, before an application performs background operations such as compressing or paginating a file, it should check whether the system is on batteries.</span></span> <span data-ttu-id="94493-112">Ein weiteres Beispiel: eine Anwendung, die einen langwierigen Vorgang startet, sollte den Status überprüfen, um zu ermitteln, ob genügend Akkuleistung vorhanden ist, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="94493-112">As another example, an application that is beginning a lengthy operation should check the status to determine whether enough battery power exists to complete the operation.</span></span>

<span data-ttu-id="94493-113">Standardmäßig werden Anwendungen oder Treiber während des standbyübergangs vom System nicht abgefragt.</span><span class="sxs-lookup"><span data-stu-id="94493-113">By default, the system does not query applications or drivers during sleep transitions.</span></span>

> [!Note]  
> <span data-ttu-id="94493-114">Wenn die Stromversorgung gering ist, kann eine Anwendung einen Benutzereingriff anfordern oder anfordern, dass das System sich selbst anhält.</span><span class="sxs-lookup"><span data-stu-id="94493-114">If power is low, an application can request user intervention or request that the system suspend itself.</span></span> <span data-ttu-id="94493-115">Sie können den Systembetrieb mithilfe der [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) -Funktion aussetzen.</span><span class="sxs-lookup"><span data-stu-id="94493-115">You can suspend system operation by using the [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="94493-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="94493-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94493-117">Informationen zur Energie Verwaltung</span><span class="sxs-lookup"><span data-stu-id="94493-117">About Power Management</span></span>](about-power-management.md)
</dt> </dl>

 

 



