---
title: Imsrdpclientshell isremoteprogramclientinstallierte (Eigenschaft)
description: Ruft ab, ob der Remotedesktopverbindung-Client (RDC) Windows Server 2008 R2 RemoteApp-Funktionalität unterstützt.
ms.assetid: ce2fec74-c567-48e1-91d6-655c539d1fb9
ms.tgt_platform: multiple
keywords:
- Isremoteprogramclientinstallierte-Eigenschaft Remotedesktopdienste
- Isremoteprogramclientinstallierte-Eigenschaft Remotedesktopdienste, imsrdpclientshell-Schnittstelle
- Imsrdpclientshell-Schnittstelle Remotedesktopdienste, isremoteprogramclientinstallierte-Eigenschaft
topic_type:
- apiref
api_name:
- IMsRdpClientShell.IsRemoteProgramClientInstalled
- IMsRdpClientShell.get_IsRemoteProgramClientInstalled
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 787d45f10e109a89429be5032fda245aa3609567
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103270"
---
# <a name="imsrdpclientshellisremoteprogramclientinstalled-property"></a><span data-ttu-id="f0acf-106">Imsrdpclientshell:: isremoteprogramclientinstallierte-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="f0acf-106">IMsRdpClientShell::IsRemoteProgramClientInstalled property</span></span>

<span data-ttu-id="f0acf-107">Ruft ab, ob der Remotedesktopverbindung-Client (RDC) Windows Server 2008 R2 RemoteApp-Funktionalität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f0acf-107">Retrieves whether the Remote Desktop Connection (RDC) client supports Windows Server 2008 R2 RemoteApp functionality.</span></span>

<span data-ttu-id="f0acf-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f0acf-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0acf-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0acf-109">Syntax</span></span>


```C++
HRESULT get_IsRemoteProgramClientInstalled(
  [out] VARIANT_BOOL *pbClientInstalled
);
```



## <a name="property-value"></a><span data-ttu-id="f0acf-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="f0acf-110">Property value</span></span>

<span data-ttu-id="f0acf-111">Ruft ab, ob der Remotedesktopverbindung-Client (RDC) die RemoteApp-Funktionalität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f0acf-111">Retrieves whether the Remote Desktop Connection (RDC) client supports RemoteApp functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0acf-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f0acf-112">Requirements</span></span>



| <span data-ttu-id="f0acf-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f0acf-113">Requirement</span></span> | <span data-ttu-id="f0acf-114">Wert</span><span class="sxs-lookup"><span data-stu-id="f0acf-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0acf-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f0acf-115">Minimum supported client</span></span><br/> | <span data-ttu-id="f0acf-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f0acf-116">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f0acf-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f0acf-117">Minimum supported server</span></span><br/> | <span data-ttu-id="f0acf-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f0acf-118">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f0acf-119">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="f0acf-119">Type library</span></span><br/>             | <dl> <span data-ttu-id="f0acf-120"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0acf-120"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f0acf-121">DLL</span><span class="sxs-lookup"><span data-stu-id="f0acf-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0acf-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0acf-122"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f0acf-123">IID</span><span class="sxs-lookup"><span data-stu-id="f0acf-123">IID</span></span><br/>                      | <span data-ttu-id="f0acf-124">IID \_ imsrdpclientshell ist als d012ae6d-C19A-4bfe-b367-201f8911f134 definiert.</span><span class="sxs-lookup"><span data-stu-id="f0acf-124">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="f0acf-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0acf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0acf-126">**Imsrdpclientshell**</span><span class="sxs-lookup"><span data-stu-id="f0acf-126">**IMsRdpClientShell**</span></span>](imsrdpclientshell.md)
</dt> </dl>

 

 





