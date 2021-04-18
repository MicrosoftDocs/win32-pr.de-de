---
description: 'Die getsubobjectguidb-Methode ruft die GUID des untergeordneten Objekts ab, das diesem Zeitachsen Objekt zugeordnet ist. Diese Methode entspricht iamtimelineobj:: getsubobjectguid, empfängt aber einen BSTR-Wert.'
ms.assetid: 693cafda-78c8-4ba4-90d7-23fedcd1fc52
title: 'Iamtimelineobj:: getsubobjectguidb-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetSubObjectGUIDB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 903c6638eececd635af2facd964adabe26f0c106
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358331"
---
# <a name="iamtimelineobjgetsubobjectguidb-method"></a><span data-ttu-id="65311-104">Iamtimelineobj:: getsubobjectguidb-Methode</span><span class="sxs-lookup"><span data-stu-id="65311-104">IAMTimelineObj::GetSubObjectGUIDB method</span></span>

> [!Note]  
> <span data-ttu-id="65311-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="65311-105">\[Deprecated.</span></span> <span data-ttu-id="65311-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="65311-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="65311-107">Die- `GetSubObjectGUIDB` Methode ruft die GUID des untergeordneten Objekts ab, das diesem Zeitachsen Objekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="65311-107">The `GetSubObjectGUIDB` method retrieves the GUID of the subobject associated with this timeline object.</span></span> <span data-ttu-id="65311-108">Diese Methode entspricht [**iamtimelineobj:: getsubobjectguid**](iamtimelineobj-getsubobjectguid.md), empfängt aber einen **BSTR** -Wert.</span><span class="sxs-lookup"><span data-stu-id="65311-108">This method is equivalent to [**IAMTimelineObj::GetSubObjectGUID**](iamtimelineobj-getsubobjectguid.md), but receives a **BSTR** value.</span></span>

## <a name="syntax"></a><span data-ttu-id="65311-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="65311-109">Syntax</span></span>


```C++
HRESULT GetSubObjectGUIDB(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="65311-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="65311-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65311-111">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="65311-111">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="65311-112">Empfängt eine Zeichenfolge, die die untergeordnete GUID darstellt.</span><span class="sxs-lookup"><span data-stu-id="65311-112">Receives a string representing the subobject GUID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65311-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65311-113">Return value</span></span>

<span data-ttu-id="65311-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="65311-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="65311-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="65311-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="65311-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="65311-116">Remarks</span></span>

<span data-ttu-id="65311-117">Die-Methode ordnet Speicher für die Zeichenfolge zu.</span><span class="sxs-lookup"><span data-stu-id="65311-117">The method allocates memory for the string.</span></span> <span data-ttu-id="65311-118">Die Anwendung muss **SysFreeString** aufzurufen, um den Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="65311-118">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="65311-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="65311-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="65311-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="65311-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="65311-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="65311-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="65311-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65311-122">Requirements</span></span>



| <span data-ttu-id="65311-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65311-123">Requirement</span></span> | <span data-ttu-id="65311-124">Wert</span><span class="sxs-lookup"><span data-stu-id="65311-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65311-125">Header</span><span class="sxs-lookup"><span data-stu-id="65311-125">Header</span></span><br/>  | <dl> <span data-ttu-id="65311-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="65311-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="65311-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="65311-127">Library</span></span><br/> | <dl> <span data-ttu-id="65311-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="65311-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65311-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65311-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65311-130">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="65311-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="65311-131">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="65311-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




