---
description: Das dbglog-Makro sendet eine Zeichenfolge an den debugausgabeort, wenn die Protokollierung für den angegebenen Typ und die angegebene Ebene aktiviert ist. Dieses Makro wird bei Einzelhandels Builds ignoriert.
ms.assetid: 10e95d63-14f2-4fdb-a1b8-c5bf654f9819
title: Dbglog-Makro (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLog
api_type:
- HeaderDef
api_location:
- Wxdebug.h
ms.openlocfilehash: 1cd3f4e53c61fef1f030f654bbb0363cd7c97381
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369677"
---
# <a name="dbglog-macro"></a><span data-ttu-id="05ae8-104">Dbglog-Makro</span><span class="sxs-lookup"><span data-stu-id="05ae8-104">DbgLog macro</span></span>

<span data-ttu-id="05ae8-105">Das **dbglog** -Makro sendet eine Zeichenfolge an den debugausgabeort, wenn die Protokollierung für den angegebenen Typ und die angegebene Ebene aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="05ae8-105">The **DbgLog** macro sends a string to the debug output location, if logging is enabled for the specified type and level.</span></span> <span data-ttu-id="05ae8-106">Dieses Makro wird bei Einzelhandels Builds ignoriert.</span><span class="sxs-lookup"><span data-stu-id="05ae8-106">This macro is ignored in retail builds.</span></span>

## <a name="syntax"></a><span data-ttu-id="05ae8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="05ae8-107">Syntax</span></span>


```C++
void DbgLog(
         DWORD Types,
         DWORD Level,
   const TCHAR *pFormat,
               ...
);
```



## <a name="parameters"></a><span data-ttu-id="05ae8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="05ae8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05ae8-109">*Typen*</span><span class="sxs-lookup"><span data-stu-id="05ae8-109">*Types*</span></span> 
</dt> <dd>

<span data-ttu-id="05ae8-110">Bitweise Kombination von einem oder mehreren Nachrichten Typen.</span><span class="sxs-lookup"><span data-stu-id="05ae8-110">Bitwise combination of one or more message types.</span></span>

</dd> <dt>

<span data-ttu-id="05ae8-111">*Level*</span><span class="sxs-lookup"><span data-stu-id="05ae8-111">*Level*</span></span> 
</dt> <dd>

<span data-ttu-id="05ae8-112">Protokolliergrad für diese Nachricht.</span><span class="sxs-lookup"><span data-stu-id="05ae8-112">Logging level for this message.</span></span>

</dd> <dt>

<span data-ttu-id="05ae8-113">*pformat*</span><span class="sxs-lookup"><span data-stu-id="05ae8-113">*pFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="05ae8-114">Eine Format Zeichenfolge im **printf** -Format.</span><span class="sxs-lookup"><span data-stu-id="05ae8-114">A **printf** -style format string.</span></span>

</dd> <dt>

<span data-ttu-id="05ae8-115">*...*</span><span class="sxs-lookup"><span data-stu-id="05ae8-115">*...*</span></span> 
</dt> <dd>

<span data-ttu-id="05ae8-116">Zusätzliche Argumente für die Format Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="05ae8-116">Additional arguments for the format string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05ae8-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05ae8-117">Return value</span></span>

<span data-ttu-id="05ae8-118">Dieses Makro gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="05ae8-118">This macro does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="05ae8-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="05ae8-119">Remarks</span></span>

<span data-ttu-id="05ae8-120">Wenn die Debugprotokollierung für einen der Nachrichten Typen auf die angegebene Ebene oder höher festgelegt ist, sendet dieses Makro die formatierte Zeichenfolge an den debugausgabespeicherort.</span><span class="sxs-lookup"><span data-stu-id="05ae8-120">If debug logging for any of the message types is set to the specified level or higher, this macro sends the formatted string to the debug output location.</span></span>

<span data-ttu-id="05ae8-121">Das Makro fügt der Ausgabe Zeichenfolge automatisch ein Zeilen Trennzeichen hinzu.</span><span class="sxs-lookup"><span data-stu-id="05ae8-121">The macro automatically adds a newline character to the output string.</span></span>

> [!Note]  
> <span data-ttu-id="05ae8-122">Ein zusätzlicher Satz Klammern muss die Makro Parameter einschließen:</span><span class="sxs-lookup"><span data-stu-id="05ae8-122">An additional set of parentheses must enclose the macro parameters:</span></span>

 


```C++
DbgLog((LOG_TRACE, 3, TEXT("Connected input pin %d"), nPinNumber));
```



## <a name="requirements"></a><span data-ttu-id="05ae8-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05ae8-123">Requirements</span></span>



| <span data-ttu-id="05ae8-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05ae8-124">Requirement</span></span> | <span data-ttu-id="05ae8-125">Wert</span><span class="sxs-lookup"><span data-stu-id="05ae8-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05ae8-126">Header</span><span class="sxs-lookup"><span data-stu-id="05ae8-126">Header</span></span><br/> | <dl> <span data-ttu-id="05ae8-127"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="05ae8-127"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="05ae8-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05ae8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05ae8-129">Debug-Ausgabefunktionen</span><span class="sxs-lookup"><span data-stu-id="05ae8-129">Debug Output Functions</span></span>](debug-output-functions.md)
</dt> </dl>

 

 




