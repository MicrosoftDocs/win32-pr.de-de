---
description: Stellt eine Linie im oberen Bereich der Ereignisanzeige bereit, die als Container für alle möglichen Daten dient, die in eine Spalte eingefügt werden.
ms.assetid: 2ad32c23-5dbe-46be-b0cc-ccf7a6fe8ec3
title: Nmcolumnvariant-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NMCOLUMNVARIANT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: e9f70d2d1a0caf63411fcd2b44d5ed8bdcbecd00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352765"
---
# <a name="nmcolumnvariant-structure"></a><span data-ttu-id="dce19-103">Nmcolumnvariant-Struktur</span><span class="sxs-lookup"><span data-stu-id="dce19-103">NMCOLUMNVARIANT structure</span></span>

<span data-ttu-id="dce19-104">Die **nmcolumnvariant** -Struktur stellt eine Linie im oberen Bereich der Ereignisanzeige bereit, die als Container für alle möglichen Daten dient, die in eine Spalte eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="dce19-104">The **NMCOLUMNVARIANT** structure provides a line in the top pane of the Event Viewer that serves as a container for all possible data inserted into a column.</span></span>

## <a name="syntax"></a><span data-ttu-id="dce19-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dce19-105">Syntax</span></span>


```C++
typedef struct {
  NMCOLUMNTYPE Type;
  union {
    BYTE        Uint8Val;
    char        Sint8Val;
    WORD        Uint16Val;
    short       Sint16Val;
    DWORD       Uint32Val;
    LONG        Sint32Val;
    DOUBLE      Float64Val;
    DWORD       FrameVal;
    BOOL        YesNoVal;
    BOOL        OnOffVal;
    BOOL        TrueFalseVal;
    BYTE        MACAddrVal[MAC_ADDRESS_SIZE];
    IPX_ADDRESS IPXAddrVal;
    DWORD       IPAddrVal;
    DOUBLE      VarTimeVal;
    LPSTR       pStringVal;
  } Value;
} NMCOLUMNVARIANT;
```



## <a name="members"></a><span data-ttu-id="dce19-106">Member</span><span class="sxs-lookup"><span data-stu-id="dce19-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="dce19-107">**Type**</span><span class="sxs-lookup"><span data-stu-id="dce19-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="dce19-108">Ein Wert aus dem [**nmcolumntype**](nmcolumntype.md) -Enumerationstyp.</span><span class="sxs-lookup"><span data-stu-id="dce19-108">A value from the [**NMCOLUMNTYPE**](nmcolumntype.md) enumeration type.</span></span>

</dd> <dt>

<span data-ttu-id="dce19-109">**Wert**</span><span class="sxs-lookup"><span data-stu-id="dce19-109">**Value**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dce19-110">**Uint8Val**</span><span class="sxs-lookup"><span data-stu-id="dce19-110">**Uint8Val**</span></span>
</dt> <dd>

<span data-ttu-id="dce19-111">ganzzahliger 8-Bit-Wert ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="dce19-111">8-bit unsigned integer value.</span></span>

</dd> <dt>

<span data-ttu-id="dce19-112">**Sint8Val**</span><span class="sxs-lookup"><span data-stu-id="dce19-112">**Sint8Val**</span></span>
</dt> <dd>

<span data-ttu-id="dce19-113">ganzzahliger 8-Bit-Wert mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="dce19-113">8-bit signed integer value.</span></span>

</dd> <dt>

<span data-ttu-id="dce19-114">**Uint16Val**</span><span class="sxs-lookup"><span data-stu-id="dce19-114">**Uint16Val**</span></span>
</dt> <dd>

<span data-ttu-id="dce19-115">ganzzahliger 16-Bit-Wert ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="dce19-115">16-bit unsigned integer value.</span></span>

</dd> <dt>

<span data-ttu-id="dce19-116">**Sint16Val**</span><span class="sxs-lookup"><span data-stu-id="dce19-116">**Sint16Val**</span></span>
</dt> <dd>

<span data-ttu-id="dce19-117">ganzzahliger 16-Bit-Wert mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="dce19-117">16-bit signed integer value.</span></span>

</dd> <dt>

<span data-ttu-id="dce19-118">**Uint32Val**</span><span class="sxs-lookup"><span data-stu-id="dce19-118">**Uint32Val**</span></span>
</dt> <dd>

<span data-ttu-id="dce19-119">32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="dce19-119">32-bit unsigned integer value.</span></span>

</dd> <dt>

<span data-ttu-id="dce19-120">**Sint32Val**</span><span class="sxs-lookup"><span data-stu-id="dce19-120">**Sint32Val**</span></span>
</dt> <dd>

<span data-ttu-id="dce19-121">32-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="dce19-121">32-bit signed integer value.</span></span>

</dd> <dt>

