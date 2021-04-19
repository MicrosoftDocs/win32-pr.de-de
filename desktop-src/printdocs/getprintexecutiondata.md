---
description: Getprintexecutiondata Ruft den aktuellen Druck Kontext ab.
ms.assetid: bb9506aa-a0da-46bc-a86a-84a79587cd50
title: Getprintexecutiondata-Funktion (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintExecutionData
api_type:
- DllExport
api_location:
- winspool.drv
ms.openlocfilehash: a1b2f2674c9ef186338c91ed2e4500d8408964d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373330"
---
# <a name="getprintexecutiondata-function"></a><span data-ttu-id="261a4-103">Getprintexecutiondata-Funktion</span><span class="sxs-lookup"><span data-stu-id="261a4-103">GetPrintExecutionData function</span></span>

<span data-ttu-id="261a4-104">**Getprintexecutiondata** Ruft den aktuellen Druck Kontext ab.</span><span class="sxs-lookup"><span data-stu-id="261a4-104">The **GetPrintExecutionData** retrieves the current print context.</span></span>

> [!Note]  
> <span data-ttu-id="261a4-105">Diese Funktion ist für die Verwendung durch Druckertreiber vorgesehen, die im Kontext des Druck Spoolers ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="261a4-105">This function is intended for use by printer drivers that are running in the context of the print spooler.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="261a4-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="261a4-106">Syntax</span></span>


```C++
BOOL WINAPI GetPrintExecutionData(
  _Out_ PRINT_EXECUTION_DATA *pData
);
```



## <a name="parameters"></a><span data-ttu-id="261a4-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="261a4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="261a4-108">*pData* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="261a4-108">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="261a4-109">Ein Zeiger auf eine Variable, die die Adresse der [**Druck \_ Ausführungs \_ Daten**](print-execution-data.md) -Struktur empfängt.</span><span class="sxs-lookup"><span data-stu-id="261a4-109">A pointer to a variable that receives the address of the [**PRINT\_EXECUTION\_DATA**](print-execution-data.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="261a4-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="261a4-110">Return value</span></span>

<span data-ttu-id="261a4-111">Gibt **true** zurück, wenn die Funktion erfolgreich ausgeführt wurde. andernfalls **false**.</span><span class="sxs-lookup"><span data-stu-id="261a4-111">Returns **TRUE** if the function succeeds; otherwise **FALSE**.</span></span> <span data-ttu-id="261a4-112">Wenn der Rückgabewert **false** ist, können Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) aufrufen, um den Fehlerstatus abzurufen.</span><span class="sxs-lookup"><span data-stu-id="261a4-112">If the return value is **FALSE**, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the error status.</span></span>

## <a name="remarks"></a><span data-ttu-id="261a4-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="261a4-113">Remarks</span></span>

<span data-ttu-id="261a4-114">Druckertreiber sollten [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) für das winspool. drv-Modul aufrufen, um die Adresse der **getprintexecutiondata** -Funktion abzurufen, da **getprintexecutiondata** unter Windows Vista oder früheren Versionen von Windows nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="261a4-114">Printer drivers should call [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) on the winspool.drv module to get the address of the **GetPrintExecutionData** function because **GetPrintExecutionData** is not supported on Windows Vista or earlier versions of Windows.</span></span>

<span data-ttu-id="261a4-115">**Getprintexecutiondata** schlägt nur fehl, wenn der Wert von *pData* **null** ist.</span><span class="sxs-lookup"><span data-stu-id="261a4-115">**GetPrintExecutionData** only fails if the value of *pData* is **NULL**.</span></span>

<span data-ttu-id="261a4-116">Der Wert des **clientapppid** -Members der [**Druck \_ Ausführungs \_ Daten**](print-execution-data.md) ist nur sinnvoll, wenn der Wert des **Kontexts** " **Druck \_ Ausführungs \_ Kontext \_ WOW64**" ist.</span><span class="sxs-lookup"><span data-stu-id="261a4-116">The value of the **clientAppPID** member of [**PRINT\_EXECUTION\_DATA**](print-execution-data.md) is only meaningful if the value of **context** is **PRINT\_EXECUTION\_CONTEXT\_WOW64**.</span></span> <span data-ttu-id="261a4-117">Wenn der Wert des **Kontexts** nicht der **Druck \_ Ausführungs \_ Kontext \_ WOW64** ist, ist der Wert von **clientapppid** 0.</span><span class="sxs-lookup"><span data-stu-id="261a4-117">If the value of **context** is not **PRINT\_EXECUTION\_CONTEXT\_WOW64**, the value of **clientAppPID** is 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="261a4-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="261a4-118">Requirements</span></span>



| <span data-ttu-id="261a4-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="261a4-119">Requirement</span></span> | <span data-ttu-id="261a4-120">Wert</span><span class="sxs-lookup"><span data-stu-id="261a4-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="261a4-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="261a4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="261a4-122">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="261a4-122">Windows 7 \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="261a4-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="261a4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="261a4-124">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="261a4-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="261a4-125">Header</span><span class="sxs-lookup"><span data-stu-id="261a4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="261a4-126"><dt>Winspool. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="261a4-126"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="261a4-127">DLL</span><span class="sxs-lookup"><span data-stu-id="261a4-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="261a4-128"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="261a4-128"><dt>Winspool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="261a4-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="261a4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="261a4-130">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="261a4-130">**GetLastError**</span></span>](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="261a4-131">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="261a4-131">**GetProcAddress**</span></span>](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="261a4-132">**Druck \_ Ausführungs \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="261a4-132">**PRINT\_EXECUTION\_CONTEXT**</span></span>](print-execution-context.md)
</dt> <dt>

[<span data-ttu-id="261a4-133">**\_Ausführungs \_ Daten drucken**</span><span class="sxs-lookup"><span data-stu-id="261a4-133">**PRINT\_EXECUTION\_DATA**</span></span>](print-execution-data.md)
</dt> </dl>

 

