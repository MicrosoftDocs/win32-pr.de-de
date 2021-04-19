---
description: Zeigt ein Meldungs Feld mit der angegebenen Zeichenfolge, dem Namen der Quelldatei und der Zeilennummer an. Der Benutzer kann die Nachricht ignorieren, den Debugger eingeben oder die Anwendung beenden. Wird in Einzelhandels Builds ignoriert.
ms.assetid: ac4da7da-f9d0-44ae-9ad1-9a5908b288fb
title: Dbgbreak-Makro (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgBreak
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 099344a295de2657b40218b993ab9c4cb6411353
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372723"
---
# <a name="dbgbreak-macro"></a><span data-ttu-id="07798-105">Dbgbreak-Makro</span><span class="sxs-lookup"><span data-stu-id="07798-105">DbgBreak macro</span></span>

<span data-ttu-id="07798-106">Zeigt ein Meldungs Feld mit der angegebenen Zeichenfolge, dem Namen der Quelldatei und der Zeilennummer an.</span><span class="sxs-lookup"><span data-stu-id="07798-106">Displays a message box with the specified string, the name of the source file, and the line number.</span></span> <span data-ttu-id="07798-107">Der Benutzer kann die Nachricht ignorieren, den Debugger eingeben oder die Anwendung beenden.</span><span class="sxs-lookup"><span data-stu-id="07798-107">The user can ignore the message, enter the debugger, or quit the application.</span></span> <span data-ttu-id="07798-108">Wird in Einzelhandels Builds ignoriert.</span><span class="sxs-lookup"><span data-stu-id="07798-108">Ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="07798-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="07798-109">Syntax</span></span>


```C++
void DbgBreak(
    strLiteral
);
```



## <a name="parameters"></a><span data-ttu-id="07798-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="07798-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07798-111">*"Straume"*</span><span class="sxs-lookup"><span data-stu-id="07798-111">*strLiteral*</span></span> 
</dt> <dd>

<span data-ttu-id="07798-112">Text Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="07798-112">Text string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07798-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07798-113">Return value</span></span>

<span data-ttu-id="07798-114">Dieses Makro gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="07798-114">This macro does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="07798-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="07798-115">Examples</span></span>


```C++
DbgBreak("Unrecoverable error occurred.");
```



## <a name="requirements"></a><span data-ttu-id="07798-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="07798-116">Requirements</span></span>



| <span data-ttu-id="07798-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07798-117">Requirement</span></span> | <span data-ttu-id="07798-118">Wert</span><span class="sxs-lookup"><span data-stu-id="07798-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07798-119">Header</span><span class="sxs-lookup"><span data-stu-id="07798-119">Header</span></span><br/> | <dl> <span data-ttu-id="07798-120"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="07798-120"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07798-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07798-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07798-122">Assert-und breakpointmakros</span><span class="sxs-lookup"><span data-stu-id="07798-122">Assert and Breakpoint Macros</span></span>](assert-and-breakpoint-macros.md)
</dt> </dl>

 

 




