---
description: Die Methode "Set tresizerguid" gibt die CLSID eines benutzerdefinierten Videos zum Ändern der Größenänderung an.
ms.assetid: 709a6e7f-64ae-406d-bb6d-29f6c65b63a8
title: 'IRenderEngine2:: stresizerguid-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine2.SetResizerGUID
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 864053c2c5def6ef1b23ca2c2ee712664e132079
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356071"
---
# <a name="irenderengine2setresizerguid-method"></a><span data-ttu-id="360ac-103">IRenderEngine2:: stresizerguid-Methode</span><span class="sxs-lookup"><span data-stu-id="360ac-103">IRenderEngine2::SetResizerGUID method</span></span>

> [!Note]  
> <span data-ttu-id="360ac-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="360ac-104">\[Deprecated.</span></span> <span data-ttu-id="360ac-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="360ac-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="360ac-106">Die- `SetResizerGUID` Methode gibt die CLSID eines benutzerdefinierten Videos zum Ändern der Größenänderung an.</span><span class="sxs-lookup"><span data-stu-id="360ac-106">The `SetResizerGUID` method specifies the CLSID of a custom video resizing filter.</span></span> <span data-ttu-id="360ac-107">Verwenden Sie diese Methode, um den von DirectShow-Bearbeitungs Diensten verwendeten Standardfilter für die Größe der Größe zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="360ac-107">Call this method to replace the default resizing filter used by DirectShow Editing Services.</span></span> <span data-ttu-id="360ac-108">Der Filter muss als COM-Objekt im System des Benutzers registriert sein, und er muss die [**iresize**](iresize.md) -Schnittstelle unterstützen.</span><span class="sxs-lookup"><span data-stu-id="360ac-108">Your filter must be registered as a COM object on the user's system, and it must support the [**IResize**](iresize.md) interface.</span></span>

<span data-ttu-id="360ac-109">Rufen Sie diese Methode auf, bevor Sie " [**irienderengine:: connectfrontend**](irenderengine-connectfrontend.md)" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="360ac-109">Call this method before calling [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="360ac-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="360ac-110">Syntax</span></span>


```C++
HRESULT SetResizerGUID(
  [in] GUID ResizerGuid
);
```



## <a name="parameters"></a><span data-ttu-id="360ac-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="360ac-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="360ac-112">*Resizerguid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="360ac-112">*ResizerGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="360ac-113">Die CLSID des Filters.</span><span class="sxs-lookup"><span data-stu-id="360ac-113">The CLSID of the filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="360ac-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="360ac-114">Return value</span></span>

<span data-ttu-id="360ac-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="360ac-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="360ac-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="360ac-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="360ac-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="360ac-117">Remarks</span></span>

<span data-ttu-id="360ac-118">Verwenden Sie die folgende CLSID, um zum Standardwert für den des-Resizer zurückzukehren:</span><span class="sxs-lookup"><span data-stu-id="360ac-118">To revert to the default DES resizer, use the following CLSID:</span></span>


```C++
// {F97B8A60-31AD-11CF-B2DE-00DD01101B85}
DEFINE_GUID(CLSID_Resize, 
0xF97B8A60, 0x31AD, 0x11CF, 0xB2, 0xDE, 0x00, 0xDD, 0x01, 0x10, 0x1B, 0x85);
```



> [!Note]  
> <span data-ttu-id="360ac-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="360ac-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="360ac-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="360ac-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="360ac-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="360ac-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="360ac-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="360ac-122">Requirements</span></span>



| <span data-ttu-id="360ac-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="360ac-123">Requirement</span></span> | <span data-ttu-id="360ac-124">Wert</span><span class="sxs-lookup"><span data-stu-id="360ac-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="360ac-125">Version</span><span class="sxs-lookup"><span data-stu-id="360ac-125">Version</span></span><br/> | <span data-ttu-id="360ac-126">DirectX 9,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="360ac-126">DirectX 9.0 or later</span></span><br/>                                                         |
| <span data-ttu-id="360ac-127">Header</span><span class="sxs-lookup"><span data-stu-id="360ac-127">Header</span></span><br/>  | <dl> <span data-ttu-id="360ac-128"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="360ac-128"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="360ac-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="360ac-129">Library</span></span><br/> | <dl> <span data-ttu-id="360ac-130"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="360ac-130"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="360ac-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="360ac-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="360ac-132">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="360ac-132">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="360ac-133">**IRenderEngine2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="360ac-133">**IRenderEngine2 Interface**</span></span>](irenderengine2.md)
</dt> </dl>

 

 




