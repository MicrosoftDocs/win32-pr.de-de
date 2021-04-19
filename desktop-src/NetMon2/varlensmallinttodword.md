---
description: Die varlensmallinttodword-Funktion konvertiert eine kleine Ganzzahl variabler Länge in ein DWORD-Zeichen.
ms.assetid: e26dc206-ac85-4346-9fcf-93ebc8948ced
title: Varlensmallinttodword-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VarLenSmallIntToDword
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4b0e2fa0813c4b384b17ea45af45f9938bcd85c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106362411"
---
# <a name="varlensmallinttodword-function"></a><span data-ttu-id="39ba6-103">Varlensmallinttodword-Funktion</span><span class="sxs-lookup"><span data-stu-id="39ba6-103">VarLenSmallIntToDword function</span></span>

<span data-ttu-id="39ba6-104">Die **varlensmallinttodword** -Funktion konvertiert eine kleine Ganzzahl variabler Länge in ein **DWORD**-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="39ba6-104">The **VarLenSmallIntToDword** function converts a variable-length, small integer to a **DWORD**.</span></span>

## <a name="syntax"></a><span data-ttu-id="39ba6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="39ba6-105">Syntax</span></span>


```C++
LPDWORD WINAPI VarLenSmallIntToDword(
   LPBYTE  pValue,
   WORD    ValueLen,
   BOOL    fIsByteswapped,
   LPDWORD lpDword
);
```



## <a name="parameters"></a><span data-ttu-id="39ba6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="39ba6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39ba6-107">*pValue*</span><span class="sxs-lookup"><span data-stu-id="39ba6-107">*pValue*</span></span> 
</dt> <dd>

<span data-ttu-id="39ba6-108">Ein Zeiger auf die ganze Zahl mit variabler Länge.</span><span class="sxs-lookup"><span data-stu-id="39ba6-108">Pointer to the variable-length, small integer.</span></span>

</dd> <dt>

<span data-ttu-id="39ba6-109">*Valuelen*</span><span class="sxs-lookup"><span data-stu-id="39ba6-109">*ValueLen*</span></span> 
</dt> <dd>

<span data-ttu-id="39ba6-110">Länge (in Byte) der Variablen Länge, Small Integer.</span><span class="sxs-lookup"><span data-stu-id="39ba6-110">Length (in bytes) of the variable-length, small integer .</span></span>

</dd> <dt>

<span data-ttu-id="39ba6-111">*fisbyteswgetauscht*</span><span class="sxs-lookup"><span data-stu-id="39ba6-111">*fIsByteswapped*</span></span> 
</dt> <dd>

<span data-ttu-id="39ba6-112">Flag, das angibt, ob die Länge der Variablen Länge kleiner als Byte ausgetauscht wird.</span><span class="sxs-lookup"><span data-stu-id="39ba6-112">Flag that indicates whether the variable length small integer is byte-swapped.</span></span>

</dd> <dt>

<span data-ttu-id="39ba6-113">*LPDWORD*</span><span class="sxs-lookup"><span data-stu-id="39ba6-113">*lpDword*</span></span> 
</dt> <dd>

<span data-ttu-id="39ba6-114">Das **DWORD** , in das die ganze Zahl konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="39ba6-114">The **DWORD** that the integer is converted to.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39ba6-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39ba6-115">Return value</span></span>

<span data-ttu-id="39ba6-116">Der Rückgabewert ist ein Zeiger auf das **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="39ba6-116">The return value is a pointer to the **DWORD**.</span></span>

## <a name="requirements"></a><span data-ttu-id="39ba6-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39ba6-117">Requirements</span></span>



| <span data-ttu-id="39ba6-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39ba6-118">Requirement</span></span> | <span data-ttu-id="39ba6-119">Wert</span><span class="sxs-lookup"><span data-stu-id="39ba6-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="39ba6-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39ba6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="39ba6-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39ba6-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="39ba6-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39ba6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="39ba6-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="39ba6-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="39ba6-124">Header</span><span class="sxs-lookup"><span data-stu-id="39ba6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="39ba6-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="39ba6-125"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="39ba6-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="39ba6-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="39ba6-127"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39ba6-127"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="39ba6-128">DLL</span><span class="sxs-lookup"><span data-stu-id="39ba6-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39ba6-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39ba6-129"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




