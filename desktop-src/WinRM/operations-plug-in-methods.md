---
title: Vorgangs-Plug-in-Methoden
description: Vorgangs-Plug-in-Methoden
ms.assetid: 81fe751f-51fd-4da6-b44a-0af9007eea9a
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff64a53c4c63b9e552efe90ac057b8a31d603b64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947292"
---
# <a name="operations-plug-in-methods"></a><span data-ttu-id="d9b0b-103">Vorgangs-Plug-in-Methoden</span><span class="sxs-lookup"><span data-stu-id="d9b0b-103">Operations Plug-in Methods</span></span>

<span data-ttu-id="d9b0b-104">Alle Vorgänge Plug-in-Einstiegspunkte verfügen über einen Rückrufmechanismus, um den Erfolg oder Misserfolg des Aufrufs zu melden.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-104">All operations plug-in entry points have a callback mechanism to report the success or failure of the call.</span></span> <span data-ttu-id="d9b0b-105">Einige Rückruf Mechanismen werden mehrmals aufgerufen, bis alle Ergebnisse gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-105">Some callback mechanisms are called multiple times, until all of the results are reported.</span></span>

<span data-ttu-id="d9b0b-106">In der folgenden Tabelle finden Sie eine Übersicht über die Vorgangs Rückruf Methoden.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-106">The following table provides an overview of the operations callback methods.</span></span>



| <span data-ttu-id="d9b0b-107">Methode</span><span class="sxs-lookup"><span data-stu-id="d9b0b-107">Method</span></span>                                                                         | <span data-ttu-id="d9b0b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9b0b-108">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d9b0b-109">**Wsmanpluginfreerequestdetails**</span><span class="sxs-lookup"><span data-stu-id="d9b0b-109">**WSManPluginFreeRequestDetails**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginfreerequestdetails)         | <span data-ttu-id="d9b0b-110">Gibt Arbeitsspeicher frei, der der [**WSMAN-Plug-in- \_ \_ Anforderungs**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request) Struktur zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-110">Releases memory that is allocated for the [**WSMAN\_PLUGIN\_REQUEST**](/windows/desktop/api/Wsman/ns-wsman-wsman_plugin_request) structure.</span></span>                                          |
| [<span data-ttu-id="d9b0b-111">**Wsmanplugingetoperationparameters**</span><span class="sxs-lookup"><span data-stu-id="d9b0b-111">**WSManPluginGetOperationParameters**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanplugingetoperationparameters) | <span data-ttu-id="d9b0b-112">Ruft Betriebsinformationen ab, z. b. Timeouts und Daten Einschränkungen, die einem Vorgang zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-112">Gets operational information, such as time-outs and data restrictions that are associated with an operation.</span></span>                                         |
| [<span data-ttu-id="d9b0b-113">**Wsmanpluginoperationcomplete**</span><span class="sxs-lookup"><span data-stu-id="d9b0b-113">**WSManPluginOperationComplete**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginoperationcomplete)           | <span data-ttu-id="d9b0b-114">Zeichnet den Abschluss eines Vorgangs auf.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-114">Records the completion of an operation.</span></span>                                                                                                              |
| [<span data-ttu-id="d9b0b-115">**Wsmanpluginreceiveresult**</span><span class="sxs-lookup"><span data-stu-id="d9b0b-115">**WSManPluginReceiveResult**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreceiveresult)                   | <span data-ttu-id="d9b0b-116">Meldet Ergebnisse an Windows-Remoteverwaltung (WinRM)-Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-116">Reports results to Windows Remote Management (WinRM) plug-ins.</span></span>                                                                                       |
| [<span data-ttu-id="d9b0b-117">**Wsmanpluginreportcontext**</span><span class="sxs-lookup"><span data-stu-id="d9b0b-117">**WSManPluginReportContext**</span></span>](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginreportcontext)                   | <span data-ttu-id="d9b0b-118">Meldet die Shell und den Befehls Kontext zurück zur WinRM-Infrastruktur, sodass weitere Vorgänge für die Shell und/oder den Befehl ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="d9b0b-118">Reports the shell and command context back to the WinRM infrastructure so that further operations can be performed against the shell and/or command.</span></span> |



 

 

 




