---
description: Wird vom Compiler aufgerufen, um strukturierte Ausnahme Behandlungs Erweiterungen zu implementieren.
ms.assetid: 6EAE0B4E-35E1-48EB-A8A9-0C1DC5387B03
title: __C_specific_handler-Funktion (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __C_specific_handler
- __C_specific_handler
api_type:
- DllExport
api_location:
- ntoskrnl.exe
- NTDll.dll
- wpdupfltr.sys
ms.openlocfilehash: fc89105a6a68c920fccb123dd95a08ed4ddee696
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366008"
---
# <a name="__c_specific_handler-function"></a><span data-ttu-id="b199a-103">\_\_C- \_ spezifische \_ Handlerfunktion</span><span class="sxs-lookup"><span data-stu-id="b199a-103">\_\_C\_specific\_handler function</span></span>

<span data-ttu-id="b199a-104">Wird vom Compiler aufgerufen, um strukturierte Ausnahme Behandlungs Erweiterungen zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="b199a-104">Called by the compiler to implement structured exception handling extensions.</span></span>

<span data-ttu-id="b199a-105">Die relative Adresse des sprachspezifischen Handlers ist in den Informationen zum Entladen enthalten, \_ Wenn Flags UNW- \_ Flag " \_ ehandler" oder "UNW \_ Flag \_ uhandler" festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="b199a-105">The relative address of the language specific handler is present in the UNWIND\_INFO whenever flags UNW\_FLAG\_EHANDLER or UNW\_FLAG\_UHANDLER are set.</span></span> <span data-ttu-id="b199a-106">Der sprachspezifische Handler wird als Teil der Suche nach einem Ausnahmehandler oder als Teil einer Entladung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b199a-106">The language specific handler is called as part of the search for an exception handler or as part of an unwind.</span></span> <span data-ttu-id="b199a-107">Weitere Informationen finden Sie unter [sprachspezifischer Handler](/cpp/build/language-specific-handler).</span><span class="sxs-lookup"><span data-stu-id="b199a-107">For more information see [Language Specific Handler](/cpp/build/language-specific-handler).</span></span>

## <a name="syntax"></a><span data-ttu-id="b199a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b199a-108">Syntax</span></span>


```C++
_CRTIMP  __C_specific_handler(
  _In_    struct _EXCEPTION_RECORD   *ExceptionRecord,
  _In_    void                       *EstablisherFrame,
  _Inout_ struct _CONTEXT            *ContextRecord,
  _Inout_ struct _DISPATCHER_CONTEXT *DispatcherContext
);
```



## <a name="parameters"></a><span data-ttu-id="b199a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b199a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b199a-110">*ExceptionRecord* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b199a-110">*ExceptionRecord* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b199a-111">Stellt einen Zeiger auf einen Ausnahme Daten Satz mit der Win64-Standard Definition bereit.</span><span class="sxs-lookup"><span data-stu-id="b199a-111">Supplies a pointer to an exception record, which has the standard Win64 definition.</span></span>

</dd> <dt>

<span data-ttu-id="b199a-112">" *Framesherframe* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="b199a-112">*EstablisherFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b199a-113">Die Adresse der Basis der fixierten Stapel Zuordnung für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="b199a-113">The address of the base of the fixed stack allocation for this function.</span></span>

</dd> <dt>

<span data-ttu-id="b199a-114">*ContextRecord* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b199a-114">*ContextRecord* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b199a-115">Zeigt auf den Ausnahme Kontext zu dem Zeitpunkt, zu dem die Ausnahme ausgelöst wurde (im Ausnahmehandler), oder im aktuellen "Entlade Kontext" (im Fall eines Beendigungs Handlers).</span><span class="sxs-lookup"><span data-stu-id="b199a-115">Points to the exception context at the time the exception was raised (in the exception handler case) or the current "unwind" context (in the termination handler case).</span></span>

</dd> <dt>

<span data-ttu-id="b199a-116">*DispatcherContext* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b199a-116">*DispatcherContext* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b199a-117">Verweist auf den Verteiler Kontext für diese Funktion.</span><span class="sxs-lookup"><span data-stu-id="b199a-117">Points to the dispatcher context for this function.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b199a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b199a-118">Requirements</span></span>



| <span data-ttu-id="b199a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b199a-119">Requirement</span></span> | <span data-ttu-id="b199a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b199a-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b199a-121">Header</span><span class="sxs-lookup"><span data-stu-id="b199a-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b199a-122"><dt>WDM. h</dt></span><span class="sxs-lookup"><span data-stu-id="b199a-122"><dt>Wdm.h</dt></span></span> </dl>        |
| <span data-ttu-id="b199a-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b199a-123">Library</span></span><br/> | <dl> <span data-ttu-id="b199a-124"><dt>Nzu-nl. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b199a-124"><dt>NtosKrnl.lib</dt></span></span> </dl> |
| <span data-ttu-id="b199a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b199a-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="b199a-126"><dt>Ntoskrnl.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b199a-126"><dt>Ntoskrnl.exe</dt></span></span> </dl> |



 

