---
description: Aktiviert dieses Plug & Play Gerät.
ms.assetid: 8f2096c4-03b4-4005-9b97-0086f2b41080
ms.tgt_platform: multiple
title: Enable-Methode der Win32_PnPEntity-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.Enable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8f64c833a29f4df3b353a7e9782ffea39396cece
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345431"
---
# <a name="enable-method-of-the-win32_pnpentity-class"></a><span data-ttu-id="cf0db-103">Enable-Methode der Win32- \_ pnptity-Klasse</span><span class="sxs-lookup"><span data-stu-id="cf0db-103">Enable method of the Win32\_PnPEntity class</span></span>

<span data-ttu-id="cf0db-104">Aktiviert dieses Plug & Play Gerät.</span><span class="sxs-lookup"><span data-stu-id="cf0db-104">Enables this Plug and Play device.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf0db-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf0db-105">Syntax</span></span>


```mof
Uint32 Enable(
  [out] boolean rebootNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="cf0db-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf0db-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf0db-107">*neubootbedarf* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cf0db-107">*rebootNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf0db-108">Gibt an, ob ein Neustart erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cf0db-108">Whether a reboot is needed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf0db-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf0db-109">Requirements</span></span>



| <span data-ttu-id="cf0db-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf0db-110">Requirement</span></span> | <span data-ttu-id="cf0db-111">Wert</span><span class="sxs-lookup"><span data-stu-id="cf0db-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf0db-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf0db-112">Minimum supported client</span></span><br/> | <span data-ttu-id="cf0db-113">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf0db-113">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cf0db-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf0db-114">Minimum supported server</span></span><br/> | <span data-ttu-id="cf0db-115">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="cf0db-115">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="cf0db-116">Namespace</span><span class="sxs-lookup"><span data-stu-id="cf0db-116">Namespace</span></span><br/>                | <span data-ttu-id="cf0db-117">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="cf0db-117">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cf0db-118">MOF</span><span class="sxs-lookup"><span data-stu-id="cf0db-118">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf0db-119"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cf0db-119"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf0db-120">DLL</span><span class="sxs-lookup"><span data-stu-id="cf0db-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf0db-121"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf0db-121"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf0db-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf0db-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf0db-123">**Win32- \_ pnptity**</span><span class="sxs-lookup"><span data-stu-id="cf0db-123">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
</dt> </dl>

 

 




