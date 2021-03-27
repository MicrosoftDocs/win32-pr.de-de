---
description: Die hwconfig- \_ NIC-Klasse ist die Ereignistyp Klasse für Konfigurations Ereignisse der Netzwerkschnittstellenkarte. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: e544a27b-17f8-402c-9c92-578cf2a38ca8
title: HWConfig_NIC-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HWConfig_NIC
- HWConfig_NIC.NICName
api_type:
- NA
api_location: ''
ms.openlocfilehash: df3897c67ed65eeec5ace49dac1088ca35223a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050366"
---
# <a name="hwconfig_nic-class"></a><span data-ttu-id="c5a52-104">Hwconfig- \_ NIC-Klasse</span><span class="sxs-lookup"><span data-stu-id="c5a52-104">HWConfig\_NIC class</span></span>

<span data-ttu-id="c5a52-105">Die **hwconfig- \_ NIC** -Klasse ist die Ereignistyp Klasse für Konfigurations Ereignisse der Netzwerkschnittstellenkarte.</span><span class="sxs-lookup"><span data-stu-id="c5a52-105">The **HWConfig\_NIC** class is the event type class for network interface card configuration events.</span></span>

<span data-ttu-id="c5a52-106">Die folgende Syntax wird durch den MOF-Code vereinfacht.</span><span class="sxs-lookup"><span data-stu-id="c5a52-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5a52-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5a52-107">Syntax</span></span>

``` syntax
[EventType(13), EventTypeName("NIC")]
class HWConfig_NIC : HWConfig
{
  string NICName;
};
```

## <a name="members"></a><span data-ttu-id="c5a52-108">Member</span><span class="sxs-lookup"><span data-stu-id="c5a52-108">Members</span></span>

<span data-ttu-id="c5a52-109">Die **hwconfig- \_ NIC** -Klasse verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c5a52-109">The **HWConfig\_NIC** class has these types of members:</span></span>

-   [<span data-ttu-id="c5a52-110">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c5a52-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c5a52-111">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c5a52-111">Properties</span></span>

<span data-ttu-id="c5a52-112">Die **hwconfig- \_ NIC** -Klasse verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c5a52-112">The **HWConfig\_NIC** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c5a52-113">NICNAME</span><span class="sxs-lookup"><span data-stu-id="c5a52-113">NICName</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c5a52-114">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c5a52-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c5a52-115">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c5a52-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c5a52-116">Qualifizierer: wmidataid (1), stringbeendigung ("nullterminiert"), Format ("w")</span><span class="sxs-lookup"><span data-stu-id="c5a52-116">Qualifiers: WmiDataId(1), StringTermination("NullTerminated"), Format("w")</span></span>
</dt> </dl>

<span data-ttu-id="c5a52-117">Der Name der Netzwerkschnittstellenkarte.</span><span class="sxs-lookup"><span data-stu-id="c5a52-117">Name of the network interface card.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c5a52-118">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c5a52-118">Requirements</span></span>



| <span data-ttu-id="c5a52-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c5a52-119">Requirement</span></span> | <span data-ttu-id="c5a52-120">Wert</span><span class="sxs-lookup"><span data-stu-id="c5a52-120">Value</span></span> |
|-------------------------------------|---------------------------------------------|
| <span data-ttu-id="c5a52-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c5a52-121">Minimum supported client</span></span><br/> | <span data-ttu-id="c5a52-122">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c5a52-122">Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="c5a52-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c5a52-123">Minimum supported server</span></span><br/> | <span data-ttu-id="c5a52-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c5a52-124">None supported</span></span><br/>                   |



## <a name="see-also"></a><span data-ttu-id="c5a52-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c5a52-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5a52-126">**Hwconfig**</span><span class="sxs-lookup"><span data-stu-id="c5a52-126">**HWConfig**</span></span>](hwconfig.md)
</dt> </dl>

 

 




