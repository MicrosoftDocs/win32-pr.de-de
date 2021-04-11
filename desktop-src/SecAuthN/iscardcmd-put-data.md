---
description: Legt das Datenfeld in der Application Protocol Data Unit (APDU) fest.
ms.assetid: 4508e00c-2b1d-4be5-b3a7-083b367a2158
title: Iscardcmd::p ut_Data-Methode (scarddat. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Data
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 58c1fa7d709eff1ed0618f52a83825f5110c4457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130260"
---
# <a name="iscardcmdput_data-method"></a><span data-ttu-id="c6e22-103">Iscardcmd::p UT- \_ Daten Methode</span><span class="sxs-lookup"><span data-stu-id="c6e22-103">ISCardCmd::put\_Data method</span></span>

<span data-ttu-id="c6e22-104">\[Die **Put \_ Data** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c6e22-104">\[The **put\_Data** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c6e22-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c6e22-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c6e22-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="c6e22-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="c6e22-107">Die **Put \_ Data** -Methode legt das Datenfeld in der [*Application Protocol Data Unit*](../secgloss/a-gly.md) (APDU) fest.</span><span class="sxs-lookup"><span data-stu-id="c6e22-107">The **put\_Data** method sets the data field in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span>

## <a name="syntax"></a><span data-ttu-id="c6e22-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6e22-108">Syntax</span></span>


```C++
HRESULT put_Data(
  [in] LPBYTEBUFFER pData
);
```



## <a name="parameters"></a><span data-ttu-id="c6e22-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6e22-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c6e22-110">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c6e22-110">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c6e22-111">Ein Zeiger auf das Byte Puffer Objekt (**IStream**), das in das APDU-Datenfeld kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6e22-111">Pointer to the byte buffer object (**IStream**) to be copied into the APDU data field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c6e22-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c6e22-112">Return value</span></span>

<span data-ttu-id="c6e22-113">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="c6e22-113">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="c6e22-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c6e22-114">Return code</span></span>                                                                                   | <span data-ttu-id="c6e22-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6e22-115">Description</span></span>                                     |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="c6e22-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c6e22-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c6e22-117">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c6e22-117">Operation completed successfully.</span></span><br/>    |
| <dl> <span data-ttu-id="c6e22-118"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="c6e22-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c6e22-119">Der *pData* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c6e22-119">The *pData* parameter is not valid.</span></span><br/>  |
| <dl> <span data-ttu-id="c6e22-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="c6e22-120"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c6e22-121">Ein fehlerhafter Zeiger wurde in *pData* übergeben.</span><span class="sxs-lookup"><span data-stu-id="c6e22-121">A bad pointer was passed in *pData*.</span></span><br/> |
| <dl> <span data-ttu-id="c6e22-122"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="c6e22-122"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c6e22-123">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="c6e22-123">Out of memory.</span></span><br/>                       |



 

## <a name="remarks"></a><span data-ttu-id="c6e22-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6e22-124">Remarks</span></span>

<span data-ttu-id="c6e22-125">Wenn Sie einen neuen Datenteil der Nachricht festlegen, wird die Länge des Daten Felds berechnet und im P3-Parameter von APDU gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c6e22-125">When you set a new data portion of the message, the length of the data field is calculated and stored in the P3 parameter of the APDU.</span></span> <span data-ttu-id="c6e22-126">Rufen [**Sie get \_ P3**](iscardcmd-get-p3.md)auf, um die Länge des Daten Felds abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c6e22-126">To retrieve the length of the data field, call [**get\_P3**](iscardcmd-get-p3.md).</span></span>

<span data-ttu-id="c6e22-127">Rufen [**Sie get \_ Data**](iscardcmd-get-data.md)auf, um das Datenfeld aus dem APDU abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c6e22-127">To retrieve the data field from the APDU, call [**get\_Data**](iscardcmd-get-data.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c6e22-128">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6e22-128">Examples</span></span>

<span data-ttu-id="c6e22-129">Im folgenden Beispiel wird gezeigt, wie das Datenfeld in der [*Anwendungsprotokoll Dateneinheit (Application Protocol Data Unit*](../secgloss/a-gly.md) , APDU) festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="c6e22-129">The following example shows how to set the data field in the [*application protocol data unit*](../secgloss/a-gly.md) (APDU).</span></span> <span data-ttu-id="c6e22-130">In diesem Beispiel wird davon ausgegangen, dass pibytedata ein gültiger Zeiger auf eine Instanz der [**ibytebuffer**](ibytebuffer.md) -Schnittstelle ist und dass "piscardcmd" ein gültiger Zeiger auf eine Instanz der [**iscardcmd**](iscardcmd.md) -Schnittstelle ist.</span><span class="sxs-lookup"><span data-stu-id="c6e22-130">The example assumes that pIByteData is a valid pointer to an instance of the [**IByteBuffer**](ibytebuffer.md) interface, and that pISCardCmd is a valid pointer to an instance of the [**ISCardCmd**](iscardcmd.md) interface.</span></span>


```C++
HRESULT    hr;

// pIByteData is a pointer to an instance of IByteBuffer.
// Set the data.
hr = pISCardCmd->put_Data(pIByteData);
if (FAILED(hr)) 
{
    printf("Failed put_Data.\n");
    // Take other error handling action as needed.
}
```



## <a name="requirements"></a><span data-ttu-id="c6e22-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6e22-131">Requirements</span></span>



| <span data-ttu-id="c6e22-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6e22-132">Requirement</span></span> | <span data-ttu-id="c6e22-133">Wert</span><span class="sxs-lookup"><span data-stu-id="c6e22-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c6e22-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c6e22-134">Minimum supported client</span></span><br/> | <span data-ttu-id="c6e22-135">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6e22-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c6e22-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c6e22-136">Minimum supported server</span></span><br/> | <span data-ttu-id="c6e22-137">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c6e22-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c6e22-138">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c6e22-138">End of client support</span></span><br/>    | <span data-ttu-id="c6e22-139">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c6e22-139">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="c6e22-140">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="c6e22-140">End of server support</span></span><br/>    | <span data-ttu-id="c6e22-141">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c6e22-141">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="c6e22-142">Header</span><span class="sxs-lookup"><span data-stu-id="c6e22-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6e22-143"><dt>"Scarddat. h"</dt></span><span class="sxs-lookup"><span data-stu-id="c6e22-143"><dt>Scarddat.h</dt></span></span> </dl>   |
| <span data-ttu-id="c6e22-144">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c6e22-144">Type library</span></span><br/>             | <dl> <span data-ttu-id="c6e22-145"><dt>Scarddat. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c6e22-145"><dt>Scarddat.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c6e22-146">DLL</span><span class="sxs-lookup"><span data-stu-id="c6e22-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6e22-147"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c6e22-147"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c6e22-148">IID</span><span class="sxs-lookup"><span data-stu-id="c6e22-148">IID</span></span><br/>                      | <span data-ttu-id="c6e22-149">IID \_ iscardcmd ist als D5778AE3-43DE-11D0-9171-00AA00C18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="c6e22-149">IID\_ISCardCmd is defined as D5778AE3-43DE-11D0-9171-00AA00C18068</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="c6e22-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6e22-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6e22-151">**\_Daten erhalten**</span><span class="sxs-lookup"><span data-stu-id="c6e22-151">**get\_Data**</span></span>](iscardcmd-get-data.md)
</dt> <dt>

[<span data-ttu-id="c6e22-152">**\_P3 erhalten**</span><span class="sxs-lookup"><span data-stu-id="c6e22-152">**get\_P3**</span></span>](iscardcmd-get-p3.md)
</dt> <dt>

[<span data-ttu-id="c6e22-153">**Iscardcmd**</span><span class="sxs-lookup"><span data-stu-id="c6e22-153">**ISCardCmd**</span></span>](iscardcmd.md)
</dt> </dl>

 

 
