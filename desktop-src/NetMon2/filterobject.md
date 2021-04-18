---
description: Definiert ein einzelnes Objekt eines Anzeige Filters.
ms.assetid: 865b55f3-9294-43c5-b4dc-eb5128ce3a38
title: Filterobject-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FILTEROBJECT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 7649ab294f2ecad90946926dcc68d6937b357666
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345481"
---
# <a name="filterobject-structure"></a><span data-ttu-id="d7d3d-103">Filterobject-Struktur</span><span class="sxs-lookup"><span data-stu-id="d7d3d-103">FILTEROBJECT structure</span></span>

<span data-ttu-id="d7d3d-104">Die **filterobject** -Struktur definiert ein einzelnes Objekt eines Anzeige Filters.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-104">The **FILTEROBJECT** structure defines a single object of a display filter.</span></span> <span data-ttu-id="d7d3d-105">Die [**FilterAddObject**](filteraddobject.md) -Funktion verwendet **filterobject** , um einen Anzeige Filter zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-105">The [**FilterAddObject**](filteraddobject.md) function uses **FILTEROBJECT** to build a display filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7d3d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7d3d-106">Syntax</span></span>


```C++
typedef struct _FILTEROBJECT {
  FILTERACTIONTYPE     Action;
  HPROPERTY            hProperty;
  union {
    VALUETYPE           Value;
    HPROTOCOL           hProtocol;
    LPVOID              lpArray;
    LPPROTOCOLTABLETYPE lpProtocolTable;
    LPADDRESS           lpAddress;
    ULPLARGEINT         lpLargeInt;
    ULPTIME             lpTime;
    LPOBJECT_IDENTIFIER lpOID;
  };
  union {
    WORD ByteCount;
    WORD ByteOffset;
  };
  struct _FILTEROBJECT  *pNext;
} FILTEROBJECT, *LPFILTEROBJECT;
```



## <a name="members"></a><span data-ttu-id="d7d3d-107">Member</span><span class="sxs-lookup"><span data-stu-id="d7d3d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="d7d3d-108">**Aktion**</span><span class="sxs-lookup"><span data-stu-id="d7d3d-108">**Action**</span></span>
</dt> <dd>

<span data-ttu-id="d7d3d-109">Flag, das die **filterobject** -Aktion angibt.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-109">Flag that specifies the **FILTEROBJECT** action.</span></span> <span data-ttu-id="d7d3d-110">Ein Flag kann eine Eigenschaft, einen Wert oder einen Operator angeben.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-110">A flag can specify a property, value, or operator.</span></span>

<span data-ttu-id="d7d3d-111">In der folgenden Tabelle sind die Eigenschaftenflags für Aktions Member aufgelistet</span><span class="sxs-lookup"><span data-stu-id="d7d3d-111">The following table lists Action member property flags.</span></span>



| <span data-ttu-id="d7d3d-112">Wert</span><span class="sxs-lookup"><span data-stu-id="d7d3d-112">Value</span></span>                                                                                                                                                                                                | <span data-ttu-id="d7d3d-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d7d3d-113">Meaning</span></span>                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span id="FILTERACTION_PROPERTY"></span><span id="filteraction_property"></span><dl> <span data-ttu-id="d7d3d-114"><dt>**filteraction ( \_ Eigenschaft)**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-114"><dt>**FILTERACTION\_PROPERTY**</dt></span></span> </dl>                | <span data-ttu-id="d7d3d-115">Enthält diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-115">Contains this property.</span></span><br/>                                     |
| <span id="FILTERACTION_PROPERTYEXIST"></span><span id="filteraction_propertyexist"></span><dl> <span data-ttu-id="d7d3d-116"><dt>**filteraction \_ PropertyExist**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-116"><dt>**FILTERACTION\_PROPERTYEXIST**</dt></span></span> </dl> | <span data-ttu-id="d7d3d-117">Gibt an, dass eine Filter Aktions Eigenschaft bereits definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-117">Indicates that a filter action property is already defined.</span></span><br/> |



 

<span data-ttu-id="d7d3d-118">In der folgenden Tabelle sind die wertflags für Aktions Mitglieder aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-118">The following table lists Action member value flags.</span></span>



