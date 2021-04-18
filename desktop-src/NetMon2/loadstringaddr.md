---
description: Die loadstringaddr-Funktion transformiert eine Zeichenfolge (z \# . b. &0034; 157.54.32.45&\# 0034;) und erstellt eine DWORD-Adresse.
ms.assetid: 305e0072-b597-4cd5-975e-94103a1680aa
title: Loadstringaddr-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LoadStringAddr
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3317c8e842c23daa08f260063a8310404c92aed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368112"
---
# <a name="loadstringaddr-function"></a><span data-ttu-id="650c0-103">Loadstringaddr-Funktion</span><span class="sxs-lookup"><span data-stu-id="650c0-103">LoadStringAddr function</span></span>

<span data-ttu-id="650c0-104">Die **loadstringaddr** -Funktion transformiert eine Zeichenfolge (z. b. "157.54.32.45") und erstellt eine **DWORD** -Adresse.</span><span class="sxs-lookup"><span data-stu-id="650c0-104">The **LoadStringAddr** function transforms a string (such as "157.54.32.45") and creates a **DWORD** address.</span></span>

## <a name="syntax"></a><span data-ttu-id="650c0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="650c0-105">Syntax</span></span>


```C++
BOOL LoadStringAddr(
         DWORD *pAddress,
   const char  *str
);
```



## <a name="parameters"></a><span data-ttu-id="650c0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="650c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="650c0-107">*pAddress*</span><span class="sxs-lookup"><span data-stu-id="650c0-107">*pAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="650c0-108">Zeiger auf ein **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="650c0-108">Pointer to a **DWORD**.</span></span>

</dd> <dt>

<span data-ttu-id="650c0-109">*str*</span><span class="sxs-lookup"><span data-stu-id="650c0-109">*str*</span></span> 
</dt> <dd>

<span data-ttu-id="650c0-110">Zeiger auf eine Zeichenfolge mit x. x. x. x-Darstellung einer IP-Adresse (z. b. 127.0.0.1).</span><span class="sxs-lookup"><span data-stu-id="650c0-110">Pointer to a character string with x.x.x.x representation of an IP address (for example,127.0.0.1).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="650c0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="650c0-111">Return value</span></span>

<span data-ttu-id="650c0-112">, Wenn die Funktion erfolgreich ausgeführt wurde (der Adress Name wurde gefunden); der Rückgabewert ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="650c0-112">If the function is successful (the address name was found); the return value is **TRUE**.</span></span>

<span data-ttu-id="650c0-113">Wenn die Funktion nicht erfolgreich ist, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="650c0-113">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="650c0-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="650c0-114">Requirements</span></span>



| <span data-ttu-id="650c0-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="650c0-115">Requirement</span></span> | <span data-ttu-id="650c0-116">Wert</span><span class="sxs-lookup"><span data-stu-id="650c0-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="650c0-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="650c0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="650c0-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="650c0-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="650c0-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="650c0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="650c0-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="650c0-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="650c0-121">Header</span><span class="sxs-lookup"><span data-stu-id="650c0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="650c0-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="650c0-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="650c0-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="650c0-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="650c0-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="650c0-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="650c0-125">DLL</span><span class="sxs-lookup"><span data-stu-id="650c0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="650c0-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="650c0-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




