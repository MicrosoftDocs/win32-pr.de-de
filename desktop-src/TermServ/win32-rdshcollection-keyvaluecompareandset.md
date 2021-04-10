---
title: Keyvaluecompareandset-Methode der Win32_RDSHCollection-Klasse
description: Vergleicht den angegebenen Schlüssel in der Auflistung mit einem comparand. Stimmen Sie zu, wird der Schlüssel auf einen neuen Wert festgelegt. Wenn der Schlüssel nicht vorhanden ist, fügt die Methode den Schlüssel in die Auflistung ein.
ms.assetid: ea6195b3-1a20-4d5b-b9a3-796976818b4f
ms.tgt_platform: multiple
keywords:
- Keyvaluecompareandset-Methode Remotedesktopdienste
- Keyvaluecompareandset-Methode Remotedesktopdienste, Win32_RDSHCollection-Klasse
- Win32_RDSHCollection-Klasse Remotedesktopdienste, keyvaluecompareandset-Methode
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.KeyValueCompareAndSet
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b90d703b40cf76f59cc3caf5d8f197f387cfe8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858805"
---
# <a name="keyvaluecompareandset-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="33e61-107">Keyvaluecompareandset-Methode der Win32 \_ rdshcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="33e61-107">KeyValueCompareAndSet method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="33e61-108">Vergleicht den angegebenen Schlüssel in der Auflistung mit einem comparand. Stimmen Sie zu, wird der Schlüssel auf einen neuen Wert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="33e61-108">Compares the specified key in the collection with a comparand; if they match, the key is set to a new value.</span></span> <span data-ttu-id="33e61-109">Wenn der Schlüssel nicht vorhanden ist, fügt die Methode den Schlüssel in die Auflistung ein.</span><span class="sxs-lookup"><span data-stu-id="33e61-109">If the key does not exist, the method will insert the key into the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="33e61-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="33e61-110">Syntax</span></span>


```mof
uint32 KeyValueCompareAndSet(
  [in]  string Key,
  [in]  string NewValue,
  [in]  string Comparand,
  [out] string InitialValue
);
```



## <a name="parameters"></a><span data-ttu-id="33e61-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="33e61-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33e61-112">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33e61-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33e61-113">Der zu vergleichende Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="33e61-113">The key to compare.</span></span>

</dd> <dt>

<span data-ttu-id="33e61-114">*NewValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33e61-114">*NewValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33e61-115">Der neue Wert.</span><span class="sxs-lookup"><span data-stu-id="33e61-115">The new value.</span></span>

</dd> <dt>

<span data-ttu-id="33e61-116">*Comparand* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="33e61-116">*Comparand* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33e61-117">Die Zeichenfolge, mit der der Schlüssel verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="33e61-117">The string to compare the key to.</span></span>

</dd> <dt>

<span data-ttu-id="33e61-118">*InitialValue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="33e61-118">*InitialValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="33e61-119">Bei Erfolg oder Fehler enthält den Anfangswert des Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="33e61-119">On success or failure, contains the initial value of the key.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33e61-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="33e61-120">Remarks</span></span>

<span data-ttu-id="33e61-121">Beachten Sie, dass diese Methode den Wert des Schlüssels abrufen kann und damit die Funktionalität von [**keyvalueget**](win32-rdshcollection-keyvalueget.md)kapselt.</span><span class="sxs-lookup"><span data-stu-id="33e61-121">Note that this method can retrieve the value of the key, and as such encapsulates the functionality of [**KeyValueGet**](win32-rdshcollection-keyvalueget.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="33e61-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="33e61-122">Requirements</span></span>



| <span data-ttu-id="33e61-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="33e61-123">Requirement</span></span> | <span data-ttu-id="33e61-124">Wert</span><span class="sxs-lookup"><span data-stu-id="33e61-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="33e61-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="33e61-125">Minimum supported client</span></span><br/> | <span data-ttu-id="33e61-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="33e61-126">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="33e61-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="33e61-127">Minimum supported server</span></span><br/> | <span data-ttu-id="33e61-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="33e61-128">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="33e61-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="33e61-129">Namespace</span></span><br/>                | <span data-ttu-id="33e61-130">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="33e61-130">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="33e61-131">MOF</span><span class="sxs-lookup"><span data-stu-id="33e61-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33e61-132"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="33e61-132"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="33e61-133">DLL</span><span class="sxs-lookup"><span data-stu-id="33e61-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33e61-134"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="33e61-134"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="33e61-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33e61-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33e61-136">**Win32- \_ rdshcollection**</span><span class="sxs-lookup"><span data-stu-id="33e61-136">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