| <span data-ttu-id="d7d3d-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d7d3d-119">Value</span></span>                                                                                                                                                                                        | <span data-ttu-id="d7d3d-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d7d3d-120">Meaning</span></span>                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="FILTERACTION_VALUE"></span><span id="filteraction_value"></span><dl> <span data-ttu-id="d7d3d-121"><dt>**filteraction- \_ Wert**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-121"><dt>**FILTERACTION\_VALUE**</dt></span></span> </dl>                 | <span data-ttu-id="d7d3d-122">Enthält diesen Wert.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-122">Contains this value.</span></span><br/>                                             |
| <span id="FILTERACTION_STRING"></span><span id="filteraction_string"></span><dl> <span data-ttu-id="d7d3d-123"><dt>**filteraction- \_ Zeichenfolge**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-123"><dt>**FILTERACTION\_STRING**</dt></span></span> </dl>              | <span data-ttu-id="d7d3d-124">Enthält diese Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-124">Contains this string.</span></span><br/>                                            |
| <span id="FILTERACTION_ARRAY"></span><span id="filteraction_array"></span><dl> <span data-ttu-id="d7d3d-125"><dt>**filteraction- \_ Array**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-125"><dt>**FILTERACTION\_ARRAY**</dt></span></span> </dl>                 | <span data-ttu-id="d7d3d-126">Enthält dieses Array.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-126">Contains this array.</span></span><br/>                                             |
| <span id="FILTERACTION_CONTAINSNC"></span><span id="filteraction_containsnc"></span><dl> <span data-ttu-id="d7d3d-127"><dt>**filteraction ( \_ kontainsnc)**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-127"><dt>**FILTERACTION\_CONTAINSNC**</dt></span></span> </dl>  | <span data-ttu-id="d7d3d-128">Gibt an, dass eine Eigenschaft eine Teil Zeichenfolge ohne Beachtung der Groß-und klein</span><span class="sxs-lookup"><span data-stu-id="d7d3d-128">Indicates that a property contains a case-insensitive substring.</span></span><br/> |
| <span id="FILTERACTION_CONTAINS"></span><span id="filteraction_contains"></span><dl> <span data-ttu-id="d7d3d-129"><dt>**filteraction \_ enthält**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-129"><dt>**FILTERACTION\_CONTAINS**</dt></span></span> </dl>        | <span data-ttu-id="d7d3d-130">Gibt an, dass eine Eigenschaft eine Teil Zeichenfolge mit Beachtung der groß-</span><span class="sxs-lookup"><span data-stu-id="d7d3d-130">Indicates that a property contains a case sensitive substring.</span></span><br/>   |
| <span id="FILTERACTION_ADDRESS"></span><span id="filteraction_address"></span><dl> <span data-ttu-id="d7d3d-131"><dt>**filteraction- \_ Adresse**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-131"><dt>**FILTERACTION\_ADDRESS**</dt></span></span> </dl>           | <span data-ttu-id="d7d3d-132">Enthält die Mac-Adresse.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-132">Contains the MAC address.</span></span><br/>                                        |
| <span id="FILTERACTION_ADDRESSANY"></span><span id="filteraction_addressany"></span><dl> <span data-ttu-id="d7d3d-133"><dt>**"filteraction \_ addressany"**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-133"><dt>**FILTERACTION\_ADDRESSANY**</dt></span></span> </dl>  | <span data-ttu-id="d7d3d-134">Entspricht einer beliebigen Mac-Adresse.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-134">Matches any MAC address.</span></span><br/>                                         |
| <span id="FILTERACTION_FROM"></span><span id="filteraction_from"></span><dl> <span data-ttu-id="d7d3d-135"><dt>**filteraction \_ aus**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-135"><dt>**FILTERACTION\_FROM**</dt></span></span> </dl>                    | <span data-ttu-id="d7d3d-136">Gibt die **von Mac** -Adresse an.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-136">Indicates the **From MAC** address.</span></span><br/>                              |
| <span id="FILTERACTION_TO"></span><span id="filteraction_to"></span><dl> <span data-ttu-id="d7d3d-137"><dt>**filteraction \_ in**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-137"><dt>**FILTERACTION\_TO**</dt></span></span> </dl>                          | <span data-ttu-id="d7d3d-138">Gibt die **an Mac** -Adresse an.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-138">Indicates the **To MAC** address.</span></span><br/>                                |
| <span id="FILTERACTION_FROMTO"></span><span id="filteraction_fromto"></span><dl> <span data-ttu-id="d7d3d-139"><dt>**filteraction \_ FromTo**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-139"><dt>**FILTERACTION\_FROMTO**</dt></span></span> </dl>              | <span data-ttu-id="d7d3d-140">Gibt eine **from/to-** Kopplung von Mac-Adressen an.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-140">Indicates a **From/To** pairing of MAC addresses.</span></span><br/>                |
| <span id="FILTERACTION_LARGEINT"></span><span id="filteraction_largeint"></span><dl> <span data-ttu-id="d7d3d-141"><dt>**filteraction \_ largeint**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-141"><dt>**FILTERACTION\_LARGEINT**</dt></span></span> </dl>        | <span data-ttu-id="d7d3d-142">Enthält eine große Ganzzahl.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-142">Contains a large integer.</span></span><br/>                                        |
| <span id="FILTERACTION_TIME"></span><span id="filteraction_time"></span><dl> <span data-ttu-id="d7d3d-143"><dt>**filteraction- \_ Zeit**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-143"><dt>**FILTERACTION\_TIME**</dt></span></span> </dl>                    | <span data-ttu-id="d7d3d-144">Enthält eine **SYSTEMTIME** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-144">Contains a **SYSTEMTIME** structure.</span></span><br/>                             |
| <span id="FILTERACTION_ADDR_ETHER"></span><span id="filteraction_addr_ether"></span><dl> <span data-ttu-id="d7d3d-145"><dt>**filteraction- \_ addr- \_ Äther**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-145"><dt>**FILTERACTION\_ADDR\_ETHER**</dt></span></span> </dl> | <span data-ttu-id="d7d3d-146">Enthält eine Ethernet-MAC-Adresse.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-146">Contains an Ethernet MAC address.</span></span><br/>                                |
| <span id="FILTERACTION_ADDR_TOKEN"></span><span id="filteraction_addr_token"></span><dl> <span data-ttu-id="d7d3d-147"><dt>**filteraction- \_ addr- \_ Token**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-147"><dt>**FILTERACTION\_ADDR\_TOKEN**</dt></span></span> </dl> | <span data-ttu-id="d7d3d-148">Enthält eine TokenRing-Mac-Adresse.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-148">Contains a token ring MAC address.</span></span><br/>                               |
| <span id="FILTERACTION_ADDR_FDDI"></span><span id="filteraction_addr_fddi"></span><dl> <span data-ttu-id="d7d3d-149"><dt>**filteraction \_ addr- \_ fiddi**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-149"><dt>**FILTERACTION\_ADDR\_FDDI**</dt></span></span> </dl>    | <span data-ttu-id="d7d3d-150">Enthält eine GDDI-Mac-Adresse.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-150">Contains a FDDI MAC address.</span></span><br/>                                     |
| <span id="FILTERACTION_ADDR_IPX"></span><span id="filteraction_addr_ipx"></span><dl> <span data-ttu-id="d7d3d-151"><dt>**filteraction \_ addr \_ IPX**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-151"><dt>**FILTERACTION\_ADDR\_IPX**</dt></span></span> </dl>       | <span data-ttu-id="d7d3d-152">Enthält eine IPX-Mac-Adresse.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-152">Contains an IPX MAC address.</span></span><br/>                                     |
| <span id="FILTERACTION_ADDR_IP"></span><span id="filteraction_addr_ip"></span><dl> <span data-ttu-id="d7d3d-153"><dt>**filteraction \_ addr \_ -IP**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-153"><dt>**FILTERACTION\_ADDR\_IP**</dt></span></span> </dl>          | <span data-ttu-id="d7d3d-154">Enthält eine IP-MAC-Adresse.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-154">Contains an IP MAC address.</span></span><br/>                                      |
| <span id="FILTERACTION_OID"></span><span id="filteraction_oid"></span><dl> <span data-ttu-id="d7d3d-155"><dt>**filteraction- \_ OID**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-155"><dt>**FILTERACTION\_OID**</dt></span></span> </dl>                       | <span data-ttu-id="d7d3d-156">Enthält einen Objekt Bezeichner (OID).</span><span class="sxs-lookup"><span data-stu-id="d7d3d-156">Contains an Object Identifier (OID).</span></span><br/>                             |



 

