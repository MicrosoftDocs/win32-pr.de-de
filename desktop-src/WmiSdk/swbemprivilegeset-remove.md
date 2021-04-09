---
description: Die Remove-Methode des-Objekts von "Swap" löscht eine Berechtigung aus der Auflistung.
ms.assetid: 4c0b6d49-262c-4840-955b-35b16b68f29f
ms.tgt_platform: multiple
title: Taubemprivilegeset. Remove-Methode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
- ISWbemPrivilegeSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f277e291a4296253d7c0b1b11c694952ddc17ddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865659"
---
# <a name="swbemprivilegesetremove-method"></a><span data-ttu-id="bc3de-103">Taubemprivilegeset. Remove-Methode</span><span class="sxs-lookup"><span data-stu-id="bc3de-103">SWbemPrivilegeSet.Remove method</span></span>

<span data-ttu-id="bc3de-104">Die **Remove** -Methode des-Objekts von " [**Swap**](swbemprivilegeset.md) " löscht eine Berechtigung aus der Auflistung.</span><span class="sxs-lookup"><span data-stu-id="bc3de-104">The **Remove** method of the [**SWbemPrivilegeSet**](swbemprivilegeset.md) object deletes a privilege from the collection.</span></span>

<span data-ttu-id="bc3de-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="bc3de-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bc3de-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc3de-106">Syntax</span></span>


```VB
SWbemPrivilegeSet.Remove( _
  ByVal iPrivilege _
)
```



## <a name="parameters"></a><span data-ttu-id="bc3de-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc3de-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc3de-108">*iprivilege*</span><span class="sxs-lookup"><span data-stu-id="bc3de-108">*iPrivilege*</span></span> 
</dt> <dd>

<span data-ttu-id="bc3de-109">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bc3de-109">Required.</span></span> <span data-ttu-id="bc3de-110">Dies ist eine der WMI-Konstanten aus der [**wbemprivilegeenum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) -Gruppe.</span><span class="sxs-lookup"><span data-stu-id="bc3de-110">This is one of the WMI constants from the [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) group.</span></span> <span data-ttu-id="bc3de-111">Diese Konstanten sind im wesentlichen ganze Zahlen, die bestimmte Berechtigungen darstellen.</span><span class="sxs-lookup"><span data-stu-id="bc3de-111">These constants are essentially integers that represent specific privileges.</span></span> <span data-ttu-id="bc3de-112">Um beispielsweise die Berechtigung zu entfernen, mit der Sie ein Windows-System Herunterfahren können, verwenden Sie die " **wbemprivilegeshutdown** "-Konstante oder die numerische Entsprechung von "0x17".</span><span class="sxs-lookup"><span data-stu-id="bc3de-112">For example, to remove the privilege that allows you to shut down a Windows system, use the **wbemPrivilegeShutdown** constant or the numeric equivalent of 0x17.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc3de-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc3de-113">Return value</span></span>

<span data-ttu-id="bc3de-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="bc3de-114">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bc3de-115">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="bc3de-115">Error codes</span></span>

<span data-ttu-id="bc3de-116">Nach Abschluss der **Remove** -Methode kann das **Err** -Objekt einen der Fehlercodes in der folgenden Liste enthalten.</span><span class="sxs-lookup"><span data-stu-id="bc3de-116">Upon completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="bc3de-117">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="bc3de-117">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="bc3de-118">Unbekannter Fehler.</span><span class="sxs-lookup"><span data-stu-id="bc3de-118">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="bc3de-119">**wbemErrNotFound** -2147749890 (0x80041002 angezeigt)</span><span class="sxs-lookup"><span data-stu-id="bc3de-119">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="bc3de-120">Die angegebene Berechtigung ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="bc3de-120">Specified privilege does not exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc3de-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc3de-121">Requirements</span></span>



| <span data-ttu-id="bc3de-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc3de-122">Requirement</span></span> | <span data-ttu-id="bc3de-123">Wert</span><span class="sxs-lookup"><span data-stu-id="bc3de-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bc3de-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc3de-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bc3de-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bc3de-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bc3de-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc3de-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bc3de-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bc3de-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bc3de-128">Header</span><span class="sxs-lookup"><span data-stu-id="bc3de-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc3de-129"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc3de-129"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc3de-130">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="bc3de-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="bc3de-131"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bc3de-131"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bc3de-132">DLL</span><span class="sxs-lookup"><span data-stu-id="bc3de-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc3de-133"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc3de-133"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bc3de-134">CLSID</span><span class="sxs-lookup"><span data-stu-id="bc3de-134">CLSID</span></span><br/>                    | <span data-ttu-id="bc3de-135">CLSID- \_ Swap-taubemprivilegeset</span><span class="sxs-lookup"><span data-stu-id="bc3de-135">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="bc3de-136">IID</span><span class="sxs-lookup"><span data-stu-id="bc3de-136">IID</span></span><br/>                      | <span data-ttu-id="bc3de-137">IID \_ iswbemprivilegeset</span><span class="sxs-lookup"><span data-stu-id="bc3de-137">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="bc3de-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc3de-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc3de-139">**Swap-Privileg**</span><span class="sxs-lookup"><span data-stu-id="bc3de-139">**SWbemPrivilegeSet**</span></span>](swbemprivilegeset.md)
</dt> <dt>

[<span data-ttu-id="bc3de-140">**Austauschen von "taubemprivilegeset. Add"**</span><span class="sxs-lookup"><span data-stu-id="bc3de-140">**SWbemPrivilegeSet.Add**</span></span>](swbemprivilegeset-add.md)
</dt> </dl>

 

 




