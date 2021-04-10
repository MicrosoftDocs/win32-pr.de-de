---
title: ILockBytes-Implementierung des globalen Speichers
description: Die Implementierung des globalen ILockBytes-Speichers wird in einem Bytearray-Objekt implementiert, das einem com-Verbund Dateispeicher Objekt zugrunde liegt und für das Lesen und schreiben direkt in den globalen Speicher konzipiert ist.
ms.assetid: 6ab019b0-34d7-4b6e-ba77-6b6881fabd29
keywords:
- ILockBytes, geg, Implementierungen, globaler Speicher
- "\"ILockBytes\", \"STG\", Implementierungen"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d7cae82c1503fcb53d2cfd8fee39095eb60801
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309472"
---
# <a name="ilockbytes---global-memory-implementation"></a><span data-ttu-id="61f64-105">ILockBytes-Implementierung des globalen Speichers</span><span class="sxs-lookup"><span data-stu-id="61f64-105">ILockBytes - Global Memory Implementation</span></span>

<span data-ttu-id="61f64-106">Die Implementierung des globalen ILockBytes-Speichers wird in einem Bytearray-Objekt implementiert, das einem com-Verbund Dateispeicher Objekt zugrunde liegt und für das Lesen und schreiben direkt in den globalen Speicher konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="61f64-106">The ILockBytes global memory implementation is implemented on a byte array object underlying a COM compound file storage object, and designed to read and write directly to global memory.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="61f64-107">Verwendungs Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="61f64-107">When to Use</span></span>

<span data-ttu-id="61f64-108">Methoden von [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) werden von den Verbund Datei Implementierungen von [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) und [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) auf dem Verbund Dateispeicher Objekt aufgerufen, das durch einen Aufruf von [**stganatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="61f64-108">Methods of [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) are called from the compound file implementations of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) and [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) on the compound file storage object created through a call to [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile).</span></span>

## <a name="remarks"></a><span data-ttu-id="61f64-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61f64-109">Remarks</span></span>

<span data-ttu-id="61f64-110">Im folgenden finden Sie die Methoden der Implementierung des globalen [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) -Speichers.</span><span class="sxs-lookup"><span data-stu-id="61f64-110">The following are the methods of the [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) Global Memory Implementation.</span></span>

<dl> <dt>

<span data-ttu-id="61f64-111"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes:: Read at**</span><span class="sxs-lookup"><span data-stu-id="61f64-111"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes::ReadAt**</span></span>
</dt> <dd>

<span data-ttu-id="61f64-112">Liest einen Byteblock aus einem angegebenen Offset am Anfang des Bytearrays.</span><span class="sxs-lookup"><span data-stu-id="61f64-112">Reads a block of bytes from a specified offset at the beginning of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="61f64-113"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes:: Write-at**</span><span class="sxs-lookup"><span data-stu-id="61f64-113"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes::WriteAt**</span></span>
</dt> <dd>

<span data-ttu-id="61f64-114">Schreibt den Block von Bytes aus einem angegebenen Offset am Anfang des Bytearrays.</span><span class="sxs-lookup"><span data-stu-id="61f64-114">Writes the block of bytes from a specified offset at the beginning of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="61f64-115"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes:: Flush**</span><span class="sxs-lookup"><span data-stu-id="61f64-115"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes::Flush**</span></span>
</dt> <dd>

<span data-ttu-id="61f64-116">Anders als bei der dateibasierten Implementierung hat das Aufrufen dieser Methode in der Implementierung des globalen Speichers keinerlei Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="61f64-116">Unlike file-based implementation, calling this method in global memory implementation has no effect.</span></span>

</dd> <dt>

<span data-ttu-id="61f64-117"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes:: SetSize**</span><span class="sxs-lookup"><span data-stu-id="61f64-117"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes::SetSize**</span></span>
</dt> <dd>

<span data-ttu-id="61f64-118">Legt die Größe des Bytearrays fest.</span><span class="sxs-lookup"><span data-stu-id="61f64-118">Sets the size of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="61f64-119"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes:: LockRegion**</span><span class="sxs-lookup"><span data-stu-id="61f64-119"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes::LockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="61f64-120">Diese Implementierung unterstützt keine Sperren, weshalb *dwlockstype* auf 0 (null) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="61f64-120">This implementation does not support locking, so *dwLocksType* is set to zero.</span></span> <span data-ttu-id="61f64-121">Der Aufrufer muss sicherstellen, dass Zugriffe gültig und sich gegenseitig ausschließen</span><span class="sxs-lookup"><span data-stu-id="61f64-121">The caller must ensure accesses are valid and mutually exclusive.</span></span>

</dd> <dt>

<span data-ttu-id="61f64-122"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes:: UnlockRegion**</span><span class="sxs-lookup"><span data-stu-id="61f64-122"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes::UnlockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="61f64-123">Diese Implementierung unterstützt keine Sperren.</span><span class="sxs-lookup"><span data-stu-id="61f64-123">This implementation does not support locking.</span></span>

</dd> <dt>

<span data-ttu-id="61f64-124"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes:: stat**</span><span class="sxs-lookup"><span data-stu-id="61f64-124"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes::Stat**</span></span>
</dt> <dd>

<span data-ttu-id="61f64-125">Die von com bereitgestellte [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) -Implementierung ruft die [**ILockBytes:: stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) -Methode auf, um Daten zum Bytearray-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="61f64-125">The COM-provided [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) implementation calls the [**ILockBytes::Stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) method to retrieve data about the byte array object.</span></span> <span data-ttu-id="61f64-126">Wenn kein angemessener Name für das Bytearray vorhanden ist, gibt die von com bereitgestellte **ILockBytes:: stat** -Methode **null** im **pwcsName** -Member der [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="61f64-126">If there is no reasonable name for the byte array, the COM-provided **ILockBytes::Stat** method returns **NULL** in the **pwcsName** member of the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="61f64-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="61f64-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61f64-128">**ILockBytes**</span><span class="sxs-lookup"><span data-stu-id="61f64-128">**ILockBytes**</span></span>](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[<span data-ttu-id="61f64-129">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="61f64-129">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="61f64-130">**IStream**</span><span class="sxs-lookup"><span data-stu-id="61f64-130">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