<span data-ttu-id="d7d3d-157">In der folgenden Tabelle sind Aktionsmember-Operator Flags aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-157">The following table lists Action member operator flags.</span></span>



| <span data-ttu-id="d7d3d-158">Wert</span><span class="sxs-lookup"><span data-stu-id="d7d3d-158">Value</span></span>                                                                                                                                                                                                        | <span data-ttu-id="d7d3d-159">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d7d3d-159">Meaning</span></span>                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILTERACTION_INVALID"></span><span id="filteraction_invalid"></span><dl> <span data-ttu-id="d7d3d-160"><dt>**filteraction ist \_ ungültig.**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-160"><dt>**FILTERACTION\_INVALID**</dt></span></span> </dl>                           | <span data-ttu-id="d7d3d-161">Gibt eine ungültige Filter Aktion an.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-161">Indicates an invalid filter action.</span></span><br/>                                                                                  |
| <span id="FILTERACTION_AND"></span><span id="filteraction_and"></span><dl> <span data-ttu-id="d7d3d-162"><dt>**filteraction \_ und**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-162"><dt>**FILTERACTION\_AND**</dt></span></span> </dl>                                       | <span data-ttu-id="d7d3d-163">Gibt eine logische **and-** Anweisung an.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-163">Indicates a logical **AND** statement.</span></span><br/>                                                                               |
| <span id="FILTERACTION_OR"></span><span id="filteraction_or"></span><dl> <span data-ttu-id="d7d3d-164"><dt>**filteraction \_ oder**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-164"><dt>**FILTERACTION\_OR**</dt></span></span> </dl>                                          | <span data-ttu-id="d7d3d-165">Gibt eine logische **or** -Anweisung an.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-165">Indicates a logical **OR** statement.</span></span><br/>                                                                                |
| <span id="FILTERACTION_XOR"></span><span id="filteraction_xor"></span><dl> <span data-ttu-id="d7d3d-166"><dt>**filteraction- \_ Xor**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-166"><dt>**FILTERACTION\_XOR**</dt></span></span> </dl>                                       | <span data-ttu-id="d7d3d-167">Gibt eine logische exklusive **or** -Anweisung (XOR) an.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-167">Indicates a logical exclusive **OR** (XOR) statement.</span></span><br/>                                                                |
| <span id="FILTERACTION_NOT"></span><span id="filteraction_not"></span><dl> <span data-ttu-id="d7d3d-168"><dt>**filteraction \_ nicht**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-168"><dt>**FILTERACTION\_NOT**</dt></span></span> </dl>                                       | <span data-ttu-id="d7d3d-169">Gibt eine logische **Not** -Anweisung an.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-169">Indicates a logical **NOT** statement.</span></span><br/>                                                                               |
| <span id="FILTERACTION_EQUALNC"></span><span id="filteraction_equalnc"></span><dl> <span data-ttu-id="d7d3d-170"><dt>**filteraction \_ equalnc**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-170"><dt>**FILTERACTION\_EQUALNC**</dt></span></span> </dl>                           | <span data-ttu-id="d7d3d-171">Filter Aktion ist gleich und Groß-/Kleinschreibung nicht beachtet</span><span class="sxs-lookup"><span data-stu-id="d7d3d-171">Filter action is equal and case insensitive.</span></span><br/>                                                                         |
| <span id="FILTERACTION_EQUAL"></span><span id="filteraction_equal"></span><dl> <span data-ttu-id="d7d3d-172"><dt>**filteraction \_ gleich**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-172"><dt>**FILTERACTION\_EQUAL**</dt></span></span> </dl>                                 | <span data-ttu-id="d7d3d-173">Filter Aktion ist gleich und Groß-/Kleinschreibung beachtet.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-173">Filter action is equal and case sensitive.</span></span><br/>                                                                           |
| <span id="FILTERACTION_NOTEQUALNC"></span><span id="filteraction_notequalnc"></span><dl> <span data-ttu-id="d7d3d-174"><dt>**filteraction \_ notequalnc**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-174"><dt>**FILTERACTION\_NOTEQUALNC**</dt></span></span> </dl>                  | <span data-ttu-id="d7d3d-175">Die logische NOT-Anweisung ist gleich und unterscheidet **nicht** .</span><span class="sxs-lookup"><span data-stu-id="d7d3d-175">Logical **NOT** statement is equal and case insensitive.</span></span><br/>                                                             |
| <span id="FILTERACTION_NOTEQUAL"></span><span id="filteraction_notequal"></span><dl> <span data-ttu-id="d7d3d-176"><dt>**filteraction- \_ NotEqual**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-176"><dt>**FILTERACTION\_NOTEQUAL**</dt></span></span> </dl>                        | <span data-ttu-id="d7d3d-177">Die logische **Not** -Anweisung ist gleich und berücksichtigt die Groß-/Kleinschreibung</span><span class="sxs-lookup"><span data-stu-id="d7d3d-177">Logical **NOT** statement is equal and is case sensitive.</span></span><br/>                                                            |
| <span id="FILTERACTION_GREATERNC"></span><span id="filteraction_greaternc"></span><dl> <span data-ttu-id="d7d3d-178"><dt>**filteraction \_ greaternc**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-178"><dt>**FILTERACTION\_GREATERNC**</dt></span></span> </dl>                     | <span data-ttu-id="d7d3d-179">Die Filter Aktion ist größer als (>) und Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-179">Filter action is greater than (>) and case insensitive.</span></span><br/>                                                           |
| <span id="FILTERACTION_GREATER"></span><span id="filteraction_greater"></span><dl> <span data-ttu-id="d7d3d-180"><dt>**filteraction \_ größer**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-180"><dt>**FILTERACTION\_GREATER**</dt></span></span> </dl>                           | <span data-ttu-id="d7d3d-181">Die Filter Aktion ist größer als (>) und Groß-/Kleinschreibung beachten.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-181">Filter action is greater than (>) and case sensitive.</span></span><br/>                                                             |
| <span id="FILTERACTION_LESSNC"></span><span id="filteraction_lessnc"></span><dl> <span data-ttu-id="d7d3d-182"><dt>**filteraction \_ lessnc**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-182"><dt>**FILTERACTION\_LESSNC**</dt></span></span> </dl>                              | <span data-ttu-id="d7d3d-183">Die Filter Aktion ist kleiner als (<) und Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-183">Filter action is less than (<) and case insensitive.</span></span><br/>                                                              |
| <span id="FILTERACTION_LESS"></span><span id="filteraction_less"></span><dl> <span data-ttu-id="d7d3d-184"><dt>**weniger filteraction \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-184"><dt>**FILTERACTION\_LESS**</dt></span></span> </dl>                                    | <span data-ttu-id="d7d3d-185">Filter Aktion ist kleiner als (<) und Unterscheidung nach Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-185">Filter action is less than (<) and case sensitive.</span></span><br/>                                                                |
| <span id="FILTERACTION_GREATEREQUALNC"></span><span id="filteraction_greaterequalnc"></span><dl> <span data-ttu-id="d7d3d-186"><dt>**filteraction \_ greaterequalnc**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-186"><dt>**FILTERACTION\_GREATEREQUALNC**</dt></span></span> </dl>      | <span data-ttu-id="d7d3d-187">Die Filter Aktion ist größer als oder gleich (>=) und Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-187">Filter action is greater than or equal to (>=) and case insensitive.</span></span><br/>                                              |
| <span id="FILTERACTION_GREATEREQUAL"></span><span id="filteraction_greaterequal"></span><dl> <span data-ttu-id="d7d3d-188"><dt>**filteraction \_ greaterequal**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-188"><dt>**FILTERACTION\_GREATEREQUAL**</dt></span></span> </dl>            | <span data-ttu-id="d7d3d-189">Die Filter Aktion ist größer als oder gleich (>=) und Unterscheidung nach Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-189">Filter action is greater than or equal to (>=) and case sensitive.</span></span><br/>                                                |
| <span id="FILTERACTION_LESSEQUALNC"></span><span id="filteraction_lessequalnc"></span><dl> <span data-ttu-id="d7d3d-190"><dt>**filteraction \_ lessequalnc**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-190"><dt>**FILTERACTION\_LESSEQUALNC**</dt></span></span> </dl>               | <span data-ttu-id="d7d3d-191">Die Filter Aktion ist kleiner oder gleich (<=) und Groß-/Kleinschreibung nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-191">Filter action is less than or equal to (<=) and case insensitive.</span></span><br/>                                                 |
| <span id="FILTERACTION_LESSEQUAL"></span><span id="filteraction_lessequal"></span><dl> <span data-ttu-id="d7d3d-192"><dt>**filteraction- \_ lessequenz**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-192"><dt>**FILTERACTION\_LESSEQUAL**</dt></span></span> </dl>                     | <span data-ttu-id="d7d3d-193">Die Filter Aktion ist kleiner als oder gleich (<=) und beachtet die Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-193">Filter action is less than or equal to (<=) and is case sensitive.</span></span><br/>                                                |
| <span id="FILTERACTION_PLUS"></span><span id="filteraction_plus"></span><dl> <span data-ttu-id="d7d3d-194"><dt>**filteraction \_ Plus**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-194"><dt>**FILTERACTION\_PLUS**</dt></span></span> </dl>                                    | <span data-ttu-id="d7d3d-195">Operator hinzufügen (+).</span><span class="sxs-lookup"><span data-stu-id="d7d3d-195">Add operator (+).</span></span><br/>                                                                                                    |
| <span id="FILTERACTION_MINUS"></span><span id="filteraction_minus"></span><dl> <span data-ttu-id="d7d3d-196"><dt>**filteraction \_ minus**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-196"><dt>**FILTERACTION\_MINUS**</dt></span></span> </dl>                                 | <span data-ttu-id="d7d3d-197">Subtract-Operator (-).</span><span class="sxs-lookup"><span data-stu-id="d7d3d-197">Subtract operator (-).</span></span><br/>                                                                                               |
| <span id="FILTERACTION_AREBITSON"></span><span id="filteraction_arebitson"></span><dl> <span data-ttu-id="d7d3d-198"><dt>**filteraction \_ arebitson**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-198"><dt>**FILTERACTION\_AREBITSON**</dt></span></span> </dl>                     | <span data-ttu-id="d7d3d-199">Gibt eine bitweise-Operation an.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-199">Indicates a bitwise operation.</span></span><br/>                                                                                       |
| <span id="FILTERACTION_AREBITSOFF"></span><span id="filteraction_arebitsoff"></span><dl> <span data-ttu-id="d7d3d-200"><dt>**filteraction \_ arebitsoff**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-200"><dt>**FILTERACTION\_AREBITSOFF**</dt></span></span> </dl>                  | <span data-ttu-id="d7d3d-201">Gibt eine nicht bitweise-Operation an.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-201">Indicates a non-bitwise operation.</span></span><br/>                                                                                   |
| <span id="FILTERACTION_PROTOCOLSEXIST"></span><span id="filteraction_protocolsexist"></span><dl> <span data-ttu-id="d7d3d-202"><dt>**filteraction \_ protocolsexistisch**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-202"><dt>**FILTERACTION\_PROTOCOLSEXIST**</dt></span></span> </dl>      | <span data-ttu-id="d7d3d-203">Gibt an, dass die ausgewählten Protokolle vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-203">Indicates that the selected protocols exist.</span></span><br/>                                                                         |
| <span id="FILTERACTION_PROTOCOLEXIST"></span><span id="filteraction_protocolexist"></span><dl> <span data-ttu-id="d7d3d-204"><dt>**filteraction \_ protocolexist**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-204"><dt>**FILTERACTION\_PROTOCOLEXIST**</dt></span></span> </dl>         | <span data-ttu-id="d7d3d-205">Gibt an, dass das ausgewählte Protokoll vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-205">Indicates that the selected protocol exists.</span></span><br/>                                                                         |
| <span id="FILTERACTION_ARRAYEQUAL"></span><span id="filteraction_arrayequal"></span><dl> <span data-ttu-id="d7d3d-206"><dt>**filteraction \_ arrayequal**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-206"><dt>**FILTERACTION\_ARRAYEQUAL**</dt></span></span> </dl>                  | <span data-ttu-id="d7d3d-207">Gibt an, dass der Array Inhalt gleich ist.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-207">Indicates that array contents are equal.</span></span> <span data-ttu-id="d7d3d-208">Das Flag muss mit einer **filteraction- \_ Array** Struktur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-208">The flag must be used with a **FILTERACTION\_ARRAY** structure.</span></span><br/>             |
| <span id="FILTERACTION_DEREFPROPERTY"></span><span id="filteraction_derefproperty"></span><dl> <span data-ttu-id="d7d3d-209"><dt>**filteraction- \_ derefproperty**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-209"><dt>**FILTERACTION\_DEREFPROPERTY**</dt></span></span> </dl>         | <span data-ttu-id="d7d3d-210">Beschreibt eine Muster Übereinstimmung mit einem Offset (in Bytes) aus dem Protokoll.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-210">Describes a pattern match at an offset (in bytes), from the protocol.</span></span><br/>                                                |
| <span id="FILTERACTION_OID_CONTAINS"></span><span id="filteraction_oid_contains"></span><dl> <span data-ttu-id="d7d3d-211"><dt>**filteraction- \_ OID \_ enthält**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-211"><dt>**FILTERACTION\_OID\_CONTAINS**</dt></span></span> </dl>           | <span data-ttu-id="d7d3d-212">Wertet eine Teil Zeichenfolge in einem Objekt Bezeichner aus.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-212">Evaluates a substring within an object identifier.</span></span> <span data-ttu-id="d7d3d-213">Die Aktion muss mit der " **filteraction \_ OID** "-Struktur verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-213">The action must be used with the **FILTERACTION\_OID** structure.</span></span><br/> |
| <span id="FILTERACTION_OID_BEGINS_WITH"></span><span id="filteraction_oid_begins_with"></span><dl> <span data-ttu-id="d7d3d-214"><dt>**filteraction \_ OID \_ beginnt \_ mit**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-214"><dt>**FILTERACTION\_OID\_BEGINS\_WITH**</dt></span></span> </dl> | <span data-ttu-id="d7d3d-215">Wertet eine Teil Zeichenfolge aus, die einen Objekt Bezeichner startet.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-215">Evaluates a substring that begins an object identifier.</span></span> <span data-ttu-id="d7d3d-216">Das Flag muss mit der **filteraction- \_ OID** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-216">The flag must be used with **FILTERACTION\_OID**.</span></span><br/>            |
| <span id="FILTERACTION_OID_ENDS_WITH"></span><span id="filteraction_oid_ends_with"></span><dl> <span data-ttu-id="d7d3d-217"><dt>**filteraction- \_ OID \_ endet \_ mit**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-217"><dt>**FILTERACTION\_OID\_ENDS\_WITH**</dt></span></span> </dl>       | <span data-ttu-id="d7d3d-218">Wertet eine Teil Zeichenfolge aus, die einen Objekt Bezeichner beendet.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-218">Evaluates a substring that ends an object identifier.</span></span> <span data-ttu-id="d7d3d-219">Das Flag muss mit der **filteraction- \_ OID** verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-219">The flag must be used with **FILTERACTION\_OID**.</span></span><br/>              |
| <span id="FILTERACTION_ADDR_VINES"></span><span id="filteraction_addr_vines"></span><dl> <span data-ttu-id="d7d3d-220"><dt>**filteraction \_ addr- \_ Reben**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-220"><dt>**FILTERACTION\_ADDR\_VINES**</dt></span></span> </dl>                 | <span data-ttu-id="d7d3d-221">Enthält die Mac-Adresse der Reben.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-221">Contains a Vines MAC address.</span></span><br/>                                                                                        |
| <span id="FILTERACTION_EXPRESSION"></span><span id="filteraction_expression"></span><dl> <span data-ttu-id="d7d3d-222"><dt>**filteraction- \_ Ausdruck**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-222"><dt>**FILTERACTION\_EXPRESSION**</dt></span></span> </dl>                  | <span data-ttu-id="d7d3d-223">Enthält einen Aktions Ausdruck.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-223">Contains an action expression.</span></span><br/>                                                                                       |
| <span id="FILTERACTION_BOOL"></span><span id="filteraction_bool"></span><dl> <span data-ttu-id="d7d3d-224"><dt>**filteraction \_ bool**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-224"><dt>**FILTERACTION\_BOOL**</dt></span></span> </dl>                                    | <span data-ttu-id="d7d3d-225">Enthält einen **booleschen** Datentyp.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-225">Contains a **BOOL** data type.</span></span><br/>                                                                                       |
| <span id="FILTER_DIRECTION_NEXT"></span><span id="filter_direction_next"></span><dl> <span data-ttu-id="d7d3d-226"><dt>**\_Richtung \_ weiter filtern**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-226"><dt>**FILTER\_DIRECTION\_NEXT**</dt></span></span> </dl>                       | <span data-ttu-id="d7d3d-227">Steuert die sequenzielle Richtung (Nächster Frame) innerhalb einer Erfassungs Datei.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-227">Controls sequential direction (Next frame) within a capture file.</span></span><br/>                                                    |
| <span id="FILTER_DIRECTION_PREV"></span><span id="filter_direction_prev"></span><dl> <span data-ttu-id="d7d3d-228"><dt>**Filter \_ Richtung ( \_ Prev)**</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-228"><dt>**FILTER\_DIRECTION\_PREV**</dt></span></span> </dl>                       | <span data-ttu-id="d7d3d-229">Steuert die sequenzielle Richtung (Vorheriger Frame) innerhalb einer Erfassungs Datei.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-229">Controls sequential direction (Previous frame) within a capture file.</span></span><br/>                                                |



 

