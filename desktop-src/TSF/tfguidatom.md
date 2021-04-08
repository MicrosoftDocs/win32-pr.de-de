---
title: Tfguidatom (msctf. h)
description: Der tfguidatom-Datentyp identifiziert eine GUID in TSF. Ein tfguidatom wird durch Aufrufen von itfcategorymgr registerguid abgerufen.
ms.assetid: 91696612-1829-4052-81d1-eddc23278d35
keywords:
- Tfguidatom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c05d3c9a3bc7d725bf2df38069d7bc6112dad08b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102827"
---
# <a name="tfguidatom"></a><span data-ttu-id="3c85a-105">Tfguidatom</span><span class="sxs-lookup"><span data-stu-id="3c85a-105">TfGuidAtom</span></span>

<span data-ttu-id="3c85a-106">Der **tfguidatom** -Datentyp identifiziert eine **GUID** in TSF.</span><span class="sxs-lookup"><span data-stu-id="3c85a-106">The **TfGuidAtom** data type identifies a **GUID** within TSF.</span></span> <span data-ttu-id="3c85a-107">Ein **tfguidatom** wird durch Aufrufen von [**itfcategorymgr:: registerguid**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3c85a-107">A **TfGuidAtom** is obtained by calling [**ITfCategoryMgr::RegisterGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span></span>


```C++
typedef DWORD TfGuidAtom;
```



## <a name="remarks"></a><span data-ttu-id="3c85a-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3c85a-108">Remarks</span></span>

<span data-ttu-id="3c85a-109">Ein **tfguidatom** -Wert ist nur innerhalb des Prozesses gültig, von dem **itfcategorymgr:: registerguid** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3c85a-109">A **TfGuidAtom** value is only valid within the process that **ITfCategoryMgr::RegisterGUID** is called from.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c85a-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c85a-110">Requirements</span></span>



| <span data-ttu-id="3c85a-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c85a-111">Requirement</span></span> | <span data-ttu-id="3c85a-112">Wert</span><span class="sxs-lookup"><span data-stu-id="3c85a-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="3c85a-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c85a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="3c85a-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c85a-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="3c85a-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c85a-115">Minimum supported server</span></span><br/> | <span data-ttu-id="3c85a-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c85a-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="3c85a-117">Verteilbare Komponente</span><span class="sxs-lookup"><span data-stu-id="3c85a-117">Redistributable</span></span><br/>          | <span data-ttu-id="3c85a-118">TSF 1,0 unter Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="3c85a-118">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="3c85a-119">Header</span><span class="sxs-lookup"><span data-stu-id="3c85a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c85a-120"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c85a-120"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c85a-121">IDL</span><span class="sxs-lookup"><span data-stu-id="3c85a-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3c85a-122"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3c85a-122"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c85a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c85a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c85a-124">**ITF categorymgr:: GetGuid**</span><span class="sxs-lookup"><span data-stu-id="3c85a-124">**ITfCategoryMgr::GetGUID**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[<span data-ttu-id="3c85a-125">**ITF categorymgr:: isequaltf guidatom**</span><span class="sxs-lookup"><span data-stu-id="3c85a-125">**ITfCategoryMgr::IsEqualTfGuidAtom**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-isequaltfguidatom)
</dt> <dt>

[<span data-ttu-id="3c85a-126">**ITF categorymgr:: registerguid**</span><span class="sxs-lookup"><span data-stu-id="3c85a-126">**ITfCategoryMgr::RegisterGUID**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> </dl>

 

 





