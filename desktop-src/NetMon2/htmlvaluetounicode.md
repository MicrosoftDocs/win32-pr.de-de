---
description: Die htmlvaluetounicode-Funktion konvertiert eine HTML CP- \_ UTF8-Zeichenfolge in eine Unicode-Zeichenfolge.
ms.assetid: d175476e-9c84-48b8-9c89-00255b7cb638
title: Htmlvaluetounicode-Funktion (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HTMLValueToUnicode
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8ef5f4a2b49139ce1ab5366dac3f6c141425653e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750065"
---
# <a name="htmlvaluetounicode-function"></a><span data-ttu-id="9bbd1-103">Htmlvaluetounicode-Funktion</span><span class="sxs-lookup"><span data-stu-id="9bbd1-103">HTMLValueToUnicode function</span></span>

<span data-ttu-id="9bbd1-104">Die **htmlvaluetounicode** -Funktion konvertiert eine HTML CP- \_ UTF8-Zeichenfolge in eine Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9bbd1-104">The **HTMLValueToUnicode** function converts an HTML CP\_UTF8 string to a Unicode string.</span></span>

## <a name="syntax"></a><span data-ttu-id="9bbd1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9bbd1-105">Syntax</span></span>


```C++
WCHAR* HTMLValueToUnicode(
  _Inout_ const char *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="9bbd1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9bbd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9bbd1-107">*pValue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="9bbd1-107">*pValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9bbd1-108">Bei Eingabe ein Zeiger auf die HTML-Zeichenfolge, die von mcsvc bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9bbd1-108">On input, pointer to the HTML string supplied by the MCSVC.</span></span>

<span data-ttu-id="9bbd1-109">Bei Ausgabe, Zeiger auf die konvertierte Unicode-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="9bbd1-109">On output, pointer to the converted Unicode string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9bbd1-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9bbd1-110">Return value</span></span>

<span data-ttu-id="9bbd1-111">Die-Funktion gibt die Unicode-Entsprechung der Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="9bbd1-111">The function returns the Unicode equivalent of the string.</span></span>

## <a name="requirements"></a><span data-ttu-id="9bbd1-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9bbd1-112">Requirements</span></span>



| <span data-ttu-id="9bbd1-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9bbd1-113">Requirement</span></span> | <span data-ttu-id="9bbd1-114">Wert</span><span class="sxs-lookup"><span data-stu-id="9bbd1-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9bbd1-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9bbd1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9bbd1-116">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9bbd1-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9bbd1-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9bbd1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9bbd1-118">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9bbd1-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9bbd1-119">Header</span><span class="sxs-lookup"><span data-stu-id="9bbd1-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="9bbd1-120"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="9bbd1-120"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="9bbd1-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9bbd1-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="9bbd1-122"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9bbd1-122"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="9bbd1-123">DLL</span><span class="sxs-lookup"><span data-stu-id="9bbd1-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9bbd1-124"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9bbd1-124"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




