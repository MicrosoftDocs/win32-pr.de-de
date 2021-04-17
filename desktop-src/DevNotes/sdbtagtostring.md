---
description: Ruft den anzeigen amen des angegebenen Tags ab.
ms.assetid: e382d443-aab2-476c-90dd-7ab38e737f52
title: Sdbtagto String-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbTagToString
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 5c781db801077bcef001a860c4ff08c4455daff0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483123"
---
# <a name="sdbtagtostring-function"></a><span data-ttu-id="57f87-103">Sdbtagto String-Funktion</span><span class="sxs-lookup"><span data-stu-id="57f87-103">SdbTagToString function</span></span>

<span data-ttu-id="57f87-104">Ruft den anzeigen amen des angegebenen Tags ab.</span><span class="sxs-lookup"><span data-stu-id="57f87-104">Retrieves the display name of the specified TAG.</span></span>

## <a name="syntax"></a><span data-ttu-id="57f87-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="57f87-105">Syntax</span></span>


```C++
LPCTSTR WINAPI SdbTagToString(
  _In_ TAG tag
);
```



## <a name="parameters"></a><span data-ttu-id="57f87-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="57f87-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57f87-107">*Tag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="57f87-107">*tag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57f87-108">Das-Tag.</span><span class="sxs-lookup"><span data-stu-id="57f87-108">The TAG.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57f87-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="57f87-109">Return value</span></span>

<span data-ttu-id="57f87-110">Die-Funktion gibt einen Zeiger auf die NULL-terminierte Zeichenfolge oder "invalidtag" zurück.</span><span class="sxs-lookup"><span data-stu-id="57f87-110">The function returns a pointer to the null-terminated string or "InvalidTag".</span></span>

## <a name="requirements"></a><span data-ttu-id="57f87-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="57f87-111">Requirements</span></span>



| <span data-ttu-id="57f87-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="57f87-112">Requirement</span></span> | <span data-ttu-id="57f87-113">Wert</span><span class="sxs-lookup"><span data-stu-id="57f87-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57f87-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="57f87-114">Minimum supported client</span></span><br/> | <span data-ttu-id="57f87-115">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57f87-115">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="57f87-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="57f87-116">Minimum supported server</span></span><br/> | <span data-ttu-id="57f87-117">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="57f87-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="57f87-118">DLL</span><span class="sxs-lookup"><span data-stu-id="57f87-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="57f87-119"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="57f87-119"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57f87-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57f87-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57f87-121">**Tag**</span><span class="sxs-lookup"><span data-stu-id="57f87-121">**TAG**</span></span>](tag.md)
</dt> </dl>

 

 




