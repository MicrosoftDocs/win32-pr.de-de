---
description: 'SetAsyncTraceParamsEx-Funktion: Beendet das Einrichten eines Ablaufverfolgungspuffers mit optionalen Feldern für Sprintf-Ablaufverfolgungen.'
ms.assetid: 6c23e61c-0285-47ba-b614-b73bd001d552
title: SetAsyncTraceParamsEx-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetAsyncTraceParamsEx
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: 5a9dc0eee2f4ea3f65fa45914c3340a99ac2d45b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085768"
---
# <a name="setasynctraceparamsex-function"></a><span data-ttu-id="39856-103">SetAsyncTraceParamsEx-Funktion</span><span class="sxs-lookup"><span data-stu-id="39856-103">SetAsyncTraceParamsEx function</span></span>

<span data-ttu-id="39856-104">Beendet das Einrichten eines Ablaufverfolgungspuffers mit optionalen Feldern für Sprintf-Ablaufverfolgungen. </span><span class="sxs-lookup"><span data-stu-id="39856-104">Finishes setting up a trace buffer with optional fields for **sprintf**-style traces.</span></span>

## <a name="syntax"></a><span data-ttu-id="39856-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="39856-105">Syntax</span></span>


```C++
int SetAsyncTraceParamsEx(
   LPSTR pszModule,
   LPSTR pszFile,
   int   lLine,
   LPSTR pszFunction,
   DWORD dwTraceMask
);
```



## <a name="parameters"></a><span data-ttu-id="39856-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="39856-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39856-107">*pszModule*</span><span class="sxs-lookup"><span data-stu-id="39856-107">*pszModule*</span></span> 
</dt> <dd>

<span data-ttu-id="39856-108">Der Name des Moduls, das der Ablaufverfolgung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="39856-108">The name of the module that is associated with the trace.</span></span>

</dd> <dt>

<span data-ttu-id="39856-109">*pszFile*</span><span class="sxs-lookup"><span data-stu-id="39856-109">*pszFile*</span></span> 
</dt> <dd>

<span data-ttu-id="39856-110">Der Name der Quelldatei, die die Ausnahme enthält.</span><span class="sxs-lookup"><span data-stu-id="39856-110">The name of the source file that contains the exception.</span></span>

</dd> <dt>

<span data-ttu-id="39856-111">*lLine*</span><span class="sxs-lookup"><span data-stu-id="39856-111">*lLine*</span></span> 
</dt> <dd>

<span data-ttu-id="39856-112">Die Zeilennummer der Ausnahme in der Quelldatei.</span><span class="sxs-lookup"><span data-stu-id="39856-112">The line number of the exception in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="39856-113">*pszFunction*</span><span class="sxs-lookup"><span data-stu-id="39856-113">*pszFunction*</span></span> 
</dt> <dd>

<span data-ttu-id="39856-114">Der Funktionsname der Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="39856-114">The function name of the exception.</span></span>

</dd> <dt>

<span data-ttu-id="39856-115">*dwTraceMask*</span><span class="sxs-lookup"><span data-stu-id="39856-115">*dwTraceMask*</span></span> 
</dt> <dd>

<span data-ttu-id="39856-116">Eine Ablaufverfolgungsflag-Konstante, die einen der verfügbaren Ablaufverfolgungstypen darstellt.</span><span class="sxs-lookup"><span data-stu-id="39856-116">A trace flag constant that represents one of the available trace types.</span></span> <span data-ttu-id="39856-117">Dieser Parameter kann einen der folgenden Werte enthalten.</span><span class="sxs-lookup"><span data-stu-id="39856-117">This parameter can be any of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="39856-118"><span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**SCHWERWIEGENDER FEHLER \_ TRACE \_ MASK** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="39856-118"><span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**FATAL\_TRACE\_MASK** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="39856-119"><span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**FEHLER \_ TRACE \_ MASK** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="39856-119"><span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**ERROR\_TRACE\_MASK** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="39856-120"><span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**DEBUGGEN \_ TRACE \_ MASK** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="39856-120"><span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**DEBUG\_TRACE\_MASK** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="39856-121"><span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**STATE \_ TRACE \_ MASK** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="39856-121"><span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**STATE\_TRACE\_MASK** (0x00000008)</span></span>
</dt> <dt>

<span data-ttu-id="39856-122"><span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**FUNCT \_ TRACE \_ MASK** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="39856-122"><span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**FUNCT\_TRACE\_MASK** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="39856-123"><span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**MESSAGE \_ TRACE \_ MASK** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="39856-123"><span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**MESSAGE\_TRACE\_MASK** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="39856-124"><span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**ALLE \_ TRACE \_ MASK** (0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="39856-124"><span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**ALL\_TRACE\_MASK** (0xFFFFFFFF)</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39856-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39856-125">Return value</span></span>

<span data-ttu-id="39856-126">Diese Funktion gibt 1 zurück, wenn die Funktion erfolgreich ist. Andernfalls wird 0 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="39856-126">This function returns 1 if the function succeeds; otherwise, it returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="39856-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39856-127">Remarks</span></span>

<span data-ttu-id="39856-128">Exstrace.dll ist eine optionale Komponente, die mit dem Simple Mail Transfer Protocol (SMTP) und dem Network News Transfer Protocol (NNTP) installiert wird.</span><span class="sxs-lookup"><span data-stu-id="39856-128">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="39856-129">Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="39856-129">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="39856-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39856-130">Requirements</span></span>



| <span data-ttu-id="39856-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39856-131">Requirement</span></span> | <span data-ttu-id="39856-132">Wert</span><span class="sxs-lookup"><span data-stu-id="39856-132">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39856-133">DLL</span><span class="sxs-lookup"><span data-stu-id="39856-133">DLL</span></span><br/> | <dl> <span data-ttu-id="39856-134"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39856-134"><dt>Exstrace.dll</dt></span></span> </dl> |



 

 
