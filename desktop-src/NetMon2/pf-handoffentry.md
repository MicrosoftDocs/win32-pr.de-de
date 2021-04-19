---
description: Die PF- \_ handoffentry-Struktur definiert ein Protokoll, das Netzwerkmonitor dem Übergabe Satz eines Parsers hinzufügt.
ms.assetid: c26bee6e-7dbf-4994-a0a7-a280cf4838be
title: PF_HANDOFFENTRY Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PF_HANDOFFENTRY
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 5ad431e936265be96831778f9949ae67ef737beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364068"
---
# <a name="pf_handoffentry-structure"></a><span data-ttu-id="5e2c8-103">PF- \_ handoffentry-Struktur</span><span class="sxs-lookup"><span data-stu-id="5e2c8-103">PF\_HANDOFFENTRY structure</span></span>

<span data-ttu-id="5e2c8-104">Die **PF- \_ handoffentry** -Struktur definiert ein Protokoll, das Netzwerkmonitor dem Übergabe Satz eines Parsers hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-104">The **PF\_HANDOFFENTRY** structure defines a protocol that Network Monitor adds to the handoff set of a parser.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e2c8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e2c8-105">Syntax</span></span>


```C++
typedef struct _PF_HANDOFFENTRY {
  char                      szIniFile[MAX_PATH];
  char                      szIniSection[MAX_PATH];
  char                      szProtocol[MAX_PROTOCOL_NAME_LEN];
  DWORD                     dwHandOffValue;
  PF_HANDOFFVALUEFORMATBASE ValueFormatBase;
} PF_HANDOFFENTRY, *PPF_HANDOFFENTRY;
```



## <a name="members"></a><span data-ttu-id="5e2c8-106">Member</span><span class="sxs-lookup"><span data-stu-id="5e2c8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="5e2c8-107">**szinifile**</span><span class="sxs-lookup"><span data-stu-id="5e2c8-107">**szIniFile**</span></span>
</dt> <dd>

<span data-ttu-id="5e2c8-108">Der Name der INI-Datei, die dem Protokoll zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-108">Name of the INI file associated with the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="5e2c8-109">**szinisection**</span><span class="sxs-lookup"><span data-stu-id="5e2c8-109">**szIniSection**</span></span>
</dt> <dd>

<span data-ttu-id="5e2c8-110">Abschnitts Bezeichnung in der INI-Datei.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-110">Section label within the INI file.</span></span>

</dd> <dt>

<span data-ttu-id="5e2c8-111">**szprotocol**</span><span class="sxs-lookup"><span data-stu-id="5e2c8-111">**szProtocol**</span></span>
</dt> <dd>

<span data-ttu-id="5e2c8-112">Der Name des Protokolls.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-112">Name of the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="5e2c8-113">**dwhandoffvalue**</span><span class="sxs-lookup"><span data-stu-id="5e2c8-113">**dwHandOffValue**</span></span>
</dt> <dd>

<span data-ttu-id="5e2c8-114">Der Wert, der dem Protokoll zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-114">Value associated with the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="5e2c8-115">**Valueformatbase**</span><span class="sxs-lookup"><span data-stu-id="5e2c8-115">**ValueFormatBase**</span></span>
</dt> <dd>

<span data-ttu-id="5e2c8-116">Numerische Basis des Protokoll Werts, der in **dwhandoffvalue** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-116">Numeric base of the protocol value that is specified in **dwHandOffValue**.</span></span> <span data-ttu-id="5e2c8-117">Die **valueformatbase** -Funktion muss auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="5e2c8-117">The **ValueFormatBase** function must be set to one of the following:</span></span>



| <span data-ttu-id="5e2c8-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5e2c8-118">Value</span></span>                                                                                                                                                                                                                        | <span data-ttu-id="5e2c8-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="5e2c8-119">Meaning</span></span>                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| <span id="HANDOFF_VALUE_FORMAT_BASE_UNKNOWN"></span><span id="handoff_value_format_base_unknown"></span><dl> <span data-ttu-id="5e2c8-120"><dt>**das Format des Handoff- \_ Werts ist \_ \_ \_ unbekannt.**</dt></span><span class="sxs-lookup"><span data-stu-id="5e2c8-120"><dt>**HANDOFF\_VALUE\_FORMAT\_BASE\_UNKNOWN**</dt></span></span> </dl> | <span data-ttu-id="5e2c8-121">Unbekannte Basis</span><span class="sxs-lookup"><span data-stu-id="5e2c8-121">Unknown base</span></span><br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_DECIMAL"></span><span id="handoff_value_format_base_decimal"></span><dl> <span data-ttu-id="5e2c8-122"><dt>**Grund für das Format des Handoff- \_ Werts \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5e2c8-122"><dt>**HANDOFF\_VALUE\_FORMAT\_BASE\_DECIMAL**</dt></span></span> </dl> | <span data-ttu-id="5e2c8-123">Dezimaltrennzeichen</span><span class="sxs-lookup"><span data-stu-id="5e2c8-123">Decimal base</span></span><br/>     |
| <span id="HANDOFF_VALUE_FORMAT_BASE_HEX"></span><span id="handoff_value_format_base_hex"></span><dl> <span data-ttu-id="5e2c8-124"><dt>**Format für Übergabe \_ Wert \_ Format \_ Basis \_ Hex**</dt></span><span class="sxs-lookup"><span data-stu-id="5e2c8-124"><dt>**HANDOFF\_VALUE\_FORMAT\_BASE\_HEX**</dt></span></span> </dl>             | <span data-ttu-id="5e2c8-125">Hexadezimale Basis</span><span class="sxs-lookup"><span data-stu-id="5e2c8-125">Hexadecimal base</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5e2c8-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e2c8-126">Remarks</span></span>

<span data-ttu-id="5e2c8-127">Ein Array der **PF- \_ handoffentry** -Strukturen wird in der [PF- \_ handoffset](pf-handoffset.md) -Struktur verwendet.</span><span class="sxs-lookup"><span data-stu-id="5e2c8-127">An array of the **PF\_HANDOFFENTRY** structures is used in the [PF\_HANDOFFSET](pf-handoffset.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e2c8-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e2c8-128">Requirements</span></span>



| <span data-ttu-id="5e2c8-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e2c8-129">Requirement</span></span> | <span data-ttu-id="5e2c8-130">Wert</span><span class="sxs-lookup"><span data-stu-id="5e2c8-130">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="5e2c8-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5e2c8-131">Minimum supported client</span></span><br/> | <span data-ttu-id="5e2c8-132">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e2c8-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="5e2c8-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5e2c8-133">Minimum supported server</span></span><br/> | <span data-ttu-id="5e2c8-134">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e2c8-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="5e2c8-135">Header</span><span class="sxs-lookup"><span data-stu-id="5e2c8-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e2c8-136"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e2c8-136"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e2c8-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e2c8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e2c8-138">PF- \_ handoffset</span><span class="sxs-lookup"><span data-stu-id="5e2c8-138">PF\_HANDOFFSET</span></span>](pf-handoffset.md)
</dt> </dl>

 

 




