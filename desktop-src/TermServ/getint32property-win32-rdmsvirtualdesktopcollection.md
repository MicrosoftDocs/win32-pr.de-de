---
title: GetInt32Property-Methode der Win32_RDMSVirtualDesktopCollection-Klasse (Microsoft. Diagnostics. appanalysis. h)
description: Ruft eine ganzzahlige Eigenschaft aus einer Sammlung virtueller Desktops ab.
ms.assetid: 18ffca65-e7c0-4b17-902f-d74b2a81aba2
ms.tgt_platform: multiple
keywords:
- GetInt32Property-Methode Remotedesktopdienste
- GetInt32Property-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktopCollection-Klasse
- Win32_RDMSVirtualDesktopCollection-Klasse Remotedesktopdienste, GetInt32Property-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64e8e5518590bece8e8b904ea56bf7572b436b66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338523"
---
# <a name="getint32property-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="a96d5-106">GetInt32Property-Methode der Win32 \_ rdmsvirtualdesktopcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="a96d5-106">GetInt32Property method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="a96d5-107">Ruft eine ganzzahlige Eigenschaft aus einer Sammlung virtueller Desktops ab.</span><span class="sxs-lookup"><span data-stu-id="a96d5-107">Retrieves an integer property from a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a96d5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a96d5-108">Syntax</span></span>


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="a96d5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a96d5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a96d5-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a96d5-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a96d5-111">Ein Schlüssel, der die abzurufende Eigenschaft identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a96d5-111">A key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="a96d5-112">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a96d5-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a96d5-113">Eine ganze Zahl, die den abgerufenen Wert empfängt.</span><span class="sxs-lookup"><span data-stu-id="a96d5-113">An integer that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a96d5-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a96d5-114">Return value</span></span>

<span data-ttu-id="a96d5-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a96d5-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="a96d5-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a96d5-116">Requirements</span></span>



| <span data-ttu-id="a96d5-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a96d5-117">Requirement</span></span> | <span data-ttu-id="a96d5-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a96d5-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a96d5-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a96d5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a96d5-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a96d5-120">None supported</span></span><br/>                                                                                      |
| <span data-ttu-id="a96d5-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a96d5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a96d5-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a96d5-122">Windows Server 2012</span></span><br/>                                                                                 |
| <span data-ttu-id="a96d5-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="a96d5-123">Namespace</span></span><br/>                | <span data-ttu-id="a96d5-124">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="a96d5-124">Root\\CIMv2\\rdms</span></span><br/>                                                                                   |
| <span data-ttu-id="a96d5-125">Header</span><span class="sxs-lookup"><span data-stu-id="a96d5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a96d5-126"><dt>Microsoft. Diagnostics. appanalysis. h</dt></span><span class="sxs-lookup"><span data-stu-id="a96d5-126"><dt>Microsoft.diagnostics.appanalysis.h</dt></span></span> </dl> |
| <span data-ttu-id="a96d5-127">MOF</span><span class="sxs-lookup"><span data-stu-id="a96d5-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a96d5-128"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a96d5-128"><dt>RDManagement.mof</dt></span></span> </dl>                    |
| <span data-ttu-id="a96d5-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a96d5-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a96d5-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a96d5-130"><dt>RDMS.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="a96d5-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a96d5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a96d5-132">**Win32 \_ rdmsvirtualdesktopcollection**</span><span class="sxs-lookup"><span data-stu-id="a96d5-132">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