</dd> <dt>

<span data-ttu-id="d7d3d-230">**hproperty**</span><span class="sxs-lookup"><span data-stu-id="d7d3d-230">**hProperty**</span></span>
</dt> <dd>

<span data-ttu-id="d7d3d-231">Handle für einen Eigenschafts Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-231">Handle to a property key.</span></span>

</dd> <dt>

<span data-ttu-id="d7d3d-232">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d7d3d-232">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="d7d3d-233">Der Wert eines Objekts.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-233">Value of an object.</span></span>

</dd> <dt>

<span data-ttu-id="d7d3d-234">**hprotocol**</span><span class="sxs-lookup"><span data-stu-id="d7d3d-234">**hProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="d7d3d-235">Handle zum Anzeigen des Filter Protokolls.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-235">Handle to display filter protocol.</span></span>

</dd> <dt>

<span data-ttu-id="d7d3d-236">**lpArray**</span><span class="sxs-lookup"><span data-stu-id="d7d3d-236">**lpArray**</span></span>
</dt> <dd>

<span data-ttu-id="d7d3d-237">Zeiger auf ein Array.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-237">Pointer to an array.</span></span>

</dd> <dt>

<span data-ttu-id="d7d3d-238">**lpprotocoltable**</span><span class="sxs-lookup"><span data-stu-id="d7d3d-238">**lpProtocolTable**</span></span>
</dt> <dd>

