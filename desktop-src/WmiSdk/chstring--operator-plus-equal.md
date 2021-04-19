---
description: Der Operator + = Concatenations Operator verknüpft Zeichen am Ende dieser Zeichenfolge. Der Operator akzeptiert ein anderes chstring-Objekt, einen Zeichen Zeiger oder ein einzelnes Zeichen.
ms.assetid: 026ff9af-4cda-4261-aa27-e215d49b80ce
ms.tgt_platform: multiple
title: 'Chstring:: Operator + = (chstring. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683ca6b6264169cd156e89c3447c63fa59f03585
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356207"
---
# <a name="chstringoperator"></a><span data-ttu-id="4db48-104">Chstring:: Operator + =</span><span class="sxs-lookup"><span data-stu-id="4db48-104">CHString::operator+=</span></span>

<span data-ttu-id="4db48-105">\[Die [**chstring**](chstring.md) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt im Endzustand behandelt wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="4db48-105">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="4db48-106">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="4db48-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="4db48-107">Der Operator + = Concatenations Operator verknüpft Zeichen am Ende dieser Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="4db48-107">The += concatenation operator joins characters to the end of this string.</span></span> <span data-ttu-id="4db48-108">Der Operator akzeptiert ein anderes [**chstring**](chstring.md) -Objekt, einen Zeichen Zeiger oder ein einzelnes Zeichen.</span><span class="sxs-lookup"><span data-stu-id="4db48-108">The operator accepts another [**CHString**](chstring.md) object, a character pointer, or a single character.</span></span>

``` syntax
const CHString& operator +=(
  const CHString& string )
throw( CHeap_Exception );

const CHString& operator +=(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator +=(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString operator +=(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a><span data-ttu-id="4db48-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4db48-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4db48-110"><span id="string"></span><span id="STRING"></span>*Schnür*</span><span class="sxs-lookup"><span data-stu-id="4db48-110"><span id="string"></span><span id="STRING"></span>*string*</span></span>
</dt> <dd>

<span data-ttu-id="4db48-111">Eine [**Zeichen**](chstring.md) folgen Zeichenfolge, die diese Zeichenfolge verkettet.</span><span class="sxs-lookup"><span data-stu-id="4db48-111">A [**CHString**](chstring.md) string that concatenates to this string.</span></span>

</dd> <dt>

<span data-ttu-id="4db48-112"><span id="ch"></span><span id="CH"></span>*ch*</span><span class="sxs-lookup"><span data-stu-id="4db48-112"><span id="ch"></span><span id="CH"></span>*ch*</span></span>
</dt> <dd>

<span data-ttu-id="4db48-113">Ein Zeichen, das mit dieser Zeichenfolge verkettet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4db48-113">A character to concatenate to this string.</span></span>

</dd> <dt>

<span data-ttu-id="4db48-114"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span><span class="sxs-lookup"><span data-stu-id="4db48-114"><span id="lpsz"></span><span id="LPSZ"></span>*lpsz*</span></span>
</dt> <dd>

<span data-ttu-id="4db48-115">Zeiger auf eine mit **null** endenden Zeichenfolge, die mit dieser Zeichenfolge verkettet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4db48-115">Pointer to a **NULL**-terminated string to concatenate to this string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4db48-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4db48-116">Remarks</span></span>

<span data-ttu-id="4db48-117">Beachten Sie, dass Arbeitsspeicher Ausnahmen immer auftreten können, wenn Sie diesen Verkettungs Operator verwenden, da neuer Speicher für Zeichen zugeordnet werden kann, die diesem [**chstring**](chstring.md) -Objekt hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4db48-117">Be aware that memory exceptions can occur whenever you use this concatenation operator because new storage may be allocated for characters added to this [**CHString**](chstring.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="4db48-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4db48-118">Examples</span></span>

<span data-ttu-id="4db48-119">Das folgende Beispiel zeigt die Verwendung von **chstring:: Operator + =**:</span><span class="sxs-lookup"><span data-stu-id="4db48-119">The following example shows the use of **CHString::operator +=**:</span></span>


```C++
CHString s( L"abc" );
assert( ( s += L"def" ) == L"abcdef" );
```



## <a name="requirements"></a><span data-ttu-id="4db48-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4db48-120">Requirements</span></span>



| <span data-ttu-id="4db48-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4db48-121">Requirement</span></span> | <span data-ttu-id="4db48-122">Wert</span><span class="sxs-lookup"><span data-stu-id="4db48-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4db48-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4db48-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4db48-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4db48-124">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="4db48-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4db48-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4db48-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4db48-126">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="4db48-127">Header</span><span class="sxs-lookup"><span data-stu-id="4db48-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4db48-128"><dt>Chstring. h (Include-Datei "f")</dt></span><span class="sxs-lookup"><span data-stu-id="4db48-128"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4db48-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4db48-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="4db48-130"><dt>Framedyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4db48-130"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="4db48-131">DLL</span><span class="sxs-lookup"><span data-stu-id="4db48-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4db48-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4db48-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4db48-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4db48-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4db48-134">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="4db48-134">**CHString**</span></span>](chstring.md)
</dt> </dl>

 

