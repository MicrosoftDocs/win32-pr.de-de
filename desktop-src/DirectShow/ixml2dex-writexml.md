---
description: Die Methode "Write texml" übersetzt eine Zeitachse in eine XML-Zeichenfolge.
ms.assetid: 1039c6fc-b2ba-4052-90b6-b7468b94c071
title: 'IXml2Dex:: Write texml-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IXml2Dex.WriteXML
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4ab8a4421244f2c2ee21c5243923f5d0827317e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372251"
---
# <a name="ixml2dexwritexml-method"></a><span data-ttu-id="fe650-103">IXml2Dex:: Write texml-Methode</span><span class="sxs-lookup"><span data-stu-id="fe650-103">IXml2Dex::WriteXML method</span></span>

> [!Note]  
> <span data-ttu-id="fe650-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="fe650-104">\[Deprecated.</span></span> <span data-ttu-id="fe650-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="fe650-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fe650-106">Die- `WriteXML` Methode übersetzt eine Zeitachse in eine XML-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="fe650-106">The `WriteXML` method translates a timeline to an XML string.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe650-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe650-107">Syntax</span></span>


```C++
HRESULT WriteXML(
   IUnknown *pTimeline,
   BSTR     *pbstrXML
);
```



## <a name="parameters"></a><span data-ttu-id="fe650-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe650-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe650-109">*ptimeline*</span><span class="sxs-lookup"><span data-stu-id="fe650-109">*pTimeline*</span></span> 
</dt> <dd>

<span data-ttu-id="fe650-110">Zeiger auf die **IUnknown** -Schnittstelle des Timeline-Objekts.</span><span class="sxs-lookup"><span data-stu-id="fe650-110">Pointer to the timeline object's **IUnknown** interface.</span></span>

</dd> <dt>

<span data-ttu-id="fe650-111">*pbstrauxml*</span><span class="sxs-lookup"><span data-stu-id="fe650-111">*pbstrXML*</span></span> 
</dt> <dd>

<span data-ttu-id="fe650-112">Zeiger auf eine Variable vom Typ BSTR, die die XML-Zeichenfolge empfängt, die die Zeitachse beschreibt.</span><span class="sxs-lookup"><span data-stu-id="fe650-112">Pointer to a variable of type BSTR that receives the XML string describing the timeline.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe650-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe650-113">Return value</span></span>

<span data-ttu-id="fe650-114">Gibt \_ bei Erfolg S OK zurück.</span><span class="sxs-lookup"><span data-stu-id="fe650-114">Returns S\_OK if successful.</span></span> <span data-ttu-id="fe650-115">Wenn nicht genügend Arbeitsspeicher für die Konvertierung vorhanden ist, wird E \_ outoiden Speicher zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fe650-115">If there is insufficient memory for the conversion, returns E\_OUTOFMEMORY.</span></span> <span data-ttu-id="fe650-116">Andernfalls wird ein anderer Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fe650-116">Otherwise, returns another error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe650-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fe650-117">Remarks</span></span>

<span data-ttu-id="fe650-118">Die-Methode ordnet Speicher für die Zeichenfolge zu.</span><span class="sxs-lookup"><span data-stu-id="fe650-118">The method allocates memory for the string.</span></span> <span data-ttu-id="fe650-119">Die Anwendung muss **SysFreeString** aufzurufen, um den Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="fe650-119">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="fe650-120">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="fe650-120">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fe650-121">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="fe650-121">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fe650-122">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fe650-122">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fe650-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe650-123">Requirements</span></span>



| <span data-ttu-id="fe650-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe650-124">Requirement</span></span> | <span data-ttu-id="fe650-125">Wert</span><span class="sxs-lookup"><span data-stu-id="fe650-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fe650-126">Version</span><span class="sxs-lookup"><span data-stu-id="fe650-126">Version</span></span><br/> | <span data-ttu-id="fe650-127">Internet Explorer 4,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="fe650-127">Internet Explorer 4.0 or later</span></span><br/>                                               |
| <span data-ttu-id="fe650-128">Header</span><span class="sxs-lookup"><span data-stu-id="fe650-128">Header</span></span><br/>  | <dl> <span data-ttu-id="fe650-129"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="fe650-129"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fe650-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fe650-130">Library</span></span><br/> | <dl> <span data-ttu-id="fe650-131"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="fe650-131"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe650-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe650-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe650-133">**IXml2Dex-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="fe650-133">**IXml2Dex Interface**</span></span>](ixml2dex.md)
</dt> <dt>

[<span data-ttu-id="fe650-134">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="fe650-134">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




