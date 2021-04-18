---
description: Die printxml-Methode konvertiert Eigenschafts Daten in eine XML-Zeichenfolge.
ms.assetid: 24638489-b5ed-4bdd-b40e-6d61c0db1533
title: Ipropertysetter::P rintxml-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.PrintXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f31d36e8642cb669f5e365d6ffe25b538268bd1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361559"
---
# <a name="ipropertysetterprintxml-method"></a><span data-ttu-id="3e963-103">Ipropertysetter::P rintxml-Methode</span><span class="sxs-lookup"><span data-stu-id="3e963-103">IPropertySetter::PrintXML method</span></span>

> [!Note]  
> <span data-ttu-id="3e963-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="3e963-104">\[Deprecated.</span></span> <span data-ttu-id="3e963-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="3e963-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="3e963-106">Die- `PrintXML` Methode konvertiert Eigenschafts Daten in eine XML-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="3e963-106">The `PrintXML` method converts property data into an XML string.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e963-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e963-107">Syntax</span></span>


```C++
HRESULT PrintXML(
  [out] char *pszXML,
  [in]  int  cbXML,
  [out] int  *pcbPrinted,
  [in]  int  indent
);
```



## <a name="parameters"></a><span data-ttu-id="3e963-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e963-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e963-109">*pszxml* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3e963-109">*pszXML* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e963-110">Zeiger auf einen Puffer, der die XML-Zeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="3e963-110">Pointer to a buffer that receives the XML string.</span></span>

</dd> <dt>

<span data-ttu-id="3e963-111">*cbxml* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e963-111">*cbXML* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e963-112">Größe des Puffers, auf den *pszxml* zeigt (in Bytes).</span><span class="sxs-lookup"><span data-stu-id="3e963-112">Size of the buffer pointed to by *pszXML*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3e963-113">*pcbprint* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3e963-113">*pcbPrinted* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3e963-114">Ein Zeiger auf eine Variable, die die Länge der XML-Zeichenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="3e963-114">Pointer to a variable that receives the length of the XML string.</span></span> <span data-ttu-id="3e963-115">Kann **null** sein.</span><span class="sxs-lookup"><span data-stu-id="3e963-115">Can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="3e963-116">*Einzug* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e963-116">*indent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e963-117">Anzahl der Einzugs Ebenen für das äußerste Tag.</span><span class="sxs-lookup"><span data-stu-id="3e963-117">Number of indent levels for the outermost tag.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e963-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e963-118">Return value</span></span>

<span data-ttu-id="3e963-119">Gibt \_ bei Erfolg S OK zurück.</span><span class="sxs-lookup"><span data-stu-id="3e963-119">Returns S\_OK if successful.</span></span> <span data-ttu-id="3e963-120">Andernfalls wird ein **HRESULT** -Wert zurückgegeben, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="3e963-120">Otherwise, returns an **HRESULT** value indicating the cause of the error.</span></span> <span data-ttu-id="3e963-121">Wenn die XML-Zeichenfolge länger als der Puffer ist, gibt die Methode E \_ outo-Memory zurück.</span><span class="sxs-lookup"><span data-stu-id="3e963-121">If the XML string is longer than the buffer, the method returns E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e963-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e963-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3e963-123">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="3e963-123">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="3e963-124">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="3e963-124">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="3e963-125">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3e963-125">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3e963-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e963-126">Requirements</span></span>



| <span data-ttu-id="3e963-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e963-127">Requirement</span></span> | <span data-ttu-id="3e963-128">Wert</span><span class="sxs-lookup"><span data-stu-id="3e963-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e963-129">Header</span><span class="sxs-lookup"><span data-stu-id="3e963-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3e963-130"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="3e963-130"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="3e963-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3e963-131">Library</span></span><br/> | <dl> <span data-ttu-id="3e963-132"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="3e963-132"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e963-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e963-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e963-134">**Ipropertysetter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="3e963-134">**IPropertySetter Interface**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="3e963-135">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="3e963-135">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




