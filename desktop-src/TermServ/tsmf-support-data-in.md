---
title: TSMF_SUPPORT_DATA_IN Struktur
description: Enthält Informationen zu Medienformaten. | TSMF_SUPPORT_DATA_IN Struktur
ms.assetid: cd1a8295-22b7-4d75-8325-94da4d7380d0
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_DATA_IN Struktur Remotedesktopdienste
- PTSMF_SUPPORT_DATA_IN Struktur Zeiger Remotedesktopdienste
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_IN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2072363978cb0e70d64a09d855ed2861341e9cf0
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106371855"
---
# <a name="tsmf_support_data_in-structure"></a><span data-ttu-id="c35b6-106">Tsmf- \_ Unterstützungs \_ Daten \_ in der Struktur</span><span class="sxs-lookup"><span data-stu-id="c35b6-106">TSMF\_SUPPORT\_DATA\_IN structure</span></span>

<span data-ttu-id="c35b6-107">Enthält Informationen zu Medienformaten.</span><span class="sxs-lookup"><span data-stu-id="c35b6-107">Contains information about media formats.</span></span> <span data-ttu-id="c35b6-108">Diese Struktur wird von der [**queryproperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) -Methode während der **\_ \_ \_ \_ Unterstützung** von Abfragen im wrds-Abfrage-MF-Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="c35b6-108">This structure is used by the [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) method during **WRDS\_QUERY\_MF\_FORMAT\_SUPPORT** queries.</span></span>

## <a name="syntax"></a><span data-ttu-id="c35b6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c35b6-109">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_DATA_IN {
  GUID                     guidMfSession;
  UINT32                   numEntries;
  TSMF_SUPPORT_NODEDATA_IN ...;
} TSMF_SUPPORT_DATA_IN, *PTSMF_SUPPORT_DATA_IN;
```



## <a name="members"></a><span data-ttu-id="c35b6-110">Member</span><span class="sxs-lookup"><span data-stu-id="c35b6-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="c35b6-111">**guidmf Session**</span><span class="sxs-lookup"><span data-stu-id="c35b6-111">**guidMfSession**</span></span>
</dt> <dd>

<span data-ttu-id="c35b6-112">Die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="c35b6-112">The session.</span></span>

</dd> <dt>

<span data-ttu-id="c35b6-113">**numentries**</span><span class="sxs-lookup"><span data-stu-id="c35b6-113">**numEntries**</span></span>
</dt> <dd>

<span data-ttu-id="c35b6-114">Die Anzahl der Strukturen in den Daten variabler Länge.</span><span class="sxs-lookup"><span data-stu-id="c35b6-114">The number of structures in the variable length data.</span></span>

</dd> <dt>

<span data-ttu-id="c35b6-115">**...**</span><span class="sxs-lookup"><span data-stu-id="c35b6-115">**...**</span></span>
</dt> <dd>

<span data-ttu-id="c35b6-116">Eine Variable Anzahl von Strukturen, die Daten im Medienformat enthalten.</span><span class="sxs-lookup"><span data-stu-id="c35b6-116">A variable number of structures containing media format data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c35b6-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c35b6-117">Requirements</span></span>



| <span data-ttu-id="c35b6-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c35b6-118">Requirement</span></span> | <span data-ttu-id="c35b6-119">Wert</span><span class="sxs-lookup"><span data-stu-id="c35b6-119">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="c35b6-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c35b6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c35b6-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c35b6-121">None supported</span></span><br/>         |
| <span data-ttu-id="c35b6-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c35b6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c35b6-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c35b6-123">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c35b6-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c35b6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c35b6-125">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="c35b6-125">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="c35b6-126">**tsmf \_ unterstützt \_ nodedata \_ in**</span><span class="sxs-lookup"><span data-stu-id="c35b6-126">**TSMF\_SUPPORT\_NODEDATA\_IN**</span></span>](tsmf-support-nodedata-in.md)
</dt> </dl>

 

 





