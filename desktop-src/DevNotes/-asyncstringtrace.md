---
description: 'AsyncStringTrace-Funktion: Beendet das Einrichten eines Ablaufverfolgungspuffers mit optionalen Feldern für Sprintf-Ablaufverfolgungen.'
ms.assetid: a5f3ecbe-d335-4fd0-99aa-4d5a748ca4e1
title: AsyncStringTrace-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AsyncStringTrace
api_type:
- DllExport
api_location:
- Exstrace.dll
ms.openlocfilehash: 342670dc406cb84588984d0a9ab10fae280c5483
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085798"
---
# <a name="asyncstringtrace-function"></a><span data-ttu-id="035ed-103">AsyncStringTrace-Funktion</span><span class="sxs-lookup"><span data-stu-id="035ed-103">AsyncStringTrace function</span></span>

<span data-ttu-id="035ed-104">Beendet das Einrichten eines Ablaufverfolgungspuffers mit optionalen Feldern für Sprintf-Ablaufverfolgungen. </span><span class="sxs-lookup"><span data-stu-id="035ed-104">Finishes setting up a trace buffer with optional fields for **sprintf**-style traces.</span></span>

## <a name="syntax"></a><span data-ttu-id="035ed-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="035ed-105">Syntax</span></span>


```C++
int AsyncStringTrace(
   LPARAM  lParam,
   LPCSTR  szFormat,
   va_list marker
);
```



## <a name="parameters"></a><span data-ttu-id="035ed-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="035ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="035ed-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="035ed-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="035ed-108">Ein 32-Bit-Ablaufverfolgungsparameter, der für die Filterung auf Anwendungsebene verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="035ed-108">A 32-bit trace parameter that is used for application-level filtering.</span></span>

</dd> <dt>

<span data-ttu-id="035ed-109">*szFormat*</span><span class="sxs-lookup"><span data-stu-id="035ed-109">*szFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="035ed-110">Eine mit 0 (null) beendete Zeichenfolge, die das Format der Ablaufverfolgung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="035ed-110">A zero-terminated string that describes the format of the trace.</span></span>

</dd> <dt>

<span data-ttu-id="035ed-111">*Marker*</span><span class="sxs-lookup"><span data-stu-id="035ed-111">*marker*</span></span> 
</dt> <dd>

<span data-ttu-id="035ed-112">Ein Marker für **vsprintf-Funktionen.**</span><span class="sxs-lookup"><span data-stu-id="035ed-112">A marker for **vsprintf** functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="035ed-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="035ed-113">Return value</span></span>

<span data-ttu-id="035ed-114">Diese Funktion gibt die Länge der Ablaufverfolgungs-Anweisung in Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="035ed-114">This function returns the length of the trace statement, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="035ed-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="035ed-115">Remarks</span></span>

<span data-ttu-id="035ed-116">Exstrace.dll ist eine optionale Komponente, die mit dem Simple Mail Transfer Protocol (SMTP) und dem Network News Transfer Protocol (NNTP) installiert wird.</span><span class="sxs-lookup"><span data-stu-id="035ed-116">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="035ed-117">Der **datentyp va \_ list** ist ein Standardtyp, der zum Enthalten von Informationen verwendet wird, die von **va \_ arg-** und **\_ va-End-Makros benötigt** werden.</span><span class="sxs-lookup"><span data-stu-id="035ed-117">The **va\_list** data type is a standard type that is used to hold information needed by **va\_arg** and **va\_end** macros.</span></span> <span data-ttu-id="035ed-118">Weitere Informationen finden Sie unter [Standardtypen.](/cpp/c-runtime-library/standard-types?view=vs-2019)</span><span class="sxs-lookup"><span data-stu-id="035ed-118">For more information, see [Standard Types](/cpp/c-runtime-library/standard-types?view=vs-2019).</span></span>

<span data-ttu-id="035ed-119">Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="035ed-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="035ed-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="035ed-120">Requirements</span></span>



| <span data-ttu-id="035ed-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="035ed-121">Requirement</span></span> | <span data-ttu-id="035ed-122">Wert</span><span class="sxs-lookup"><span data-stu-id="035ed-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="035ed-123">DLL</span><span class="sxs-lookup"><span data-stu-id="035ed-123">DLL</span></span><br/> | <dl> <span data-ttu-id="035ed-124"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="035ed-124"><dt>Exstrace.dll</dt></span></span> </dl> |



 