<span data-ttu-id="d7d3d-239">Ein Zeiger auf eine Protokoll Liste, mit der das vorhanden sein des Protokolls in einem Frame getestet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-239">Pointer to a protocol list designed to test the existence of protocol in a frame.</span></span>

</dd> <dt>

<span data-ttu-id="d7d3d-240">**lpAddress**</span><span class="sxs-lookup"><span data-stu-id="d7d3d-240">**lpAddress**</span></span>
</dt> <dd>

<span data-ttu-id="d7d3d-241">Zeiger auf die kerneltyp Adresse.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-241">Pointer to the kernel type address.</span></span> <span data-ttu-id="d7d3d-242">Beispielsweise Mac oder IP.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-242">For example, MAC or IP.</span></span>

</dd> <dt>

<span data-ttu-id="d7d3d-243">**lplargeint**</span><span class="sxs-lookup"><span data-stu-id="d7d3d-243">**lpLargeInt**</span></span>
</dt> <dd>

<span data-ttu-id="d7d3d-244">Doppeltes **DWORD** , das in einer Windows NT-oder Windows 2000-Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-244">Double **DWORD** used in a Windows NT or Windows 2000 application.</span></span>

</dd> <dt>

<span data-ttu-id="d7d3d-245">**lptime**</span><span class="sxs-lookup"><span data-stu-id="d7d3d-245">**lpTime**</span></span>
</dt> <dd>

