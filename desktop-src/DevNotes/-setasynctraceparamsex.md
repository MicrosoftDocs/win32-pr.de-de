---
description: Beendet das Einrichten eines Ablauf Verfolgungs Puffers mit optionalen Feldern für Ablauf Verfolgungen im sprintf-Stil.
ms.assetid: 6c23e61c-0285-47ba-b614-b73bd001d552
title: Setasynctraceparamsex-Funktion
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
ms.openlocfilehash: e5f99af2e6226e39ecc06a1c4c2bb7f2ad3c3b8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354110"
---
# <a name="setasynctraceparamsex-function"></a><span data-ttu-id="99fbe-103">Setasynctraceparamsex-Funktion</span><span class="sxs-lookup"><span data-stu-id="99fbe-103">SetAsyncTraceParamsEx function</span></span>

<span data-ttu-id="99fbe-104">Beendet das Einrichten eines Ablauf Verfolgungs Puffers mit optionalen Feldern für Ablauf Verfolgungen im **sprintf**-Stil.</span><span class="sxs-lookup"><span data-stu-id="99fbe-104">Finishes setting up a trace buffer with optional fields for **sprintf**-style traces.</span></span>

## <a name="syntax"></a><span data-ttu-id="99fbe-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="99fbe-105">Syntax</span></span>


```C++
int SetAsyncTraceParamsEx(
   LPSTR pszModule,
   LPSTR pszFile,
   int   lLine,
   LPSTR pszFunction,
   DWORD dwTraceMask
);
```



## <a name="parameters"></a><span data-ttu-id="99fbe-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="99fbe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99fbe-107">*pszmodule*</span><span class="sxs-lookup"><span data-stu-id="99fbe-107">*pszModule*</span></span> 
</dt> <dd>

<span data-ttu-id="99fbe-108">Der Name des Moduls, das der Ablauf Verfolgung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="99fbe-108">The name of the module that is associated with the trace.</span></span>

</dd> <dt>

<span data-ttu-id="99fbe-109">*pszFile*</span><span class="sxs-lookup"><span data-stu-id="99fbe-109">*pszFile*</span></span> 
</dt> <dd>

<span data-ttu-id="99fbe-110">Der Name der Quelldatei, die die Ausnahme enthält.</span><span class="sxs-lookup"><span data-stu-id="99fbe-110">The name of the source file that contains the exception.</span></span>

</dd> <dt>

<span data-ttu-id="99fbe-111">*Lline*</span><span class="sxs-lookup"><span data-stu-id="99fbe-111">*lLine*</span></span> 
</dt> <dd>

<span data-ttu-id="99fbe-112">Die Zeilennummer der Ausnahme in der Quelldatei.</span><span class="sxs-lookup"><span data-stu-id="99fbe-112">The line number of the exception in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="99fbe-113">*pszfunction*</span><span class="sxs-lookup"><span data-stu-id="99fbe-113">*pszFunction*</span></span> 
</dt> <dd>

<span data-ttu-id="99fbe-114">Der Funktionsname der Ausnahme.</span><span class="sxs-lookup"><span data-stu-id="99fbe-114">The function name of the exception.</span></span>

</dd> <dt>

<span data-ttu-id="99fbe-115">*dwtracemask*</span><span class="sxs-lookup"><span data-stu-id="99fbe-115">*dwTraceMask*</span></span> 
</dt> <dd>

<span data-ttu-id="99fbe-116">Eine Ablaufverfolgungsflag-Konstante, die einen der verfügbaren Ablauf Verfolgungs Typen darstellt.</span><span class="sxs-lookup"><span data-stu-id="99fbe-116">A trace flag constant that represents one of the available trace types.</span></span> <span data-ttu-id="99fbe-117">Dieser Parameter kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="99fbe-117">This parameter can be any of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="99fbe-118"><span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>Schwerwiegend **\_ Ablauf Verfolgungs \_ Maske** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="99fbe-118"><span id="FATAL_TRACE_MASK"></span><span id="fatal_trace_mask"></span>**FATAL\_TRACE\_MASK** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="99fbe-119"><span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**Fehler \_ Ablauf Verfolgungs \_ Maske** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="99fbe-119"><span id="ERROR_TRACE_MASK"></span><span id="error_trace_mask"></span>**ERROR\_TRACE\_MASK** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="99fbe-120"><span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**Debuggen \_ Ablauf Verfolgungs \_ Maske** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="99fbe-120"><span id="DEBUG_TRACE_MASK"></span><span id="debug_trace_mask"></span>**DEBUG\_TRACE\_MASK** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="99fbe-121"><span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**Status \_ Ablauf Verfolgungs \_ Maske** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="99fbe-121"><span id="STATE_TRACE_MASK"></span><span id="state_trace_mask"></span>**STATE\_TRACE\_MASK** (0x00000008)</span></span>
</dt> <dt>

<span data-ttu-id="99fbe-122"><span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**Funct \_ Ablauf Verfolgungs \_ Maske** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="99fbe-122"><span id="FUNCT_TRACE_MASK"></span><span id="funct_trace_mask"></span>**FUNCT\_TRACE\_MASK** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="99fbe-123"><span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**Nachricht \_ Ablauf Verfolgungs \_ Maske** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="99fbe-123"><span id="MESSAGE_TRACE_MASK"></span><span id="message_trace_mask"></span>**MESSAGE\_TRACE\_MASK** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="99fbe-124"><span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**Alle \_ Ablauf Verfolgungs \_ Maske** (0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="99fbe-124"><span id="ALL_TRACE_MASK"></span><span id="all_trace_mask"></span>**ALL\_TRACE\_MASK** (0xFFFFFFFF)</span></span>
</dt> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99fbe-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99fbe-125">Return value</span></span>

<span data-ttu-id="99fbe-126">Diese Funktion gibt 1 zurück, wenn die Funktion erfolgreich ausgeführt wird. Andernfalls wird 0 zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="99fbe-126">This function returns 1 if the function succeeds; otherwise, it returns 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="99fbe-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99fbe-127">Remarks</span></span>

<span data-ttu-id="99fbe-128">Exstrace.dll ist eine optionale Komponente, die mit dem Simple Mail Transfer Protocol (SMTP) und dem Network News Transfer Protocol (NNTP) installiert wird.</span><span class="sxs-lookup"><span data-stu-id="99fbe-128">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="99fbe-129">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="99fbe-129">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="99fbe-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="99fbe-130">Requirements</span></span>



| <span data-ttu-id="99fbe-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="99fbe-131">Requirement</span></span> | <span data-ttu-id="99fbe-132">Wert</span><span class="sxs-lookup"><span data-stu-id="99fbe-132">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99fbe-133">DLL</span><span class="sxs-lookup"><span data-stu-id="99fbe-133">DLL</span></span><br/> | <dl> <span data-ttu-id="99fbe-134"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99fbe-134"><dt>Exstrace.dll</dt></span></span> </dl> |



 

 
