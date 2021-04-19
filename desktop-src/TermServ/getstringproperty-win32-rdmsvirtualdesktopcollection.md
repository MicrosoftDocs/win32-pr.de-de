---
title: GetStringProperty-Methode der Win32_RDMSVirtualDesktopCollection-Klasse
description: Ruft eine Zeichen folgen Eigenschaft aus einer Sammlung virtueller Desktops ab.
ms.assetid: 4a122fc5-1635-4d74-a90d-2347c0714fc7
ms.tgt_platform: multiple
keywords:
- GetStringProperty-Methode Remotedesktopdienste
- GetStringProperty-Methode Remotedesktopdienste, Win32_RDMSVirtualDesktopCollection-Klasse
- Win32_RDMSVirtualDesktopCollection-Klasse Remotedesktopdienste, GetStringProperty-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d242d973d7ec8d320ed589933567b337a035f0e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339314"
---
# <a name="getstringproperty-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a><span data-ttu-id="1fd15-106">GetStringProperty-Methode der Win32 \_ rdmsvirtualdesktopcollection-Klasse</span><span class="sxs-lookup"><span data-stu-id="1fd15-106">GetStringProperty method of the Win32\_RDMSVirtualDesktopCollection class</span></span>

<span data-ttu-id="1fd15-107">Ruft eine Zeichen folgen Eigenschaft aus einer Sammlung virtueller Desktops ab.</span><span class="sxs-lookup"><span data-stu-id="1fd15-107">Retrieves a string property from a virtual desktop collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fd15-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fd15-108">Syntax</span></span>


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a><span data-ttu-id="1fd15-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fd15-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fd15-110">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1fd15-110">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fd15-111">Ein Schlüssel, der die abzurufende Eigenschaft identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1fd15-111">A key that identifies the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="1fd15-112">*Wert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1fd15-112">*Value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fd15-113">Eine Zeichenfolge, die den abgerufenen Wert empfängt.</span><span class="sxs-lookup"><span data-stu-id="1fd15-113">A string that receives the retrieved value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fd15-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1fd15-114">Return value</span></span>

<span data-ttu-id="1fd15-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1fd15-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fd15-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1fd15-116">Requirements</span></span>



| <span data-ttu-id="1fd15-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1fd15-117">Requirement</span></span> | <span data-ttu-id="1fd15-118">Wert</span><span class="sxs-lookup"><span data-stu-id="1fd15-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fd15-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1fd15-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1fd15-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1fd15-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="1fd15-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1fd15-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1fd15-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1fd15-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="1fd15-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="1fd15-123">Namespace</span></span><br/>                | <span data-ttu-id="1fd15-124">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="1fd15-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="1fd15-125">MOF</span><span class="sxs-lookup"><span data-stu-id="1fd15-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1fd15-126"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1fd15-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="1fd15-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1fd15-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fd15-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fd15-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="1fd15-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fd15-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fd15-130">**Win32 \_ rdmsvirtualdesktopcollection**</span><span class="sxs-lookup"><span data-stu-id="1fd15-130">**Win32\_RDMSVirtualDesktopCollection**</span></span>](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





