---
description: Weitere Informationen finden Sie in den System Parametern für Extensible Storage Engine.
title: System Parameter für Extensible Storage Engine
TOCTitle: Extensible Storage Engine System Parameters
ms:assetid: f95c2e87-b25e-4be5-8c17-8486ba37dad4
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294139(v=EXCHG.10)
ms:contentKeyID: 32765753
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 43473f1bf5f599ba8efd06bd31345485acc07061
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527989"
---
# <a name="extensible-storage-engine-system-parameters"></a><span data-ttu-id="13b61-103">System Parameter für Extensible Storage Engine</span><span class="sxs-lookup"><span data-stu-id="13b61-103">Extensible Storage Engine System Parameters</span></span>


<span data-ttu-id="13b61-104">_**Gilt für:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="13b61-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-system-parameters"></a><span data-ttu-id="13b61-105">System Parameter für Extensible Storage Engine</span><span class="sxs-lookup"><span data-stu-id="13b61-105">Extensible Storage Engine System Parameters</span></span>

<span data-ttu-id="13b61-106">Die folgenden Konstanten werden als Werte für den *paramID* -Parameter der Funktionen [jetgetsystemparameter](./jetgetsystemparameter-function.md) und [jetsetsystemparameter](./jetsetsystemparameter-function.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="13b61-106">The following constants are used as values for the *paramid* parameter of the [JetGetSystemParameter](./jetgetsystemparameter-function.md) and [JetSetSystemParameter](./jetsetsystemparameter-function.md) functions.</span></span>

  - [<span data-ttu-id="13b61-107">Sicherungs-und Wiederherstellungs Parameter</span><span class="sxs-lookup"><span data-stu-id="13b61-107">Backup and Restore Parameters</span></span>](./backup-and-restore-parameters.md)

  - [<span data-ttu-id="13b61-108">Rückruf Parameter</span><span class="sxs-lookup"><span data-stu-id="13b61-108">Callback Parameters</span></span>](./callback-parameters.md)

  - [<span data-ttu-id="13b61-109">Datenbankparameter</span><span class="sxs-lookup"><span data-stu-id="13b61-109">Database Parameters</span></span>](./database-parameters.md)

  - [<span data-ttu-id="13b61-110">Daten Bank Cache Parameter</span><span class="sxs-lookup"><span data-stu-id="13b61-110">Database Cache Parameters</span></span>](./database-cache-parameters.md)

  - [<span data-ttu-id="13b61-111">Fehler Behandlungsparameter</span><span class="sxs-lookup"><span data-stu-id="13b61-111">Error Handling Parameters</span></span>](./error-handling-parameters.md)

  - [<span data-ttu-id="13b61-112">Ereignisprotokoll Parameter</span><span class="sxs-lookup"><span data-stu-id="13b61-112">Event Log Parameters</span></span>](./event-log-parameters.md)

  - [<span data-ttu-id="13b61-113">I/O-Parameter</span><span class="sxs-lookup"><span data-stu-id="13b61-113">I/O Parameters</span></span>](./i-o-parameters.md)

  - [<span data-ttu-id="13b61-114">Indexparameter</span><span class="sxs-lookup"><span data-stu-id="13b61-114">Index Parameters</span></span>](./index-parameters.md)

  - [<span data-ttu-id="13b61-115">Informations Parameter</span><span class="sxs-lookup"><span data-stu-id="13b61-115">Informational Parameters</span></span>](./informational-parameters.md)

  - [<span data-ttu-id="13b61-116">Meta-Parameter</span><span class="sxs-lookup"><span data-stu-id="13b61-116">Meta Parameters</span></span>](./meta-parameters.md)

  - [<span data-ttu-id="13b61-117">Ressourcenparameter</span><span class="sxs-lookup"><span data-stu-id="13b61-117">Resource Parameters</span></span>](./resource-parameters.md)

  - [<span data-ttu-id="13b61-118">Temporäre Daten Bank Parameter</span><span class="sxs-lookup"><span data-stu-id="13b61-118">Temporary Database Parameters</span></span>](./temporary-database-parameters.md)

  - [<span data-ttu-id="13b61-119">Transaktionsprotokollparameters</span><span class="sxs-lookup"><span data-stu-id="13b61-119">Transaction Log Parameters</span></span>](./transaction-log-parameters.md)

### <a name="system-parameter-description-format"></a><span data-ttu-id="13b61-120">Systemparameterbeschreibungs-Format</span><span class="sxs-lookup"><span data-stu-id="13b61-120">System Parameter Description Format</span></span>

<span data-ttu-id="13b61-121">Jeder Systemparameter wird im folgenden Format beschrieben:</span><span class="sxs-lookup"><span data-stu-id="13b61-121">Each system parameter will be described using the following format:</span></span>

<span data-ttu-id="13b61-122">JET_paramX</span><span class="sxs-lookup"><span data-stu-id="13b61-122">JET_paramX</span></span>

<span data-ttu-id="13b61-123">Die Beschreibung des JET_paramX System Parameters.</span><span class="sxs-lookup"><span data-stu-id="13b61-123">Description of the JET_paramX system parameter.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="13b61-124">Standardwert:</span><span class="sxs-lookup"><span data-stu-id="13b61-124">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="13b61-125">Der Standardwert des Parameters.</span><span class="sxs-lookup"><span data-stu-id="13b61-125">The default value of the parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13b61-126">Typ:</span><span class="sxs-lookup"><span data-stu-id="13b61-126">Type:</span></span></p></td>
<td><p><span data-ttu-id="13b61-127">Der Datentyp des Parameters.</span><span class="sxs-lookup"><span data-stu-id="13b61-127">The data type of the parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13b61-128">Gültiger Bereich:</span><span class="sxs-lookup"><span data-stu-id="13b61-128">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="13b61-129">Die zulässigen Werte für den Parameter.</span><span class="sxs-lookup"><span data-stu-id="13b61-129">The legal values for the parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13b61-130">Umfang:</span><span class="sxs-lookup"><span data-stu-id="13b61-130">Scope:</span></span></p></td>
<td><p><span data-ttu-id="13b61-131">Ist der Parameter Global oder pro Instanz?</span><span class="sxs-lookup"><span data-stu-id="13b61-131">Is the parameter Global or per Instance?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13b61-132">Nach <a href="gg269354(v=exchg.10).md">jetkreateinstance</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="13b61-132">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="13b61-133">Kann der Parameter festgelegt werden, wenn Instanzen vorhanden sind?</span><span class="sxs-lookup"><span data-stu-id="13b61-133">Can the parameter be set if any instances exist?</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13b61-134">Nach <a href="gg294068(v=exchg.10).md">jetinit</a>festlegen:</span><span class="sxs-lookup"><span data-stu-id="13b61-134">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="13b61-135">Kann der Parameter bei der Initialisierung festgelegt werden?</span><span class="sxs-lookup"><span data-stu-id="13b61-135">Can the parameter be set when initialized?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13b61-136">Hat Auswirkungen auf das physische Layout:</span><span class="sxs-lookup"><span data-stu-id="13b61-136">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="13b61-137">Wirkt sich der Parameter auf die Dateien auf dem Datenträger aus?</span><span class="sxs-lookup"><span data-stu-id="13b61-137">Does the parameter affect the files on disk?</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13b61-138">Beeinträchtigt die Zuverlässigkeit:</span><span class="sxs-lookup"><span data-stu-id="13b61-138">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="13b61-139">Wirkt sich der Parameter auf die Engine-Zuverlässigkeit aus?</span><span class="sxs-lookup"><span data-stu-id="13b61-139">Does the parameter affect engine reliability?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13b61-140">Beeinträchtigt die Leistung:</span><span class="sxs-lookup"><span data-stu-id="13b61-140">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="13b61-141">Wirkt sich der Parameter auf die Engine-Leistung aus?</span><span class="sxs-lookup"><span data-stu-id="13b61-141">Does the parameter affect engine performance?</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="13b61-142">Betrifft Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="13b61-142">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="13b61-143">Wirkt sich der Parameter auf Engine-Ressourcen aus?</span><span class="sxs-lookup"><span data-stu-id="13b61-143">Does the parameter affect engine resources?</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="13b61-144">Verfügbarkeit:</span><span class="sxs-lookup"><span data-stu-id="13b61-144">Availability:</span></span></p></td>
<td><p><span data-ttu-id="13b61-145">Versionen von Windows, die den-Parameter unterstützen.</span><span class="sxs-lookup"><span data-stu-id="13b61-145">Releases of Windows that support the parameter.</span></span></p></td>
</tr>
</tbody>
</table>
