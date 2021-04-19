---
description: Die protocolinfo-Struktur beschreibt ein Protokoll.
ms.assetid: 7f936c93-a942-4591-9abc-59872df0964e
title: Protocolinfo-Struktur (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROTOCOLINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: ed1410148a72c57b860fdfdaee447dcca505d99c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373193"
---
# <a name="protocolinfo-structure"></a><span data-ttu-id="615b2-103">Protocolinfo-Struktur</span><span class="sxs-lookup"><span data-stu-id="615b2-103">PROTOCOLINFO structure</span></span>

<span data-ttu-id="615b2-104">Die **protocolinfo** -Struktur beschreibt ein Protokoll.</span><span class="sxs-lookup"><span data-stu-id="615b2-104">The **PROTOCOLINFO** structure describes a protocol.</span></span>

## <a name="syntax"></a><span data-ttu-id="615b2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="615b2-105">Syntax</span></span>


```C++
typedef struct _PROTOCOLINFO {
  DWORD              ProtocolID;
  LPPROPERTYDATABASE PropertyDatabase;
  BYTE               ProtocolName[16];
  BYTE               HelpFile[16];
  BYTE               Comment[128];
} PROTOCOLINFO, *LPPROTOCOLINFO;
```



## <a name="members"></a><span data-ttu-id="615b2-106">Member</span><span class="sxs-lookup"><span data-stu-id="615b2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="615b2-107">**Protokolid**</span><span class="sxs-lookup"><span data-stu-id="615b2-107">**ProtocolID**</span></span>
</dt> <dd>

<span data-ttu-id="615b2-108">Die vom System zugewiesene Protokoll Kennung der angegebenen Lauf Sitzung.</span><span class="sxs-lookup"><span data-stu-id="615b2-108">System-assigned protocol identifier of the specified run session.</span></span>

</dd> <dt>

<span data-ttu-id="615b2-109">**Propertydatabase**</span><span class="sxs-lookup"><span data-stu-id="615b2-109">**PropertyDatabase**</span></span>
</dt> <dd>

<span data-ttu-id="615b2-110">Die Eigenschaften Datenbank des angegebenen Protokolls.</span><span class="sxs-lookup"><span data-stu-id="615b2-110">Property database of the specified protocol.</span></span>

</dd> <dt>

<span data-ttu-id="615b2-111">**ProtocolName**</span><span class="sxs-lookup"><span data-stu-id="615b2-111">**ProtocolName**</span></span>
</dt> <dd>

<span data-ttu-id="615b2-112">Abgekürzte Protokoll Name.</span><span class="sxs-lookup"><span data-stu-id="615b2-112">Abbreviated protocol name.</span></span>

</dd> <dt>

<span data-ttu-id="615b2-113">**HelpFile**</span><span class="sxs-lookup"><span data-stu-id="615b2-113">**HelpFile**</span></span>
</dt> <dd>

<span data-ttu-id="615b2-114">Optionaler Name der Hilfedatei, die dem Protokoll zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="615b2-114">Optional Help file name associated with the protocol.</span></span>

</dd> <dt>

<span data-ttu-id="615b2-115">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="615b2-115">**Comment**</span></span>
</dt> <dd>

<span data-ttu-id="615b2-116">Ein Kommentar, der das Protokoll beschreibt.</span><span class="sxs-lookup"><span data-stu-id="615b2-116">A comment describing the protocol.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="615b2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="615b2-117">Requirements</span></span>



| <span data-ttu-id="615b2-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="615b2-118">Requirement</span></span> | <span data-ttu-id="615b2-119">Wert</span><span class="sxs-lookup"><span data-stu-id="615b2-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="615b2-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="615b2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="615b2-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="615b2-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="615b2-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="615b2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="615b2-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="615b2-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="615b2-124">Header</span><span class="sxs-lookup"><span data-stu-id="615b2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="615b2-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="615b2-125"><dt>Netmon.h</dt></span></span> </dl> |



 

 




