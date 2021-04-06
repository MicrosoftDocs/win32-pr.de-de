---
description: Gibt an, ob Kontext Meldungen an die Fenster Prozedur des besitzenden Fensters gesendet werden sollen.
ms.assetid: 57ecf10a-8a02-4353-b916-9080ebc0b270
title: CONTEXT_ENABLE_TYPE-Enumeration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONTEXT_ENABLE_TYPE
api_type:
- NA
api_location: ''
ms.openlocfilehash: cd741eeff1cc3e2ce055a84dd646c3aa2563f217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758856"
---
# <a name="context_enable_type-enumeration"></a><span data-ttu-id="ce0dc-103">Kontext \_ enable \_ Type-Enumeration</span><span class="sxs-lookup"><span data-stu-id="ce0dc-103">CONTEXT\_ENABLE\_TYPE enumeration</span></span>

<span data-ttu-id="ce0dc-104">Gibt an, ob Kontext Meldungen an die Fenster Prozedur des besitzenden Fensters gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ce0dc-104">Indicates whether context messages should be sent to the owning window's window procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce0dc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce0dc-105">Syntax</span></span>


```C++
typedef enum _CONTEXT_ENABLE_TYPE { 
  CONTEXT_ENABLE   = 1,
  CONTEXT_DISABLE  = 2
} CONTEXT_ENABLE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="ce0dc-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="ce0dc-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ce0dc-107"><span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**Kontext \_ Aktivierung**</span><span class="sxs-lookup"><span data-stu-id="ce0dc-107"><span id="CONTEXT_ENABLE"></span><span id="context_enable"></span>**CONTEXT\_ENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="ce0dc-108">Der Tablet-Kontext sollte aktiviert werden, was dazu führt, dass Kontext Meldungen an die Fenster Prozedur des besitzenden Fensters gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce0dc-108">The tablet context should be enabled, resulting in context messages being sent to the owning window's window procedure.</span></span>

</dd> <dt>

<span data-ttu-id="ce0dc-109"><span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**Kontext \_ Deaktivieren**</span><span class="sxs-lookup"><span data-stu-id="ce0dc-109"><span id="CONTEXT_DISABLE"></span><span id="context_disable"></span>**CONTEXT\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="ce0dc-110">Der Tablet-Kontext sollte deaktiviert werden, wodurch verhindert wird, dass weitere Kontext Nachrichten an die Fenster Prozedur oder Ereignis Senke des besitzenden Fensters gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="ce0dc-110">The tablet context should be disabled, preventing any further context messages from being sent to the owning window's window procedure or event sink.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce0dc-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce0dc-111">Requirements</span></span>



| <span data-ttu-id="ce0dc-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce0dc-112">Requirement</span></span> | <span data-ttu-id="ce0dc-113">Wert</span><span class="sxs-lookup"><span data-stu-id="ce0dc-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="ce0dc-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ce0dc-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ce0dc-115">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ce0dc-115">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ce0dc-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ce0dc-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ce0dc-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ce0dc-117">None supported</span></span><br/>                                     |



## <a name="see-also"></a><span data-ttu-id="ce0dc-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce0dc-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce0dc-119">**ITablet:: kreatecontext-Methode**</span><span class="sxs-lookup"><span data-stu-id="ce0dc-119">**ITablet::CreateContext Method**</span></span>](itablet-createcontext.md)
</dt> </dl>

 

 




