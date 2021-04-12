---
description: Die ibytebuffer-Schnittstelle wird zum Lesen, schreiben und Verwalten von Streamobjekten bereitgestellt. Bei diesem Objekt handelt es sich im Wesentlichen um einen Wrapper für das IStream-Objekt.
ms.assetid: dbc46d53-a421-45c0-a86b-b8a0a212a672
title: Ibytebuffer-Schnittstelle (scardssp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: dfba15dee78134a9787bf7af994f1d4e2b064339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960542"
---
# <a name="ibytebuffer-interface"></a><span data-ttu-id="3adcd-104">Ibytebuffer-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3adcd-104">IByteBuffer interface</span></span>

<span data-ttu-id="3adcd-105">\[Die **ibytebuffer** -Schnittstelle ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="3adcd-105">\[The **IByteBuffer** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3adcd-106">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3adcd-106">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3adcd-107">Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="3adcd-107">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="3adcd-108">Die **ibytebuffer** -Schnittstelle wird zum Lesen, schreiben und Verwalten von Streamobjekten bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="3adcd-108">The **IByteBuffer** interface is provided to read, write and manage stream objects.</span></span> <span data-ttu-id="3adcd-109">Bei diesem Objekt handelt es sich im Wesentlichen um einen Wrapper für das **IStream** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="3adcd-109">This object essentially is a wrapper for the **IStream** object.</span></span>

## <a name="members"></a><span data-ttu-id="3adcd-110">Member</span><span class="sxs-lookup"><span data-stu-id="3adcd-110">Members</span></span>

<span data-ttu-id="3adcd-111">Die **ibytebuffer** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3adcd-111">The **IByteBuffer** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="3adcd-112">**Ibytebuffer** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3adcd-112">**IByteBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="3adcd-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="3adcd-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="3adcd-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="3adcd-114">Methods</span></span>

<span data-ttu-id="3adcd-115">Die **ibytebuffer** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="3adcd-115">The **IByteBuffer** interface has these methods.</span></span>



| <span data-ttu-id="3adcd-116">Methode</span><span class="sxs-lookup"><span data-stu-id="3adcd-116">Method</span></span>                                           | <span data-ttu-id="3adcd-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3adcd-117">Description</span></span>                                                                                               |
|:-------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3adcd-118">**Klon**</span><span class="sxs-lookup"><span data-stu-id="3adcd-118">**Clone**</span></span>](ibytebuffer-clone.md)               | <span data-ttu-id="3adcd-119">Klont ein **ibytebuffer** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="3adcd-119">Clones an **IByteBuffer** object.</span></span><br/>                                                              |
| [<span data-ttu-id="3adcd-120">**Einzusetzen**</span><span class="sxs-lookup"><span data-stu-id="3adcd-120">**Commit**</span></span>](ibytebuffer-commit.md)             | <span data-ttu-id="3adcd-121">Führt einen Commit einer [*Transaktion*](/windows/desktop/SecGloss/t-gly)aus.</span><span class="sxs-lookup"><span data-stu-id="3adcd-121">Commits a [*transaction*](/windows/desktop/SecGloss/t-gly).</span></span><br/> |
| [<span data-ttu-id="3adcd-122">**CopyTo**</span><span class="sxs-lookup"><span data-stu-id="3adcd-122">**CopyTo**</span></span>](ibytebuffer-copyto.md)             | <span data-ttu-id="3adcd-123">Kopiert Bytes in ein anderes Objekt.</span><span class="sxs-lookup"><span data-stu-id="3adcd-123">Copies bytes to another object.</span></span><br/>                                                                |
| [<span data-ttu-id="3adcd-124">**Initialisieren**</span><span class="sxs-lookup"><span data-stu-id="3adcd-124">**Initialize**</span></span>](ibytebuffer-initialize.md)     | <span data-ttu-id="3adcd-125">Initialisiert das **ibytebuffer** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="3adcd-125">Initializes the **IByteBuffer** object.</span></span><br/>                                                        |
| [<span data-ttu-id="3adcd-126">**Lock Region**</span><span class="sxs-lookup"><span data-stu-id="3adcd-126">**LockRegion**</span></span>](ibytebuffer-lockregion.md)     | <span data-ttu-id="3adcd-127">Schränkt den Zugriff auf einen Bereich von Bytes ein.</span><span class="sxs-lookup"><span data-stu-id="3adcd-127">Restricts access to a range of bytes.</span></span><br/>                                                          |
| [<span data-ttu-id="3adcd-128">**Lesen**</span><span class="sxs-lookup"><span data-stu-id="3adcd-128">**Read**</span></span>](ibytebuffer-read.md)                 | <span data-ttu-id="3adcd-129">Liest Bytes in den Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="3adcd-129">Reads bytes into memory.</span></span><br/>                                                                       |
| [<span data-ttu-id="3adcd-130">**Umzukehren**</span><span class="sxs-lookup"><span data-stu-id="3adcd-130">**Revert**</span></span>](ibytebuffer-revert.md)             | <span data-ttu-id="3adcd-131">Verwirft Änderungen seit dem letzten [**Commit**](ibytebuffer-commit.md) -Befehl.</span><span class="sxs-lookup"><span data-stu-id="3adcd-131">Discards changes since the last [**Commit**](ibytebuffer-commit.md) call.</span></span><br/>                     |
| [<span data-ttu-id="3adcd-132">**Seek**</span><span class="sxs-lookup"><span data-stu-id="3adcd-132">**Seek**</span></span>](ibytebuffer-seek.md)                 | <span data-ttu-id="3adcd-133">Ändert den Such Zeiger.</span><span class="sxs-lookup"><span data-stu-id="3adcd-133">Changes the seek pointer.</span></span><br/>                                                                      |
| [<span data-ttu-id="3adcd-134">**SetSize**</span><span class="sxs-lookup"><span data-stu-id="3adcd-134">**SetSize**</span></span>](ibytebuffer-setsize.md)           | <span data-ttu-id="3adcd-135">Ändert die Größe des Streamobjekts.</span><span class="sxs-lookup"><span data-stu-id="3adcd-135">Changes the size of the stream object.</span></span><br/>                                                         |
| [<span data-ttu-id="3adcd-136">**Stat**</span><span class="sxs-lookup"><span data-stu-id="3adcd-136">**Stat**</span></span>](ibytebuffer-stat.md)                 | <span data-ttu-id="3adcd-137">Ruft statistische Informationen zu einem Stream ab.</span><span class="sxs-lookup"><span data-stu-id="3adcd-137">Retrieves statistical information about a stream.</span></span><br/>                                              |
| [<span data-ttu-id="3adcd-138">**UnlockRegion**</span><span class="sxs-lookup"><span data-stu-id="3adcd-138">**UnlockRegion**</span></span>](ibytebuffer-unlockregion.md) | <span data-ttu-id="3adcd-139">Entfernt die Zugriffs Einschränkung, die zuvor von [**LockRegion**](ibytebuffer-lockregion.md)festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="3adcd-139">Removes access restriction previously set by [**LockRegion**](ibytebuffer-lockregion.md).</span></span><br/>     |
| [<span data-ttu-id="3adcd-140">**Schreiben**</span><span class="sxs-lookup"><span data-stu-id="3adcd-140">**Write**</span></span>](ibytebuffer-write.md)               | <span data-ttu-id="3adcd-141">Schreibt Bytes in den Stream.</span><span class="sxs-lookup"><span data-stu-id="3adcd-141">Writes bytes to the stream.</span></span><br/>                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="3adcd-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3adcd-142">Requirements</span></span>



| <span data-ttu-id="3adcd-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3adcd-143">Requirement</span></span> | <span data-ttu-id="3adcd-144">Wert</span><span class="sxs-lookup"><span data-stu-id="3adcd-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3adcd-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3adcd-145">Minimum supported client</span></span><br/> | <span data-ttu-id="3adcd-146">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3adcd-146">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3adcd-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3adcd-147">Minimum supported server</span></span><br/> | <span data-ttu-id="3adcd-148">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3adcd-148">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3adcd-149">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="3adcd-149">End of client support</span></span><br/>    | <span data-ttu-id="3adcd-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3adcd-150">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="3adcd-151">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="3adcd-151">End of server support</span></span><br/>    | <span data-ttu-id="3adcd-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3adcd-152">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="3adcd-153">Header</span><span class="sxs-lookup"><span data-stu-id="3adcd-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="3adcd-154"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="3adcd-154"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3adcd-155">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="3adcd-155">Type library</span></span><br/>             | <dl> <span data-ttu-id="3adcd-156"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3adcd-156"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3adcd-157">DLL</span><span class="sxs-lookup"><span data-stu-id="3adcd-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3adcd-158"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3adcd-158"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3adcd-159">IID</span><span class="sxs-lookup"><span data-stu-id="3adcd-159">IID</span></span><br/>                      | <span data-ttu-id="3adcd-160">IID \_ ibytebuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.</span><span class="sxs-lookup"><span data-stu-id="3adcd-160">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

