---
description: Initialisiert die IME-Freigabe.
ms.assetid: 7f58564e-d660-4936-b74c-af4eb93e2442
title: Finitimeshare-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FInitIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 0724bb6cb9e44dc86699a66da37616050ce54e18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365513"
---
# <a name="finitimeshare-function"></a><span data-ttu-id="7a98a-103">Finitimeshare-Funktion</span><span class="sxs-lookup"><span data-stu-id="7a98a-103">FInitIMEShare function</span></span>

<span data-ttu-id="7a98a-104">Initialisiert die IME-Freigabe.</span><span class="sxs-lookup"><span data-stu-id="7a98a-104">Initializes IME Share.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a98a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a98a-105">Syntax</span></span>


```C++
BOOL __cdecl FInitIMEShare(void);
```



## <a name="parameters"></a><span data-ttu-id="7a98a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a98a-106">Parameters</span></span>

<span data-ttu-id="7a98a-107">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7a98a-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7a98a-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a98a-108">Return value</span></span>

<span data-ttu-id="7a98a-109">Andernfalls gibt die Funktion **true** bei Success oder **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="7a98a-109">The function returns **TRUE** on success or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a98a-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a98a-110">Remarks</span></span>

<span data-ttu-id="7a98a-111">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="7a98a-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="7a98a-112">Diese Funktion sollte aufgerufen werden, bevor andere IME-Freigabe Funktionen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7a98a-112">This function should be called before any other IME Share functions are called.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a98a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a98a-113">Requirements</span></span>



| <span data-ttu-id="7a98a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a98a-114">Requirement</span></span> | <span data-ttu-id="7a98a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="7a98a-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a98a-116">DLL</span><span class="sxs-lookup"><span data-stu-id="7a98a-116">DLL</span></span><br/> | <dl> <span data-ttu-id="7a98a-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a98a-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a98a-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a98a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a98a-119">**Umdimeshare**</span><span class="sxs-lookup"><span data-stu-id="7a98a-119">**EndIMEShare**</span></span>](endimeshare.md)
</dt> </dl>

 

 
