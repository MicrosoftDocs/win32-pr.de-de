---
description: Diese Funktion aktiviert oder deaktiviert die Unterstützung für Endbenutzer definierte Zeichen (EUDC).
ms.assetid: 9e531d8c-6008-4189-ae25-cda707be5e2c
title: Enableeudc-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnableEUDC
api_type:
- DllExport
api_location:
- Gdi32.dll
ms.openlocfilehash: 755ce2e0a659593b17487e86e28f5d454e48122c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978632"
---
# <a name="enableeudc-function"></a><span data-ttu-id="1645f-103">Enableeudc-Funktion</span><span class="sxs-lookup"><span data-stu-id="1645f-103">EnableEUDC function</span></span>

<span data-ttu-id="1645f-104">Diese Funktion aktiviert oder deaktiviert die Unterstützung für Endbenutzer definierte Zeichen (EUDC).</span><span class="sxs-lookup"><span data-stu-id="1645f-104">This function enables or disables support for end-user-defined characters (EUDC).</span></span>

## <a name="syntax"></a><span data-ttu-id="1645f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1645f-105">Syntax</span></span>


```C++
BOOL EnableEUDC(
  _In_ HDC BOOL fEnableEUDC
);
```



## <a name="parameters"></a><span data-ttu-id="1645f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1645f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1645f-107">*fenableeudc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1645f-107">*fEnableEUDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1645f-108">Boolescher Wert, der auf **true** festgelegt ist, um EUDC zu aktivieren, und auf **false** , um EUDC zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="1645f-108">Boolean that is set to **TRUE** to enable EUDC, and to **FALSE** to disable EUDC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1645f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1645f-109">Return value</span></span>

<span data-ttu-id="1645f-110">Wenn die Funktion erfolgreich ist, ist der Rückgabewert ungleich Null.</span><span class="sxs-lookup"><span data-stu-id="1645f-110">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="1645f-111">Wenn die Funktion fehlerhaft ist, ist der Rückgabewert null.</span><span class="sxs-lookup"><span data-stu-id="1645f-111">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1645f-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1645f-112">Remarks</span></span>

<span data-ttu-id="1645f-113">Wenn EUDC deaktiviert ist, führt der Versuch, EUDC-Zeichen anzuzeigen, zu fehlenden oder ungültigen Symbolen.</span><span class="sxs-lookup"><span data-stu-id="1645f-113">If EUDC is disabled, trying to display EUDC characters will result in missing or bad glyphs.</span></span>

<span data-ttu-id="1645f-114">Während der mehrfach Sitzung wirkt sich diese Funktion nur auf die aktuelle Sitzung aus.</span><span class="sxs-lookup"><span data-stu-id="1645f-114">During multi-session, this function affects the current session only.</span></span>

<span data-ttu-id="1645f-115">Es wird empfohlen, diese Funktion mit Windows XP SP2 oder höher zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1645f-115">It is recommended that you use this function with Windows XP SP2 or later.</span></span>

## <a name="requirements"></a><span data-ttu-id="1645f-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1645f-116">Requirements</span></span>



| <span data-ttu-id="1645f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1645f-117">Requirement</span></span> | <span data-ttu-id="1645f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="1645f-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1645f-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1645f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1645f-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1645f-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1645f-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1645f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1645f-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1645f-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1645f-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1645f-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="1645f-124"><dt>Gdi32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1645f-124"><dt>Gdi32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1645f-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1645f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1645f-126"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1645f-126"><dt>Gdi32.dll</dt></span></span> </dl> |



 

 




