---
description: Schränkt den Zugriff auf einen angegebenen Bereich von Bytes im Buffer-Objekt ein.
ms.assetid: 7bcb3c1e-5739-41f7-a3aa-2943542943ed
title: 'Ibytebuffer:: LockRegion-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.LockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ae227d11892b604ab1382cb328dc492e4596f278
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217776"
---
# <a name="ibytebufferlockregion-method"></a><span data-ttu-id="9e5c7-103">Ibytebuffer:: LockRegion-Methode</span><span class="sxs-lookup"><span data-stu-id="9e5c7-103">IByteBuffer::LockRegion method</span></span>

<span data-ttu-id="9e5c7-104">\[Die **LockRegion** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-104">\[The **LockRegion** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9e5c7-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9e5c7-106">Die [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) -Schnittstelle bietet eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="9e5c7-106">The [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) interface provides similar functionality.\]</span></span>

<span data-ttu-id="9e5c7-107">Die **LockRegion** -Methode schränkt den Zugriff auf einen angegebenen Bereich von Bytes im Buffer-Objekt ein.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-107">The **LockRegion** method restricts access to a specified range of bytes in the buffer object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e5c7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e5c7-108">Syntax</span></span>


```C++
HRESULT LockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a><span data-ttu-id="9e5c7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e5c7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e5c7-110">*liboffset* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e5c7-110">*libOffset* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5c7-111">Eine ganze Zahl, die den Byte Offset für den Anfang des Bereichs angibt.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-111">Integer that specifies the byte offset for the beginning of the range.</span></span>

</dd> <dt>

<span data-ttu-id="9e5c7-112">*CB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e5c7-112">*cb* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5c7-113">Eine ganze Zahl, die die Länge des Bereichs (in Bytes) angibt, der eingeschränkt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-113">Integer that specifies the length of the range, in bytes, to be restricted.</span></span>

</dd> <dt>

<span data-ttu-id="9e5c7-114">*dwLockType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e5c7-114">*dwLockType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e5c7-115">Gibt die Einschränkungen an, die beim Zugriff auf den Bereich angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-115">Specifies the restrictions being requested on accessing the range.</span></span> <span data-ttu-id="9e5c7-116">Dies kann einer der Werte in der folgenden Tabelle sein.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-116">This can be one of the values in the following table.</span></span>



| <span data-ttu-id="9e5c7-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9e5c7-117">Value</span></span>                                                                                                                                                            | <span data-ttu-id="9e5c7-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9e5c7-118">Meaning</span></span>                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOCK_WRITE"></span><span id="lock_write"></span><dl> <span data-ttu-id="9e5c7-119"><dt>**Sperr \_ Schreibvorgang**</dt></span><span class="sxs-lookup"><span data-stu-id="9e5c7-119"><dt>**LOCK\_WRITE**</dt></span></span> </dl>             | <span data-ttu-id="9e5c7-120">Der angegebene Bereich von Bytes kann beliebig oft geöffnet und gelesen werden, aber das Schreiben in den gesperrten Bereich ist mit Ausnahme des Besitzers, dem diese Sperre erteilt wurde, nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-120">The specified range of bytes can be opened and read any number of times, but writing to the locked range is prohibited except for the owner that was granted this lock.</span></span><br/>                                                                      |
| <span id="LOCK_EXCLUSIVE"></span><span id="lock_exclusive"></span><dl> <span data-ttu-id="9e5c7-121"><dt>**\_exklusiv sperren**</dt></span><span class="sxs-lookup"><span data-stu-id="9e5c7-121"><dt>**LOCK\_EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="9e5c7-122">Das Schreiben in den angegebenen Byte Bereich ist mit Ausnahme des Besitzers, dem diese Sperre erteilt wurde, nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-122">Writing to the specified range of bytes is prohibited except for the owner that was granted this lock.</span></span><br/>                                                                                                                                       |
| <span id="LOCK_ONLYONCE"></span><span id="lock_onlyonce"></span><dl> <span data-ttu-id="9e5c7-123"><dt>**\_onlyonce Sperren**</dt></span><span class="sxs-lookup"><span data-stu-id="9e5c7-123"><dt>**LOCK\_ONLYONCE**</dt></span></span> </dl>    | <span data-ttu-id="9e5c7-124">Wenn diese Sperre erteilt wird, kann keine andere Lock \_ onlyonce-Sperre für den Bereich abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-124">If this lock is granted, no other LOCK\_ONLYONCE lock can be obtained on the range.</span></span> <span data-ttu-id="9e5c7-125">In der Regel handelt es sich bei diesem Sperrentyp um einen Alias für einen anderen Sperrentyp.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-125">Usually this lock type is an alias for some other lock type.</span></span> <span data-ttu-id="9e5c7-126">Folglich können bestimmte Implementierungen über zusätzliches Verhalten verfügen, das diesem Sperrentyp zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-126">Thus, specific implementations can have additional behavior associated with this lock type.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e5c7-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e5c7-127">Return value</span></span>

<span data-ttu-id="9e5c7-128">Der Rückgabewert ist ein **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-128">The return value is an **HRESULT**.</span></span> <span data-ttu-id="9e5c7-129">Der Wert S OK gibt an, dass \_ der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-129">A value of S\_OK indicates the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e5c7-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e5c7-130">Remarks</span></span>

<span data-ttu-id="9e5c7-131">Der Byte Bereich kann nach dem aktuellen Ende des Streams erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-131">The byte range can extend past the current end of the stream.</span></span> <span data-ttu-id="9e5c7-132">Das Sperren über das Ende eines Datenstroms hinaus ist als Kommunikationsmethode zwischen verschiedenen Instanzen des Streams nützlich, ohne dass Daten geändert werden, die tatsächlich Teil des Streams sind.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-132">Locking beyond the end of a stream is useful as a method of communication between different instances of the stream without changing data that is actually part of the stream.</span></span>

<span data-ttu-id="9e5c7-133">Es können drei Arten von Sperren unterstützt werden: Sperren, um andere Writer auszuschließen, sperren, um andere Reader oder Writer auszuschließen, und sperren, die nur einem Anforderer erlauben, eine Sperre für den angegebenen Bereich zu erhalten, was normalerweise ein Alias für einen der beiden anderen Sperr Typen ist.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-133">Three types of locking can be supported: locking to exclude other writers, locking to exclude other readers or writers, and locking that allows only one requester to obtain a lock on the given range, which is usually an alias for one of the other two lock types.</span></span> <span data-ttu-id="9e5c7-134">Eine angegebene Datenstrom Instanz unterstützt möglicherweise einen der beiden ersten Typen oder beides.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-134">A given stream instance might support either of the first two types, or both.</span></span> <span data-ttu-id="9e5c7-135">Der Sperrentyp wird von *dwLockType* mit einem Wert aus der [**LockType**](/windows/win32/api/objidl/ne-objidl-locktype) -Enumeration angegeben.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-135">The lock type is specified by *dwLockType*, using a value from the [**LOCKTYPE**](/windows/win32/api/objidl/ne-objidl-locktype) enumeration.</span></span>

<span data-ttu-id="9e5c7-136">Alle mit **LockRegion** gesperrten Bereiche müssen später explizit entsperrt werden, indem [**ibytebuffer:: UnlockRegion**](ibytebuffer-unlockregion.md) mit exakt denselben Werten für die Parameter *liboffset*, *CB* und *dwLockType* aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-136">Any region locked with **LockRegion** must later be explicitly unlocked by calling [**IByteBuffer::UnlockRegion**](ibytebuffer-unlockregion.md) with exactly the same values for the *libOffset*, *cb*, and *dwLockType* parameters.</span></span> <span data-ttu-id="9e5c7-137">Die Region muss entsperrt werden, bevor der Stream freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-137">The region must be unlocked before the stream is released.</span></span> <span data-ttu-id="9e5c7-138">Zwei angrenzende Regionen können nicht separat gesperrt und dann mit einem einzigen Unlock-Befehl entsperrt werden.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-138">Two adjacent regions cannot be locked separately and then unlocked with a single unlock call.</span></span>

## <a name="examples"></a><span data-ttu-id="9e5c7-139">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9e5c7-139">Examples</span></span>

<span data-ttu-id="9e5c7-140">Das folgende Beispiel zeigt, wie der Zugriff auf einen Bereich von Bytes beschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-140">The following example shows restricting access to a range of bytes.</span></span>


```C++
HRESULT  hr;

