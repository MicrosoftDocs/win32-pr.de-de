---
description: Diese Index Operatoren legen das Element am angegebenen Index fest oder erhalten es. Diese Operatoren sind eine bequeme Ersetzung für die Methoden "Methode" und "GetAt".
ms.assetid: 93b10bef-908e-4c5e-aac3-b13051b2e7c9
ms.tgt_platform: multiple
title: 'Chstringarray:: Operator [] (chstrarr. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92b30768b9d013bfca672548a7c58b0eeffb455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351031"
---
# <a name="chstringarrayoperator--"></a><span data-ttu-id="0109b-104">Chstringarray::-Operator \[\]</span><span class="sxs-lookup"><span data-stu-id="0109b-104">CHStringArray::operator \[ \]</span></span>

<span data-ttu-id="0109b-105">\[Die [**chstringarray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt als Endzustand betrachtet wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="0109b-105">\[The [**CHStringArray**](/windows/desktop/api/ChStrArr/nl-chstrarr-chstringarray) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="0109b-106">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="0109b-106">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="0109b-107">Diese Index Operatoren legen das Element am angegebenen Index fest oder erhalten es.</span><span class="sxs-lookup"><span data-stu-id="0109b-107">These subscript operators set or get the element at the specified index.</span></span> <span data-ttu-id="0109b-108">Diese Operatoren sind eine bequeme Ersetzung für die Methoden "Methode [**" und "**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr)) [**GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int)) ".</span><span class="sxs-lookup"><span data-stu-id="0109b-108">These operators are a convenient substitute for the [**SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr)) and [**GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int)) methods.</span></span>

``` syntax
CHString& operator []( 
  int nIndex
);

CHString operator []( 
  int nIndex
) const;
```

## <a name="parameters"></a><span data-ttu-id="0109b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0109b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0109b-110"><span id="nIndex"></span><span id="nindex"></span><span id="NINDEX"></span>*nIndex*</span><span class="sxs-lookup"><span data-stu-id="0109b-110"><span id="nIndex"></span><span id="nindex"></span><span id="NINDEX"></span>*nIndex*</span></span>
</dt> <dd>

<span data-ttu-id="0109b-111">Ein ganzzahliger Index, der größer oder gleich 0 (null) und kleiner oder gleich dem von [ **GetUpperBound** zurückgegebenen Wert ist.](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)</span><span class="sxs-lookup"><span data-stu-id="0109b-111">An integer index that is greater than or equal to zero and less than or equal to the value returned by [**GetUpperBound**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getupperbound)</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="0109b-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="0109b-112">Return Values</span></span>

<span data-ttu-id="0109b-113">Die Index Operatoren geben das [**chstring**](chstring.md) -Zeiger Element zurück, das sich derzeit an diesem Index befindet.</span><span class="sxs-lookup"><span data-stu-id="0109b-113">The subscript operators return the [**CHString**](chstring.md) pointer element currently at this index.</span></span>

## <a name="remarks"></a><span data-ttu-id="0109b-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0109b-114">Remarks</span></span>

<span data-ttu-id="0109b-115">Sie können den ersten Operator verwenden, der für Arrays, die nicht **konstant** sind, entweder auf der rechten (r-Wert) oder der linken (l-Wert)-Seite einer Zuweisungsanweisung aufruft.</span><span class="sxs-lookup"><span data-stu-id="0109b-115">You can use the first operator, which calls for arrays that are not **const**, on either the right (r-value) or the left (l-value) side of an assignment statement.</span></span> <span data-ttu-id="0109b-116">Die zweite, die für **Konstanten** Arrays aufruft, kann nur auf der rechten Seite verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0109b-116">The second, which calls for **const** arrays, can be used only on the right.</span></span>

<span data-ttu-id="0109b-117">Die Debugversion der Bibliothek bestätigt, ob der Index (entweder auf der linken oder rechten Seite einer Zuweisungsanweisung) außerhalb des gültigen Bereichs liegt.</span><span class="sxs-lookup"><span data-stu-id="0109b-117">The debug version of the library asserts if the subscript (either on the left or right side of an assignment statement) is out of bounds.</span></span>

## <a name="examples"></a><span data-ttu-id="0109b-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0109b-118">Examples</span></span>

<span data-ttu-id="0109b-119">Das folgende Codebeispiel zeigt die Verwendung von [**chstringarray:: Operator \[ \]**](/previous-versions/windows/desktop/legacy/aa384934(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0109b-119">The following code example shows the use of [**CHStringArray::operator \[\]**](/previous-versions/windows/desktop/legacy/aa384934(v=vs.85)).</span></span>


```C++
CHStringArray array;
CHString s;

array.Add( L"String 1" ); // Element 0 
array.Add( L"String 2" ); // Element 1 
s = array[0]; // Get element 0
assert( s == L"String 1" ); 

array[0] = L"String 3"; // Replace element 0 
assert( array[0] == L"String 3" );
```



## <a name="requirements"></a><span data-ttu-id="0109b-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0109b-120">Requirements</span></span>



| <span data-ttu-id="0109b-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0109b-121">Requirement</span></span> | <span data-ttu-id="0109b-122">Wert</span><span class="sxs-lookup"><span data-stu-id="0109b-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0109b-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0109b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0109b-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0109b-124">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="0109b-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0109b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0109b-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0109b-126">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="0109b-127">Header</span><span class="sxs-lookup"><span data-stu-id="0109b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0109b-128"><dt>Chstrauarr. h (Include-Datei "f")</dt></span><span class="sxs-lookup"><span data-stu-id="0109b-128"><dt>ChStrArr.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="0109b-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0109b-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="0109b-130"><dt>Framedyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0109b-130"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="0109b-131">DLL</span><span class="sxs-lookup"><span data-stu-id="0109b-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0109b-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0109b-132"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0109b-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0109b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0109b-134">**Chstringarray:: Add**</span><span class="sxs-lookup"><span data-stu-id="0109b-134">**CHStringArray::Add**</span></span>](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-add)
</dt> <dt>

<span data-ttu-id="0109b-135">[**Chstringarray:: GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))</span><span class="sxs-lookup"><span data-stu-id="0109b-135">[**CHStringArray::GetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-getat(int))</span></span>
</dt> <dt>

<span data-ttu-id="0109b-136">[**Chstringarray::**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))</span><span class="sxs-lookup"><span data-stu-id="0109b-136">[**CHStringArray::SetAt**](/windows/desktop/api/ChStrArr/nf-chstrarr-chstringarray-setat(int_lpcwstr))</span></span>
</dt> </dl>

