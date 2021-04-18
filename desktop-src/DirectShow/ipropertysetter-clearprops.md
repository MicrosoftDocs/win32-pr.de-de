---
description: Die clearrequirequismethode löscht alle Eigenschaften Daten aus dem Eigenschaften Setter. Die Anwendung kann neue Eigenschaften Daten festlegen, nachdem diese Funktion aufgerufen wurde.
ms.assetid: f3c31864-ddc3-4f3c-a097-2bab9d7f6a2a
title: 'Ipropertysetter:: clearrequiproperemethode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.ClearProps
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 62bb30b69ba0e4ba795b0d39af72a156b63cac11
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358264"
---
# <a name="ipropertysetterclearprops-method"></a><span data-ttu-id="c600b-104">Ipropertysetter:: clearrequismethode</span><span class="sxs-lookup"><span data-stu-id="c600b-104">IPropertySetter::ClearProps method</span></span>

> [!Note]  
> <span data-ttu-id="c600b-105">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c600b-105">\[Deprecated.</span></span> <span data-ttu-id="c600b-106">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="c600b-106">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c600b-107">Die- `ClearProps` Methode löscht alle Eigenschaften Daten aus dem Eigenschaften Setter.</span><span class="sxs-lookup"><span data-stu-id="c600b-107">The `ClearProps` method clears all property data from the property setter.</span></span> <span data-ttu-id="c600b-108">Die Anwendung kann neue Eigenschaften Daten festlegen, nachdem diese Funktion aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="c600b-108">The application can set new property data after calling this function.</span></span>

<span data-ttu-id="c600b-109">Wenn Sie die Eigenschafts Daten löschen, werden die Eigenschaften des Objekts nicht auf die ursprünglichen Werte wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="c600b-109">Clearing the property data does not restore the object's properties to their original values.</span></span> <span data-ttu-id="c600b-110">Dadurch wird lediglich verhindert, dass DirectShow weitere Änderungen anwendet.</span><span class="sxs-lookup"><span data-stu-id="c600b-110">It simply prevents DirectShow from applying any further changes.</span></span> <span data-ttu-id="c600b-111">Eigenschaftswerte werden zur Laufzeit angewendet, wenn das Projekt gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="c600b-111">Property values are applied at run time when the project renders.</span></span>

## <a name="syntax"></a><span data-ttu-id="c600b-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="c600b-112">Syntax</span></span>


```C++
HRESULT ClearProps();
```



## <a name="parameters"></a><span data-ttu-id="c600b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c600b-113">Parameters</span></span>

<span data-ttu-id="c600b-114">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c600b-114">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c600b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c600b-115">Return value</span></span>

<span data-ttu-id="c600b-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c600b-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c600b-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c600b-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c600b-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c600b-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c600b-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="c600b-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="c600b-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="c600b-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="c600b-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c600b-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c600b-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c600b-122">Requirements</span></span>



| <span data-ttu-id="c600b-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c600b-123">Requirement</span></span> | <span data-ttu-id="c600b-124">Wert</span><span class="sxs-lookup"><span data-stu-id="c600b-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c600b-125">Header</span><span class="sxs-lookup"><span data-stu-id="c600b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c600b-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="c600b-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="c600b-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c600b-127">Library</span></span><br/> | <dl> <span data-ttu-id="c600b-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="c600b-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c600b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c600b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c600b-130">**Ipropertysetter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c600b-130">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="c600b-131">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="c600b-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