<span data-ttu-id="dce19-122">**Float64Val**</span><span class="sxs-lookup"><span data-stu-id="dce19-122">**Float64Val**</span></span>
</dt> <dd>

<span data-ttu-id="dce19-123">64-Bit-Float-Wert.</span><span class="sxs-lookup"><span data-stu-id="dce19-123">64-bit float value.</span></span>

</dd> <dt>

<span data-ttu-id="dce19-124">**Frameval**</span><span class="sxs-lookup"><span data-stu-id="dce19-124">**FrameVal**</span></span>
</dt> <dd>

<span data-ttu-id="dce19-125">Frame Nummer.</span><span class="sxs-lookup"><span data-stu-id="dce19-125">Frame number.</span></span>

</dd> <dt>

<span data-ttu-id="dce19-126">**Yesnoval**</span><span class="sxs-lookup"><span data-stu-id="dce19-126">**YesNoVal**</span></span>
</dt> <dd>

<span data-ttu-id="dce19-127">Zeigt ja oder Nein an.</span><span class="sxs-lookup"><span data-stu-id="dce19-127">Displays Yes or No.</span></span>

</dd> <dt>

<span data-ttu-id="dce19-128">**Onoffval**</span><span class="sxs-lookup"><span data-stu-id="dce19-128">**OnOffVal**</span></span>
</dt> <dd>

<span data-ttu-id="dce19-129">Wird ein-oder ausgeschaltet angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dce19-129">Displays On or Off.</span></span>

</dd> <dt>

<span data-ttu-id="dce19-130">**Truefalsee Val**</span><span class="sxs-lookup"><span data-stu-id="dce19-130">**TrueFalseVal**</span></span>
</dt> <dd>

<span data-ttu-id="dce19-131">Zeigt True oder false an.</span><span class="sxs-lookup"><span data-stu-id="dce19-131">Displays True or False.</span></span>

</dd> <dt>

<span data-ttu-id="dce19-132">**Macaddrval**</span><span class="sxs-lookup"><span data-stu-id="dce19-132">**MACAddrVal**</span></span>
</dt> <dd>

<span data-ttu-id="dce19-133">MAC-Adresse</span><span class="sxs-lookup"><span data-stu-id="dce19-133">MAC address.</span></span>

</dd> <dt>

<span data-ttu-id="dce19-134">**Ipxaddrval**</span><span class="sxs-lookup"><span data-stu-id="dce19-134">**IPXAddrVal**</span></span>
</dt> <dd>

<span data-ttu-id="dce19-135">IPX-Adresse</span><span class="sxs-lookup"><span data-stu-id="dce19-135">IPX address.</span></span>

</dd> <dt>

<span data-ttu-id="dce19-136">**Ipaddrval**</span><span class="sxs-lookup"><span data-stu-id="dce19-136">**IPAddrVal**</span></span>
</dt> <dd>

<span data-ttu-id="dce19-137">IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="dce19-137">IP address.</span></span>

</dd> <dt>

<span data-ttu-id="dce19-138">**Vartimeval**</span><span class="sxs-lookup"><span data-stu-id="dce19-138">**VarTimeVal**</span></span>
</dt> <dd>

<span data-ttu-id="dce19-139">Variant-Zeit.</span><span class="sxs-lookup"><span data-stu-id="dce19-139">Variant time.</span></span> <span data-ttu-id="dce19-140">Verwenden Sie **varianttimeumsystemtime** , um in die Systemzeit zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="dce19-140">Use **VariantTimetoSystemTime** to convert to system time.</span></span>

</dd> <dt>

<span data-ttu-id="dce19-141">**pstringval**</span><span class="sxs-lookup"><span data-stu-id="dce19-141">**pStringVal**</span></span>
</dt> <dd>

<span data-ttu-id="dce19-142">Zeiger auf eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="dce19-142">Pointer to a string.</span></span>

</dd> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dce19-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dce19-143">Requirements</span></span>



| <span data-ttu-id="dce19-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dce19-144">Requirement</span></span> | <span data-ttu-id="dce19-145">Wert</span><span class="sxs-lookup"><span data-stu-id="dce19-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dce19-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="dce19-146">Minimum supported client</span></span><br/> | <span data-ttu-id="dce19-147">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dce19-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="dce19-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="dce19-148">Minimum supported server</span></span><br/> | <span data-ttu-id="dce19-149">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="dce19-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="dce19-150">Header</span><span class="sxs-lookup"><span data-stu-id="dce19-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="dce19-151"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="dce19-151"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dce19-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dce19-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dce19-153">**Nmcolumntype**</span><span class="sxs-lookup"><span data-stu-id="dce19-153">**NMCOLUMNTYPE**</span></span>](nmcolumntype.md)
</dt> </dl>

 

 




