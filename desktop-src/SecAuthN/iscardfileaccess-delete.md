---
description: Mit der Delete-Methode wird eine Datei an einem bestimmten Speicherort innerhalb des Smartcard-Dateisystems gelöscht.
ms.assetid: f51b0329-c5dc-4f70-a92e-19dc0dbc55f8
title: Iscardfileaccess::D Elete-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardFileAccess.Delete
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6331225cd3baf105682e2d275ad6be53f16f5b64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343599"
---
# <a name="iscardfileaccessdelete-method"></a><span data-ttu-id="86275-103">Iscardfileaccess::D Elete-Methode</span><span class="sxs-lookup"><span data-stu-id="86275-103">ISCardFileAccess::Delete method</span></span>

<span data-ttu-id="86275-104">\[Die **Delete** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="86275-104">\[The **Delete** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="86275-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="86275-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="86275-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="86275-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="86275-107">Mit der **Delete** -Methode wird eine Datei an einem bestimmten Speicherort innerhalb des [*Smartcard*](../secgloss/s-gly.md) -Dateisystems gelöscht.</span><span class="sxs-lookup"><span data-stu-id="86275-107">The **Delete** method deletes a file at a given location within the [*smart card*](../secgloss/s-gly.md) file system.</span></span>

## <a name="syntax"></a><span data-ttu-id="86275-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="86275-108">Syntax</span></span>


```C++
HRESULT Delete(
  [in] REFTYPE     refType,
  [in] BSTR        bstrPathSpec,
  [in] SCARD_FLAGS flags
);
```



## <a name="parameters"></a><span data-ttu-id="86275-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="86275-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86275-110">*RefType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86275-110">*refType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86275-111">Der Referenztyp, der in *bstrinpathspec* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="86275-111">Type of reference used in *bstrPathSpec*.</span></span>

<dl><span id="SC_TYPE_BY_NAME"></span><span id="sc_type_by_name"></span><dt>

<span data-ttu-id="86275-112">**SC- \_ Typ \_ nach \_ Name**</span><span class="sxs-lookup"><span data-stu-id="86275-112">**SC\_TYPE\_BY\_NAME**</span></span>
</dt><span id="SC_TYPE_BY_ID"></span><span id="sc_type_by_id"></span><dt>

<span data-ttu-id="86275-113">**SC- \_ Typ \_ nach \_ ID**</span><span class="sxs-lookup"><span data-stu-id="86275-113">**SC\_TYPE\_BY\_ID**</span></span>
</dt><span id="SC_TYPE_BY_SHORT"></span><span id="sc_type_by_short"></span><dt>

<span data-ttu-id="86275-114">**SC \_ - \_ Typ \_ kurz**</span><span class="sxs-lookup"><span data-stu-id="86275-114">**SC\_TYPE\_BY\_SHORT**</span></span>
</dt><span id="SC_TYPE_BY_ANY"></span><span id="sc_type_by_any"></span><dt>

<span data-ttu-id="86275-115">**SC- \_ Typ \_ nach \_ beliebigen**</span><span class="sxs-lookup"><span data-stu-id="86275-115">**SC\_TYPE\_BY\_ANY**</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="86275-116">*bstrinpathspec* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86275-116">*bstrPathSpec* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86275-117">Der Bezeichner der zu löschenden Datei.</span><span class="sxs-lookup"><span data-stu-id="86275-117">Identifier of the file to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="86275-118">*Flags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86275-118">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86275-119">Gibt an, ob sicheres Messaging verwendet werden muss und welche Daten vorab zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="86275-119">Specifies whether secure messaging has to be used and data preallocated.</span></span>

<dl><span id="SC_FL_SECURE_MESSAGING"></span><span id="sc_fl_secure_messaging"></span><dt>

<span data-ttu-id="86275-120">**SC \_ FL \_ Secure \_ Messaging**</span><span class="sxs-lookup"><span data-stu-id="86275-120">**SC\_FL\_SECURE\_MESSAGING**</span></span>
</dt><span id="SC_FL_PREALLOCATED"></span><span id="sc_fl_preallocated"></span><dt>

<span data-ttu-id="86275-121">**SC \_ FL, \_ vorab zugeordnet**</span><span class="sxs-lookup"><span data-stu-id="86275-121">**SC\_FL\_PREALLOCATED**</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86275-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="86275-122">Return value</span></span>

<span data-ttu-id="86275-123">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="86275-123">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="86275-124">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="86275-124">Return code</span></span>                                                                                  | <span data-ttu-id="86275-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86275-125">Description</span></span>                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="86275-126"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="86275-126"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="86275-127">Der Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="86275-127">Operation was completed successfully.</span></span><br/>          |
| <dl> <span data-ttu-id="86275-128"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="86275-128"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="86275-129">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="86275-129">Invalid parameter.</span></span><br/>                             |
| <dl> <span data-ttu-id="86275-130"><dt>**E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="86275-130"><dt>**E\_NOTIMPL**</dt></span></span> </dl>    | <span data-ttu-id="86275-131">Diese Methode wurde von der-Schnittstelle nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="86275-131">The interface has not implemented this method.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="86275-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86275-132">Remarks</span></span>

<span data-ttu-id="86275-133">Eine Liste aller Methoden, die durch diese Schnittstelle definiert werden, finden Sie unter [**iscardfileaccess**](iscardfileaccess.md).</span><span class="sxs-lookup"><span data-stu-id="86275-133">For a list of all the methods defined by this interface, see [**ISCardFileAccess**](iscardfileaccess.md).</span></span>

<span data-ttu-id="86275-134">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="86275-134">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="86275-135">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="86275-135">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="86275-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="86275-136">Requirements</span></span>



| <span data-ttu-id="86275-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="86275-137">Requirement</span></span> | <span data-ttu-id="86275-138">Wert</span><span class="sxs-lookup"><span data-stu-id="86275-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="86275-139">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="86275-139">Minimum supported client</span></span><br/> | <span data-ttu-id="86275-140">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86275-140">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="86275-141">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="86275-141">Minimum supported server</span></span><br/> | <span data-ttu-id="86275-142">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="86275-142">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="86275-143">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="86275-143">End of client support</span></span><br/>    | <span data-ttu-id="86275-144">Windows XP</span><span class="sxs-lookup"><span data-stu-id="86275-144">Windows XP</span></span><br/>                                |
| <span data-ttu-id="86275-145">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="86275-145">End of server support</span></span><br/>    | <span data-ttu-id="86275-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="86275-146">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="86275-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="86275-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86275-148">**Stelle**</span><span class="sxs-lookup"><span data-stu-id="86275-148">**Create**</span></span>](iscardfileaccess-create.md)
</dt> <dt>

[<span data-ttu-id="86275-149">**Iscardfileaccess**</span><span class="sxs-lookup"><span data-stu-id="86275-149">**ISCardFileAccess**</span></span>](iscardfileaccess.md)
</dt> </dl>

 

 
