---
description: Beschreibt die Konsistenz mit Lese-und Schreibzugriff, die Isolation mit Lese-und Schreibzugriff sowie die Konzepte von Transaktions Sperren in Transaktions-NTFS.
ms.assetid: 18579c4a-a832-4c89-8fb1-cd2542e4375e
title: Grundlegende TxF-Konzepte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f2f5d0885795f20a8dfb5e0963468ff04bb8e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347819"
---
# <a name="basic-txf-concepts"></a><span data-ttu-id="24891-103">Grundlegende TxF-Konzepte</span><span class="sxs-lookup"><span data-stu-id="24891-103">Basic TxF Concepts</span></span>

## <a name="read-isolation"></a><span data-ttu-id="24891-104">Lese Isolation</span><span class="sxs-lookup"><span data-stu-id="24891-104">Read Isolation</span></span>

<span data-ttu-id="24891-105">Transaktionale NTFS (TxF) bieten Konsistenz mit Lesezugriff.</span><span class="sxs-lookup"><span data-stu-id="24891-105">Transactional NTFS (TxF) provides read-committed consistency.</span></span>

<span data-ttu-id="24891-106">Ein [*transaktiver Writer*](glossary.md) verweist auf ein transaktives Datei Handle, das mit einer beliebigen Berechtigung geöffnet wurde, die nicht Teil des generischen Lese Zugriffs ist, aber Teil des generischen Schreibzugriffs ist.</span><span class="sxs-lookup"><span data-stu-id="24891-106">A [*transacted writer*](glossary.md) refers to a transacted file handle opened with any permission that is not part of generic read access but is part of generic write access.</span></span> <span data-ttu-id="24891-107">Ein *transaktiver Writer* zeigt die neueste Version einer Datei an, die alle Änderungen durch dieselbe Transaktion enthält.</span><span class="sxs-lookup"><span data-stu-id="24891-107">A *transacted writer* views the most recent version of a file that includes all of the changes by the same transaction.</span></span> <span data-ttu-id="24891-108">Pro Datei kann nur ein transaktiver Writer vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="24891-108">There can be only one transacted writer per file.</span></span> <span data-ttu-id="24891-109">Nicht transaktive Writer werden immer von einem transaktiven Writer blockiert, auch wenn die Datei mit freigegebenen Schreibberechtigungen geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="24891-109">Non-transacted writers are always blocked by a transacted writer, even if the file is opened with shared-write permissions.</span></span>

<span data-ttu-id="24891-110">Ein [*transaktiver Reader*](glossary.md) verweist auf ein transaktives Datei Handle, das mit einer beliebigen Berechtigung geöffnet ist, die Teil des generischen Lese Zugriffs ist, aber nicht Teil des generischen Schreibzugriffs ist.</span><span class="sxs-lookup"><span data-stu-id="24891-110">A [*transacted reader*](glossary.md) refers to a transacted file handle opened with any permission that is a part of generic read access but is not part of generic write access.</span></span> <span data-ttu-id="24891-111">Ein *transaktiver Reader* zeigt eine zugesicherte Version der Datei an, die zum Zeitpunkt des Öffnens des Datei Handles vorhanden war.</span><span class="sxs-lookup"><span data-stu-id="24891-111">A *transacted reader* views a committed version of the file that existed at the time the file handle was opened.</span></span> <span data-ttu-id="24891-112">Der transaktive Reader ist von den Auswirkungen von transaktiven Writern isoliert.</span><span class="sxs-lookup"><span data-stu-id="24891-112">The transacted reader is isolated from the effects of transacted writers.</span></span> <span data-ttu-id="24891-113">Dies bietet eine konsistente Ansicht der Datei nur für die Lebensdauer des Datei Handles und blockiert nicht transaktive Writer.</span><span class="sxs-lookup"><span data-stu-id="24891-113">This provides a consistent view of the file only for the life of the file handle and blocks non-transacted writers.</span></span>

> [!Note]  
> <span data-ttu-id="24891-114">Wenn ein Handle für die Änderung mit der Funktion " [**fiatefiletransfailed**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) " geöffnet wurde, werden alle nachfolgenden Dateien innerhalb dieser Transaktion, unabhängig davon, ob schreibgeschützt oder nicht, vom System in einen transaktiven Writer konvertiert, um die Isolation und andere Transaktions Semantik zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="24891-114">When a handle has been opened for modification with the [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) function, all subsequent opens of the file within that transaction whether read-only or not are converted by the system to be a transacted writer for the purposes of isolation and other transactional semantics.</span></span> <span data-ttu-id="24891-115">Dies bedeutet Folgendes: Wenn ein Handle für den schreibgeschützten Zugriff geöffnet wird, empfängt das Handle vor dem Start der Transaktion keine Ansicht der Datei. Er empfängt die aktive Transaktions Ansicht der Datei.</span><span class="sxs-lookup"><span data-stu-id="24891-115">This means that subsequently, when a handle is opened for read-only access, the handle does not receive a view of the file prior to the start of the transaction; it receives the active transaction view of the file.</span></span>

 

