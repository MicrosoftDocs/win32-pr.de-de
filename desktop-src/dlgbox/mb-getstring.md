---
title: MB_GetString-Funktion (User. h)
description: Gibt Zeichen folgen für standardmäßige Meldungs Feld Schaltflächen
ms.assetid: D2AF238D-F5A8-477D-BF47-0F5D4D68B27E
keywords:
- Dialog Felder für die MB_GetString Funktion
topic_type:
- apiref
api_name:
- MB_GetString
api_location:
- user32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eafd33f268f2ef1ef87755b79aba6d5d0aa77bb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362063"
---
# <a name="mb_getstring-function"></a><span data-ttu-id="2bc8f-104">MB \_ GetString-Funktion</span><span class="sxs-lookup"><span data-stu-id="2bc8f-104">MB\_GetString function</span></span>

<span data-ttu-id="2bc8f-105">Gibt Zeichen folgen für standardmäßige Meldungs Feld Schaltflächen</span><span class="sxs-lookup"><span data-stu-id="2bc8f-105">Returns strings for standard message box buttons.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bc8f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2bc8f-106">Syntax</span></span>


```C++
LPCWSTR WINAPI MB_GetString(
   UINT wBtn
);
```



## <a name="parameters"></a><span data-ttu-id="2bc8f-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2bc8f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bc8f-108">*wbtn*</span><span class="sxs-lookup"><span data-stu-id="2bc8f-108">*wBtn*</span></span> 
</dt> <dd>

<span data-ttu-id="2bc8f-109">Die ID der zurück zugebende Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="2bc8f-109">The id of the string to return.</span></span> <span data-ttu-id="2bc8f-110">Diese werden durch die Befehls-ID-Werte des Dialog Felds identifiziert, die in winuser. h aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="2bc8f-110">These are identified by the Dialog Box Command ID values listed in winuser.h.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bc8f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2bc8f-111">Return value</span></span>

<span data-ttu-id="2bc8f-112">Die Zeichenfolge oder NULL, wenn Sie nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="2bc8f-112">The string, or NULL if not found.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bc8f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2bc8f-113">Requirements</span></span>



| <span data-ttu-id="2bc8f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2bc8f-114">Requirement</span></span> | <span data-ttu-id="2bc8f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="2bc8f-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2bc8f-116">Header</span><span class="sxs-lookup"><span data-stu-id="2bc8f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2bc8f-117"><dt>User. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bc8f-117"><dt>User.h</dt></span></span> </dl>     |
| <span data-ttu-id="2bc8f-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2bc8f-118">Library</span></span><br/> | <dl> <span data-ttu-id="2bc8f-119"><dt>User32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2bc8f-119"><dt>User32.lib</dt></span></span> </dl> |
| <span data-ttu-id="2bc8f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="2bc8f-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="2bc8f-121"><dt>User32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2bc8f-121"><dt>User32.dll</dt></span></span> </dl> |



 

 





