---
title: GetInt32Property-Methode der Win32_RDSHServer-Klasse (Microsoft. Diagnostics. appanalysis. h)
description: Ruft einen ganzzahligen Eigenschafts Wert eines Win32- \_ rdshserver-Objekts ab.
ms.assetid: 4601e9cb-927b-4af8-a12b-09a8ca44c2f7
ms.tgt_platform: multiple
keywords:
- GetInt32Property-Methode Remotedesktopdienste
- GetInt32Property-Methode Remotedesktopdienste, Win32_RDSHServer-Klasse
- Win32_RDSHServer-Klasse Remotedesktopdienste, GetInt32Property-Methode
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a2427cfa19a84a8b8988cceacf3e0b836a031f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956679"
---
# <a name="getint32property-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="b87fd-106">GetInt32Property-Methode der Win32 \_ rdshserver-Klasse</span><span class="sxs-lookup"><span data-stu-id="b87fd-106">GetInt32Property method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="b87fd-107">Ruft einen ganzzahligen Eigenschafts Wert eines [**Win32- \_ rdshserver**](win32-rdshserver.md) -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="b87fd-107">Retrieves an integer property value of a [**Win32\_RDSHServer**](win32-rdshserver.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b87fd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b87fd-108">Syntax</span></span>


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a><span data-ttu-id="b87fd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b87fd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b87fd-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b87fd-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b87fd-111">Der Schlüssel, der die abzurufende Eigenschaft identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b87fd-111">The key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="b87fd-112">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b87fd-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b87fd-113">Empfängt den abgerufenen Eigenschafts Wert.</span><span class="sxs-lookup"><span data-stu-id="b87fd-113">Receives the retrieved property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b87fd-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b87fd-114">Return value</span></span>

<span data-ttu-id="b87fd-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b87fd-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b87fd-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b87fd-116">Requirements</span></span>



| <span data-ttu-id="b87fd-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b87fd-117">Requirement</span></span> | <span data-ttu-id="b87fd-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b87fd-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b87fd-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b87fd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b87fd-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b87fd-120">None supported</span></span><br/>                                                                                      |
| <span data-ttu-id="b87fd-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b87fd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b87fd-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b87fd-122">Windows Server 2012</span></span><br/>                                                                                 |
| <span data-ttu-id="b87fd-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="b87fd-123">Namespace</span></span><br/>                | <span data-ttu-id="b87fd-124">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="b87fd-124">Root\\CIMv2\\rdms</span></span><br/>                                                                                   |
| <span data-ttu-id="b87fd-125">Header</span><span class="sxs-lookup"><span data-stu-id="b87fd-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b87fd-126"><dt>Microsoft. Diagnostics. appanalysis. h</dt></span><span class="sxs-lookup"><span data-stu-id="b87fd-126"><dt>Microsoft.diagnostics.appanalysis.h</dt></span></span> </dl> |
| <span data-ttu-id="b87fd-127">MOF</span><span class="sxs-lookup"><span data-stu-id="b87fd-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b87fd-128"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="b87fd-128"><dt>RDManagement.mof</dt></span></span> </dl>                    |
| <span data-ttu-id="b87fd-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b87fd-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b87fd-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b87fd-130"><dt>RDMS.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="b87fd-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b87fd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b87fd-132">**Win32- \_ rdshserver**</span><span class="sxs-lookup"><span data-stu-id="b87fd-132">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





