---
description: Eine zyklische Redundanz Überprüfung (CRC) von Dateien ist mit Windows Installer verfügbar.
ms.assetid: c895488b-6e60-4175-8865-4ba4b0cb2d9a
title: CRC-Überprüfung während einer Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56e03bb6754b0259aa8b27333c8137408e7dc956
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217178"
---
# <a name="crc-checking-during-an-installation"></a><span data-ttu-id="d2b53-103">CRC-Überprüfung während einer Installation</span><span class="sxs-lookup"><span data-stu-id="d2b53-103">CRC Checking During an Installation</span></span>

<span data-ttu-id="d2b53-104">Eine zyklische Redundanz Überprüfung (CRC) von Dateien ist mit Windows Installer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d2b53-104">A Cyclic Redundancy Check (CRC) of files is available with Windows Installer.</span></span> <span data-ttu-id="d2b53-105">Die CRC-Überprüfung ist ein Fehler Überprüfungsverfahren, ähnlich wie eine Prüfsumme, mit dem eine Anwendung ermitteln kann, ob die Informationen in einer Datei geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="d2b53-105">CRC checking is an error-checking mechanism, similar to a checksum, that enables an application to determine whether the information in a file has been modified.</span></span> <span data-ttu-id="d2b53-106">Nachdem die Windows Installer das Kopieren einer Datei abgeschlossen hat, ruft Sie einen CRC-Wert aus den Quell-und Zieldateien ab.</span><span class="sxs-lookup"><span data-stu-id="d2b53-106">After the Windows Installer finishes copying a file, it gets a CRC value from both the source and destination files.</span></span> <span data-ttu-id="d2b53-107">Das Installationsprogramm überprüft den ursprünglichen CRC-Stempel in die Datei und vergleicht diesen mit dem CRC, der aus der Kopie berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="d2b53-107">The installer checks the original CRC stamped into the file and compares this to the CRC calculated from the copy.</span></span> <span data-ttu-id="d2b53-108">Die CRC-Überprüfung schlägt fehl, wenn der ursprüngliche CRC-Wert ungleich NULL ist und sich von dem CRC unterscheidet, der für den Kopiervorgang berechnet wurde.</span><span class="sxs-lookup"><span data-stu-id="d2b53-108">The CRC check fails if the original CRC value is non-null and is different from the CRC calculated on the copy.</span></span> <span data-ttu-id="d2b53-109">Wenn das ursprüngliche CRC NULL ist, erfolgt keine Überprüfung.</span><span class="sxs-lookup"><span data-stu-id="d2b53-109">If the original CRC is null, no check occurs.</span></span>

<span data-ttu-id="d2b53-110">Der Windows Installer führt in den folgenden Fällen eine CRC-Prüfung für eine Datei durch:</span><span class="sxs-lookup"><span data-stu-id="d2b53-110">The Windows Installer does a CRC check on a file in the following cases:</span></span>

-   <span data-ttu-id="d2b53-111">Wenn die [msicheckcrcs-Eigenschaft](msicheckcrcs.md) festgelegt ist und **msidbFileAttributesChecksum** im Feld Attribute des Datensatzes der Datei in der [Dateitabelle](file-table.md)enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d2b53-111">If the [MSICHECKCRCS property](msicheckcrcs.md) is set and **msidbFileAttributesChecksum** is included in the Attributes field of the file's record in the [File table](file-table.md).</span></span> <span data-ttu-id="d2b53-112">Das Installationsprogramm führt die CRC-Prüfung einmal nach dem installieren, duplizieren oder Verschieben der Datei durch.</span><span class="sxs-lookup"><span data-stu-id="d2b53-112">The installer does the CRC check once after installing, duplicating, or moving the file.</span></span>
-   <span data-ttu-id="d2b53-113">Wenn die [Eigenschaft msicheckcrcs](msicheckcrcs.md) festgelegt ist und **msidbFileAttributesChecksum** im Feld Attribute des Datensatzes der Datei in der [Dateitabelle](file-table.md)enthalten ist, führt das Installationsprogramm nach dem Patchen der Datei eine CRC-Prüfung durch.</span><span class="sxs-lookup"><span data-stu-id="d2b53-113">If the [MSICHECKCRCS property](msicheckcrcs.md) is set and **msidbFileAttributesChecksum** is included in the Attributes field of the file's record in the [File table](file-table.md), the installer does a CRC check after patching the file.</span></span>
-   <span data-ttu-id="d2b53-114">Wenn **msidbFileAttributesChecksum** im Feld Attribute des Datensatzes der Datei in der [Dateitabelle](file-table.md)enthalten ist, führt das Installationsprogramm eine CRC-Überprüfung vor dem Binden von Images durch.</span><span class="sxs-lookup"><span data-stu-id="d2b53-114">If the **msidbFileAttributesChecksum** is included in the Attributes field of the file's record in the [File table](file-table.md), the installer does a CRC check before binding images.</span></span>

