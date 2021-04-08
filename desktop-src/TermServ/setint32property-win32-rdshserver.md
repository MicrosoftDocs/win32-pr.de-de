---
title: SetInt32Property-Methode der Win32_RDSHServer-Klasse
description: Aktualisiert einen ganzzahligen Eigenschafts Wert eines Win32- \_ rdshserver-Objekts.
ms.assetid: fa8df023-120d-4174-adc1-868f08fdce56
ms.tgt_platform: multiple
keywords:
- SetInt32Property-Methode Remotedesktopdienste
- SetInt32Property-Methode Remotedesktopdienste, Win32_RDSHServer-Klasse
- Win32_RDSHServer-Klasse Remotedesktopdienste, SetInt32Property-Methode
topic_type:
- apiref
api_name:
- Win32_RDSHServer.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66c22c8da9c046e0a42a6ec41f6ad5b3073c8d1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741297"
---
# <a name="setint32property-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="c18de-106">SetInt32Property-Methode der Win32 \_ rdshserver-Klasse</span><span class="sxs-lookup"><span data-stu-id="c18de-106">SetInt32Property method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="c18de-107">Aktualisiert einen ganzzahligen Eigenschafts Wert eines [**Win32- \_ rdshserver**](win32-rdshserver.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="c18de-107">Updates an integer property value of a [**Win32\_RDSHServer**](win32-rdshserver.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c18de-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c18de-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="c18de-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c18de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c18de-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c18de-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c18de-111">Der Schlüssel, der die zu Aktualisier enswerte Eigenschaft identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c18de-111">The key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="c18de-112">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c18de-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c18de-113">Der neue Eigenschaftswert.</span><span class="sxs-lookup"><span data-stu-id="c18de-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c18de-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c18de-114">Return value</span></span>

<span data-ttu-id="c18de-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c18de-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c18de-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c18de-116">Requirements</span></span>



| <span data-ttu-id="c18de-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c18de-117">Requirement</span></span> | <span data-ttu-id="c18de-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c18de-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="c18de-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c18de-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c18de-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c18de-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="c18de-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c18de-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c18de-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c18de-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="c18de-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="c18de-123">Namespace</span></span><br/>                | <span data-ttu-id="c18de-124">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="c18de-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="c18de-125">MOF</span><span class="sxs-lookup"><span data-stu-id="c18de-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c18de-126"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c18de-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="c18de-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c18de-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c18de-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c18de-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="c18de-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c18de-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c18de-130">**Win32- \_ rdshserver**</span><span class="sxs-lookup"><span data-stu-id="c18de-130">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





