---
description: Die Set-Struktur definiert einen Satz von Werten.
ms.assetid: 88e0ffa1-71a2-4a3f-bdf1-964de0adea62
title: Struktur festlegen (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SET
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: fdefc6f1233f820321bae6795f457e345fb5d4b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216029"
---
# <a name="set-structure"></a><span data-ttu-id="a64ad-103">Struktur festlegen</span><span class="sxs-lookup"><span data-stu-id="a64ad-103">SET structure</span></span>

<span data-ttu-id="a64ad-104">Die **Set** -Struktur definiert einen Satz von Werten.</span><span class="sxs-lookup"><span data-stu-id="a64ad-104">The **SET** structure defines a set of values.</span></span>

## <a name="syntax"></a><span data-ttu-id="a64ad-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a64ad-105">Syntax</span></span>


```C++
typedef struct _SET {
  DWORD nEntries;
  union {
    LPBYTE               lpByteTable;
    LPWORD               lpWordTable;
    LPDWORD              lpDwordTable;
    LPLARGEINT           lpLargeIntTable;
    LPSYSTEMTIME         lpSystemTimeTable;
    LPLABELED_BYTE       lpLabeledByteTable;
    LPLABELED_WORD       lpLabeledWordTable;
    LPLABELED_DWORD      lpLabeledDwordTable;
    LPLABELED_LARGEINT   lpLabeledLargeIntTable;
    LPLABELED_SYSTEMTIME lpLabeledSystemTimeTable;
    LPLABELED_BIT        lpLabeledBit;
    LPVOID               lpVoidTable;
  };
} SET, *LPSET;
```



## <a name="members"></a><span data-ttu-id="a64ad-106">Member</span><span class="sxs-lookup"><span data-stu-id="a64ad-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a64ad-107">**nentries**</span><span class="sxs-lookup"><span data-stu-id="a64ad-107">**nEntries**</span></span>
</dt> <dd>

<span data-ttu-id="a64ad-108">Die Gesamtanzahl der Einträge in einer Menge.</span><span class="sxs-lookup"><span data-stu-id="a64ad-108">Total number of entries in a set.</span></span>

</dd> <dt>

<span data-ttu-id="a64ad-109">**lpbytetable**</span><span class="sxs-lookup"><span data-stu-id="a64ad-109">**lpByteTable**</span></span>
</dt> <dd>

<span data-ttu-id="a64ad-110">Zeiger auf ein Array von Byte Werten.</span><span class="sxs-lookup"><span data-stu-id="a64ad-110">Pointer to an array of BYTE values.</span></span>

</dd> <dt>

<span data-ttu-id="a64ad-111">**lpwordtable**</span><span class="sxs-lookup"><span data-stu-id="a64ad-111">**lpWordTable**</span></span>
</dt> <dd>

<span data-ttu-id="a64ad-112">Zeiger auf ein Array von Wort Werten.</span><span class="sxs-lookup"><span data-stu-id="a64ad-112">Pointer to an array of WORD values.</span></span>

</dd> <dt>

<span data-ttu-id="a64ad-113">**lpdwordtable**</span><span class="sxs-lookup"><span data-stu-id="a64ad-113">**lpDwordTable**</span></span>
</dt> <dd>

<span data-ttu-id="a64ad-114">Zeiger auf ein Array von DWORD-Werten.</span><span class="sxs-lookup"><span data-stu-id="a64ad-114">Pointer to an array of DWORD values.</span></span>

</dd> <dt>

<span data-ttu-id="a64ad-115">**lplargeingetbar**</span><span class="sxs-lookup"><span data-stu-id="a64ad-115">**lpLargeIntTable**</span></span>
</dt> <dd>

<span data-ttu-id="a64ad-116">Zeiger auf ein Array von [largeint](largeint.md) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="a64ad-116">Pointer to an array of [LARGEINT](largeint.md) structures.</span></span>

</dd> <dt>

<span data-ttu-id="a64ad-117">**lpsystemplan**</span><span class="sxs-lookup"><span data-stu-id="a64ad-117">**lpSystemTimeTable**</span></span>
</dt> <dd>

<span data-ttu-id="a64ad-118">Zeiger auf ein Array von SYSTEMTIME-Werten.</span><span class="sxs-lookup"><span data-stu-id="a64ad-118">Pointer to an array of SYSTEMTIME values.</span></span>

</dd> <dt>

<span data-ttu-id="a64ad-119">**lplabeledbytetable**</span><span class="sxs-lookup"><span data-stu-id="a64ad-119">**lpLabeledByteTable**</span></span>
</dt> <dd>

<span data-ttu-id="a64ad-120">Zeiger auf ein Array von [markierten \_ Byte](labeled-byte.md) Strukturen.</span><span class="sxs-lookup"><span data-stu-id="a64ad-120">Pointer to an array of [LABELED\_BYTE](labeled-byte.md) structures.</span></span> <span data-ttu-id="a64ad-121">Jede **bezeichnete \_ Byte** Struktur definiert einen Wert und eine Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="a64ad-121">Each **LABELED\_BYTE** structure defines a value and label.</span></span> <span data-ttu-id="a64ad-122">Netzwerkmonitor eine Bezeichnung anzeigt, wenn ein entsprechender Wert im Protokoll Paket gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="a64ad-122">Network Monitor displays a label if it finds a corresponding value in the protocol packet.</span></span>

</dd> <dt>

<span data-ttu-id="a64ad-123">**lplabeledwordtable**</span><span class="sxs-lookup"><span data-stu-id="a64ad-123">**lpLabeledWordTable**</span></span>
</dt> <dd>

<span data-ttu-id="a64ad-124">Ein Zeiger auf ein Array von [gekennzeichneten \_ Word](labeled-word.md) -Strukturen, die einen Satz von Wort Werten und Beschriftungen definieren.</span><span class="sxs-lookup"><span data-stu-id="a64ad-124">Pointer to an array of [LABELED\_WORD](labeled-word.md) structures that define a set of WORD values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="a64ad-125">**lplabeleddwordtable**</span><span class="sxs-lookup"><span data-stu-id="a64ad-125">**lpLabeledDwordTable**</span></span>
</dt> <dd>

<span data-ttu-id="a64ad-126">Ein Zeiger auf ein Array mit [beschrifteten \_ DWORD](labeled-dword.md) -Strukturen, die einen Satz von DWORD-Werten und-Bezeichnungen definieren.</span><span class="sxs-lookup"><span data-stu-id="a64ad-126">Pointer to an array of [LABELED\_DWORD](labeled-dword.md) structures that define a set of DWORD values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="a64ad-127">**lplabeledlargeintbar**</span><span class="sxs-lookup"><span data-stu-id="a64ad-127">**lpLabeledLargeIntTable**</span></span>
</dt> <dd>

<span data-ttu-id="a64ad-128">Zeiger auf ein Array mit [beschrifteten \_ largeint](labeled-largeint.md) -Strukturen, die einen Satz von largeint-Werten und-Bezeichnungen definieren.</span><span class="sxs-lookup"><span data-stu-id="a64ad-128">Pointer to an array of [LABELED\_LARGEINT](labeled-largeint.md) structures that define a set of LARGEINT values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="a64ad-129">**lplabeledsystemplan**</span><span class="sxs-lookup"><span data-stu-id="a64ad-129">**lpLabeledSystemTimeTable**</span></span>
</dt> <dd>

<span data-ttu-id="a64ad-130">Zeiger auf ein Array von [bezeichneten \_ SYSTEMTIME](labeled-systemtime.md) -Strukturen, die einen Satz von System Werten und Beschriftungen definieren.</span><span class="sxs-lookup"><span data-stu-id="a64ad-130">Pointer to an array of [LABELED\_SYSTEMTIME](labeled-systemtime.md) structures that define a set of SYSTEM values and labels.</span></span>

</dd> <dt>

<span data-ttu-id="a64ad-131">**lplabeledbit**</span><span class="sxs-lookup"><span data-stu-id="a64ad-131">**lpLabeledBit**</span></span>
</dt> <dd>

<span data-ttu-id="a64ad-132">Ein Zeiger auf ein Array von [beschrifteten \_ bitstrukturen](labeled-bit.md) , die einen Satz von gekennzeichneten Bitpaaren definieren.</span><span class="sxs-lookup"><span data-stu-id="a64ad-132">Pointer to an array of [LABELED\_BIT](labeled-bit.md) structures that define a set of labeled BIT pairs.</span></span> <span data-ttu-id="a64ad-133">Jedes Bit kann zwei Bezeichnungen jeweils eine Bezeichnung für jeden Zustand (0 oder 1) des Bits angeben.</span><span class="sxs-lookup"><span data-stu-id="a64ad-133">Each BIT can specify two labels   one label for each state (0 or 1) of the BIT.</span></span>

</dd> <dt>

<span data-ttu-id="a64ad-134">**lpvoidtable**</span><span class="sxs-lookup"><span data-stu-id="a64ad-134">**lpVoidTable**</span></span>
</dt> <dd>

<span data-ttu-id="a64ad-135">Zeiger auf ein Array von-Werten.</span><span class="sxs-lookup"><span data-stu-id="a64ad-135">Pointer to an array of values.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a64ad-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a64ad-136">Remarks</span></span>

<span data-ttu-id="a64ad-137">Die **Set** -Struktur wird verwendet, um einen Satz von Vergleichsdaten zu definieren, die Netzwerkmonitor verwenden können, um den Wert einer Eigenschaft in einem Protokoll Paket zu interpretieren.</span><span class="sxs-lookup"><span data-stu-id="a64ad-137">The **SET** structure is used to define a set of comparison data that Network Monitor can use to interpret the value of a property in a protocol packet.</span></span> <span data-ttu-id="a64ad-138">Wenn ein Satz von Vergleichsdaten erforderlich ist, wird ein Zeiger auf die **festgelegte** Struktur im **lpset** -Member der [PropertyInfo](propertyinfo.md) -Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="a64ad-138">When a set of comparison data is required, a pointer to the **SET** structure is specified in the **lpSet** member of the [PROPERTYINFO](propertyinfo.md) structure.</span></span>

<span data-ttu-id="a64ad-139">Die Parser-DLL kann einen Werte Satz und einen Bezeichnungs Satz bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a64ad-139">The parser DLL can provide a value set and a label set.</span></span> <span data-ttu-id="a64ad-140">Der Member der **Union** , den Sie in einer **festgelegten** Struktur auswählen, verweist auf ein Array von-Strukturen, die jeden Member einer Menge definieren.</span><span class="sxs-lookup"><span data-stu-id="a64ad-140">The member of the **UNION** that you select in a **SET** structure points to an array of structures that define each member of a set.</span></span>

-   <span data-ttu-id="a64ad-141">Wert festgelegt</span><span class="sxs-lookup"><span data-stu-id="a64ad-141">Value set</span></span>

    <span data-ttu-id="a64ad-142">Ein festgelegter Wert wird verwendet, wenn Netzwerkmonitor einen in-Set-oder einen nicht in-Set-Indikator mit dem Wert enthalten soll, der im Protokoll Paket enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a64ad-142">A value set is used when you want Network Monitor to include an in-set or not-in-set indicator with the value found in the protocol packet.</span></span> <span data-ttu-id="a64ad-143">Wenn z. b. ein DWORD-Satz angegeben ist, zeigt Netzwerkmonitor eine Bezeichnung für jeden DWORD-Wert an, der im Protokoll Paket enthalten ist, und gibt an, dass das DWORD-oder nicht im Satz angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="a64ad-143">For example, if a DWORD set is specified, Network Monitor displays a label for each DWORD value found in the protocol packet, indicating that the DWORD is or is not specified in the set.</span></span>

    <span data-ttu-id="a64ad-144">Ein festgelegtes Wert kann auf den Datentypen Byte, Word, DWORD, largeint und SYSTEMTIME basieren.</span><span class="sxs-lookup"><span data-stu-id="a64ad-144">A value set can be based on BYTE, WORD, DWORD, LARGEINT, and SYSTEMTIME data types.</span></span>

-   <span data-ttu-id="a64ad-145">Bezeichnungs Satz</span><span class="sxs-lookup"><span data-stu-id="a64ad-145">Label set</span></span>

    <span data-ttu-id="a64ad-146">Ein Bezeichnungs Satz wird verwendet, wenn Sie Netzwerkmonitor eine benutzerdefinierte Bezeichnung anstelle der in einer Menge angegebenen Eigenschaftswerte anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="a64ad-146">A label set is used when you want Network Monitor to display a user-defined label instead of the property values specified in a set.</span></span>

    <span data-ttu-id="a64ad-147">Ein Bezeichnungs Satz kann auf Byte-, Word-, DWORD-, largeint-, SYSTEMTIME-und Bit-Bezeichnungs Paaren basieren.</span><span class="sxs-lookup"><span data-stu-id="a64ad-147">A label set can be based on BYTE, WORD, DWORD, LARGEINT, SYSTEMTIME and BIT label pairs.</span></span>

## <a name="requirements"></a><span data-ttu-id="a64ad-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a64ad-148">Requirements</span></span>



| <span data-ttu-id="a64ad-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a64ad-149">Requirement</span></span> | <span data-ttu-id="a64ad-150">Wert</span><span class="sxs-lookup"><span data-stu-id="a64ad-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a64ad-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a64ad-151">Minimum supported client</span></span><br/> | <span data-ttu-id="a64ad-152">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a64ad-152">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a64ad-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a64ad-153">Minimum supported server</span></span><br/> | <span data-ttu-id="a64ad-154">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a64ad-154">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a64ad-155">Header</span><span class="sxs-lookup"><span data-stu-id="a64ad-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="a64ad-156"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a64ad-156"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a64ad-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a64ad-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a64ad-158">beschriftetes \_ Bit</span><span class="sxs-lookup"><span data-stu-id="a64ad-158">LABELED\_BIT</span></span>](labeled-bit.md)
</dt> <dt>

[<span data-ttu-id="a64ad-159">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="a64ad-159">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> </dl>

 

 




