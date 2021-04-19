---
title: SetStringProperty-Methode der Win32_RDMSVirtualDesktopCollection-Klasse (CertEnroll. h)
description: Aktualisiert eine Zeichen folgen Eigenschaft einer Sammlung virtueller Desktops.
ms.assetid: d76d5f77-3b51-41b9-8ec5-a737ddc0a9d3
ms.tgt_platform: multiple
keywords:
- SetStringProperty-Methode Remotedesktopdienste
- SetStringProperty-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktopCollection-Klasse
- Win32_RDMSVirtualDesktopCollection-Klasse Remotedesktopdienste, setStringProperty-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.SetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97fd85ef6611cd02dc80ca66816c5c4ce13f6cd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345907"
---
# <a name="setstringproperty-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="9fae2-106">SetStringProperty-Methode der Win32 \_ rdmsvirtualdesktopcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="9fae2-106">SetStringProperty method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="9fae2-107">Aktualisiert eine Zeichen folgen Eigenschaft einer Sammlung virtueller Desktops.</span><span class="sxs-lookup"><span data-stu-id="9fae2-107">Updates a string property of a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9fae2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9fae2-108">Syntax</span></span>


```mof
uint32 SetStringProperty(
  [in] string Key,
  [in] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="9fae2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9fae2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9fae2-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fae2-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fae2-111">Ein Schlüssel, der die zu Aktualisier enswerte Eigenschaft identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9fae2-111">A key that identifies the property to update.</span></span>

</dd> <dt>

<span data-ttu-id="9fae2-112">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9fae2-112">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9fae2-113">Der neue Eigenschaftswert.</span><span class="sxs-lookup"><span data-stu-id="9fae2-113">The new property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9fae2-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9fae2-114">Return value</span></span>

<span data-ttu-id="9fae2-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9fae2-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9fae2-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9fae2-116">Requirements</span></span>



| <span data-ttu-id="9fae2-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9fae2-117">Requirement</span></span> | <span data-ttu-id="9fae2-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9fae2-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fae2-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9fae2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9fae2-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9fae2-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="9fae2-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9fae2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9fae2-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9fae2-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="9fae2-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="9fae2-123">Namespace</span></span><br/>                | <span data-ttu-id="9fae2-124">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="9fae2-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="9fae2-125">Header</span><span class="sxs-lookup"><span data-stu-id="9fae2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9fae2-126"><dt>CertEnroll. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fae2-126"><dt>Certenroll.h</dt></span></span> </dl>     |
| <span data-ttu-id="9fae2-127">MOF</span><span class="sxs-lookup"><span data-stu-id="9fae2-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9fae2-128"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9fae2-128"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="9fae2-129">DLL</span><span class="sxs-lookup"><span data-stu-id="9fae2-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9fae2-130"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9fae2-130"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="9fae2-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fae2-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fae2-132">**Win32 \_ rdmsvirtualdesktopcollection**</span><span class="sxs-lookup"><span data-stu-id="9fae2-132">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





