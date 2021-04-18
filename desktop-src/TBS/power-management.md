---
title: Energie Verwaltung (TPM-Basisdienste)
description: Die TSB empfängt Energie Verwaltungs Ereignisse.
ms.assetid: 21f76bea-a313-46b7-99b3-422f17376a5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e21f2c6a2292b7d49fae3b15691703fa34667a
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2019
ms.locfileid: "106339037"
---
# <a name="power-management-tpm-base-services"></a><span data-ttu-id="8487f-103">Energie Verwaltung (TPM-Basisdienste)</span><span class="sxs-lookup"><span data-stu-id="8487f-103">Power Management (TPM Base Services)</span></span>

<span data-ttu-id="8487f-104">Die TSB empfängt Energie Verwaltungs Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="8487f-104">The TBS receives power management events.</span></span> <span data-ttu-id="8487f-105">Wenn ein Hinweis darauf eingeht, dass das TPM oder andere Teile der Plattform in einen Energiezustand eintreten werden, in dem die Ausführung unterbrochen wird oder der TPM-Status verloren geht, prüft die TSB, ob der aktuell ausgeführte Befehl wahrscheinlich abgeschlossen ist, bevor das System ausfällt.</span><span class="sxs-lookup"><span data-stu-id="8487f-105">When an indication is received that the TPM or other parts of the platform are about to enter a power state in which execution will be interrupted or TPM state will be lost, the TBS checks to determine whether the currently executing command is likely to finish before the system powers down.</span></span> <span data-ttu-id="8487f-106">Im allgemeinen ermöglicht die TSB die Fertigstellung von Befehlen für kurze und mittlere Dauer, bricht jedoch Befehle mit langer Ausführungsdauer ab.</span><span class="sxs-lookup"><span data-stu-id="8487f-106">In general, the TBS allows short and medium duration commands to finish, but cancels long duration commands.</span></span> <span data-ttu-id="8487f-107">Nachdem der Befehl zurückgegeben wurde, sendet der TSB keine neuen Befehle an das TPM und bereitet sich selbst auf den Ruhezustand vor.</span><span class="sxs-lookup"><span data-stu-id="8487f-107">After the command has returned, the TBS stops sending new commands to the TPM and prepares itself for hibernation.</span></span> <span data-ttu-id="8487f-108">Wenn die Stromversorgung wieder hergestellt wird, gibt die TSB das Ergebnis des Befehls an den Aufrufer zurück und fährt dann mit der Verarbeitung ausstehender TSB-Befehle fort.</span><span class="sxs-lookup"><span data-stu-id="8487f-108">When power is restored, the TBS returns the result of the command to the caller, and then proceeds with processing pending TBS commands.</span></span> <span data-ttu-id="8487f-109">Der TSB-Energie Verwaltungs Code wird asynchron ausgeführt, sodass Energie Verwaltungsanforderungen verarbeitet werden können, auch wenn das TPM einen langen Befehl verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="8487f-109">The TBS power management code runs asynchronously, so it can handle power management requests even if the TPM is processing a long command.</span></span>

<span data-ttu-id="8487f-110">Wenn ein Computer in den Standbymodus wechselt, einschließlich S3 (Standby) und S4 (Ruhezustand), wird das TPM ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="8487f-110">When a computer enters sleep states, including S3 (sleep) and S4 (hibernation), the TPM is powered off.</span></span> <span data-ttu-id="8487f-111">Daher gehen alle nicht persistenten TPM-Zustände verloren.</span><span class="sxs-lookup"><span data-stu-id="8487f-111">Thus, all nonpersistent TPM states are lost.</span></span> <span data-ttu-id="8487f-112">Vor der Eingabe dieser Zustände wird erwartet, dass sich die Anwendungssoftware auf den Verlust flüchtiger TPM-Zustände vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="8487f-112">Before entering these states, application software is expected to prepare for the loss of volatile TPM states.</span></span> <span data-ttu-id="8487f-113">Wenn das System aus dem Ruhezustand zurückkehrt, wird die TSB mit dem TPM synchronisiert, sodass der TSB-Status mit dem TPM-Status konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="8487f-113">When the system returns from a sleep state, the TBS synchronizes with the TPM so that the TBS state is consistent with the TPM state.</span></span> <span data-ttu-id="8487f-114">Möglicherweise müssen von der Anwendungssoftware nicht unterbrochene Befehle neu ausgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8487f-114">Application software may need to reissue commands that were interrupted.</span></span>

 

 




