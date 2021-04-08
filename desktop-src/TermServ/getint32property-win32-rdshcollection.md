---
title: GetInt32Property-Methode der Win32_RDSHCollection-Klasse (Microsoft. Diagnostics. appanalysis. h)
description: Ruft einen ganzzahligen Eigenschafts Wert eines Win32- \_ rdshcollection-Objekts ab.
ms.assetid: ab68f357-057d-4a36-ae39-f47198768a49
ms.tgt_platform: multiple
keywords:
- GetInt32Property-Methode Remotedesktopdienste
- GetInt32Property-Methode Remotedesktopdienste, Win32_RDSHCollection-Klasse
- Win32_RDSHCollection-Klasse Remotedesktopdienste, GetInt32Property-Methode
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5cc29234fe3bb1b92e68e728423931da965391f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740408"
---
# <a name="getint32property-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="cdbf2-106">GetInt32Property-Methode der Win32 \_ rdshcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="cdbf2-106">GetInt32Property method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="cdbf2-107">Ruft einen ganzzahligen Eigenschafts Wert eines [**Win32- \_ rdshcollection**](win32-rdshcollection.md) -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="cdbf2-107">Retrieves an integer property value of a [**Win32\_RDSHCollection**](win32-rdshcollection.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="cdbf2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cdbf2-108">Syntax</span></span>


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="cdbf2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cdbf2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cdbf2-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cdbf2-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cdbf2-111">Der Schlüssel, der die abzurufende Eigenschaft identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cdbf2-111">The key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="cdbf2-112">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cdbf2-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cdbf2-113">Empfängt den abgerufenen Eigenschafts Wert.</span><span class="sxs-lookup"><span data-stu-id="cdbf2-113">Receives the retrieved property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cdbf2-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cdbf2-114">Return value</span></span>

<span data-ttu-id="cdbf2-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cdbf2-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="cdbf2-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cdbf2-116">Requirements</span></span>



| <span data-ttu-id="cdbf2-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cdbf2-117">Requirement</span></span> | <span data-ttu-id="cdbf2-118">Wert</span><span class="sxs-lookup"><span data-stu-id="cdbf2-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cdbf2-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cdbf2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cdbf2-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cdbf2-120">None supported</span></span><br/>                                                                                      |
| <span data-ttu-id="cdbf2-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cdbf2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cdbf2-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="cdbf2-122">Windows Server 2012</span></span><br/>                                                                                 |
| <span data-ttu-id="cdbf2-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="cdbf2-123">Namespace</span></span><br/>                | <span data-ttu-id="cdbf2-124">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="cdbf2-124">Root\\CIMv2\\rdms</span></span><br/>                                                                                   |
| <span data-ttu-id="cdbf2-125">Header</span><span class="sxs-lookup"><span data-stu-id="cdbf2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cdbf2-126"><dt>Microsoft. Diagnostics. appanalysis. h</dt></span><span class="sxs-lookup"><span data-stu-id="cdbf2-126"><dt>Microsoft.diagnostics.appanalysis.h</dt></span></span> </dl> |
| <span data-ttu-id="cdbf2-127">MOF</span><span class="sxs-lookup"><span data-stu-id="cdbf2-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cdbf2-128"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cdbf2-128"><dt>RDManagement.mof</dt></span></span> </dl>                    |
| <span data-ttu-id="cdbf2-129">DLL</span><span class="sxs-lookup"><span data-stu-id="cdbf2-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cdbf2-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cdbf2-130"><dt>RDMS.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="cdbf2-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdbf2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cdbf2-132">**Win32- \_ rdshcollection**</span><span class="sxs-lookup"><span data-stu-id="cdbf2-132">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





