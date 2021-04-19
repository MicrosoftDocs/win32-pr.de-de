---
description: Die getuserdata-Methode ruft die von der Anwendung definierten persistenten Daten ab.
ms.assetid: dd2cdb37-9c4f-4356-a35f-2d42b7588da6
title: 'Iamtimelineobj:: getuserdata-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.GetUserData
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 9dda74980dcdae9cd73e749d9cb4324b4c6357f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352072"
---
# <a name="iamtimelineobjgetuserdata-method"></a><span data-ttu-id="9c1e2-103">Iamtimelineobj:: getuserdata-Methode</span><span class="sxs-lookup"><span data-stu-id="9c1e2-103">IAMTimelineObj::GetUserData method</span></span>

> [!Note]  
> <span data-ttu-id="9c1e2-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="9c1e2-104">\[Deprecated.</span></span> <span data-ttu-id="9c1e2-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="9c1e2-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="9c1e2-106">Die `GetUserData` -Methode ruft die von der Anwendung definierten persistenten Daten ab.</span><span class="sxs-lookup"><span data-stu-id="9c1e2-106">The `GetUserData` method retrieves the application-defined persistent data.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c1e2-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c1e2-107">Syntax</span></span>


```C++
HRESULT GetUserData(
   BYTE *pData,
   long *pSize
);
```



## <a name="parameters"></a><span data-ttu-id="9c1e2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9c1e2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c1e2-109">*pData*</span><span class="sxs-lookup"><span data-stu-id="9c1e2-109">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="9c1e2-110">Zeiger auf einen Puffer, der die Daten empfängt.</span><span class="sxs-lookup"><span data-stu-id="9c1e2-110">Pointer to a buffer that receives the data.</span></span> <span data-ttu-id="9c1e2-111">Legen Sie diesen Parameter auf **null** fest, um die Größe des zuzuordnenden Puffers zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="9c1e2-111">To determine the size of buffer to allocate, set this parameter to **NULL**.</span></span> <span data-ttu-id="9c1e2-112">Die erforderliche Größe wird in " *Psize*" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9c1e2-112">The required size is returned in *pSize*.</span></span>

</dd> <dt>

<span data-ttu-id="9c1e2-113">*Psize*</span><span class="sxs-lookup"><span data-stu-id="9c1e2-113">*pSize*</span></span> 
</dt> <dd>

<span data-ttu-id="9c1e2-114">Empfängt die Größe der Daten in Bytes.</span><span class="sxs-lookup"><span data-stu-id="9c1e2-114">Receives the size of the data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c1e2-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9c1e2-115">Return value</span></span>

<span data-ttu-id="9c1e2-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="9c1e2-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9c1e2-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9c1e2-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="9c1e2-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9c1e2-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="9c1e2-119">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="9c1e2-119">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="9c1e2-120">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="9c1e2-120">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="9c1e2-121">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9c1e2-121">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9c1e2-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9c1e2-122">Requirements</span></span>



| <span data-ttu-id="9c1e2-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9c1e2-123">Requirement</span></span> | <span data-ttu-id="9c1e2-124">Wert</span><span class="sxs-lookup"><span data-stu-id="9c1e2-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c1e2-125">Header</span><span class="sxs-lookup"><span data-stu-id="9c1e2-125">Header</span></span><br/>  | <dl> <span data-ttu-id="9c1e2-126"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="9c1e2-126"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="9c1e2-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9c1e2-127">Library</span></span><br/> | <dl> <span data-ttu-id="9c1e2-128"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="9c1e2-128"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c1e2-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c1e2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c1e2-130">**Iamtimelineobj-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="9c1e2-130">**IAMTimelineObj Interface**</span></span>](iamtimelineobj.md)
</dt> <dt>

[<span data-ttu-id="9c1e2-131">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="9c1e2-131">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




