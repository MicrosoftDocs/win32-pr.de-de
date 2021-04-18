---
description: Ruft die Zeitdauer in Minuten seit der letzten Aktivität des Benutzers ab.
ms.assetid: 2d1e68ad-6f65-4e64-afbf-505b2c9d3423
title: Getidleminutes-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetIdleMinutes
api_type:
- DllExport
api_location:
- Msidle.dll
ms.openlocfilehash: da3064ea96eb8e9835ed1e9d2f564bf922d2f091
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371053"
---
# <a name="getidleminutes-function"></a><span data-ttu-id="444c8-103">Getidleminutes-Funktion</span><span class="sxs-lookup"><span data-stu-id="444c8-103">GetIdleMinutes function</span></span>

<span data-ttu-id="444c8-104">\[Diese Funktion wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="444c8-104">\[This function is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="444c8-105">Verwenden Sie stattdessen die **getlastinputinfo** -Funktion.\]</span><span class="sxs-lookup"><span data-stu-id="444c8-105">Instead, use the **GetLastInputInfo** function.\]</span></span>

<span data-ttu-id="444c8-106">Ruft die Zeitdauer in Minuten seit der letzten Aktivität des Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="444c8-106">Gets the length of time, in minutes, since the user's last activity.</span></span>

## <a name="syntax"></a><span data-ttu-id="444c8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="444c8-107">Syntax</span></span>


```C++
DWORD WINAPI GetIdleMinutes(
   DWORD dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="444c8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="444c8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="444c8-109">*dwReserved*</span><span class="sxs-lookup"><span data-stu-id="444c8-109">*dwReserved*</span></span> 
</dt> <dd>

<span data-ttu-id="444c8-110">Dieser Parameter muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="444c8-110">This parameter must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="444c8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="444c8-111">Return value</span></span>

<span data-ttu-id="444c8-112">Gibt die Anzahl von Minuten seit der letzten Aktivität des Benutzers zurück.</span><span class="sxs-lookup"><span data-stu-id="444c8-112">Returns the number of minutes since the user's last activity.</span></span>

## <a name="remarks"></a><span data-ttu-id="444c8-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="444c8-113">Remarks</span></span>

<span data-ttu-id="444c8-114">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="444c8-114">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span> <span data-ttu-id="444c8-115">Diese Funktion wird nicht nach dem Namen exportiert. Geben Sie beim Aufruf von **GetProcAddress** die Ordinalzahl 8 an.</span><span class="sxs-lookup"><span data-stu-id="444c8-115">This function is not exported by name; specify ordinal 8 when calling **GetProcAddress**.</span></span>

## <a name="requirements"></a><span data-ttu-id="444c8-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="444c8-116">Requirements</span></span>



| <span data-ttu-id="444c8-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="444c8-117">Requirement</span></span> | <span data-ttu-id="444c8-118">Wert</span><span class="sxs-lookup"><span data-stu-id="444c8-118">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="444c8-119">DLL</span><span class="sxs-lookup"><span data-stu-id="444c8-119">DLL</span></span><br/> | <dl> <span data-ttu-id="444c8-120"><dt>Msidle.dll</dt></span><span class="sxs-lookup"><span data-stu-id="444c8-120"><dt>Msidle.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="444c8-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="444c8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="444c8-122">**Getlastinputinfo**</span><span class="sxs-lookup"><span data-stu-id="444c8-122">**GetLastInputInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getlastinputinfo)
</dt> </dl>

 

 
