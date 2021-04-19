---
title: Enableuservhd-Methode der Win32_TSSessionDirectory-Klasse
description: Aktiviert eine Benutzerprofil-VHD auf einem RDSH-Server.
ms.assetid: bb39fa19-38eb-4caf-ae81-2bccd901ee2f
ms.tgt_platform: multiple
keywords:
- Enableuservhd-Methode Remotedesktopdienste
- Enableuservhd-Methode Remotedesktopdienste, Win32_TSSessionDirectory-Klasse
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste, enableuservhd-Methode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.EnableUserVhd
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 464e105d2f8f0c80126e6b9ca5e5a383b2d17628
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346770"
---
# <a name="enableuservhd-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="e31f3-106">Enableuservhd-Methode der Win32- \_ Klasse "tssessiondirectory"</span><span class="sxs-lookup"><span data-stu-id="e31f3-106">EnableUserVhd method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="e31f3-107">Aktiviert eine Benutzerprofil-VHD auf einem RDSH-Server.</span><span class="sxs-lookup"><span data-stu-id="e31f3-107">Enables a user profile VHD on an RDSH server.</span></span>

## <a name="syntax"></a><span data-ttu-id="e31f3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e31f3-108">Syntax</span></span>


```mof
uint32 EnableUserVhd(
  [in] string UvhdShareUrl,
  [in] string UvhdRoamingPolicyXml
);
```



## <a name="parameters"></a><span data-ttu-id="e31f3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e31f3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e31f3-110">*Uvhdshareurl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e31f3-110">*UvhdShareUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e31f3-111">Der Speicherort der Freigabe, in der alle Benutzerprofil-VHDs gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="e31f3-111">The location of the share where all user profile VHDs are stored.</span></span>

</dd> <dt>

<span data-ttu-id="e31f3-112">*Uvhdroamingpolicyxml* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e31f3-112">*UvhdRoamingPolicyXml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e31f3-113">Die roamingrichtlinie für die Benutzerprofil-VHD.</span><span class="sxs-lookup"><span data-stu-id="e31f3-113">The roaming policy for the user profile VHD.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e31f3-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e31f3-114">Requirements</span></span>



| <span data-ttu-id="e31f3-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e31f3-115">Requirement</span></span> | <span data-ttu-id="e31f3-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e31f3-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e31f3-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e31f3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e31f3-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e31f3-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e31f3-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e31f3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e31f3-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e31f3-120">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="e31f3-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="e31f3-121">Namespace</span></span><br/>                | <span data-ttu-id="e31f3-122">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e31f3-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e31f3-123">MOF</span><span class="sxs-lookup"><span data-stu-id="e31f3-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e31f3-124"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e31f3-124"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e31f3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="e31f3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e31f3-126"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e31f3-126"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e31f3-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e31f3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e31f3-128">**Win32- \_ tssessiondirectory**</span><span class="sxs-lookup"><span data-stu-id="e31f3-128">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

 





