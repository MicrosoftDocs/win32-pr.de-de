---
description: Ermöglicht einem Debugger, Informationen zu dynamischen Funktionstabellen zu überprüfen.
ms.assetid: 32fd0dfd-ca7c-45e4-9d59-2b3318d7e13d
title: Rtlgetfunctiontablelisderad-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetFunctionTableListHead
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 3dde476ee9958952d85c66816a113b92529aa13e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368667"
---
# <a name="rtlgetfunctiontablelisthead-function"></a><span data-ttu-id="742d6-103">Rtlgetfunctiontablelisderad-Funktion</span><span class="sxs-lookup"><span data-stu-id="742d6-103">RtlGetFunctionTableListHead function</span></span>

<span data-ttu-id="742d6-104">\[Diese Funktion kann ohne vorherige Ankündigung geändert oder aus Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="742d6-104">\[This function may be changed or removed from Windows without further notice.\]</span></span>

<span data-ttu-id="742d6-105">Ermöglicht einem Debugger, Informationen zu dynamischen Funktionstabellen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="742d6-105">Enables a debugger to examine dynamic function table information.</span></span>

## <a name="syntax"></a><span data-ttu-id="742d6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="742d6-106">Syntax</span></span>


```C++
PLIST_ENTRY RtlGetFunctionTableListHead(void);
```



## <a name="parameters"></a><span data-ttu-id="742d6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="742d6-107">Parameters</span></span>

<span data-ttu-id="742d6-108">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="742d6-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="742d6-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="742d6-109">Return value</span></span>

<span data-ttu-id="742d6-110">Gibt einen Zeiger auf den Anfang der Funktionstabellen Liste zurück.</span><span class="sxs-lookup"><span data-stu-id="742d6-110">Returns a pointer to the head of the function table list.</span></span>

## <a name="remarks"></a><span data-ttu-id="742d6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="742d6-111">Remarks</span></span>

<span data-ttu-id="742d6-112">Beachten Sie, dass die Windows Driver Kit (WDK)-Header Datei ntdef. h für einige Definitionen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="742d6-112">Note that the Windows Driver Kit (WDK) header file Ntdef.h is required for some definitions.</span></span> <span data-ttu-id="742d6-113">Die zugehörige Import Bibliothek ntdll. lib ist im WDK verfügbar.</span><span class="sxs-lookup"><span data-stu-id="742d6-113">The associated import library, Ntdll.lib, is available in the WDK.</span></span> <span data-ttu-id="742d6-114">Sie können auch die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um dynamisch mit Ntdll.dll zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="742d6-114">You can also use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="742d6-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="742d6-115">Requirements</span></span>



| <span data-ttu-id="742d6-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="742d6-116">Requirement</span></span> | <span data-ttu-id="742d6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="742d6-117">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="742d6-118">DLL</span><span class="sxs-lookup"><span data-stu-id="742d6-118">DLL</span></span><br/> | <dl> <span data-ttu-id="742d6-119"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="742d6-119"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
