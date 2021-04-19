---
description: Die loaddefsettings-Methode stellt die Standardeinstellungen des Übergangs Übergangs wieder her.
ms.assetid: 3f81002a-ecac-4d5a-8d2a-ada4d4884d7d
title: 'Idxtjpeg:: loaddefsettings-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.LoadDefSettings
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 51438a21782d1a703a3b43134517e8337ce9f75e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371236"
---
# <a name="idxtjpegloaddefsettings-method"></a><span data-ttu-id="fad0e-103">Idxtjpeg:: loaddefsettings-Methode</span><span class="sxs-lookup"><span data-stu-id="fad0e-103">IDxtJpeg::LoadDefSettings method</span></span>

> [!Note]  
> <span data-ttu-id="fad0e-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="fad0e-104">\[Deprecated.</span></span> <span data-ttu-id="fad0e-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="fad0e-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="fad0e-106">Die- `LoadDefSettings` Methode stellt die Standardeinstellungen des Übergangs Übergangs wieder her.</span><span class="sxs-lookup"><span data-stu-id="fad0e-106">The `LoadDefSettings` method restores the default settings of the Wipe transition.</span></span>

## <a name="syntax"></a><span data-ttu-id="fad0e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fad0e-107">Syntax</span></span>


```C++
HRESULT LoadDefSettings();
```



## <a name="parameters"></a><span data-ttu-id="fad0e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="fad0e-108">Parameters</span></span>

<span data-ttu-id="fad0e-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="fad0e-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fad0e-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fad0e-110">Return value</span></span>

<span data-ttu-id="fad0e-111">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="fad0e-111">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fad0e-112">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fad0e-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fad0e-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fad0e-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="fad0e-114">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="fad0e-114">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="fad0e-115">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="fad0e-115">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="fad0e-116">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fad0e-116">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="fad0e-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fad0e-117">Requirements</span></span>



| <span data-ttu-id="fad0e-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fad0e-118">Requirement</span></span> | <span data-ttu-id="fad0e-119">Wert</span><span class="sxs-lookup"><span data-stu-id="fad0e-119">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fad0e-120">Header</span><span class="sxs-lookup"><span data-stu-id="fad0e-120">Header</span></span><br/>  | <dl> <span data-ttu-id="fad0e-121"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="fad0e-121"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="fad0e-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fad0e-122">Library</span></span><br/> | <dl> <span data-ttu-id="fad0e-123"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="fad0e-123"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fad0e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fad0e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fad0e-125">**Idxtjpeg-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="fad0e-125">**IDxtJpeg Interface**</span></span>](idxtjpeg.md)
</dt> </dl>

 

 