// Lock a region.
hr = pIByteBuff->LockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::LockRegion\n");
```



## <a name="requirements"></a><span data-ttu-id="9e5c7-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e5c7-141">Requirements</span></span>



| <span data-ttu-id="9e5c7-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e5c7-142">Requirement</span></span> | <span data-ttu-id="9e5c7-143">Wert</span><span class="sxs-lookup"><span data-stu-id="9e5c7-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9e5c7-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9e5c7-144">Minimum supported client</span></span><br/> | <span data-ttu-id="9e5c7-145">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e5c7-145">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9e5c7-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9e5c7-146">Minimum supported server</span></span><br/> | <span data-ttu-id="9e5c7-147">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e5c7-147">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9e5c7-148">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9e5c7-148">End of client support</span></span><br/>    | <span data-ttu-id="9e5c7-149">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9e5c7-149">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="9e5c7-150">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="9e5c7-150">End of server support</span></span><br/>    | <span data-ttu-id="9e5c7-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9e5c7-151">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="9e5c7-152">Header</span><span class="sxs-lookup"><span data-stu-id="9e5c7-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e5c7-153"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="9e5c7-153"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9e5c7-154">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9e5c7-154">Type library</span></span><br/>             | <dl> <span data-ttu-id="9e5c7-155"><dt>Scardssp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9e5c7-155"><dt>Scardssp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9e5c7-156">DLL</span><span class="sxs-lookup"><span data-stu-id="9e5c7-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9e5c7-157"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9e5c7-157"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9e5c7-158">IID</span><span class="sxs-lookup"><span data-stu-id="9e5c7-158">IID</span></span><br/>                      | <span data-ttu-id="9e5c7-159">IID \_ ibytebuffer ist als E126F8FE-A7AF-11D0-B88A-00C04FD424B9 definiert.</span><span class="sxs-lookup"><span data-stu-id="9e5c7-159">IID\_IByteBuffer is defined as E126F8FE-A7AF-11D0-B88A-00C04FD424B9</span></span><br/>          |



 

