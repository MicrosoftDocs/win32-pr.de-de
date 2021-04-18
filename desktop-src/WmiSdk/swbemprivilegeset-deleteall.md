---
description: Mit der DeleteAll-Methode des Objekts "pulbemprivilegeset" werden alle Berechtigungen aus der Auflistung entfernt und somit geleert.
ms.assetid: 368caa14-1c53-4090-8569-97ea743905de
ms.tgt_platform: multiple
title: Taubemprivilegeset. DeleteAll-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.DeleteAll
- ISWbemPrivilegeSet.DeleteAll
- ISWbemPrivilegeSet.DeleteAll
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 382382b0c22c029f41c9ab33fb959287e5222d59
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352504"
---
# <a name="swbemprivilegesetdeleteall-method"></a><span data-ttu-id="50e17-103">Taubemprivilegeset. DeleteAll-Methode</span><span class="sxs-lookup"><span data-stu-id="50e17-103">SWbemPrivilegeSet.DeleteAll method</span></span>

<span data-ttu-id="50e17-104">Mit der **DeleteAll** -Methode des Objekts " [**pulbemprivilegeset**](swbemprivilegeset.md) " werden alle Berechtigungen aus der Auflistung entfernt und somit geleert.</span><span class="sxs-lookup"><span data-stu-id="50e17-104">The **DeleteAll** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object removes all privileges from the collection, thus emptying it.</span></span>

## <a name="syntax"></a><span data-ttu-id="50e17-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="50e17-105">Syntax</span></span>


```VB
SWbemPrivilegeSet.DeleteAll()
```



## <a name="parameters"></a><span data-ttu-id="50e17-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="50e17-106">Parameters</span></span>

<span data-ttu-id="50e17-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="50e17-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="50e17-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="50e17-108">Return value</span></span>

<span data-ttu-id="50e17-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="50e17-109">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="50e17-110">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="50e17-110">Error codes</span></span>

<span data-ttu-id="50e17-111">Nach Abschluss der **DeleteAll** -Methode kann das **Err** -Objekt den folgenden Fehlercode enthalten.</span><span class="sxs-lookup"><span data-stu-id="50e17-111">Upon the completion of the **DeleteAll** method, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="50e17-112">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="50e17-112">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="50e17-113">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="50e17-113">Unspecified error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50e17-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="50e17-114">Requirements</span></span>



| <span data-ttu-id="50e17-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="50e17-115">Requirement</span></span> | <span data-ttu-id="50e17-116">Wert</span><span class="sxs-lookup"><span data-stu-id="50e17-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="50e17-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="50e17-117">Minimum supported client</span></span><br/> | <span data-ttu-id="50e17-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50e17-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="50e17-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="50e17-119">Minimum supported server</span></span><br/> | <span data-ttu-id="50e17-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50e17-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="50e17-121">Header</span><span class="sxs-lookup"><span data-stu-id="50e17-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="50e17-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="50e17-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="50e17-123">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="50e17-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="50e17-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="50e17-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="50e17-125">DLL</span><span class="sxs-lookup"><span data-stu-id="50e17-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50e17-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50e17-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="50e17-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="50e17-127">CLSID</span></span><br/>                    | <span data-ttu-id="50e17-128">CLSID- \_ Swap-taubemprivilegeset</span><span class="sxs-lookup"><span data-stu-id="50e17-128">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="50e17-129">IID</span><span class="sxs-lookup"><span data-stu-id="50e17-129">IID</span></span><br/>                      | <span data-ttu-id="50e17-130">IID \_ iswbemprivilegeset</span><span class="sxs-lookup"><span data-stu-id="50e17-130">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="50e17-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50e17-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50e17-132">**Swap-Privileg**</span><span class="sxs-lookup"><span data-stu-id="50e17-132">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="50e17-133">Ausführen privilegierter Vorgänge</span><span class="sxs-lookup"><span data-stu-id="50e17-133">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="50e17-134">**"Swap-privilegeset. Remove"**</span><span class="sxs-lookup"><span data-stu-id="50e17-134">**SWbemPrivilegeSet.Remove**</span></span>](swbemprivilegeset-remove.md)
</dt> </dl>

 

 




