---
description: Beendet das Einrichten eines Ablauf Verfolgungs Puffers mit optionalen Feldern für Ablauf Verfolgungen im sprintf-Stil.
ms.assetid: a5f3ecbe-d335-4fd0-99aa-4d5a748ca4e1
title: Asyncstringtrace-Funktion
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
ms.openlocfilehash: 15bfff82f5ef0ae3f921a3a4c83b4d35fb83d95f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358336"
---
# <a name="asyncstringtrace-function"></a><span data-ttu-id="da1e7-103">Asyncstringtrace-Funktion</span><span class="sxs-lookup"><span data-stu-id="da1e7-103">AsyncStringTrace function</span></span>

<span data-ttu-id="da1e7-104">Beendet das Einrichten eines Ablauf Verfolgungs Puffers mit optionalen Feldern für Ablauf Verfolgungen im **sprintf**-Stil.</span><span class="sxs-lookup"><span data-stu-id="da1e7-104">Finishes setting up a trace buffer with optional fields for **sprintf**-style traces.</span></span>

## <a name="syntax"></a><span data-ttu-id="da1e7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="da1e7-105">Syntax</span></span>


```C++
int AsyncStringTrace(
   LPARAM  lParam,
   LPCSTR  szFormat,
   va_list marker
);
```



## <a name="parameters"></a><span data-ttu-id="da1e7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="da1e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da1e7-107">*lParam*</span><span class="sxs-lookup"><span data-stu-id="da1e7-107">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="da1e7-108">Ein 32-Bit-Ablauf Verfolgungs Parameter, der für die Filterung auf Anwendungsebene verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="da1e7-108">A 32-bit trace parameter that is used for application-level filtering.</span></span>

</dd> <dt>

<span data-ttu-id="da1e7-109">*szformat*</span><span class="sxs-lookup"><span data-stu-id="da1e7-109">*szFormat*</span></span> 
</dt> <dd>

<span data-ttu-id="da1e7-110">Eine NULL terminierte Zeichenfolge, die das Format der Ablauf Verfolgung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="da1e7-110">A zero-terminated string that describes the format of the trace.</span></span>

</dd> <dt>

<span data-ttu-id="da1e7-111">*setzen*</span><span class="sxs-lookup"><span data-stu-id="da1e7-111">*marker*</span></span> 
</dt> <dd>

<span data-ttu-id="da1e7-112">Ein Marker für **vsprintf** -Funktionen.</span><span class="sxs-lookup"><span data-stu-id="da1e7-112">A marker for **vsprintf** functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da1e7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="da1e7-113">Return value</span></span>

<span data-ttu-id="da1e7-114">Diese Funktion gibt die Länge der Ablauf Verfolgungs Anweisung in Bytes zurück.</span><span class="sxs-lookup"><span data-stu-id="da1e7-114">This function returns the length of the trace statement, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="da1e7-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da1e7-115">Remarks</span></span>

<span data-ttu-id="da1e7-116">Exstrace.dll ist eine optionale Komponente, die mit dem Simple Mail Transfer Protocol (SMTP) und dem Network News Transfer Protocol (NNTP) installiert wird.</span><span class="sxs-lookup"><span data-stu-id="da1e7-116">Exstrace.dll is an optional component that installs with the Simple Mail Transfer Protocol (SMTP) and the Network News Transfer Protocol (NNTP).</span></span>

<span data-ttu-id="da1e7-117">Beim Datentyp der **VA- \_ Liste** handelt es sich um einen Standardtyp, der für die von **VA \_ arg** und **VA \_** benötigten Informationen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="da1e7-117">The **va\_list** data type is a standard type that is used to hold information needed by **va\_arg** and **va\_end** macros.</span></span> <span data-ttu-id="da1e7-118">Weitere Informationen finden Sie unter [Standard Typen](/cpp/c-runtime-library/standard-types?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="da1e7-118">For more information, see [Standard Types](/cpp/c-runtime-library/standard-types?view=vs-2019).</span></span>

<span data-ttu-id="da1e7-119">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="da1e7-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="da1e7-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da1e7-120">Requirements</span></span>



| <span data-ttu-id="da1e7-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da1e7-121">Requirement</span></span> | <span data-ttu-id="da1e7-122">Wert</span><span class="sxs-lookup"><span data-stu-id="da1e7-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="da1e7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="da1e7-123">DLL</span></span><br/> | <dl> <span data-ttu-id="da1e7-124"><dt>Exstrace.dll</dt></span><span class="sxs-lookup"><span data-stu-id="da1e7-124"><dt>Exstrace.dll</dt></span></span> </dl> |



 

