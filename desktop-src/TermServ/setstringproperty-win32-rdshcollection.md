---
title: SetStringProperty-Methode der Win32_RDSHCollection-Klasse (CertEnroll. h)
description: Aktualisiert den Wert der Zeichen folgen Eigenschaft eines Win32- \_ rdshcollection-Objekts.
ms.assetid: 6981b47a-5480-44f5-90e3-f64d439fa2aa
ms.tgt_platform: multiple
keywords:
- SetStringProperty-Methode Remotedesktopdienste
- SetStringProperty-Methode Remotedesktopdienste, Win32_RDSHCollection-Klasse
- Win32_RDSHCollection-Klasse Remotedesktopdienste, setStringProperty-Methode
topic_type:
- apiref
api_name:
- Win32_RDSHCollection.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2606c195822432138ee67576db54f945c6834cfd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342225"
---
# <a name="setstringproperty-method-of-the-win32_rdshcollection-class"></a><span data-ttu-id="f43fc-106">SetStringProperty-Methode der Win32 \_ rdshcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="f43fc-106">SetStringProperty method of the Win32\_RDSHCollection class</span></span>

<span data-ttu-id="f43fc-107">Aktualisiert den Wert der Zeichen folgen Eigenschaft eines [**Win32- \_ rdshcollection**](win32-rdshcollection.md) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="f43fc-107">Updates a string property value of a [**Win32\_RDSHCollection**](win32-rdshcollection.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="f43fc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f43fc-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="f43fc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f43fc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f43fc-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f43fc-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f43fc-111">Der Schlüssel, der die zu Aktualisier enswerte Eigenschaft identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f43fc-111">The key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="f43fc-112">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f43fc-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f43fc-113">Der neue Eigenschaftswert.</span><span class="sxs-lookup"><span data-stu-id="f43fc-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f43fc-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f43fc-114">Return value</span></span>

<span data-ttu-id="f43fc-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f43fc-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f43fc-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f43fc-116">Requirements</span></span>



| <span data-ttu-id="f43fc-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f43fc-117">Requirement</span></span> | <span data-ttu-id="f43fc-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f43fc-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f43fc-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f43fc-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f43fc-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="f43fc-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="f43fc-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f43fc-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f43fc-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f43fc-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="f43fc-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="f43fc-123">Namespace</span></span><br/>                | <span data-ttu-id="f43fc-124">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="f43fc-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="f43fc-125">Header</span><span class="sxs-lookup"><span data-stu-id="f43fc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f43fc-126"><dt>CertEnroll. h</dt></span><span class="sxs-lookup"><span data-stu-id="f43fc-126"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="f43fc-127">MOF</span><span class="sxs-lookup"><span data-stu-id="f43fc-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f43fc-128"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f43fc-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="f43fc-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f43fc-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f43fc-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f43fc-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="f43fc-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f43fc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f43fc-132">**Win32- \_ rdshcollection**</span><span class="sxs-lookup"><span data-stu-id="f43fc-132">**Win32\_RDSHCollection**</span></span>](win32-rdshcollection.md)
</dt> </dl>

 

 





