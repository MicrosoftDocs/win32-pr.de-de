---
description: Die Create-Methode erstellt eine Datei an einem bestimmten Speicherort innerhalb des Smartcard-Dateisystems.
ms.assetid: 6bfe0b22-6aad-4818-bb2a-d5b0af4ee3a6
title: 'Iscardfileaccess:: Create-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Create
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2cfc7e1492505191a7912f23e5471f5fa72fdcd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129317"
---
# <a name="iscardfileaccesscreate-method"></a><span data-ttu-id="3edbb-103">Iscardfileaccess:: Create-Methode</span><span class="sxs-lookup"><span data-stu-id="3edbb-103">ISCardFileAccess::Create method</span></span>

<span data-ttu-id="3edbb-104">\[Die **Create** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="3edbb-104">\[The **Create** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3edbb-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3edbb-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="3edbb-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="3edbb-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="3edbb-107">Die **Create** -Methode erstellt eine Datei an einem bestimmten Speicherort innerhalb des [*Smartcard*](../secgloss/s-gly.md) -Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="3edbb-107">The **Create** method creates a file at a given location within the [*smart card*](../secgloss/s-gly.md) file system.</span></span>

## <a name="syntax"></a><span data-ttu-id="3edbb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3edbb-108">Syntax</span></span>


```C++
HRESULT Create(
  [in] REFTYPE      refType,
  [in] BSTR         bstrPathSpec,
  [in] TLV_TABLE    TLV,
  [in] SCARD_FLAGS  flags,
  [in] LPBYTEBUFFER pDataBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="3edbb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3edbb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3edbb-110">*RefType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3edbb-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3edbb-111">Der Referenztyp, der in *bstrinpathspec* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3edbb-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="3edbb-112">**SC- \_ Typ \_ nach \_ Name**</span><span class="sxs-lookup"><span data-stu-id="3edbb-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="3edbb-113">**SC- \_ Typ \_ nach \_ ID**</span><span class="sxs-lookup"><span data-stu-id="3edbb-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="3edbb-114">**SC \_ - \_ Typ \_ kurz**</span><span class="sxs-lookup"><span data-stu-id="3edbb-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="3edbb-115">**SC- \_ Typ \_ nach \_ beliebigen**</span><span class="sxs-lookup"><span data-stu-id="3edbb-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="3edbb-116">*bstrinpathspec* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3edbb-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3edbb-117">Die Datei-ID, die innerhalb des aktuellen Kontexts erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3edbb-117">File ID to be created within the current context.</span></span>

</dd> <dt>

<span data-ttu-id="3edbb-118">*TLV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3edbb-118">*TLV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3edbb-119">Liste der TLV-Strukturen (Tag, length, Wert), welche Werte festgelegt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="3edbb-119">List of TLV (tag,length,value) structures which values have to be set.</span></span>

</dd> <dt>

<span data-ttu-id="3edbb-120">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3edbb-120">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3edbb-121">Gibt an, ob sicheres Messaging verwendet werden muss und welche Daten vorab zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3edbb-121">Specifies whether secure messaging has to be used and data preallocated.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="3edbb-122">**SC \_ FL \_ Secure \_ Messaging**</span><span class="sxs-lookup"><span data-stu-id="3edbb-122">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

<span data-ttu-id="3edbb-123">**SC \_ FL, \_ vorab zugeordnet**</span><span class="sxs-lookup"><span data-stu-id="3edbb-123">**SC\_FL\_PREALLOCATED**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="3edbb-124">*pdatabuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3edbb-124">*pDataBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3edbb-125">Zeiger auf vorab zugeordnete Daten.</span><span class="sxs-lookup"><span data-stu-id="3edbb-125">Pointer to preallocated data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3edbb-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3edbb-126">Return value</span></span>

<span data-ttu-id="3edbb-127">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="3edbb-127">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="3edbb-128">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3edbb-128">Return code</span></span>                                                                                   | <span data-ttu-id="3edbb-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3edbb-129">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="3edbb-130"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3edbb-130"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="3edbb-131">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="3edbb-131">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="3edbb-132"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="3edbb-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="3edbb-133">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="3edbb-133">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="3edbb-134"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="3edbb-134"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="3edbb-135">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="3edbb-135">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="3edbb-136"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="3edbb-136"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="3edbb-137">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="3edbb-137">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="3edbb-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3edbb-138">Remarks</span></span>

<span data-ttu-id="3edbb-139">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardfileaccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="3edbb-139">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="3edbb-140">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="3edbb-140">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="3edbb-141">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="3edbb-141">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3edbb-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3edbb-142">Requirements</span></span>



| <span data-ttu-id="3edbb-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3edbb-143">Requirement</span></span> | <span data-ttu-id="3edbb-144">Wert</span><span class="sxs-lookup"><span data-stu-id="3edbb-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3edbb-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3edbb-145">Minimum supported client</span></span><br/> | <span data-ttu-id="3edbb-146">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3edbb-146">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="3edbb-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3edbb-147">Minimum supported server</span></span><br/> | <span data-ttu-id="3edbb-148">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3edbb-148">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3edbb-149">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="3edbb-149">End of client support</span></span><br/>    | <span data-ttu-id="3edbb-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="3edbb-150">Windows XP</span></span><br/>                                |
| <span data-ttu-id="3edbb-151">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="3edbb-151">End of server support</span></span><br/>    | <span data-ttu-id="3edbb-152">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3edbb-152">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="3edbb-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3edbb-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3edbb-154">**Iscardfileaccess**</span><span class="sxs-lookup"><span data-stu-id="3edbb-154">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
