---
description: Der Operator "chstring-Zuweisung (=)" Initialisiert ein vorhandenes "chstring"-Objekt mit neuen Daten erneut.
ms.assetid: 6864aacf-ac18-4b5a-be3e-3a0d8bb31e74
ms.tgt_platform: multiple
title: 'Chstring:: Operator = (chstring. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9abfa9ea2b72aa8f6830d9fb6388861c8c3b82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042368"
---
# <a name="chstringoperator"></a><span data-ttu-id="1f1b6-103">Chstring:: Operator =</span><span class="sxs-lookup"><span data-stu-id="1f1b6-103">CHString::operator=</span></span>

<span data-ttu-id="1f1b6-104">\[Die [**chstring**](chstring.md) -Klasse ist Teil des WMI-Anbieter-Frameworks, das jetzt im Endzustand behandelt wird, und keine weiteren Entwicklungen, Verbesserungen oder Updates werden für nicht sicherheitsrelevante Probleme verfügbar sein, die diese Bibliotheken betreffen.</span><span class="sxs-lookup"><span data-stu-id="1f1b6-104">\[The [**CHString**](chstring.md) class is part of the WMI Provider Framework which is now considered in final state, and no further development, enhancements, or updates will be available for non-security related issues affecting these libraries.</span></span> <span data-ttu-id="1f1b6-105">Die [Mi-APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) sollten für alle neuen Entwicklungen verwendet werden.\]</span><span class="sxs-lookup"><span data-stu-id="1f1b6-105">The [MI APIs](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure) should be used for all new development.\]</span></span>

<span data-ttu-id="1f1b6-106">Der Operator " [**chstring**](chstring.md) -Zuweisung (=)" Initialisiert ein vorhandenes "chstring"-Objekt mit neuen Daten erneut.</span><span class="sxs-lookup"><span data-stu-id="1f1b6-106">The [**CHString**](chstring.md) assignment (=) operator reinitializes an existing CHString object with new data.</span></span>

``` syntax
const CHString& operator =(
  const CHString& stringSrc )
throw( CHeap_Exception );

const CHString& operator =(
  WCHAR ch )
throw( CHeap_Exception );

const CHString& operator =(
  const unsigned char* psz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCWSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  LPCSTR lpsz )
throw( CHeap_Exception );

const CHString& operator =(
  CHString *p )
throw( CHeap_Exception );

const CHString& operator =(
  char ch )
throw( CHeap_Exception );
```

## <a name="parameters"></a><span data-ttu-id="1f1b6-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f1b6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f1b6-108"><span id="stringSrc__p"></span><span id="stringsrc__p"></span><span id="STRINGSRC__P"></span>*stringsrc*, *p*</span><span class="sxs-lookup"><span data-stu-id="1f1b6-108"><span id="stringSrc__p"></span><span id="stringsrc__p"></span><span id="STRINGSRC__P"></span>*stringSrc*, *p*</span></span>
</dt> <dd>

<span data-ttu-id="1f1b6-109">Weist diesem- [**Objekt eine Zeichen**](chstring.md) folgen Zeichenfolge zu.</span><span class="sxs-lookup"><span data-stu-id="1f1b6-109">Assigns a [**CHString**](chstring.md) string to this object.</span></span>

</dd> <dt>

<span data-ttu-id="1f1b6-110"><span id="ch"></span><span id="CH"></span>*ch*</span><span class="sxs-lookup"><span data-stu-id="1f1b6-110"><span id="ch"></span><span id="CH"></span>*ch*</span></span>
</dt> <dd>

<span data-ttu-id="1f1b6-111">Weist diesem-Objekt ein Zeichen zu.</span><span class="sxs-lookup"><span data-stu-id="1f1b6-111">Assigns a character to this object.</span></span>

</dd> <dt>

<span data-ttu-id="1f1b6-112"><span id="lpsz__psz"></span><span id="LPSZ__PSZ"></span>*lpsz*, *PSZ*</span><span class="sxs-lookup"><span data-stu-id="1f1b6-112"><span id="lpsz__psz"></span><span id="LPSZ__PSZ"></span>*lpsz*, *psz*</span></span>
</dt> <dd>

<span data-ttu-id="1f1b6-113">Weist diesem-Objekt eine **null**-terminierte Zeichenfolge zu.</span><span class="sxs-lookup"><span data-stu-id="1f1b6-113">Assigns a **NULL**-terminated string to this object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1f1b6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f1b6-114">Remarks</span></span>

<span data-ttu-id="1f1b6-115">Wenn die Ziel Zeichenfolge (d. h. die linke Seite) bereits groß genug ist, um die neuen Daten zu speichern, erfolgt keine neue Speicher Belegung.</span><span class="sxs-lookup"><span data-stu-id="1f1b6-115">If the destination string (that is, the left side) is already large enough to store the new data, no new memory allocation is performed.</span></span> <span data-ttu-id="1f1b6-116">Arbeitsspeicher Ausnahmen können jedoch immer auftreten, wenn Sie den Zuweisungs Operator verwenden, da der neue Speicher häufig dem resultierenden [**chstring**](chstring.md) -Objekt zugeordnet wird.</span><span class="sxs-lookup"><span data-stu-id="1f1b6-116">However, memory exceptions can occur whenever you use the assignment operator because new storage is often allocated to hold the resulting [**CHString**](chstring.md) object.</span></span>

## <a name="examples"></a><span data-ttu-id="1f1b6-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f1b6-117">Examples</span></span>

<span data-ttu-id="1f1b6-118">Das folgende Codebeispiel zeigt die Verwendung von **chstring:: Operator =**:</span><span class="sxs-lookup"><span data-stu-id="1f1b6-118">The following code example shows the use of **CHString::operator =**:</span></span>


```C++
CHString s1, s2;        // Empty CHString objects

s1 = L"cat";            // s1 = "cat"
s2 = s1;                // s1 and s2 each = "cat"
s1 = L"the " + s1;      // Or expressions
s1 = 'x';               // Or just individual characters
```



## <a name="requirements"></a><span data-ttu-id="1f1b6-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f1b6-119">Requirements</span></span>



| <span data-ttu-id="1f1b6-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f1b6-120">Requirement</span></span> | <span data-ttu-id="1f1b6-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1f1b6-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f1b6-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f1b6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1f1b6-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1f1b6-123">Windows Vista</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="1f1b6-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f1b6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1f1b6-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1f1b6-125">Windows Server 2008</span></span><br/>                                                                                                                                |
| <span data-ttu-id="1f1b6-126">Header</span><span class="sxs-lookup"><span data-stu-id="1f1b6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f1b6-127"><dt>Chstring. h (Include-Datei "f")</dt></span><span class="sxs-lookup"><span data-stu-id="1f1b6-127"><dt>ChString.h (include FwCommon.h)</dt></span></span> </dl>                                                    |
| <span data-ttu-id="1f1b6-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1f1b6-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="1f1b6-129"><dt>Framedyn. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1f1b6-129"><dt>FrameDyn.lib</dt></span></span> </dl>                                                                       |
| <span data-ttu-id="1f1b6-130">DLL</span><span class="sxs-lookup"><span data-stu-id="1f1b6-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1f1b6-131"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1f1b6-131"><dt>FrameDynOS.dll; </dt> <dt>FrameDyn.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f1b6-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f1b6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1f1b6-133">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="1f1b6-133">**CHString**</span></span>](chstring.md)
</dt> </dl>

 

