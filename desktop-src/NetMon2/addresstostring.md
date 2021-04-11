---
description: Die "adresstostring"-Funktion konvertiert eine Adresse in eine Zeichenfolge.
ms.assetid: 999a6142-1423-4006-a489-63895dd19ce3
title: Adresssstostring-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddressToString
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0c7c659a05167055b18c36e5c6c36465538af483
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131996"
---
# <a name="addresstostring-function"></a><span data-ttu-id="a5278-103">Adresssstostring-Funktion</span><span class="sxs-lookup"><span data-stu-id="a5278-103">AddressToString function</span></span>

<span data-ttu-id="a5278-104">Die " **adresstostring** "-Funktion konvertiert eine Adresse in eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a5278-104">The **AddressToString** function converts an address into a string.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5278-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5278-105">Syntax</span></span>


```C++
LPSTR WINAPI AddressToString(
  _Out_ LPSTR string,
  _In_  BYTE  *lpAddress
);
```



## <a name="parameters"></a><span data-ttu-id="a5278-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5278-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5278-107">*Zeichenfolge* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a5278-107">*string* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5278-108">Zeichenfolge, in die die Adresse konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="a5278-108">String that the address is converted to.</span></span>

</dd> <dt>

<span data-ttu-id="a5278-109">*lpAddress* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a5278-109">*lpAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a5278-110">Die Adresse, die gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="a5278-110">The address that is printed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5278-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a5278-111">Return value</span></span>

<span data-ttu-id="a5278-112">Der Rückgabewert ist ein Zeiger auf die konvertierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="a5278-112">The return value is a pointer to the converted string.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5278-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a5278-113">Requirements</span></span>



| <span data-ttu-id="a5278-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a5278-114">Requirement</span></span> | <span data-ttu-id="a5278-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a5278-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5278-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a5278-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a5278-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5278-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="a5278-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a5278-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a5278-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a5278-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a5278-120">Header</span><span class="sxs-lookup"><span data-stu-id="a5278-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5278-121"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5278-121"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="a5278-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a5278-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="a5278-123"><dt>Parser. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5278-123"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="a5278-124">DLL</span><span class="sxs-lookup"><span data-stu-id="a5278-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5278-125"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5278-125"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




