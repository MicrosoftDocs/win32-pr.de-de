---
description: Stellt die Methoden bereit, die zur Unterstützung der Benutzer der anderen Smartcard-com-Schnittstellen erforderlich sind.
ms.assetid: ce81706b-9201-432e-b9d0-c758769e1040
title: Iscardtypeconfiguration-Schnittstelle (scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 8863d29e3ee0f4298410c332329b30fe37dd5048
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865039"
---
# <a name="iscardtypeconv-interface"></a><span data-ttu-id="eeabd-103">Iscardtypeconfiguration-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="eeabd-103">ISCardTypeConv interface</span></span>

<span data-ttu-id="eeabd-104">\[Die **iscardtypeconfiguration** -Schnittstelle ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="eeabd-104">\[The **ISCardTypeConv** interface is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="eeabd-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="eeabd-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="eeabd-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="eeabd-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="eeabd-107">Die **iscardtypeconfiguration** -Schnittstelle stellt die Methoden bereit, die zur Unterstützung der Benutzer der anderen [*Smartcard*](../secgloss/s-gly.md) -com-Schnittstellen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="eeabd-107">The **ISCardTypeConv** interface provides the methods needed to support the users of the other [*smart card*](../secgloss/s-gly.md) COM interfaces.</span></span> <span data-ttu-id="eeabd-108">Diese Schnittstelle wird nur aus Gründen der Abwärtskompatibilität bereitgestellt und sollte nicht mehr verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eeabd-108">This interface is provided for backward compatibility only and should no longer be used.</span></span>

## <a name="members"></a><span data-ttu-id="eeabd-109">Member</span><span class="sxs-lookup"><span data-stu-id="eeabd-109">Members</span></span>

<span data-ttu-id="eeabd-110">Die **iscardtypeconfiguration** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="eeabd-110">The **ISCardTypeConv** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="eeabd-111">**Iscardtypekonv** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="eeabd-111">**ISCardTypeConv** also has these types of members:</span></span>

-   [<span data-ttu-id="eeabd-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="eeabd-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="eeabd-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="eeabd-113">Methods</span></span>

<span data-ttu-id="eeabd-114">Die **iscardtypeconfiguration** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="eeabd-114">The **ISCardTypeConv** interface has these methods.</span></span>



| <span data-ttu-id="eeabd-115">Methode</span><span class="sxs-lookup"><span data-stu-id="eeabd-115">Method</span></span>                                                                              | <span data-ttu-id="eeabd-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="eeabd-116">Description</span></span>                                                                                                                             |
|:------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="eeabd-117">**Convertbytearraytbytebuffer**</span><span class="sxs-lookup"><span data-stu-id="eeabd-117">**ConvertByteArrayToByteBuffer**</span></span>](iscardtypeconv-convertbytearraytobytebuffer.md) | <span data-ttu-id="eeabd-118">Konvertiert ein typisches C/C++-Bytearray in einen universellen Puffer von Bytes (**IStream** -Objekt).</span><span class="sxs-lookup"><span data-stu-id="eeabd-118">Converts a typical C/C++ byte array into a universal buffer of bytes (**IStream** object).</span></span><br/>                                   |
| [<span data-ttu-id="eeabd-119">**Convertbytebuffertbytearray**</span><span class="sxs-lookup"><span data-stu-id="eeabd-119">**ConvertByteBufferToByteArray**</span></span>](iscardtypeconv-convertbytebuffertobytearray.md) | <span data-ttu-id="eeabd-120">Konvertiert ein Bytearray, das in einen universellen Puffer von Bytes (**IStream** -Objekt) zugeordnet ist, in ein typisches C/C++-Bytearray.</span><span class="sxs-lookup"><span data-stu-id="eeabd-120">Converts a byte array mapped into a universal buffer of bytes (**IStream** object) into a typical C/C++ byte array.</span></span><br/>          |
| [<span data-ttu-id="eeabd-121">**Convertbytebuffertysafearray**</span><span class="sxs-lookup"><span data-stu-id="eeabd-121">**ConvertByteBufferToSafeArray**</span></span>](iscardtypeconv-convertbytebuffertosafearray.md) | <span data-ttu-id="eeabd-122">Konvertiert ein Bytearray, das in einen universellen Puffer von Bytes (**IStream** -Objekt) zugeordnet ist, in ein SAFEARRAY vom Typ Ganzzahl ohne Vorzeichen char (Byte).</span><span class="sxs-lookup"><span data-stu-id="eeabd-122">Converts a byte array mapped into a universal buffer of bytes (**IStream** object) into a SAFEARRAY of unsigned char (byte).</span></span><br/> |
| [<span data-ttu-id="eeabd-123">**Converlanafearrayto ByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="eeabd-123">**ConvertSafeArrayToByteBuffer**</span></span>](iscardtypeconv-convertsafearraytobytebuffer.md) | <span data-ttu-id="eeabd-124">Konvertiert ein als SAFEARRAY definiertes Bytearray in einen universellen Puffer von Bytes (**IStream** -Objekt).</span><span class="sxs-lookup"><span data-stu-id="eeabd-124">Converts a byte array defined as a SAFEARRAY into a universal buffer of bytes (**IStream** object).</span></span><br/>                          |
| [<span data-ttu-id="eeabd-125">**"Kreatebytearray"**</span><span class="sxs-lookup"><span data-stu-id="eeabd-125">**CreateByteArray**</span></span>](iscardtypeconv-createbytearray.md)                           | <span data-ttu-id="eeabd-126">Erstellt ein Bytearray.</span><span class="sxs-lookup"><span data-stu-id="eeabd-126">Creates an array of bytes.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="eeabd-127">**"Kreatebytebuffer"**</span><span class="sxs-lookup"><span data-stu-id="eeabd-127">**CreateByteBuffer**</span></span>](iscardtypeconv-createbytebuffer.md)                         | <span data-ttu-id="eeabd-128">Erstellt einen universellen Puffer von Bytes, der einem **IStream** -Objekt ([**ibytebuffer**](ibytebuffer.md)) zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="eeabd-128">Creates a universal buffer of bytes mapped into an **IStream** ([**IByteBuffer**](ibytebuffer.md)) object.</span></span><br/>                  |
| [<span data-ttu-id="eeabd-129">**"Anatesafearray"**</span><span class="sxs-lookup"><span data-stu-id="eeabd-129">**CreateSafeArray**</span></span>](iscardtypeconv-createsafearray.md)                           | <span data-ttu-id="eeabd-130">Erstellt ein Automation SafeArray mit nicht signierten Zeichen (Bytes).</span><span class="sxs-lookup"><span data-stu-id="eeabd-130">Creates an Automation SAFEARRAY of unsigned characters (bytes).</span></span><br/>                                                              |
| [<span data-ttu-id="eeabd-131">**Freeistreammemoryptr**</span><span class="sxs-lookup"><span data-stu-id="eeabd-131">**FreeIStreamMemoryPtr**</span></span>](iscardtypeconv-freeistreammemoryptr.md)                 | <span data-ttu-id="eeabd-132">Gibt einen Speicher Zeiger auf den von einer **IStream** -com-Schnittstelle verwalteten HGLOBAL-Speicherblock frei.</span><span class="sxs-lookup"><span data-stu-id="eeabd-132">Frees a memory pointer to the HGLOBAL memory block managed by an **IStream** COM interface.</span></span><br/>                                  |
| [<span data-ttu-id="eeabd-133">**Getatistreammemory**</span><span class="sxs-lookup"><span data-stu-id="eeabd-133">**GetAtIStreamMemory**</span></span>](iscardtypeconv-getatistreammemory.md)                     | <span data-ttu-id="eeabd-134">Ruft einen Byte Zeiger auf den hglobal-Speicherblock ab, der von der **IStream** -com-Schnittstelle verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="eeabd-134">Acquires a byte pointer to the HGLOBAL memory block that is managed by the **IStream** COM interface.</span></span><br/>                        |
| [<span data-ttu-id="eeabd-135">**Sizeofstream**</span><span class="sxs-lookup"><span data-stu-id="eeabd-135">**SizeOfIStream**</span></span>](iscardtypeconv-sizeofistream.md)                               | <span data-ttu-id="eeabd-136">Bestimmt die Größe (Byte Anzahl) einer **IStream** -com-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="eeabd-136">Determines the size (number of bytes) of an **IStream** COM interface.</span></span><br/>                                                       |



 

## <a name="requirements"></a><span data-ttu-id="eeabd-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eeabd-137">Requirements</span></span>



| <span data-ttu-id="eeabd-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eeabd-138">Requirement</span></span> | <span data-ttu-id="eeabd-139">Wert</span><span class="sxs-lookup"><span data-stu-id="eeabd-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eeabd-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eeabd-140">Minimum supported client</span></span><br/> | <span data-ttu-id="eeabd-141">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eeabd-141">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="eeabd-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eeabd-142">Minimum supported server</span></span><br/> | <span data-ttu-id="eeabd-143">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eeabd-143">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="eeabd-144">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="eeabd-144">End of client support</span></span><br/>    | <span data-ttu-id="eeabd-145">Windows XP</span><span class="sxs-lookup"><span data-stu-id="eeabd-145">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="eeabd-146">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="eeabd-146">End of server support</span></span><br/>    | <span data-ttu-id="eeabd-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="eeabd-147">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="eeabd-148">Header</span><span class="sxs-lookup"><span data-stu-id="eeabd-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="eeabd-149"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="eeabd-149"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="eeabd-150">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="eeabd-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="eeabd-151"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eeabd-151"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eeabd-152">DLL</span><span class="sxs-lookup"><span data-stu-id="eeabd-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eeabd-153"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eeabd-153"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="eeabd-154">IID</span><span class="sxs-lookup"><span data-stu-id="eeabd-154">IID</span></span><br/>                      | <span data-ttu-id="eeabd-155">IID \_ iscardtypec ist als 53b6aa63-3F 56-11D0-916b-00aa00c18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="eeabd-155">IID\_ISCardTypeConv is defined as 53B6AA63-3F56-11D0-916B-00AA00C18068</span></span><br/>       |



 

 