<span data-ttu-id="d2b53-115">Wenn die Überprüfung fehlschlägt, bevor ein Abbild gebunden wird, meldet das Installationsprogramm die folgenden beiden Fehler in der Protokolldatei und setzt die Installation fort, ohne die Datei zu binden.</span><span class="sxs-lookup"><span data-stu-id="d2b53-115">If the check fails before binding an image, the installer reports the following two errors in the log file and continues the installation without binding the file.</span></span>



| <span data-ttu-id="d2b53-116">Code</span><span class="sxs-lookup"><span data-stu-id="d2b53-116">Code</span></span> | <span data-ttu-id="d2b53-117">`Message`</span><span class="sxs-lookup"><span data-stu-id="d2b53-117">Message</span></span>                                               |
|------|-------------------------------------------------------|
| <span data-ttu-id="d2b53-118">2941</span><span class="sxs-lookup"><span data-stu-id="d2b53-118">2941</span></span> | <span data-ttu-id="d2b53-119">CRC für Datei 2 kann nicht berechnet werden \[ \] .</span><span class="sxs-lookup"><span data-stu-id="d2b53-119">Unable to compute the CRC for file \[2\].</span></span>             |
| <span data-ttu-id="d2b53-120">2942</span><span class="sxs-lookup"><span data-stu-id="d2b53-120">2942</span></span> | <span data-ttu-id="d2b53-121">Die BindImage-Aktion wurde für \[ zwei Dateien nicht ausgeführt \] .</span><span class="sxs-lookup"><span data-stu-id="d2b53-121">BindImage action has not been executed on \[2\] file.</span></span> |



 

<span data-ttu-id="d2b53-122">Wenn die Überprüfung fehlschlägt, nachdem eine nicht komprimierte Datei kopiert, dupliziert oder gepatcht wurde, meldet das Installationsprogramm den folgenden Fehler.</span><span class="sxs-lookup"><span data-stu-id="d2b53-122">If the check fails after an uncompressed file had been copied, duplicated, or patched, the installer reports the following error.</span></span> <span data-ttu-id="d2b53-123">Dieser Fehler wird auch gemeldet, wenn die Überprüfung fehlschlägt, nachdem eine komprimierte Datei kopiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d2b53-123">This error is also reported if the check fails after a compressed file is copied.</span></span> <span data-ttu-id="d2b53-124">Wenn die Datei über das **msidbfileattributesvital** -Attribut verfügt, wird die Datei als wichtig für die Installation angesehen, und der Benutzer erhält die Möglichkeit, die Installation zu wiederholen oder abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="d2b53-124">If the file has the **msidbFileAttributesVital** attribute, the file is considered vital to the installation and the user gets the option to retry or cancel the installation.</span></span> <span data-ttu-id="d2b53-125">Wenn die Datei in der Spalte Attribute der [Dateitabelle](file-table.md)als nicht entscheidend gekennzeichnet ist, kann der Benutzer den Fehler ignorieren und den Vorgang fortsetzen, den Vorgang wiederholen oder die Installation abbrechen.</span><span class="sxs-lookup"><span data-stu-id="d2b53-125">If the file is marked as nonvital in the Attributes column of the [File table](file-table.md), the user may ignore the error and continue, retry, or cancel the installation.</span></span>



| <span data-ttu-id="d2b53-126">Code</span><span class="sxs-lookup"><span data-stu-id="d2b53-126">Code</span></span> | <span data-ttu-id="d2b53-127">`Message`</span><span class="sxs-lookup"><span data-stu-id="d2b53-127">Message</span></span>                                         |
|------|-------------------------------------------------|
| <span data-ttu-id="d2b53-128">1331</span><span class="sxs-lookup"><span data-stu-id="d2b53-128">1331</span></span> | <span data-ttu-id="d2b53-129">Fehler beim Kopieren von \[ 2 \] Datei: CRC-Fehler.</span><span class="sxs-lookup"><span data-stu-id="d2b53-129">Failed to correctly copy \[2\] file: CRC error.</span></span> |



 

