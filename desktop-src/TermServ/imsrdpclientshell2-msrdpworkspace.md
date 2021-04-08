---
title: IMsRdpClientShell2 msrdpworkspace (Eigenschaft)
description: Ruft einen Zeiger auf die imsrdpworkspace-Schnittstelle ab, die zum Verwalten von RemoteApp-und Desktopverbindung Anmelde Informationen und Verbindungen verwendet wird.
ms.assetid: 5d505ce0-18cf-4e38-b1b8-026303f7069b
ms.tgt_platform: multiple
keywords:
- Msrdpworkspace-Eigenschaft Remotedesktopdienste
- Msrdpworkspace-Eigenschaft Remotedesktopdienste, IMsRdpClientShell2-Schnittstelle
- IMsRdpClientShell2 Interface Remotedesktopdienste, msrdpworkspace (Eigenschaft)
topic_type:
- apiref
api_name:
- IMsRdpClientShell2.MsRdpWorkspace
- IMsRdpClientShell2.get_MsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91eadd3f1b422e3da96d5bcd3a5178a2a0b0eb52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742400"
---
# <a name="imsrdpclientshell2msrdpworkspace-property"></a><span data-ttu-id="f3248-106">IMsRdpClientShell2:: msrdpworkspace (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f3248-106">IMsRdpClientShell2::MsRdpWorkspace property</span></span>

<span data-ttu-id="f3248-107">Ruft einen Zeiger auf die [**imsrdpworkspace**](imsrdpworkspace.md) -Schnittstelle ab, die zum Verwalten von RemoteApp-und Desktopverbindung Anmelde Informationen und Verbindungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f3248-107">Retrieves a pointer to the [**IMsRdpWorkspace**](imsrdpworkspace.md) interface, which is used to manage RemoteApp and Desktop Connection credentials and connections.</span></span>

<span data-ttu-id="f3248-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f3248-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3248-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3248-109">Syntax</span></span>


```C++
HRESULT get_MsRdpWorkspace(
  [out, retval] IMsRdpWorkspace **pVal
);
```



## <a name="property-value"></a><span data-ttu-id="f3248-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f3248-110">Property value</span></span>

<span data-ttu-id="f3248-111">Die Adresse eines Zeigers auf die [**imsrdpworkspace**](imsrdpworkspace.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f3248-111">The address of a pointer to the [**IMsRdpWorkspace**](imsrdpworkspace.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3248-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f3248-112">Remarks</span></span>

<span data-ttu-id="f3248-113">Die [**imsrdpworkspace**](imsrdpworkspace.md) -Schnittstelle wird nicht als benutzerdefinierte Schnittstelle verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="f3248-113">The [**IMsRdpWorkspace**](imsrdpworkspace.md) interface is not exposed as a custom interface.</span></span> <span data-ttu-id="f3248-114">Der Zugriff ist nur über [IDispatch](/windows/desktop/com/exposing-methods-through-idispatch) -Methoden möglich.</span><span class="sxs-lookup"><span data-stu-id="f3248-114">It is accessible through [IDispatch](/windows/desktop/com/exposing-methods-through-idispatch) methods only.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3248-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f3248-115">Requirements</span></span>



| <span data-ttu-id="f3248-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f3248-116">Requirement</span></span> | <span data-ttu-id="f3248-117">Wert</span><span class="sxs-lookup"><span data-stu-id="f3248-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3248-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f3248-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f3248-119">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f3248-119">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f3248-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f3248-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f3248-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="f3248-121">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="f3248-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f3248-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3248-123"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3248-123"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3248-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3248-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3248-125">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="f3248-125">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> </dl>

 

