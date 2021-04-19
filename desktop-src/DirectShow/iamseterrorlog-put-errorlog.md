---
description: Die Put \_ ErrorLog-Methode gibt ein Fehlerprotokoll für das-Objekt an.
ms.assetid: 39da3fb0-57d3-452f-b2ae-6dcd84fa5c8e
title: Iamenterrorlog::p ut_ErrorLog-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog.put_ErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 189f0fed57d67d7632d07839ee82dd13494eb418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367640"
---
# <a name="iamseterrorlogput_errorlog-method"></a><span data-ttu-id="7bf4a-103">Iamseterrorlog::p UT \_ ErrorLog-Methode</span><span class="sxs-lookup"><span data-stu-id="7bf4a-103">IAMSetErrorLog::put\_ErrorLog method</span></span>

> [!Note]  
> <span data-ttu-id="7bf4a-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="7bf4a-104">\[Deprecated.</span></span> <span data-ttu-id="7bf4a-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="7bf4a-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7bf4a-106">Die- `put_ErrorLog` Methode gibt ein Fehlerprotokoll für das-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="7bf4a-106">The `put_ErrorLog` method specifies an error log for the object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bf4a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bf4a-107">Syntax</span></span>


```C++
HRESULT put_ErrorLog(
  [in] IAMErrorLog *newVal
);
```



## <a name="parameters"></a><span data-ttu-id="7bf4a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bf4a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bf4a-109">*NewVal* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7bf4a-109">*newVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bf4a-110">Zeiger auf die [**iamerrorlog**](iamerrorlog.md) -Schnittstelle des Fehler Protokolls.</span><span class="sxs-lookup"><span data-stu-id="7bf4a-110">Pointer to the error log's [**IAMErrorLog**](iamerrorlog.md) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bf4a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7bf4a-111">Return value</span></span>

<span data-ttu-id="7bf4a-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="7bf4a-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7bf4a-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7bf4a-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bf4a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7bf4a-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="7bf4a-115">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="7bf4a-115">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="7bf4a-116">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="7bf4a-116">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="7bf4a-117">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7bf4a-117">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="7bf4a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7bf4a-118">Requirements</span></span>



| <span data-ttu-id="7bf4a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7bf4a-119">Requirement</span></span> | <span data-ttu-id="7bf4a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="7bf4a-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7bf4a-121">Header</span><span class="sxs-lookup"><span data-stu-id="7bf4a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7bf4a-122"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="7bf4a-122"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="7bf4a-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7bf4a-123">Library</span></span><br/> | <dl> <span data-ttu-id="7bf4a-124"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="7bf4a-124"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bf4a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bf4a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bf4a-126">**Iameinterrorlog-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7bf4a-126">**IAMSetErrorLog Interface**</span></span>](iamseterrorlog.md)
</dt> <dt>

[<span data-ttu-id="7bf4a-127">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="7bf4a-127">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