<span data-ttu-id="d7d3d-246">Ein Zeiger auf eine **SYSTEMTIME** -Struktur.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-246">A pointer to a **SYSTEMTIME** structure.</span></span>

</dd> <dt>

<span data-ttu-id="d7d3d-247">**lpoid**</span><span class="sxs-lookup"><span data-stu-id="d7d3d-247">**lpOID**</span></span>
</dt> <dd>

<span data-ttu-id="d7d3d-248">Ein Zeiger auf die **Objekt \_ Bezeichner** -Struktur (OID).</span><span class="sxs-lookup"><span data-stu-id="d7d3d-248">A pointer to the **OBJECT\_IDENTIFIER** (OID) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d7d3d-249">**ByteCount**</span><span class="sxs-lookup"><span data-stu-id="d7d3d-249">**ByteCount**</span></span>
</dt> <dd>

<span data-ttu-id="d7d3d-250">Die Zahl in Bytes im Frame.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-250">The number, in bytes, in the frame.</span></span>

</dd> <dt>

<span data-ttu-id="d7d3d-251">**Byte Offset**</span><span class="sxs-lookup"><span data-stu-id="d7d3d-251">**ByteOffset**</span></span>
</dt> <dd>

<span data-ttu-id="d7d3d-252">Der Offset Byte Wert der filterobject-Struktur, die zum Vergleichen von Arrays verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-252">The offset byte value of the FILTEROBJECT structure used to compare arrays.</span></span>

</dd> <dt>

<span data-ttu-id="d7d3d-253">**pNext**</span><span class="sxs-lookup"><span data-stu-id="d7d3d-253">**pNext**</span></span>
</dt> <dd>

<span data-ttu-id="d7d3d-254">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="d7d3d-254">Reserved.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7d3d-255">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7d3d-255">Requirements</span></span>



| <span data-ttu-id="d7d3d-256">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7d3d-256">Requirement</span></span> | <span data-ttu-id="d7d3d-257">Wert</span><span class="sxs-lookup"><span data-stu-id="d7d3d-257">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d7d3d-258">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7d3d-258">Minimum supported client</span></span><br/> | <span data-ttu-id="d7d3d-259">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7d3d-259">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d7d3d-260">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7d3d-260">Minimum supported server</span></span><br/> | <span data-ttu-id="d7d3d-261">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7d3d-261">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d7d3d-262">Header</span><span class="sxs-lookup"><span data-stu-id="d7d3d-262">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7d3d-263"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7d3d-263"><dt>Netmon.h</dt></span></span> </dl> |



 

 




