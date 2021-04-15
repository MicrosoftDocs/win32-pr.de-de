---
title: Getvirtualdesktopdetails-Methode der Win32_RDMSVirtualDesktop-Klasse
description: Ruft die zusätzlichen Informationen zum virtuellen Desktop ab.
ms.assetid: 487e3a02-4306-4639-a44e-5b9519163a67
ms.tgt_platform: multiple
keywords:
- Getvirtualdesktopdetails-Methode Remotedesktopdienste
- Getvirtualdesktopdetails-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktop-Klasse
- Win32_RDMSVirtualDesktop-Klasse Remotedesktopdienste, getvirtualdesktopdetails-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktop.GetVirtualDesktopDetails
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7382a7ea10b3e557cd7317bdf1ddb0c4bcea55d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477445"
---
# <a name="getvirtualdesktopdetails-method-of-the-win32_rdmsvirtualdesktop-class"></a><span data-ttu-id="62ad6-106">Getvirtualdesktopdetails-Methode der Win32 \_ -Klasse rdmsvirtualdesktop</span><span class="sxs-lookup"><span data-stu-id="62ad6-106">GetVirtualDesktopDetails method of the Win32\_RDMSVirtualDesktop class</span></span>

<span data-ttu-id="62ad6-107">Ruft die zusätzlichen Informationen zum virtuellen Desktop ab.</span><span class="sxs-lookup"><span data-stu-id="62ad6-107">Retrieves the additional information about the virtual desktop.</span></span>

## <a name="syntax"></a><span data-ttu-id="62ad6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="62ad6-108">Syntax</span></span>


```mof
uint32 GetVirtualDesktopDetails(
  [out] uint32  RAMSizeInMB,
  [out] boolean RemoteFXEnabled,
  [out] string  OSVersion
);
```



## <a name="parameters"></a><span data-ttu-id="62ad6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="62ad6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62ad6-110">*Ramsizzumb* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="62ad6-110">*RAMSizeInMB* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62ad6-111">Empfängt die dem virtuellen Desktop zugewiesene RAM-Größe in Bytes.</span><span class="sxs-lookup"><span data-stu-id="62ad6-111">Receives the amount of RAM assigned to the virtual desktop, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="62ad6-112">*Remotefxaktiviert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="62ad6-112">*RemoteFXEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62ad6-113">Empfängt einen Wert, der angibt, ob remotefx auf dem virtuellen Desktop aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="62ad6-113">Receives a value that indicates whether RemoteFX is enabled on the virtual desktop.</span></span> <span data-ttu-id="62ad6-114">**True** , wenn remotefx aktiviert ist. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="62ad6-114">**TRUE** if RemoteFX is enabled; otherwise, **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="62ad6-115">*OSVersion* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="62ad6-115">*OSVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="62ad6-116">Empfängt die Betriebssystemversion des virtuellen Desktops.</span><span class="sxs-lookup"><span data-stu-id="62ad6-116">Receives the OS version of the virtual desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62ad6-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62ad6-117">Return value</span></span>

<span data-ttu-id="62ad6-118">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="62ad6-118">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="62ad6-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62ad6-119">Requirements</span></span>



| <span data-ttu-id="62ad6-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62ad6-120">Requirement</span></span> | <span data-ttu-id="62ad6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="62ad6-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="62ad6-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62ad6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="62ad6-123">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="62ad6-123">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="62ad6-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62ad6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="62ad6-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="62ad6-125">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="62ad6-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="62ad6-126">Namespace</span></span><br/>                | <span data-ttu-id="62ad6-127">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="62ad6-127">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="62ad6-128">MOF</span><span class="sxs-lookup"><span data-stu-id="62ad6-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62ad6-129"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="62ad6-129"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="62ad6-130">DLL</span><span class="sxs-lookup"><span data-stu-id="62ad6-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62ad6-131"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62ad6-131"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="62ad6-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62ad6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62ad6-133">**Win32 \_ rdmsvirtualdesktop**</span><span class="sxs-lookup"><span data-stu-id="62ad6-133">**Win32\_RDMSVirtualDesktop**</span></span>](win32-rdmsvirtualdesktop.md)
</dt> </dl>

 

 





