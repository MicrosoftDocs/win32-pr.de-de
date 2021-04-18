---
description: Die stringto Address-Funktion konvertiert eine Zeichenfolge in eine Adresse.
ms.assetid: b1ada88d-04bb-4869-87c6-99f5046356c5
title: Stringtaddress-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StringToAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 70a9e6b42359a2f73fba55194c9b6e6e21ffa9a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347920"
---
# <a name="stringtoaddress-function"></a><span data-ttu-id="fe0f0-103">Stringto Address-Funktion</span><span class="sxs-lookup"><span data-stu-id="fe0f0-103">StringToAddress function</span></span>

<span data-ttu-id="fe0f0-104">Die **stringto Address** -Funktion konvertiert eine Zeichenfolge in eine Adresse.</span><span class="sxs-lookup"><span data-stu-id="fe0f0-104">The **StringToAddress** function converts a string to an address.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe0f0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fe0f0-105">Syntax</span></span>


```C++
LPBYTE WINAPI StringToAddress(
  _Out_ BYTE  *lpAddress,
  _In_  LPSTR string
);
```



## <a name="parameters"></a><span data-ttu-id="fe0f0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe0f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe0f0-107">*lpAddress* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="fe0f0-107">*lpAddress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fe0f0-108">Ein Zeiger auf die Adresse, in die die Zeichenfolge konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="fe0f0-108">Pointer to the address the string is converted to.</span></span>

</dd> <dt>

<span data-ttu-id="fe0f0-109">*Zeichenfolge* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fe0f0-109">*string* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fe0f0-110">Zeichenfolge, die in eine Adresse konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="fe0f0-110">String that is converted to an address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe0f0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe0f0-111">Return value</span></span>

<span data-ttu-id="fe0f0-112">Der Rückgabewert ist ein Zeiger auf die konvertierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="fe0f0-112">The return value is a pointer to the converted string.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe0f0-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe0f0-113">Requirements</span></span>



| <span data-ttu-id="fe0f0-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe0f0-114">Requirement</span></span> | <span data-ttu-id="fe0f0-115">Wert</span><span class="sxs-lookup"><span data-stu-id="fe0f0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe0f0-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fe0f0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="fe0f0-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe0f0-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="fe0f0-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fe0f0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="fe0f0-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fe0f0-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe0f0-120">Header</span><span class="sxs-lookup"><span data-stu-id="fe0f0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe0f0-121"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe0f0-121"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="fe0f0-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fe0f0-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="fe0f0-123"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fe0f0-123"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="fe0f0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="fe0f0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fe0f0-125"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe0f0-125"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




