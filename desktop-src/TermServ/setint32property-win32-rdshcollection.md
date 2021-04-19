---
title: SetInt32Property-Methode der Win32_RDSHCollection-Klasse
description: Aktualisiert einen ganzzahligen Eigenschafts Wert eines Win32- \_ rdshcollection-Objekts.
ms.assetid: 2a9a5d83-d147-43b3-b57c-6c744da0923d
ms.tgt_platform: multiple
keywords:
- SetInt32Property-Methode Remotedesktopdienste
- SetInt32Property-Methode Remotedesktopdienste, Win32_RDSHCollection-Klasse
- Win32_RDSHCollection-Klasse Remotedesktopdienste, SetInt32Property-Methode
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 136bb8ccf34004f747829fb43ee8080ccd1d3132
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342656"
---
# <a name="setint32property-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="26cec-106">SetInt32Property-Methode der Win32 \_ rdshcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="26cec-106">SetInt32Property method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="26cec-107">Aktualisiert einen ganzzahligen Eigenschafts Wert eines [**Win32- \_ rdshcollection**](win32-rdshcollection.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="26cec-107">Updates an integer property value of a [**Win32\_RDSHCollection**](win32-rdshcollection.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="26cec-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="26cec-108">Syntax</span></span>


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="26cec-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="26cec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26cec-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26cec-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26cec-111">Der Schlüssel, der die zu Aktualisier enswerte Eigenschaft identifiziert.</span><span class="sxs-lookup"><span data-stu-id="26cec-111">The key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="26cec-112">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26cec-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26cec-113">Der neue Eigenschaftswert.</span><span class="sxs-lookup"><span data-stu-id="26cec-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26cec-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26cec-114">Return value</span></span>

<span data-ttu-id="26cec-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="26cec-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="26cec-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26cec-116">Requirements</span></span>



| <span data-ttu-id="26cec-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26cec-117">Requirement</span></span> | <span data-ttu-id="26cec-118">Wert</span><span class="sxs-lookup"><span data-stu-id="26cec-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="26cec-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="26cec-119">Minimum supported client</span></span><br/> | <span data-ttu-id="26cec-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="26cec-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="26cec-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="26cec-121">Minimum supported server</span></span><br/> | <span data-ttu-id="26cec-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="26cec-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="26cec-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="26cec-123">Namespace</span></span><br/>                | <span data-ttu-id="26cec-124">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="26cec-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="26cec-125">MOF</span><span class="sxs-lookup"><span data-stu-id="26cec-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="26cec-126"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="26cec-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="26cec-127">DLL</span><span class="sxs-lookup"><span data-stu-id="26cec-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="26cec-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26cec-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="26cec-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26cec-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26cec-130">**Win32- \_ rdshcollection**</span><span class="sxs-lookup"><span data-stu-id="26cec-130">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





