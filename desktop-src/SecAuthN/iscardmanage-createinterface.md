---
description: Erstellt die angegebene-Schnittstelle.
ms.assetid: f4cfc407-b006-46a2-9751-834b532309ec
title: 'Iscardmanage:: up-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 99a3f7c1acd4266395917b47c81f044d5385b3d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217330"
---
# <a name="iscardmanagecreateinterface-method"></a><span data-ttu-id="80367-103">Iscardmanage:: up-Methode</span><span class="sxs-lookup"><span data-stu-id="80367-103">ISCardManage::CreateInterface method</span></span>

<span data-ttu-id="80367-104">\[Die **Methode "** Methode" ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="80367-104">\[The **CreateInterface** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="80367-105">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="80367-105">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="80367-106">Die **Methode "** Methode" erstellt die angegebene Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="80367-106">The **CreateInterface** method creates the specified interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="80367-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="80367-107">Syntax</span></span>


```C++
HRESULT CreateInterface(
  [in]  LPGUID    pguidInterface,
  [in]  BSTR      bstrName,
  [in]  LONG      *pUserData,
  [out] LPUNKNOWN *ppInterface
);
```



## <a name="parameters"></a><span data-ttu-id="80367-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="80367-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80367-109">*pguidinterface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80367-109">*pguidInterface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80367-110">Der GUID-Wert der zu erstellenden Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="80367-110">The GUID value of the interface to create.</span></span>

</dd> <dt>

<span data-ttu-id="80367-111">*bstrinname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80367-111">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80367-112">Der Name der Schnittstelle, die erstellt werden soll, wenn die GUID nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="80367-112">The name of the interface to create if the GUID is unavailable.</span></span> <span data-ttu-id="80367-113">Standard Werte sind "CryptoProvider".</span><span class="sxs-lookup"><span data-stu-id="80367-113">Standard values are "CryptoProvider".</span></span>

</dd> <dt>

<span data-ttu-id="80367-114">*puserdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="80367-114">*pUserData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80367-115">Zeiger auf benutzerspezifische Daten, die beim Erstellen einer Schnittstelle verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="80367-115">Pointer to user-specific data to use in the creation of an interface.</span></span>

</dd> <dt>

<span data-ttu-id="80367-116">*ppinterface* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="80367-116">*ppInterface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80367-117">Zeiger auf die zurückgegebene Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="80367-117">Pointer to the returned interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80367-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="80367-118">Return value</span></span>

<span data-ttu-id="80367-119">Folgende Rückgabewerte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="80367-119">The possible return values are the following:</span></span>



| <span data-ttu-id="80367-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="80367-120">Return code</span></span>                                                                                   | <span data-ttu-id="80367-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80367-121">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="80367-122"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="80367-122"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="80367-123">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="80367-123">Operation completed successfully.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="80367-124"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="80367-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="80367-125">Einer der angegebenen Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="80367-125">One of the supplied parameters are not valid.</span></span><br/>                                         |
| <dl> <span data-ttu-id="80367-126"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="80367-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="80367-127">Ein fehlerhafter Zeiger wurde entweder im *pguidinterface* -oder im *puserdata* -Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="80367-127">A bad pointer was passed in either the *pguidInterface* or the *pUserData* parameter.</span></span><br/> |
| <dl> <span data-ttu-id="80367-128"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="80367-128"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="80367-129">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="80367-129">Out of memory.</span></span><br/>                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="80367-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="80367-130">Remarks</span></span>

<span data-ttu-id="80367-131">Eine Liste aller Methoden, die von der [**iscardmanage**](iscardmanage.md) -Schnittstelle definiert werden, finden Sie unter **iscardmanage**.</span><span class="sxs-lookup"><span data-stu-id="80367-131">For a list of all the methods defined by the [**ISCardManage**](iscardmanage.md) interface, see **ISCardManage**.</span></span>

<span data-ttu-id="80367-132">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die [*Smartcard*](../secgloss/s-gly.md) zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="80367-132">In addition to the COM error codes listed above, this interface may return a [*smart card*](../secgloss/s-gly.md) error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="80367-133">Informationen zu smartcardfehlercodes finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="80367-133">For information about smart card error codes, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="80367-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80367-134">Requirements</span></span>



| <span data-ttu-id="80367-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80367-135">Requirement</span></span> | <span data-ttu-id="80367-136">Wert</span><span class="sxs-lookup"><span data-stu-id="80367-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="80367-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="80367-137">Minimum supported client</span></span><br/> | <span data-ttu-id="80367-138">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="80367-138">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="80367-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="80367-139">Minimum supported server</span></span><br/> | <span data-ttu-id="80367-140">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="80367-140">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="80367-141">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="80367-141">End of client support</span></span><br/>    | <span data-ttu-id="80367-142">Windows XP</span><span class="sxs-lookup"><span data-stu-id="80367-142">Windows XP</span></span><br/>                                |
| <span data-ttu-id="80367-143">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="80367-143">End of server support</span></span><br/>    | <span data-ttu-id="80367-144">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="80367-144">Windows Server 2003</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="80367-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80367-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80367-146">**Iscardmanage**</span><span class="sxs-lookup"><span data-stu-id="80367-146">**ISCardManage**</span></span>](iscardmanage.md)
</dt> </dl>

 

 
