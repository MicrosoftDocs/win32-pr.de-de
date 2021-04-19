---
description: Die get \_ ErrorLog-Methode ruft das aktuelle Fehlerprotokoll für dieses Objekt ab.
ms.assetid: 580b8a06-6bf2-49ef-a5fb-5e6df2f09793
title: 'Iamenterrorlog:: get_ErrorLog-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMSetErrorLog.get_ErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 508a73d6475698dca628de7e3bb96001fe13bcd0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369642"
---
# <a name="iamseterrorlogget_errorlog-method"></a><span data-ttu-id="e7b50-103">Iamseterrorlog:: get \_ ErrorLog-Methode</span><span class="sxs-lookup"><span data-stu-id="e7b50-103">IAMSetErrorLog::get\_ErrorLog method</span></span>

> [!Note]  
> <span data-ttu-id="e7b50-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="e7b50-104">\[Deprecated.</span></span> <span data-ttu-id="e7b50-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="e7b50-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e7b50-106">Die- `get_ErrorLog` Methode ruft das aktuelle Fehlerprotokoll für dieses-Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="e7b50-106">The `get_ErrorLog` method retrieves the current error log for this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7b50-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7b50-107">Syntax</span></span>


```C++
HRESULT get_ErrorLog(
  [out, retval] IAMErrorLog **pVal
);
```



## <a name="parameters"></a><span data-ttu-id="e7b50-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7b50-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7b50-109">*PVal* \[ Out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e7b50-109">*pVal* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e7b50-110">Empfängt einen Zeiger auf die [**iamerrorlog**](iamerrorlog.md) -Schnittstelle des Fehler Protokolls.</span><span class="sxs-lookup"><span data-stu-id="e7b50-110">Receives a pointer to the error log's [**IAMErrorLog**](iamerrorlog.md) interface.</span></span> <span data-ttu-id="e7b50-111">Wenn die Zeitachse kein Fehlerprotokoll enthält, wird der Wert auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e7b50-111">If the timeline does not have an error log, the value is set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7b50-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7b50-112">Return value</span></span>

<span data-ttu-id="e7b50-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="e7b50-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e7b50-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e7b50-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7b50-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7b50-115">Remarks</span></span>

<span data-ttu-id="e7b50-116">Wenn der in *PVal* zurückgegebene Wert nicht **null** ist, weist die [**iamerrorlog**](iamerrorlog.md) -Schnittstelle einen ausstehenden Verweis Zähler auf.</span><span class="sxs-lookup"><span data-stu-id="e7b50-116">If the value returned in *pVal* is not **NULL**, the [**IAMErrorLog**](iamerrorlog.md) interface has an outstanding reference count.</span></span> <span data-ttu-id="e7b50-117">Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="e7b50-117">Be sure to release the interface when you are done using it.</span></span>

> [!Note]  
> <span data-ttu-id="e7b50-118">Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.</span><span class="sxs-lookup"><span data-stu-id="e7b50-118">The header file Qedit.h is not compatible with Direct3D headers later than version 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="e7b50-119">Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter.</span><span class="sxs-lookup"><span data-stu-id="e7b50-119">To obtain Qedit.h, download the [Microsoft Windows SDK Update for Windows Vista and .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span> <span data-ttu-id="e7b50-120">"Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e7b50-120">Qedit.h is not available in the Microsoft Windows SDK for Windows 7 and .NET Framework 3.5 Service Pack 1.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e7b50-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7b50-121">Requirements</span></span>



| <span data-ttu-id="e7b50-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7b50-122">Requirement</span></span> | <span data-ttu-id="e7b50-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e7b50-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b50-124">Header</span><span class="sxs-lookup"><span data-stu-id="e7b50-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e7b50-125"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="e7b50-125"><dt>Qedit.h</dt></span></span> </dl>      |
| <span data-ttu-id="e7b50-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e7b50-126">Library</span></span><br/> | <dl> <span data-ttu-id="e7b50-127"><dt>"" "" ". Lib"</dt></span><span class="sxs-lookup"><span data-stu-id="e7b50-127"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7b50-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7b50-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7b50-129">**Iameinterrorlog-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e7b50-129">**IAMSetErrorLog Interface**</span></span>](iamseterrorlog.md)
</dt> <dt>

[<span data-ttu-id="e7b50-130">Fehler-und Erfolgs Codes</span><span class="sxs-lookup"><span data-stu-id="e7b50-130">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> </dl>

 

 




