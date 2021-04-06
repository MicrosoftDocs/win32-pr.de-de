---
title: Ifilllockbytes-Implementierung
description: Das System stellt eine ifilllockbytes-Implementierung als Teil der Implementierung der Verbund Dateien bereit.
ms.assetid: a8aed8c5-3c4c-4cce-b568-68031da0edf5
keywords:
- Ifilllockbytes-"STG", Implementierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58737d02e3e6bc2511670178825aef8cbe2dcc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947685"
---
# <a name="ifilllockbytes---implementation"></a><span data-ttu-id="ee0f4-104">Ifilllockbytes-Implementierung</span><span class="sxs-lookup"><span data-stu-id="ee0f4-104">IFillLockBytes - Implementation</span></span>

<span data-ttu-id="ee0f4-105">Das System stellt eine [**ifilllockbytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) -Implementierung als Teil der Implementierung der Verbund Dateien bereit.</span><span class="sxs-lookup"><span data-stu-id="ee0f4-105">The system provides an [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) implementation as part of the Compound Files implementation.</span></span>

<span data-ttu-id="ee0f4-106">Beim Herunterladen von Code kann eine Instanz eines asynchronen Verbund Datei Objekts durch Aufrufen von [**stgopenasyncdocfileonifilllockbytes**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes)erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="ee0f4-106">Downloading code can create an instance of an asynchronous Compound File object by calling [**StgOpenAsyncDocFileOnIFillLockBytes**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes).</span></span> <span data-ttu-id="ee0f4-107">Durch das Herunterladen von Code kann auch eine Instanz eines asynchronen Byte Array-Wrapper Objekts für ein vorhandenes Datei-oder Bytearray erstellt werden, indem entweder die Funktion " [**stggetifilllockbytesonfile**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) " oder die Funktion " [**stggetifilllockbytesonilockbytes**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes) " aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="ee0f4-107">Downloading code can also create an instance of an asynchronous byte array wrapper object on an existing file or byte array by calling either the [**StgGetIFillLockBytesOnFile**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) function or the [**StgGetIFillLockBytesOnILockBytes**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes) function.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="ee0f4-108">Verwendungs Zeitpunkt</span><span class="sxs-lookup"><span data-stu-id="ee0f4-108">When to Use</span></span>

<span data-ttu-id="ee0f4-109">Derzeit sind URL-Moniker die einzigen Benutzer der asynchronen com-Speicher Implementierung.</span><span class="sxs-lookup"><span data-stu-id="ee0f4-109">Currently, URL monikers are the only users of the COM asynchronous storage implementation.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee0f4-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee0f4-110">Remarks</span></span>

<span data-ttu-id="ee0f4-111">Im folgenden finden Sie die vier Methoden der [**ifilllockbytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) -Implementierung.</span><span class="sxs-lookup"><span data-stu-id="ee0f4-111">The following are the four methods of the [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) implementation.</span></span>

<dl> <dt>

<span data-ttu-id="ee0f4-112"><span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**Ifilllockbytes:: fillappend**</span><span class="sxs-lookup"><span data-stu-id="ee0f4-112"><span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**IFillLockBytes::FillAppend**</span></span>
</dt> <dd>

<span data-ttu-id="ee0f4-113">Schreibt einen neuen Byte Block an das Ende eines Bytearrays.</span><span class="sxs-lookup"><span data-stu-id="ee0f4-113">Writes a new block of bytes to the end of a byte array.</span></span> <span data-ttu-id="ee0f4-114">Die Größe des Blocks wird als Parameter für [**fillappend**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend)angegeben.</span><span class="sxs-lookup"><span data-stu-id="ee0f4-114">The size of the block is specified as a parameter to [**FillAppend**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend).</span></span>

</dd> <dt>

<span data-ttu-id="ee0f4-115"><span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**Ifilllockbytes:: Fillat**</span><span class="sxs-lookup"><span data-stu-id="ee0f4-115"><span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**IFillLockBytes::FillAt**</span></span>
</dt> <dd>

<span data-ttu-id="ee0f4-116">Schreibt einen neuen Datenblock an eine angegebene Position im Bytearray.</span><span class="sxs-lookup"><span data-stu-id="ee0f4-116">Writes a new block of data to a specified location in the byte array.</span></span>

</dd> <dt>

<span data-ttu-id="ee0f4-117"><span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**Ifilllockbytes:: setfillsize**</span><span class="sxs-lookup"><span data-stu-id="ee0f4-117"><span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**IFillLockBytes::SetFillSize**</span></span>
</dt> <dd>

<span data-ttu-id="ee0f4-118">Legt die Größe des Bytearrays fest.</span><span class="sxs-lookup"><span data-stu-id="ee0f4-118">Sets the size of the byte array.</span></span> <span data-ttu-id="ee0f4-119">Gibt "E Fail" bei \_ Aufrufen von [**ILockBytes:: Read an**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat) zurück, die versuchen, auf Daten über die durch die-Methode angegebene Obergrenze hinaus zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="ee0f4-119">Returns E\_FAIL from calls to [**ILockBytes::ReadAt**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat) that attempt to access data beyond the upper limit specified by the method.</span></span>

</dd> <dt>

<span data-ttu-id="ee0f4-120"><span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**Ifilllockbytes:: beenden**</span><span class="sxs-lookup"><span data-stu-id="ee0f4-120"><span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**IFillLockBytes::Terminate**</span></span>
</dt> <dd>

<span data-ttu-id="ee0f4-121">Informiert das Bytearray, dass ein Download entweder erfolgreich oder erfolglos beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="ee0f4-121">Informs the byte array that a download has been terminated, either successfully or unsuccessfully.</span></span>

</dd> </dl>

 

 




