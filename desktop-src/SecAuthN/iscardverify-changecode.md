---
description: Ersetzt den aktuellen CHV-Code (Karteninhaber Überprüfung) durch neuen CHV-Code.
ms.assetid: 8d47d842-67e8-4948-a63b-49bcfc8a69a1
title: 'Iscardverify:: ChangeCode-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardVerify.ChangeCode
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6fcb6d79e6135293ad91e3ea18fa535ef4edbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757020"
---
# <a name="iscardverifychangecode-method"></a><span data-ttu-id="22e13-103">Iscardverify:: ChangeCode-Methode</span><span class="sxs-lookup"><span data-stu-id="22e13-103">ISCardVerify::ChangeCode method</span></span>

<span data-ttu-id="22e13-104">\[Die **ChangeCode** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="22e13-104">\[The **ChangeCode** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="22e13-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="22e13-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="22e13-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="22e13-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="22e13-107">Die **ChangeCode** -Methode ersetzt den aktuellen CHV-Code (Karteninhaber Überprüfung) durch neuen CHV-Code.</span><span class="sxs-lookup"><span data-stu-id="22e13-107">The **ChangeCode** method replaces the current CHV (card holder verification) code with new CHV code.</span></span>

## <a name="syntax"></a><span data-ttu-id="22e13-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="22e13-108">Syntax</span></span>


```C++
HRESULT ChangeCode(
  [in] LPBYTEBUFFER pOldCode,
  [in] LPBYTEBUFFER pNewCode,
  [in] SCARD_FLAGS  Flags,
  [in] LONG         lRef
);
```



## <a name="parameters"></a><span data-ttu-id="22e13-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="22e13-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22e13-110">*poldcode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22e13-110">*pOldCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22e13-111">Zeiger auf einen [**ibytebuffer**](ibytebuffer.md) , der den aktuellen Code des Benutzers enthält.</span><span class="sxs-lookup"><span data-stu-id="22e13-111">Pointer to an [**IByteBuffer**](ibytebuffer.md) containing the user's current code.</span></span>

</dd> <dt>

<span data-ttu-id="22e13-112">*pnewcode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22e13-112">*pNewCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22e13-113">Ein Zeiger auf einen [**ibytebuffer**](ibytebuffer.md) , der den neuen Code enthält, der während des Änderungs Vorgangs der [*Smartcard*](../secgloss/s-gly.md) angezeigt wird, um den Benutzer zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="22e13-113">Pointer to an [**IByteBuffer**](ibytebuffer.md) containing the new code that will be presented to the [*smart card*](../secgloss/s-gly.md) during the change process to authenticate the user.</span></span>

</dd> <dt>

<span data-ttu-id="22e13-114">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="22e13-114">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22e13-115">Gibt an, ob der Code Global oder lokal ist und ob der Code aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="22e13-115">Indicates whether the code is global or local, and whether the code should be enabled or disabled.</span></span>

<dl><span id="SC_FL_IHV_GLOBAL"></span><span id="sc_fl_ihv_global"></span><dt>

<span data-ttu-id="22e13-116">**SC \_ FL \_ IHV \_ Global**</span><span class="sxs-lookup"><span data-stu-id="22e13-116">**SC\_FL\_IHV\_GLOBAL**</span></span>
</dt><span id="SC_FL_IHV_LOCAL"></span><span id="sc_fl_ihv_local"></span><dt>

<span data-ttu-id="22e13-117">**SC \_ FL \_ IHV \_ local**</span><span class="sxs-lookup"><span data-stu-id="22e13-117">**SC\_FL\_IHV\_LOCAL**</span></span>
</dt><span id="SC_FL_IHV_ENABLE"></span><span id="sc_fl_ihv_enable"></span><dt>

<span data-ttu-id="22e13-118">**SC \_ FL \_ IHV \_ aktivieren**</span><span class="sxs-lookup"><span data-stu-id="22e13-118">**SC\_FL\_IHV\_ENABLE**</span></span>
</dt><span id="SC_FL_IHV_DISABLE"></span><span id="sc_fl_ihv_disable"></span><dt>

<span data-ttu-id="22e13-119">**SC \_ FL \_ IHV \_ Deaktivieren**</span><span class="sxs-lookup"><span data-stu-id="22e13-119">**SC\_FL\_IHV\_DISABLE**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="22e13-120">*lref* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="22e13-120">*lRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22e13-121">Smartcardspezifischer Verweis.</span><span class="sxs-lookup"><span data-stu-id="22e13-121">Smart card specific reference.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22e13-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22e13-122">Return value</span></span>

<span data-ttu-id="22e13-123">Die-Methode gibt einen der folgenden möglichen Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="22e13-123">The method returns one of the following possible values:</span></span>



| <span data-ttu-id="22e13-124">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="22e13-124">Return code</span></span>                                                                                   | <span data-ttu-id="22e13-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="22e13-125">Description</span></span>                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="22e13-126"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="22e13-126"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="22e13-127">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="22e13-127">Operation completed successfully.</span></span><br/> |
| <dl> <span data-ttu-id="22e13-128"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="22e13-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="22e13-129">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="22e13-129">Invalid parameter.</span></span><br/>                |
| <dl> <span data-ttu-id="22e13-130"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="22e13-130"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="22e13-131">Es wurde ein fehlerhafter Zeiger übermittelt.</span><span class="sxs-lookup"><span data-stu-id="22e13-131">A bad pointer was passed in.</span></span><br/>      |
| <dl> <span data-ttu-id="22e13-132"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="22e13-132"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="22e13-133">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="22e13-133">Out of memory.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="22e13-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="22e13-134">Remarks</span></span>

<span data-ttu-id="22e13-135">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardverify**](iscardverify.md).</span><span class="sxs-lookup"><span data-stu-id="22e13-135">For a list of all the methods defined by this interface, see [**ISCardVerify**](iscardverify.md).</span></span>

<span data-ttu-id="22e13-136">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="22e13-136">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="22e13-137">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="22e13-137">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="22e13-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="22e13-138">Requirements</span></span>



| <span data-ttu-id="22e13-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="22e13-139">Requirement</span></span> | <span data-ttu-id="22e13-140">Wert</span><span class="sxs-lookup"><span data-stu-id="22e13-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="22e13-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="22e13-141">Minimum supported client</span></span><br/> | <span data-ttu-id="22e13-142">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22e13-142">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="22e13-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="22e13-143">Minimum supported server</span></span><br/> | <span data-ttu-id="22e13-144">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="22e13-144">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="22e13-145">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="22e13-145">End of client support</span></span><br/>    | <span data-ttu-id="22e13-146">Windows XP</span><span class="sxs-lookup"><span data-stu-id="22e13-146">Windows XP</span></span><br/>                                |
| <span data-ttu-id="22e13-147">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="22e13-147">End of server support</span></span><br/>    | <span data-ttu-id="22e13-148">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="22e13-148">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="22e13-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22e13-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22e13-150">**Ibytebuffer**</span><span class="sxs-lookup"><span data-stu-id="22e13-150">**IByteBuffer**</span></span>](ibytebuffer.md)
</dt> <dt>

[<span data-ttu-id="22e13-151">**Iscardverify**</span><span class="sxs-lookup"><span data-stu-id="22e13-151">**ISCardVerify**</span></span>](iscardverify.md)
</dt> <dt>

[<span data-ttu-id="22e13-152">Smartcard-Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="22e13-152">Smart Card Return Values</span></span>](authentication-return-values.md)
</dt> </dl>

 

 
