---
description: Die addprop-Methode fügt dem Eigenschaften Setter eine Eigenschaft mit einem Array von Zeit-Wert-Paaren hinzu, das den Wert der Eigenschaft für einen Zeitraum definiert.
ms.assetid: bf49e6ed-110d-4851-ace9-04d025f1d21f
title: 'Ipropertysetter:: addprop-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.AddProp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 230d97a3bcd5ac97359130755abd96742ae5340e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372259"
---
# <a name="ipropertysetteraddprop-method"></a><span data-ttu-id="38163-103">Ipropertysetter:: addprop-Methode</span><span class="sxs-lookup"><span data-stu-id="38163-103">IPropertySetter::AddProp method</span></span>

> [!Note]  
> <span data-ttu-id="38163-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="38163-104">\[Deprecated.</span></span> <span data-ttu-id="38163-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="38163-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="38163-106">Die- `AddProp` Methode fügt dem Eigenschaften Setter eine Eigenschaft mit einem Array von Zeit-Wert-Paaren hinzu, das den Wert der-Eigenschaft für einen Zeitraum definiert.</span><span class="sxs-lookup"><span data-stu-id="38163-106">The `AddProp` method adds a property to the property setter, with an array of time-value pairs defining the value of the property over a range of time.</span></span>

## <a name="syntax"></a><span data-ttu-id="38163-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="38163-107">Syntax</span></span>


```C++
HRESULT AddProp(
  [in] DEXTER_PARAM Param,
  [in] DEXTER_VALUE *paValue
);
```



## <a name="parameters"></a><span data-ttu-id="38163-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="38163-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38163-109">*Param* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38163-109">*Param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38163-110">[**Dexter \_ Param**](dexter-param.md) -Struktur, die die Eigenschaft angibt.</span><span class="sxs-lookup"><span data-stu-id="38163-110">[**DEXTER\_PARAM**](dexter-param.md) structure that specifies the property.</span></span> <span data-ttu-id="38163-111">Der **nvalues** -Member der-Struktur muss der Größe des Arrays entsprechen *, das im Parameter "* Parameter" angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="38163-111">The **nValues** member of the structure must equal the size of the array given in the *paValue* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="38163-112">*Wert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38163-112">*paValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38163-113">Zeiger auf ein Array von [**Dexter- \_ Wert**](dexter-value.md) -Strukturen, die Zeit Wert Paare enthalten.</span><span class="sxs-lookup"><span data-stu-id="38163-113">Pointer to an array of [**DEXTER\_VALUE**](dexter-value.md) structures that contain time-value pairs.</span></span> <span data-ttu-id="38163-114">Das Array muss sich in aufsteigender Zeitreihen Folge befinden.</span><span class="sxs-lookup"><span data-stu-id="38163-114">The array must be in ascending time order.</span></span> <span data-ttu-id="38163-115">Die Uhrzeiten sind relativ zur Startzeit des Effekts oder Übergangs.</span><span class="sxs-lookup"><span data-stu-id="38163-115">The times are relative to the starting time of the effect or transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38163-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38163-116">Return value</span></span>

<span data-ttu-id="38163-117">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="38163-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="38163-118">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="38163-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="38163-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="38163-119">Remarks</span></span>

<span data-ttu-id="38163-120">Die erste [**\_ Wert**](dexter-value.md) Struktur von "Dexter" muss eine Verweis Zeit von 0 (null) und ein Interpolations Flag (**dwinterp**) von **dexterf \_**, oder die Methode gibt einen Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="38163-120">The first [**DEXTER\_VALUE**](dexter-value.md) structure must specify a reference time of zero and an interpolation flag (**dwInterp**) of **DEXTERF\_JUMP**, or the method returns an error.</span></span>

> [!Note]  
> <span data-ttu-id="38163-121">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="38163-121">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="38163-122">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="38163-122">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="38163-123">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="38163-123">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="38163-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38163-124">Requirements</span></span>



| <span data-ttu-id="38163-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="38163-125">Requirement</span></span> | <span data-ttu-id="38163-126">Wert</span><span class="sxs-lookup"><span data-stu-id="38163-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38163-127">Header</span><span class="sxs-lookup"><span data-stu-id="38163-127">Header</span></span><br/>  | <dl> <span data-ttu-id="38163-128"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="38163-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="38163-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="38163-129">Library</span></span><br/> | <dl> <span data-ttu-id="38163-130"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="38163-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38163-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38163-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38163-132">**Ipropertysetter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="38163-132">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="38163-133">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="38163-133">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




