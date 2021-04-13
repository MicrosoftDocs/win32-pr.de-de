---
title: Wssetautfail-Funktion (webservicesdebug. h)
description: Legt den nächsten Punkt für das Einfügen eines Fehlers fest. Dies ist eine reine Debugfunktion.
ms.assetid: b453dbc5-01ff-486d-8767-254b74cc5b6e
keywords:
- Wssetauwebfail-funktionsweb Dienste für Windows
topic_type:
- apiref
api_name:
- WsSetAutoFail
api_location:
- WebServicesDebug.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ba10b8b038f270f764b064fac1cb81e675f5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518539"
---
# <a name="wssetautofail-function"></a><span data-ttu-id="51bdb-105">Wssetauto Fail-Funktion</span><span class="sxs-lookup"><span data-stu-id="51bdb-105">WsSetAutoFail function</span></span>

<span data-ttu-id="51bdb-106">Legt den nächsten Punkt für das Einfügen eines Fehlers fest.</span><span class="sxs-lookup"><span data-stu-id="51bdb-106">Sets the next point to inject a failure.</span></span> <span data-ttu-id="51bdb-107">Dies ist eine reine Debugfunktion.</span><span class="sxs-lookup"><span data-stu-id="51bdb-107">This is a DEBUG ONLY function.</span></span>

## <a name="syntax"></a><span data-ttu-id="51bdb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="51bdb-108">Syntax</span></span>


```C++
HRESULT WINAPI  WsSetAutoFail(
  _In_     ULONG     count,
  _In_opt_ WS_ERROR* error
);
```



## <a name="parameters"></a><span data-ttu-id="51bdb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="51bdb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51bdb-110">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="51bdb-110">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51bdb-111">Gibt an, wie viele Vorgänge vor dem Auftreten von Fehlern beginnen.</span><span class="sxs-lookup"><span data-stu-id="51bdb-111">Specifies how many operations before failures begin to occur.</span></span>

</dd> <dt>

<span data-ttu-id="51bdb-112">*Fehler* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="51bdb-112">*error* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="51bdb-113">Ein Zeiger auf ein [WS- \_ Fehler](ws-error.md) Objekt, in dem zusätzliche Informationen über den Fehler gespeichert werden sollen, wenn die Funktion fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="51bdb-113">A pointer to a [WS\_ERROR](ws-error.md) object where additional information about the error should be stored if the function fails.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51bdb-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51bdb-114">Return value</span></span>

<span data-ttu-id="51bdb-115">Wenn diese Funktion erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="51bdb-115">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="51bdb-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="51bdb-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="51bdb-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51bdb-117">Requirements</span></span>



| <span data-ttu-id="51bdb-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51bdb-118">Requirement</span></span> | <span data-ttu-id="51bdb-119">Wert</span><span class="sxs-lookup"><span data-stu-id="51bdb-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="51bdb-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51bdb-120">Minimum supported client</span></span><br/> | <span data-ttu-id="51bdb-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51bdb-121">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="51bdb-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51bdb-122">Minimum supported server</span></span><br/> | <span data-ttu-id="51bdb-123">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="51bdb-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="51bdb-124">Header</span><span class="sxs-lookup"><span data-stu-id="51bdb-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="51bdb-125"><dt>Webservicesdebug. h</dt></span><span class="sxs-lookup"><span data-stu-id="51bdb-125"><dt>WebServicesDebug.h</dt></span></span> </dl> |



 

 





