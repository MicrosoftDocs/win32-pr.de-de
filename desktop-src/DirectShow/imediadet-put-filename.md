---
description: Die Put \_ filename-Methode gibt den Namen der Quelldatei an, die vom Medien Detektor verwendet werden soll.
ms.assetid: 37bcc7ed-d2c1-4182-b85a-03bad92c5ba7
title: Imediadet::p ut_Filename-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet.put_Filename
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 542b84d3a1eec79b8408c7642bc08680fdc036ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369691"
---
# <a name="imediadetput_filename-method"></a><span data-ttu-id="fad0b-103">Imediadet::p UT- \_ Dateiname-Methode</span><span class="sxs-lookup"><span data-stu-id="fad0b-103">IMediaDet::put\_Filename method</span></span>

> [!Note]  
> <span data-ttu-id="fad0b-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="fad0b-104">\[Deprecated.</span></span> <span data-ttu-id="fad0b-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="fad0b-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fad0b-106">Die- `put_Filename` Methode gibt den Namen der Quelldatei an, die vom Medien Detektor verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fad0b-106">The `put_Filename` method specifies the name of the source file for the media detector to use.</span></span>

<span data-ttu-id="fad0b-107">Diese Methode darf nicht zweimal für dasselbe mediadet-Objekt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="fad0b-107">Do not call this method twice on the same MediaDet object.</span></span> <span data-ttu-id="fad0b-108">Um diese Schnittstelle mit mehr als einer Quelldatei zu verwenden, erstellen Sie separate Instanzen des mediadet-Objekts.</span><span class="sxs-lookup"><span data-stu-id="fad0b-108">To use this interface with more than one source file, create separate instances of the MediaDet object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fad0b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fad0b-109">Syntax</span></span>


```C++
HRESULT put_Filename(
  [in] BSTR newVal
);
```



## <a name="parameters"></a><span data-ttu-id="fad0b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fad0b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fad0b-111">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fad0b-111">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fad0b-112">Der Dateiname der Quelle.</span><span class="sxs-lookup"><span data-stu-id="fad0b-112">File name of the source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fad0b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fad0b-113">Return value</span></span>

<span data-ttu-id="fad0b-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="fad0b-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fad0b-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fad0b-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fad0b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fad0b-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fad0b-117">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="fad0b-117">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fad0b-118">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="fad0b-118">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fad0b-119">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fad0b-119">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fad0b-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fad0b-120">Requirements</span></span>



| <span data-ttu-id="fad0b-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fad0b-121">Requirement</span></span> | <span data-ttu-id="fad0b-122">Wert</span><span class="sxs-lookup"><span data-stu-id="fad0b-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fad0b-123">Header</span><span class="sxs-lookup"><span data-stu-id="fad0b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="fad0b-124"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="fad0b-124"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fad0b-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fad0b-125">Library</span></span><br/> | <dl> <span data-ttu-id="fad0b-126"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="fad0b-126"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fad0b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fad0b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fad0b-128">**Imediadet-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="fad0b-128">**IMediaDet Interface**</span></span>](imediadet.md)
</dt> <dt>

[<span data-ttu-id="fad0b-129">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="fad0b-129">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




