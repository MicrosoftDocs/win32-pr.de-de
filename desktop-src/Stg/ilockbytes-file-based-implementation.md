---
title: ILockBytes-File-Based-Implementierung
description: Wird für ein Bytearray-Objekt implementiert, das einem com-Verbund Dateispeicher Objekt zugrunde liegt und zum Lesen und schreiben direkt in eine Datenträger Datei konzipiert ist.
ms.assetid: 700b6a3c-1046-4c21-8887-16f344c23510
keywords:
- ILockBytes-"STG", Implementierungen, Datei basiert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93dfe09ab0157d2d24d81b7bb2798e984d3848f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388056"
---
# <a name="ilockbytes---file-based-implementation"></a><span data-ttu-id="bbe14-104">ILockBytes-File-Based-Implementierung</span><span class="sxs-lookup"><span data-stu-id="bbe14-104">ILockBytes - File-Based Implementation</span></span>

<span data-ttu-id="bbe14-105">Wird für ein Bytearray-Objekt implementiert, das einem com-Verbund Dateispeicher Objekt zugrunde liegt und zum Lesen und schreiben direkt in eine Datenträger Datei konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="bbe14-105">Implemented on a byte array object underlying a COM compound file storage object, and designed to read and write directly to a disk file.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="bbe14-106">Verwendungs Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="bbe14-106">When to Use</span></span>

<span data-ttu-id="bbe14-107">Methoden von [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) werden von den Verbund Datei Implementierungen von [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) und [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) auf dem Verbund Dateispeicher Objekt aufgerufen, das durch einen Aufruf von [**stganatedocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)erstellt wurde, sodass Sie Sie nicht direkt aufrufen müssen.</span><span class="sxs-lookup"><span data-stu-id="bbe14-107">Methods of [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) are called from the compound file implementations of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) and [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) on the compound file storage object created through a call to [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), so you do not need to call them directly.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbe14-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bbe14-108">Remarks</span></span>

<span data-ttu-id="bbe14-109">Im folgenden finden Sie die Methoden der [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) -File-Based-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="bbe14-109">The following are the methods of the [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) File-Based Implementation.</span></span>

<dl> <dt>

<span data-ttu-id="bbe14-110"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes:: Read at**</span><span class="sxs-lookup"><span data-stu-id="bbe14-110"><span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes::ReadAt**</span></span>
</dt> <dd>

<span data-ttu-id="bbe14-111">Liest einen Byteblock aus einem angegebenen Offset am Anfang des Byte Arrays.</span><span class="sxs-lookup"><span data-stu-id="bbe14-111">Reads a block of bytes from a specified offset at the beginning of the byte-array.</span></span>

</dd> <dt>

<span data-ttu-id="bbe14-112"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes:: Write-at**</span><span class="sxs-lookup"><span data-stu-id="bbe14-112"><span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes::WriteAt**</span></span>
</dt> <dd>

<span data-ttu-id="bbe14-113">Schreibt einen Block von Bytes von einem angegebenen Offset am Anfang des Bytearrays.</span><span class="sxs-lookup"><span data-stu-id="bbe14-113">Writes a block of bytes from a specified offset at the beginning of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="bbe14-114"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes:: Flush**</span><span class="sxs-lookup"><span data-stu-id="bbe14-114"><span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes::Flush**</span></span>
</dt> <dd>

<span data-ttu-id="bbe14-115">Stellt sicher, dass alle internen Puffer, die von der [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) -Implementierung verwaltet werden, in den zugrunde liegenden physischen Speicher geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="bbe14-115">Ensures that any internal buffers maintained by the [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) implementation are written out to the underlying physical storage.</span></span>

</dd> <dt>

<span data-ttu-id="bbe14-116"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes:: SetSize**</span><span class="sxs-lookup"><span data-stu-id="bbe14-116"><span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes::SetSize**</span></span>
</dt> <dd>

<span data-ttu-id="bbe14-117">Legt die Größe des Bytearrays fest.</span><span class="sxs-lookup"><span data-stu-id="bbe14-117">Sets the size of the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="bbe14-118"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes:: LockRegion**</span><span class="sxs-lookup"><span data-stu-id="bbe14-118"><span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes::LockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="bbe14-119">Der *dwlocktypes* -Parameter ist auf Lock \_ onlyonce oder Lock \_ Exclusive festgelegt, wodurch der Zugriff auf gesperrte Regionen zugelassen oder eingeschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="bbe14-119">The *dwLockTypes* parameter is set to LOCK\_ONLYONCE or LOCK\_EXCLUSIVE, which will allow or restrict access to locked regions.</span></span>

</dd> <dt>

<span data-ttu-id="bbe14-120"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes:: UnlockRegion**</span><span class="sxs-lookup"><span data-stu-id="bbe14-120"><span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes::UnlockRegion**</span></span>
</dt> <dd>

<span data-ttu-id="bbe14-121">Diese Methode entsperrt den von [**ILockBytes:: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-lockregion)gesperrten Bereich.</span><span class="sxs-lookup"><span data-stu-id="bbe14-121">This method unlocks the region locked by [**ILockBytes::LockRegion**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-lockregion).</span></span>

</dd> <dt>

<span data-ttu-id="bbe14-122"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes:: stat**</span><span class="sxs-lookup"><span data-stu-id="bbe14-122"><span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes::Stat**</span></span>
</dt> <dd>

<span data-ttu-id="bbe14-123">Die von com bereitgestellte [**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) -Implementierung ruft die [**ILockBytes:: stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) -Methode auf, um Informationen zum Bytearray-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bbe14-123">The COM-provided [**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) implementation calls the [**ILockBytes::Stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) method to retrieve information about the byte array object.</span></span> <span data-ttu-id="bbe14-124">Wenn kein angemessener Name für das Bytearray vorhanden ist, gibt die von com bereitgestellte **ILockBytes:: stat** -Methode **null** im **pwcsName** -Member der [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="bbe14-124">If there is no reasonable name for the byte array, the COM-provided **ILockBytes::Stat** method returns **NULL** in the **pwcsName** member of the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="bbe14-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bbe14-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bbe14-126">**ILockBytes**</span><span class="sxs-lookup"><span data-stu-id="bbe14-126">**ILockBytes**</span></span>](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[<span data-ttu-id="bbe14-127">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="bbe14-127">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="bbe14-128">**IStream**</span><span class="sxs-lookup"><span data-stu-id="bbe14-128">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




