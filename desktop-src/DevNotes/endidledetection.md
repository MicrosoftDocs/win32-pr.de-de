---
description: Beendet die Überwachung der Inaktivität.
ms.assetid: 26e52341-77cd-46cd-8b32-e786dfac870e
title: Endidleerkennungs-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EndIdleDetection
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: e50679c53123ad140324f7d159ef938367c02af0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354197"
---
# <a name="endidledetection-function"></a><span data-ttu-id="47d1a-103">Endidleerkennungs-Funktion</span><span class="sxs-lookup"><span data-stu-id="47d1a-103">EndIdleDetection function</span></span>

<span data-ttu-id="47d1a-104">\[Diese Funktion wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="47d1a-104">\[This function is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="47d1a-105">Verwenden Sie stattdessen die **getlastinputinfo** -Funktion.\]</span><span class="sxs-lookup"><span data-stu-id="47d1a-105">Instead, use the **GetLastInputInfo** function.\]</span></span>

<span data-ttu-id="47d1a-106">Beendet die Überwachung der Inaktivität.</span><span class="sxs-lookup"><span data-stu-id="47d1a-106">Ends monitoring of inactivity.</span></span>

## <a name="syntax"></a><span data-ttu-id="47d1a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="47d1a-107">Syntax</span></span>


```C++
BOOL WINAPI EndIdleDetection(
   DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="47d1a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="47d1a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47d1a-109">*dwReserved*</span><span class="sxs-lookup"><span data-stu-id="47d1a-109">*dwReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="47d1a-110">Dieser Parameter muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="47d1a-110">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47d1a-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47d1a-111">Return value</span></span>

<span data-ttu-id="47d1a-112">Gibt **true** zurück, wenn die Funktion erfolgreich ausgeführt wurde. Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="47d1a-112">Returns **TRUE** if the function succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="47d1a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47d1a-113">Remarks</span></span>

<span data-ttu-id="47d1a-114">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="47d1a-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span> <span data-ttu-id="47d1a-115">Diese Funktion wird nicht nach dem Namen exportiert. Geben Sie beim Aufrufen von " **GetProcAddress**" Ordnungszahl 4 an.</span><span class="sxs-lookup"><span data-stu-id="47d1a-115">This function is not exported by name; specify ordinal 4 when calling **GetProcAddress**.</span></span>

## <a name="requirements"></a><span data-ttu-id="47d1a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47d1a-116">Requirements</span></span>



| <span data-ttu-id="47d1a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47d1a-117">Requirement</span></span> | <span data-ttu-id="47d1a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="47d1a-118">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="47d1a-119">DLL</span><span class="sxs-lookup"><span data-stu-id="47d1a-119">DLL</span></span><br/> | <dl> <span data-ttu-id="47d1a-120"><dt>Msidle.dll</dt></span><span class="sxs-lookup"><span data-stu-id="47d1a-120"><dt>Msidle.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47d1a-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47d1a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47d1a-122">**Getlastinputinfo**</span><span class="sxs-lookup"><span data-stu-id="47d1a-122">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
