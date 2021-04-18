---
description: Bestimmt, ob eine Unicode-Zeichenfolge mit dem angegebenen Muster übereinstimmt.
ms.assetid: 9b220cb8-4402-4094-8209-59a9af004b4a
title: Rtlisnamenexpression-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsNameInExpression
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ac6142b364a135b62505841963fa799ce6603dbe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340111"
---
# <a name="rtlisnameinexpression-function"></a><span data-ttu-id="0cfbd-103">Rtlisnamenexpression-Funktion</span><span class="sxs-lookup"><span data-stu-id="0cfbd-103">RtlIsNameInExpression function</span></span>

<span data-ttu-id="0cfbd-104">Bestimmt, ob eine Unicode-Zeichenfolge mit dem angegebenen Muster übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="0cfbd-104">Determines whether a Unicode string matches the specified pattern.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cfbd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0cfbd-105">Syntax</span></span>


```C++
 BOOLEAN  RtlIsNameInExpression(
  _In_     PUNICODE_STRING Expression,
  _In_     PUNICODE_STRING Name,
  _In_     BOOLEAN         IgnoreCase,
  _In_opt_ PWCH            UpcaseTable
);
```



## <a name="parameters"></a><span data-ttu-id="0cfbd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0cfbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0cfbd-107">*Ausdruck* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cfbd-107">*Expression* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfbd-108">Ein Zeiger auf die Muster Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0cfbd-108">A pointer to the pattern string.</span></span> <span data-ttu-id="0cfbd-109">Diese Zeichenfolge kann Platzhalter Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="0cfbd-109">This string can contain wildcard characters.</span></span> <span data-ttu-id="0cfbd-110">Wenn der *ignoreCase* -Parameter den Wert true hat, muss die Zeichenfolge nur Großbuchstaben enthalten.</span><span class="sxs-lookup"><span data-stu-id="0cfbd-110">If the *IgnoreCase* parameter is TRUE, the string must contain only uppercase characters.</span></span>

</dd> <dt>

<span data-ttu-id="0cfbd-111">*Name* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cfbd-111">*Name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfbd-112">Ein Zeiger auf die Zeichenfolge, die mit dem Muster verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="0cfbd-112">A pointer to the string to be compared against the pattern.</span></span> <span data-ttu-id="0cfbd-113">Diese Zeichenfolge darf keine Platzhalter Zeichen enthalten.</span><span class="sxs-lookup"><span data-stu-id="0cfbd-113">This string cannot contain wildcard characters.</span></span>

</dd> <dt>

<span data-ttu-id="0cfbd-114">*IgnoreCase* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0cfbd-114">*IgnoreCase* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfbd-115">**True** **, wenn die** Groß-/Kleinschreibung nicht beachtet wird</span><span class="sxs-lookup"><span data-stu-id="0cfbd-115">**TRUE** for case-insensitive matching, or **FALSE** for case-sensitive matching.</span></span>

</dd> <dt>

<span data-ttu-id="0cfbd-116">*Upcasetable* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="0cfbd-116">*UpcaseTable* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0cfbd-117">Ein optionaler Zeiger auf eine Zeichentabelle mit Großbuchstaben, die bei Übereinstimmungen ohne Berücksichtigung der Groß-/Kleinschreibung</span><span class="sxs-lookup"><span data-stu-id="0cfbd-117">An optional pointer to an uppercase character table to use for case-insensitive matching.</span></span> <span data-ttu-id="0cfbd-118">Wenn dieser Parameter NULL ist, wird die standardmäßige System-Großbuchstaben-Zeichentabelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="0cfbd-118">If this parameter is NULL, the default system uppercase character table is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0cfbd-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0cfbd-119">Return value</span></span>

<span data-ttu-id="0cfbd-120">Gibt **true** zurück, wenn die Zeichenfolge mit dem Muster übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="0cfbd-120">Returns **TRUE** if the string matches the pattern.</span></span> <span data-ttu-id="0cfbd-121">Wenn die Zeichenfolge nicht mit dem Muster identisch ist, gibt diese Funktion **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="0cfbd-121">If the string does not match the pattern, this function returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0cfbd-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0cfbd-122">Remarks</span></span>

<span data-ttu-id="0cfbd-123">Dieser Funktion ist keine Header Datei zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="0cfbd-123">This function has no associated header file.</span></span> <span data-ttu-id="0cfbd-124">Die zugehörige Import Bibliothek ntdll. lib ist im Microsoft Windows-Treiberkit (WDK) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0cfbd-124">The associated import library, Ntdll.lib, is available in the Microsoft Windows Driver Kit (WDK).</span></span> <span data-ttu-id="0cfbd-125">Sie können diese Funktion auch aufrufen, indem Sie die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion verwenden, um eine dynamische Verknüpfung mit Ntdll.dll</span><span class="sxs-lookup"><span data-stu-id="0cfbd-125">You can also call this function using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Ntdll.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cfbd-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0cfbd-126">Requirements</span></span>



| <span data-ttu-id="0cfbd-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0cfbd-127">Requirement</span></span> | <span data-ttu-id="0cfbd-128">Wert</span><span class="sxs-lookup"><span data-stu-id="0cfbd-128">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0cfbd-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0cfbd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0cfbd-130">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0cfbd-130">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0cfbd-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0cfbd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0cfbd-132">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0cfbd-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="0cfbd-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0cfbd-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0cfbd-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0cfbd-134"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 
