---
description: Startet die Überwachung der Inaktivität.
ms.assetid: fed5e4ae-2c2b-4b00-9230-b71aec9335c8
title: Beginidleerkennungs-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BeginIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: 06cd016dc4102ef2f5b0f351aa4836a7f9980645
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361336"
---
# <a name="beginidledetection-function"></a><span data-ttu-id="d8be3-103">Beginidleerkennungs-Funktion</span><span class="sxs-lookup"><span data-stu-id="d8be3-103">BeginIdleDetection function</span></span>

<span data-ttu-id="d8be3-104">\[Diese Funktion wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="d8be3-104">\[This function is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="d8be3-105">Verwenden Sie stattdessen die **getlastinputinfo** -Funktion.\]</span><span class="sxs-lookup"><span data-stu-id="d8be3-105">Instead, use the **GetLastInputInfo** function.\]</span></span>

<span data-ttu-id="d8be3-106">Startet die Überwachung der Inaktivität.</span><span class="sxs-lookup"><span data-stu-id="d8be3-106">Begins monitoring inactivity.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8be3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8be3-107">Syntax</span></span>


```C++
DWORD WINAPI BeginIdleDetection(
   _IDLECALLBACK pfnCallback,
   DWORD         dwIdleMin,
   DWORD         dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="d8be3-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8be3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8be3-109">*pfncallback*</span><span class="sxs-lookup"><span data-stu-id="d8be3-109">*pfnCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="d8be3-110">Die Funktion, die aufgerufen wird, wenn sich der Leerlaufzustand ändert.</span><span class="sxs-lookup"><span data-stu-id="d8be3-110">The function that is called when the idle state changes.</span></span> <span data-ttu-id="d8be3-111">Dieser Rückruf wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="d8be3-111">This callback is defined as follows:</span></span>

``` syntax
typedef void (WINAPI* _IDLECALLBACK) (DWORD dwState);

#define STATE_USER_IDLE_BEGIN       1
#define STATE_USER_IDLE_END         2
```

</dd> <dt>

<span data-ttu-id="d8be3-112">*dwidlemin*</span><span class="sxs-lookup"><span data-stu-id="d8be3-112">*dwIdleMin*</span></span> 
</dt> <dd>

<span data-ttu-id="d8be3-113">Die Anzahl der Minuten der Inaktivität, bevor der Rückruf an die Rückruffunktion erfolgt.</span><span class="sxs-lookup"><span data-stu-id="d8be3-113">The number of minutes of inactivity before the call is made to the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="d8be3-114">*dwReserved*</span><span class="sxs-lookup"><span data-stu-id="d8be3-114">*dwReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="d8be3-115">Dieser Parameter muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d8be3-115">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8be3-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d8be3-116">Return value</span></span>

<span data-ttu-id="d8be3-117">Gibt 0 zurück, wenn die Funktion erfolgreich ausgeführt wird. Andernfalls wird ein Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d8be3-117">Returns 0 if the function succeeds; otherwise, it returns an error code.</span></span> <span data-ttu-id="d8be3-118">Wenn *dwReserved* beispielsweise etwas anderes als 0 ist, werden **\_ ungültige \_ Daten** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d8be3-118">For example, if *dwReserved* is anything other than 0, **ERROR\_INVALID\_DATA** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8be3-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8be3-119">Remarks</span></span>

<span data-ttu-id="d8be3-120">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d8be3-120">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span> <span data-ttu-id="d8be3-121">Diese Funktion wird nicht nach dem Namen exportiert. Geben Sie beim Aufrufen von " **GetProcAddress**" Ordnungszahl 3 an.</span><span class="sxs-lookup"><span data-stu-id="d8be3-121">This function is not exported by name; specify ordinal 3 when calling **GetProcAddress**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8be3-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8be3-122">Requirements</span></span>



| <span data-ttu-id="d8be3-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8be3-123">Requirement</span></span> | <span data-ttu-id="d8be3-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d8be3-124">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d8be3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d8be3-125">DLL</span></span><br/> | <dl> <span data-ttu-id="d8be3-126"><dt>Msidle.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8be3-126"><dt>Msidle.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8be3-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8be3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8be3-128">**Getlastinputinfo**</span><span class="sxs-lookup"><span data-stu-id="d8be3-128">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
