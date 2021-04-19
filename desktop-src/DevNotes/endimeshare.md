---
description: Beendet die IME-Freigabe.
ms.assetid: aa33b5ed-fd4a-4829-9b7f-d545a4e7bd02
title: Endimeshare-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIMEShare
api_type:
- DllExport
api_location:
- Imeshare.dll
ms.openlocfilehash: 2a0d246537f2788afbb200cd35a81f7d6809ad89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352822"
---
# <a name="endimeshare-function"></a><span data-ttu-id="f7ff7-103">Endimeshare-Funktion</span><span class="sxs-lookup"><span data-stu-id="f7ff7-103">EndIMEShare function</span></span>

<span data-ttu-id="f7ff7-104">Beendet die IME-Freigabe.</span><span class="sxs-lookup"><span data-stu-id="f7ff7-104">Terminates IME Share.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7ff7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7ff7-105">Syntax</span></span>


```C++
void __cdecl EndIMEShare(void);
```



## <a name="parameters"></a><span data-ttu-id="f7ff7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7ff7-106">Parameters</span></span>

<span data-ttu-id="f7ff7-107">Diese Funktion besitzt keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f7ff7-107">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f7ff7-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f7ff7-108">Return value</span></span>

<span data-ttu-id="f7ff7-109">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f7ff7-109">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7ff7-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7ff7-110">Remarks</span></span>

<span data-ttu-id="f7ff7-111">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f7ff7-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

<span data-ttu-id="f7ff7-112">Diese Funktion sollte aufgerufen werden, nachdem die letzte IME-Freigabe Funktion aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="f7ff7-112">This function should be called after the last IME Share function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7ff7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f7ff7-113">Requirements</span></span>



| <span data-ttu-id="f7ff7-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7ff7-114">Requirement</span></span> | <span data-ttu-id="f7ff7-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f7ff7-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7ff7-116">DLL</span><span class="sxs-lookup"><span data-stu-id="f7ff7-116">DLL</span></span><br/> | <dl> <span data-ttu-id="f7ff7-117"><dt>Imeshare.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7ff7-117"><dt>Imeshare.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7ff7-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7ff7-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7ff7-119">**Finitimeshare**</span><span class="sxs-lookup"><span data-stu-id="f7ff7-119">**FInitIMEShare**</span></span>](finitimeshare.md)
</dt> </dl>

 

 
