---
description: Deaktiviert dieses Plug & Play Gerät.
ms.assetid: 88d60218-7282-4d0e-9a2c-0ad1a8c96650
ms.tgt_platform: multiple
title: Deaktivieren der Methode der Win32_PnPEntity-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PnPEntity.Disable
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 59d08d14f8dbf32941554dcecc372d73c60bef60
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523395"
---
# <a name="disable-method-of-the-win32_pnpentity-class"></a><span data-ttu-id="8c2c6-103">Deaktivieren der Methode der Win32- \_ pnptity-Klasse</span><span class="sxs-lookup"><span data-stu-id="8c2c6-103">Disable method of the Win32\_PnPEntity class</span></span>

<span data-ttu-id="8c2c6-104">Deaktiviert dieses Plug & Play Gerät.</span><span class="sxs-lookup"><span data-stu-id="8c2c6-104">Disables this Plug and Play device.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c2c6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c2c6-105">Syntax</span></span>


```mof
Uint32 Disable(
  [out] boolean rebootNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="8c2c6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c2c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c2c6-107">*neubootbedarf* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8c2c6-107">*rebootNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8c2c6-108">Gibt an, ob ein Neustart erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="8c2c6-108">Whether a reboot is needed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8c2c6-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8c2c6-109">Requirements</span></span>



| <span data-ttu-id="8c2c6-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8c2c6-110">Requirement</span></span> | <span data-ttu-id="8c2c6-111">Wert</span><span class="sxs-lookup"><span data-stu-id="8c2c6-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8c2c6-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8c2c6-112">Minimum supported client</span></span><br/> | <span data-ttu-id="8c2c6-113">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8c2c6-113">Windows 10 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8c2c6-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8c2c6-114">Minimum supported server</span></span><br/> | <span data-ttu-id="8c2c6-115">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="8c2c6-115">Windows Server 2016</span></span><br/>                                                          |
| <span data-ttu-id="8c2c6-116">Namespace</span><span class="sxs-lookup"><span data-stu-id="8c2c6-116">Namespace</span></span><br/>                | <span data-ttu-id="8c2c6-117">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8c2c6-117">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8c2c6-118">MOF</span><span class="sxs-lookup"><span data-stu-id="8c2c6-118">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8c2c6-119"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8c2c6-119"><dt>Cimwin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8c2c6-120">DLL</span><span class="sxs-lookup"><span data-stu-id="8c2c6-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c2c6-121"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8c2c6-121"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8c2c6-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c2c6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c2c6-123">**Win32- \_ pnptity**</span><span class="sxs-lookup"><span data-stu-id="8c2c6-123">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
</dt> </dl>

 

 




