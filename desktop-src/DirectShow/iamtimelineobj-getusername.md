---
description: Die getUserName-Methode ruft den von der Anwendung definierten Namen des Objekts ab.
ms.assetid: 7d172ec5-9cb7-4418-a628-a109944077a6
title: 'Iamtimelineobj:: getUserName-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetUserName
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: efca014493cb5631e058927256bd1586aaca7ab7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358672"
---
# <a name="iamtimelineobjgetusername-method"></a><span data-ttu-id="b9df6-103">Iamtimelineobj:: getUserName-Methode</span><span class="sxs-lookup"><span data-stu-id="b9df6-103">IAMTimelineObj::GetUserName method</span></span>

> [!Note]  
> <span data-ttu-id="b9df6-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="b9df6-104">\[Deprecated.</span></span> <span data-ttu-id="b9df6-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="b9df6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="b9df6-106">Die `GetUserName` -Methode ruft den von der Anwendung definierten Namen des Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="b9df6-106">The `GetUserName` method retrieves the object's application-defined name.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9df6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9df6-107">Syntax</span></span>


```C++
HRESULT GetUserName(
  [out, retval] BSTR *pVal
);
```



## <a name="parameters"></a><span data-ttu-id="b9df6-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9df6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9df6-109">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b9df6-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b9df6-110">Empfängt den Namen des Objekts als **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="b9df6-110">Receives the name of the object as a **BSTR**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9df6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9df6-111">Return value</span></span>

<span data-ttu-id="b9df6-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="b9df6-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b9df6-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b9df6-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9df6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9df6-114">Remarks</span></span>

<span data-ttu-id="b9df6-115">Die-Methode ordnet Speicher für die Zeichenfolge zu.</span><span class="sxs-lookup"><span data-stu-id="b9df6-115">The method allocates memory for the string.</span></span> <span data-ttu-id="b9df6-116">Die Anwendung muss **SysFreeString** aufzurufen, um den Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="b9df6-116">The application must call **SysFreeString** to free the memory.</span></span>

> [!Note]  
> <span data-ttu-id="b9df6-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="b9df6-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="b9df6-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="b9df6-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="b9df6-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b9df6-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b9df6-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9df6-120">Requirements</span></span>



| <span data-ttu-id="b9df6-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9df6-121">Requirement</span></span> | <span data-ttu-id="b9df6-122">Wert</span><span class="sxs-lookup"><span data-stu-id="b9df6-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9df6-123">Header</span><span class="sxs-lookup"><span data-stu-id="b9df6-123">Header</span></span><br/>  | <dl> <span data-ttu-id="b9df6-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="b9df6-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="b9df6-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b9df6-125">Library</span></span><br/> | <dl> <span data-ttu-id="b9df6-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="b9df6-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9df6-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9df6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9df6-128">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b9df6-128">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="b9df6-129">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="b9df6-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




