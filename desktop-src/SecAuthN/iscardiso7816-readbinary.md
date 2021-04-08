---
description: Die Methode "Read Binary" erstellt einen APDU-Befehl (Application Protocol Data Unit), der eine Antwortnachricht abruft, die diesen Teil des Inhalts einer transparent strukturierten elementaren Datei enthält.
ms.assetid: 15394c21-1e07-4ea1-8f11-817e07b31f9b
title: 'ISCardISO7816:: Read Binary-Methode (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a29093d8725a3390df9837f4e2f395cfcf2eef29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867847"
---
# <a name="iscardiso7816readbinary-method"></a><span data-ttu-id="9dda6-103">ISCardISO7816:: Read Binary-Methode</span><span class="sxs-lookup"><span data-stu-id="9dda6-103">ISCardISO7816::ReadBinary method</span></span>

<span data-ttu-id="9dda6-104">\[Die Methode "read **Binary** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="9dda6-104">\[The **ReadBinary** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="9dda6-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9dda6-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9dda6-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="9dda6-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="9dda6-107">Die Methode "read **Binary** " erstellt einen APDU-Befehl ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ), der eine Antwortnachricht abruft, die diesen Teil des Inhalts einer transparent strukturierten elementaren Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="9dda6-107">The **ReadBinary** method constructs an [*application protocol data unit*](../secgloss/a-gly.md) (APDU) command that acquires a response message that gives that part of the contents of a transparent-structured elementary file.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dda6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9dda6-108">Syntax</span></span>


```C++
HRESULT ReadBinary(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="9dda6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9dda6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9dda6-110">*byP1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9dda6-110">*byP1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dda6-111">Das Feld P1-P2, versetzt zum ersten Byte, das am Anfang der Datei gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9dda6-111">The P1-P2 field, offset to the first byte to be read from the beginning of the file.</span></span> <span data-ttu-id="9dda6-112">Wenn "B8 = 1" in P1 ist, dann wird B7 und B6 von P1 auf NULL (RFU Bits) festgelegt. der Wert von B5 bis B1 von P1 ist ein kurzer EF-Bezeichner, und P2 ist der Offset des ersten Bytes, das in den Dateneinheiten vom Anfang der Datei gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9dda6-112">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span> <span data-ttu-id="9dda6-113">Wenn der Wert für "B8 = 0" in P1 \| \| beträgt, ist P1 P2 der Offset des ersten Bytes, das in Dateneinheiten vom Anfang der Datei gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9dda6-113">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="9dda6-114">*byP2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9dda6-114">*byP2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dda6-115">Das Feld P1-P2, versetzt zum ersten Byte, das am Anfang der Datei gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9dda6-115">The P1-P2 field, offset to the first byte to be read from the beginning of the file.</span></span> <span data-ttu-id="9dda6-116">Wenn "B8 = 1" in P1 ist, dann wird B7 und B6 von P1 auf NULL (RFU Bits) festgelegt. der Wert von B5 bis B1 von P1 ist ein kurzer EF-Bezeichner, und P2 ist der Offset des ersten Bytes, das in den Dateneinheiten vom Anfang der Datei gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9dda6-116">If b8=1 in P1, then b7 and b6 of P1 are set to zero (RFU bits), b5 to b1 of P1 are a short EF identifier and P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span> <span data-ttu-id="9dda6-117">Wenn der Wert für "B8 = 0" in P1 \| \| beträgt, ist P1 P2 der Offset des ersten Bytes, das in Dateneinheiten vom Anfang der Datei gelesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="9dda6-117">If b8=0 in P1, then P1\|\|P2 is the offset of the first byte to be read in data units from the beginning of the file.</span></span>

</dd> <dt>

<span data-ttu-id="9dda6-118">*lbytestoread* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9dda6-118">*lBytesToRead* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9dda6-119">Anzahl der Bytes, die aus dem transparenten EF gelesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9dda6-119">Number of bytes to read from the transparent EF.</span></span>

<span data-ttu-id="9dda6-120">Wenn das Feld "Le" nur Nullen enthält, sollten alle Bytes bis zum Ende der Datei in der Grenze von 256 für die kurze Länge oder 65536 für die erweiterte Länge gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="9dda6-120">If the Le field contains only zeros, then within the limit of 256 for short length or 65536 for extended length, all the bytes until the end of the file should be read.</span></span>

</dd> <dt>

<span data-ttu-id="9dda6-121">*ppcmd* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9dda6-121">*ppCmd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9dda6-122">Bei der Eingabe ein Zeiger auf ein [**iscardcmd**](iscardcmd.md) -Schnittstellen Objekt oder **null**.</span><span class="sxs-lookup"><span data-stu-id="9dda6-122">On input, a pointer to an [**ISCardCmd**](iscardcmd.md) interface object or **NULL**.</span></span>

<span data-ttu-id="9dda6-123">Bei der Rückgabe wird der Befehl mit dem von diesem Vorgang erstellten APDU-Befehl ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="9dda6-123">On return, it is filled with the APDU command constructed by this operation.</span></span> <span data-ttu-id="9dda6-124">Wenn *ppcmd* auf **null** festgelegt wurde, wird ein [*Smartcard*](../secgloss/s-gly.md) - [**iscardcmd**](iscardcmd.md) -Objekt intern erstellt und mit dem *ppcmd* -Zeiger zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9dda6-124">If *ppCmd* was set to **NULL**, a [*smart card*](../secgloss/s-gly.md) [**ISCardCmd**](iscardcmd.md) object is internally created and returned using the *ppCmd* pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9dda6-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9dda6-125">Return value</span></span>

<span data-ttu-id="9dda6-126">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="9dda6-126">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="9dda6-127">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9dda6-127">Return code</span></span>                                                                                   | <span data-ttu-id="9dda6-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9dda6-128">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="9dda6-129"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9dda6-129"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="9dda6-130">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="9dda6-130">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="9dda6-131"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="9dda6-131"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="9dda6-132">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="9dda6-132">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="9dda6-133"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="9dda6-133"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="9dda6-134">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="9dda6-134">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="9dda6-135"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="9dda6-135"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="9dda6-136">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="9dda6-136">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="9dda6-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9dda6-137">Remarks</span></span>

<span data-ttu-id="9dda6-138">Der gekapselte Befehl kann nur ausgeführt werden, wenn der Sicherheitsstatus der [*Smartcard*](../secgloss/s-gly.md) den Sicherheits Attributen der zu verarbeitenden elementaren Datei entspricht.</span><span class="sxs-lookup"><span data-stu-id="9dda6-138">The encapsulated command can only be performed if the security status of the [*smart card*](../secgloss/s-gly.md) satisfies the security attributes of the elementary file being processed.</span></span>

<span data-ttu-id="9dda6-139">Wenn der Befehl einen gültigen kurzen elementaren Bezeichner enthält, wird die Datei als aktuelle elementare Datei festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9dda6-139">When the command contains a valid short elementary identifier, it sets the file as current elementary file.</span></span>

<span data-ttu-id="9dda6-140">Elementare Dateien ohne transparente Struktur können nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="9dda6-140">Elementary files without a transparent structure cannot be erased.</span></span> <span data-ttu-id="9dda6-141">Der gekapselte Befehl wird abgebrochen, wenn er auf eine elementare Datei ohne transparente Struktur angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9dda6-141">The encapsulated command aborts if applied to an elementary file without a transparent structure.</span></span>

<span data-ttu-id="9dda6-142">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**ISCardISO7816**](iscardiso7816.md).</span><span class="sxs-lookup"><span data-stu-id="9dda6-142">For a list of all the methods provided by this interface, see [**ISCardISO7816**](iscardiso7816.md).</span></span>

<span data-ttu-id="9dda6-143">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="9dda6-143">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="9dda6-144">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="9dda6-144">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9dda6-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9dda6-145">Requirements</span></span>



| <span data-ttu-id="9dda6-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9dda6-146">Requirement</span></span> | <span data-ttu-id="9dda6-147">Wert</span><span class="sxs-lookup"><span data-stu-id="9dda6-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9dda6-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9dda6-148">Minimum supported client</span></span><br/> | <span data-ttu-id="9dda6-149">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9dda6-149">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9dda6-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9dda6-150">Minimum supported server</span></span><br/> | <span data-ttu-id="9dda6-151">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9dda6-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9dda6-152">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9dda6-152">End of client support</span></span><br/>    | <span data-ttu-id="9dda6-153">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9dda6-153">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="9dda6-154">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="9dda6-154">End of server support</span></span><br/>    | <span data-ttu-id="9dda6-155">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9dda6-155">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="9dda6-156">Header</span><span class="sxs-lookup"><span data-stu-id="9dda6-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="9dda6-157"><dt>"Scardssp. h"</dt></span><span class="sxs-lookup"><span data-stu-id="9dda6-157"><dt>Scardssp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9dda6-158">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="9dda6-158">Type library</span></span><br/>             | <dl> <span data-ttu-id="9dda6-159"><dt>Scardsrv. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9dda6-159"><dt>Scardsrv.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9dda6-160">DLL</span><span class="sxs-lookup"><span data-stu-id="9dda6-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9dda6-161"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9dda6-161"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9dda6-162">IID</span><span class="sxs-lookup"><span data-stu-id="9dda6-162">IID</span></span><br/>                      | <span data-ttu-id="9dda6-163">IID \_ ISCardISO7816 ist als 53b6aa68-3F 56-11D0-916b-00aa00c18068 definiert</span><span class="sxs-lookup"><span data-stu-id="9dda6-163">IID\_ISCardISO7816 is defined as 53B6AA68-3F56-11D0-916B-00AA00C18068</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="9dda6-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9dda6-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dda6-165">**Erasebinary**</span><span class="sxs-lookup"><span data-stu-id="9dda6-165">**EraseBinary**</span></span>](iscardiso7816-erasebinary.md)
</dt> <dt>

[<span data-ttu-id="9dda6-166">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="9dda6-166">**ISCardISO7816**</span></span>](iscardiso7816.md)
</dt> <dt>

[<span data-ttu-id="9dda6-167">**Updatebinary**</span><span class="sxs-lookup"><span data-stu-id="9dda6-167">**UpdateBinary**</span></span>](iscardiso7816-updatebinary.md)
</dt> <dt>

[<span data-ttu-id="9dda6-168">**"Write Binary"**</span><span class="sxs-lookup"><span data-stu-id="9dda6-168">**WriteBinary**</span></span>](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