<span data-ttu-id="d2b53-130">Beachten Sie, dass nur nicht komprimierte Dateien verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="d2b53-130">Note that only uncompressed files are moved.</span></span> <span data-ttu-id="d2b53-131">Wenn die Überprüfung fehlschlägt, nachdem eine nicht komprimierte Datei verschoben wurde, zeigt das Installationsprogramm den folgenden Fehler an.</span><span class="sxs-lookup"><span data-stu-id="d2b53-131">If the check fails after an uncompressed file is moved, the installer displays the following error.</span></span> <span data-ttu-id="d2b53-132">Wenn die Datei über das **msidbfileattributesvital** -Attribut verfügt, wird die Datei als wichtig für die Installation angesehen, und die Installation schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="d2b53-132">If the file has the **msidbFileAttributesVital** attribute, the file is considered vital to the installation and the installation fails.</span></span> <span data-ttu-id="d2b53-133">Wenn die Datei in der Spalte Attribute der [Dateitabelle](file-table.md)als nicht entscheidend gekennzeichnet ist, erhält der Benutzer die Option, den Fehler abzubrechen oder zu ignorieren und die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="d2b53-133">If the file is marked as nonvital in the Attributes column of the [File table](file-table.md), the user gets the option to cancel or to ignore the error and continue the installation.</span></span>



| <span data-ttu-id="d2b53-134">Code</span><span class="sxs-lookup"><span data-stu-id="d2b53-134">Code</span></span> | <span data-ttu-id="d2b53-135">`Message`</span><span class="sxs-lookup"><span data-stu-id="d2b53-135">Message</span></span>                                         |
|------|-------------------------------------------------|
| <span data-ttu-id="d2b53-136">1332</span><span class="sxs-lookup"><span data-stu-id="d2b53-136">1332</span></span> | <span data-ttu-id="d2b53-137">Fehler beim Verschieben von \[ 2 \] Datei: CRC-Fehler.</span><span class="sxs-lookup"><span data-stu-id="d2b53-137">Failed to correctly move \[2\] file: CRC error.</span></span> |



 

<span data-ttu-id="d2b53-138">Wenn die Überprüfung fehlschlägt, nachdem eine nicht komprimierte Datei gepatcht wurde, zeigt das Installationsprogramm den folgenden Fehler an.</span><span class="sxs-lookup"><span data-stu-id="d2b53-138">If the check fails after an uncompressed file is patched, the installer displays the following error.</span></span> <span data-ttu-id="d2b53-139">Wenn die Datei über das **msidbfileattributesvital** -Attribut verfügt, wird die Datei als wichtig für die Installation angesehen, und die Installation schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="d2b53-139">If the file has the **msidbFileAttributesVital** attribute, the file is considered vital to the installation and the installation fails.</span></span> <span data-ttu-id="d2b53-140">Wenn die Datei in der Spalte Attribute der [Dateitabelle](file-table.md)als nicht entscheidend gekennzeichnet ist, erhält der Benutzer die Option, den Fehler abzubrechen oder zu ignorieren und die Installation fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="d2b53-140">If the file is marked as nonvital in the Attributes column of the [File table](file-table.md), the user gets the option to cancel or to ignore the error and continue the installation.</span></span>



| <span data-ttu-id="d2b53-141">Code</span><span class="sxs-lookup"><span data-stu-id="d2b53-141">Code</span></span> | <span data-ttu-id="d2b53-142">`Message`</span><span class="sxs-lookup"><span data-stu-id="d2b53-142">Message</span></span>                                          |
|------|--------------------------------------------------|
| <span data-ttu-id="d2b53-143">1333</span><span class="sxs-lookup"><span data-stu-id="d2b53-143">1333</span></span> | <span data-ttu-id="d2b53-144">Fehler beim Patchen der \[ 2- \] Datei: CRC-Fehler.</span><span class="sxs-lookup"><span data-stu-id="d2b53-144">Failed to correctly patch \[2\] file: CRC error.</span></span> |



 

 

 