<span data-ttu-id="24891-116">Bei einem nicht transaktiven Datei Handle werden innerhalb einer Transaktion vorgenommene Änderungen erst angezeigt, wenn für die Transaktion ein Commit ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="24891-116">A non-transacted file handle does not see any changes made within a transaction until the transaction is committed.</span></span> <span data-ttu-id="24891-117">Das nicht transaktive Datei Handle empfängt eine isolierte Ansicht, die einem transaktiven Reader ähnelt, aber im Gegensatz zu einem transaktiven Reader empfängt er das Datei Update, wenn ein transaktiver Writer einen Commit für die Transaktion ausführt.</span><span class="sxs-lookup"><span data-stu-id="24891-117">The non-transacted file handle receives an isolated view that is similar to a transacted reader, but unlike a transacted reader, it receives the file update when a transacted writer commits the transaction.</span></span>

## <a name="isolation-levels"></a><span data-ttu-id="24891-118">Isolationsstufen</span><span class="sxs-lookup"><span data-stu-id="24891-118">Isolation Levels</span></span>

<span data-ttu-id="24891-119">TxF bietet eine Isolation mit Lesezugriff.</span><span class="sxs-lookup"><span data-stu-id="24891-119">TxF provides read-committed isolation.</span></span> <span data-ttu-id="24891-120">Dies bedeutet, dass Datei Updates außerhalb der Transaktion nicht sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="24891-120">This means that file updates are not seen outside the transaction.</span></span> <span data-ttu-id="24891-121">Wenn eine Datei beim Lesen von Dateien innerhalb der Transaktion mehrmals geöffnet wird, werden möglicherweise unterschiedliche Ergebnisse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="24891-121">In addition, if a file is opened more than once while reading files within the transaction, you may see different results with each subsequent opening.</span></span> <span data-ttu-id="24891-122">Dateien, die beim ersten Zugriff verfügbar waren, sind möglicherweise nicht verfügbar (weil Sie gelöscht wurden) oder umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="24891-122">Files that were available the first time you accessed them may not be available (because they were deleted), or vice versa.</span></span>

## <a name="transactional-locking"></a><span data-ttu-id="24891-123">Transaktionale Sperren</span><span class="sxs-lookup"><span data-stu-id="24891-123">Transactional Locking</span></span>

<span data-ttu-id="24891-124">Wenn Sie einen transaktiven Writer in einer Datei erstellen, wird die Datei in *transaktional* gesperrt.</span><span class="sxs-lookup"><span data-stu-id="24891-124">Creating a transacted writer on a file *transactionally locks* the file.</span></span> <span data-ttu-id="24891-125">Nachdem eine Datei durch eine Transaktion gesperrt wurde, treten bei anderen Dateisystem Vorgängen außerhalb der Sperr Transaktion, die versuchen, die im Transaktionsmodus gesperrte Datei zu ändern, entweder **Fehler \_ Freigabe \_ Verletzungen** oder **Fehler \_ Transaktions \_ Konflikte** auf.</span><span class="sxs-lookup"><span data-stu-id="24891-125">After a file is locked by a transaction, other file system operations external to the locking transaction that try to modify the transactionally locked file will fail with either **ERROR\_SHARING\_VIOLATION** or **ERROR\_TRANSACTIONAL\_CONFLICT**.</span></span>

<span data-ttu-id="24891-126">In der folgenden Tabelle wird die Transaktions Sperre zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="24891-126">The following table summarizes transactional locking.</span></span>



<span data-ttu-id="24891-127">Zurzeit geöffnete Datei</span><span class="sxs-lookup"><span data-stu-id="24891-127">File currently opened by</span></span>

<span data-ttu-id="24891-128">Datei öffnen versucht von</span><span class="sxs-lookup"><span data-stu-id="24891-128">File open attempted by</span></span>

<span data-ttu-id="24891-129">Transacted</span><span class="sxs-lookup"><span data-stu-id="24891-129">Transacted</span></span>

<span data-ttu-id="24891-130">Nicht transaktiv</span><span class="sxs-lookup"><span data-stu-id="24891-130">Non-Transacted</span></span>

<span data-ttu-id="24891-131">Leser</span><span class="sxs-lookup"><span data-stu-id="24891-131">Reader</span></span>

<span data-ttu-id="24891-132">Leser/Writer</span><span class="sxs-lookup"><span data-stu-id="24891-132">Reader/Writer</span></span>

<span data-ttu-id="24891-133">Leser</span><span class="sxs-lookup"><span data-stu-id="24891-133">Reader</span></span>

<span data-ttu-id="24891-134">Leser/Writer</span><span class="sxs-lookup"><span data-stu-id="24891-134">Reader/Writer</span></span>

