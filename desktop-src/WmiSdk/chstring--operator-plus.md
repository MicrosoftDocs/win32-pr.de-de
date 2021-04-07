---
description: Der Operator + Concatenations Operator verknüpft zwei Zeichen folgen und gibt ein chstring-Objekt zurück.
ms.assetid: b7ed6379-ccfa-40f9-9607-d9033179b674
ms.tgt_platform: multiple
title: 'Chstring:: Operator + (chstring. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5053a4d3059a66cb2c8e4a89a3bdd531d5f42de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758220"
---
# <a name="chstringoperator"></a><span data-ttu-id="d0ca0-103">Chstring:: Operator +</span><span class="sxs-lookup"><span data-stu-id="d0ca0-103">CHString::operator+</span></span>

<span data-ttu-id="d0ca0-104">\[Die [**chstring**](chstring.md) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt im Endzustand behandelt wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="d0ca0-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="d0ca0-105">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="d0ca0-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="d0ca0-106">Der Operator + Concatenations Operator verknüpft zwei Zeichen folgen und gibt ein [**chstring**](chstring.md) -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="d0ca0-106">The + concatenation operator joins two strings and returns a [**CHString**](chstring.md) object.</span></span>

``` syntax
friend CHString operator +(
  const CHString& str1,
  const CHString& str2 )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  WCHAR ch )
throw( CHeap_Exception );

friend CHString operator +(
  WCHAR ch,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  LPCWSTR lpsz )
throw( CHeap_Exception );

friend CHString operator +(
  LPCWSTR lpsz,
  const CHString& str )
throw( CHeap_Exception );

friend CHString operator +(
  const CHString& str,
  char ch )
throw( CHeap_Exception );

friend CHString operator +(
  char ch,
  const CHString& str )
throw( CHeap_Exception );
```

## <a name="parameters"></a><span data-ttu-id="d0ca0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0ca0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0ca0-108"><span id="str__str1__str2"></span><span id="STR__STR1__STR2"></span>*Str, str1, str2*</span><span class="sxs-lookup"><span data-stu-id="d0ca0-108"><span id="str__str1__str2"></span><span id="STR__STR1__STR2"></span>*str, str1, str2*</span></span>
</dt> <dd>

<span data-ttu-id="d0ca0-109">[**Chstring-Zeichen**](chstring.md) folgen, die verkettet werden.</span><span class="sxs-lookup"><span data-stu-id="d0ca0-109">[**CHString**](chstring.md) strings that are concatenated.</span></span>

</dd> <dt>

<span data-ttu-id="d0ca0-110"><span id="ch"></span><span id="CH"></span>*ch*</span><span class="sxs-lookup"><span data-stu-id="d0ca0-110"><span id="ch"></span><span id="CH"></span>*ch*</span></span>
</dt> <dd>

<span data-ttu-id="d0ca0-111">Ein Zeichen, das eine Zeichenfolge oder eine Zeichenfolge verkettet, die ein Zeichen verkettet.</span><span class="sxs-lookup"><span data-stu-id="d0ca0-111">A character that concatenates to a string or a string that concatenates to a character.</span></span>

</dd> <dt>

<span data-ttu-id="d0ca0-112"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span><span class="sxs-lookup"><span data-stu-id="d0ca0-112"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span></span>
</dt> <dd>

<span data-ttu-id="d0ca0-113">Zeiger auf eine mit **null** endenden Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d0ca0-113">Pointer to a **NULL**-terminated character string.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="d0ca0-114">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="d0ca0-114">Return Values</span></span>

<span data-ttu-id="d0ca0-115">Dieser Verkettungs Operator gibt ein [**chstring**](chstring.md) -Objekt zurück, das das temporäre Ergebnis der Verkettung ist.</span><span class="sxs-lookup"><span data-stu-id="d0ca0-115">This concatenation operator returns a [**CHString**](chstring.md) object that is the temporary result of the concatenation.</span></span> <span data-ttu-id="d0ca0-116">Dieser Rückgabewert ermöglicht das Kombinieren mehrerer Verkettungen im gleichen Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="d0ca0-116">This return value makes it possible to combine several concatenations in the same expression.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0ca0-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0ca0-117">Remarks</span></span>

<span data-ttu-id="d0ca0-118">Eine der beiden Argument Zeichenfolgen muss ein [**chstring**](chstring.md) -Objekt sein. der andere kann ein Zeichen Zeiger oder ein Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="d0ca0-118">One of the two argument strings must be a [**CHString**](chstring.md) object; the other can be a character pointer or a character.</span></span> <span data-ttu-id="d0ca0-119">Beachten Sie, dass Arbeitsspeicher Ausnahmen immer auftreten können, wenn Sie den Verkettungs Operator verwenden, da neuer Speicher zugeordnet werden kann, um temporäre Daten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d0ca0-119">Be aware that memory exceptions can occur whenever you use the concatenation operator because new storage may be allocated to hold temporary data.</span></span>

## <a name="examples"></a><span data-ttu-id="d0ca0-120">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d0ca0-120">Examples</span></span>

<span data-ttu-id="d0ca0-121">Das folgende Codebeispiel zeigt die Verwendung von **chstring:: Operator +**:</span><span class="sxs-lookup"><span data-stu-id="d0ca0-121">The following code example shows the use of **CHString::operator +**:</span></span>


```C++
CHString s1( L"abc" );
CHString s2( L"def" );
assert( (s1 + s2 ) == L"abcdef" );

CHString s3;
s3 = CHString( L"abc" ) + "def" ; // Correct
s3 = "abc" + "def"; // Wrong. The first argument must be a CHString.
```



## <a name="requirements"></a><span data-ttu-id="d0ca0-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0ca0-122">Requirements</span></span>



| <span data-ttu-id="d0ca0-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0ca0-123">Requirement</span></span> | <span data-ttu-id="d0ca0-124">Wert</span><span class="sxs-lookup"><span data-stu-id="d0ca0-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0ca0-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d0ca0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d0ca0-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0ca0-126">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="d0ca0-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d0ca0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d0ca0-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0ca0-128">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="d0ca0-129">Header</span><span class="sxs-lookup"><span data-stu-id="d0ca0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d0ca0-130"><dt>Chstring. h (Include-Datei "f")</dt></span><span class="sxs-lookup"><span data-stu-id="d0ca0-130"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d0ca0-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d0ca0-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="d0ca0-132"><dt>Framedyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0ca0-132"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="d0ca0-133">DLL</span><span class="sxs-lookup"><span data-stu-id="d0ca0-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0ca0-134"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0ca0-134"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0ca0-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0ca0-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0ca0-136">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d0ca0-136">**CHString**</span></span>](chstring.md)
</dt> </dl>

 