<span data-ttu-id="24891-135">Transaktive Reader</span><span class="sxs-lookup"><span data-stu-id="24891-135">Transacted Reader</span></span>

<span data-ttu-id="24891-136">Ja</span><span class="sxs-lookup"><span data-stu-id="24891-136">Yes</span></span>

<span data-ttu-id="24891-137">Ja</span><span class="sxs-lookup"><span data-stu-id="24891-137">Yes</span></span>

<span data-ttu-id="24891-138">Ja</span><span class="sxs-lookup"><span data-stu-id="24891-138">Yes</span></span>

<span data-ttu-id="24891-139">Nein 2</span><span class="sxs-lookup"><span data-stu-id="24891-139">No2</span></span>

<span data-ttu-id="24891-140">Transaktive Reader/Writer</span><span class="sxs-lookup"><span data-stu-id="24891-140">Transacted Reader/Writer</span></span>

<span data-ttu-id="24891-141">Ja</span><span class="sxs-lookup"><span data-stu-id="24891-141">Yes</span></span>

<span data-ttu-id="24891-142">Nein 2</span><span class="sxs-lookup"><span data-stu-id="24891-142">No2</span></span>

<span data-ttu-id="24891-143">Ja</span><span class="sxs-lookup"><span data-stu-id="24891-143">Yes</span></span>

<span data-ttu-id="24891-144">Nein 2</span><span class="sxs-lookup"><span data-stu-id="24891-144">No2</span></span>

<span data-ttu-id="24891-145">Nicht transaktiver Reader</span><span class="sxs-lookup"><span data-stu-id="24891-145">Non-Transacted Reader</span></span>

<span data-ttu-id="24891-146">Ja</span><span class="sxs-lookup"><span data-stu-id="24891-146">Yes</span></span>

<span data-ttu-id="24891-147">Ja</span><span class="sxs-lookup"><span data-stu-id="24891-147">Yes</span></span>

<span data-ttu-id="24891-148">Ja</span><span class="sxs-lookup"><span data-stu-id="24891-148">Yes</span></span>

<span data-ttu-id="24891-149">Ja</span><span class="sxs-lookup"><span data-stu-id="24891-149">Yes</span></span>

<span data-ttu-id="24891-150">Nicht transaktiver Reader/Writer</span><span class="sxs-lookup"><span data-stu-id="24891-150">Non-Transacted Reader/Writer</span></span>

<span data-ttu-id="24891-151">Nein</span><span class="sxs-lookup"><span data-stu-id="24891-151">No1</span></span>

<span data-ttu-id="24891-152">Nein</span><span class="sxs-lookup"><span data-stu-id="24891-152">No1</span></span>

<span data-ttu-id="24891-153">Ja</span><span class="sxs-lookup"><span data-stu-id="24891-153">Yes</span></span>

<span data-ttu-id="24891-154">Ja</span><span class="sxs-lookup"><span data-stu-id="24891-154">Yes</span></span>

1. <span data-ttu-id="24891-155">Schlägt mit **\_ fehlerellem Transaktions \_ Konflikt** fehl</span><span class="sxs-lookup"><span data-stu-id="24891-155">Fails with **ERROR\_TRANSACTIONAL\_CONFLICT**</span></span><br/> <span data-ttu-id="24891-156">2. Fehler bei **der \_ Freigabe \_ Verletzung**</span><span class="sxs-lookup"><span data-stu-id="24891-156">2. Fails with **ERROR\_SHARING\_VIOLATION**</span></span><br/>



 

<span data-ttu-id="24891-157">Wenn Sie einen benannten Stream für eine Änderung öffnen, die eine Transaktion verwendet, muss die gesamte Datei gesperrt werden.</span><span class="sxs-lookup"><span data-stu-id="24891-157">If you open a named stream for a modification that is using a transaction, the entire file is required to be locked.</span></span>

<span data-ttu-id="24891-158">Zusätzlich zum Transaktions Sperren gelten typische NTFS-Regeln für die Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="24891-158">In addition to transactional locking, typical NTFS file-sharing rules apply.</span></span>

<span data-ttu-id="24891-159">Sie müssen die folgenden beiden Dateifreigabe Modi parallel in Erwägung gezogen werden:</span><span class="sxs-lookup"><span data-stu-id="24891-159">You need to consider the following two file sharing modes in parallel:</span></span>

-   <span data-ttu-id="24891-160">Der Modus für die transaktionale Sperrung.</span><span class="sxs-lookup"><span data-stu-id="24891-160">The transactional locking mode.</span></span>
-   <span data-ttu-id="24891-161">Normaler Modus für die Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="24891-161">Normal file-sharing modes.</span></span>

<span data-ttu-id="24891-162">Welcher Modus restriktiver ist, ist der, der angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="24891-162">Whichever mode is more restrictive is the one that applies.</span></span>

 

 




