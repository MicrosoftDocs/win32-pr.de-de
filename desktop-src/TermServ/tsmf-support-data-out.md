---
title: TSMF_SUPPORT_DATA_OUT Struktur
description: Enthält Informationen zu Medienformaten. | TSMF_SUPPORT_DATA_OUT Struktur
ms.assetid: 987ede31-ad15-489f-90e5-fb707c6b38a9
ms.tgt_platform: multiple
keywords:
- TSMF_SUPPORT_DATA_OUT Struktur Remotedesktopdienste
- PTSMF_SUPPORT_DATA_OUT Struktur Zeiger Remotedesktopdienste
topic_type:
- apiref
api_name:
- TSMF_SUPPORT_DATA_OUT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9705c4c2c27eaff904e09364b029bd74ebd05d6c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961322"
---
# <a name="tsmf_support_data_out-structure"></a><span data-ttu-id="1259b-106">Tsmf- \_ Unterstützung der \_ Daten \_ out-Struktur</span><span class="sxs-lookup"><span data-stu-id="1259b-106">TSMF\_SUPPORT\_DATA\_OUT structure</span></span>

<span data-ttu-id="1259b-107">Enthält Informationen zu Medienformaten.</span><span class="sxs-lookup"><span data-stu-id="1259b-107">Contains information about media formats.</span></span> <span data-ttu-id="1259b-108">Diese Struktur wird von der [**queryproperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) -Methode während der **\_ \_ \_ \_ Unterstützung** von Abfragen im wrds-Abfrage-MF-Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="1259b-108">This structure is used by the [**QueryProperty**](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty) method during **WRDS\_QUERY\_MF\_FORMAT\_SUPPORT** queries.</span></span>

## <a name="syntax"></a><span data-ttu-id="1259b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1259b-109">Syntax</span></span>


```C++
typedef struct tagTSMF_SUPPORT_DATA_OUT {
  GUID                      guidMfSession;
  UINT32                    numEntries;
  TSMF_SUPPORT_NODEDATA_OUT ...;
} TSMF_SUPPORT_DATA_OUT, *PTSMF_SUPPORT_DATA_OUT;
```



## <a name="members"></a><span data-ttu-id="1259b-110">Member</span><span class="sxs-lookup"><span data-stu-id="1259b-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="1259b-111">**guidmf Session**</span><span class="sxs-lookup"><span data-stu-id="1259b-111">**guidMfSession**</span></span>
</dt> <dd>

<span data-ttu-id="1259b-112">Dies muss mit der **guidmf Session** -Eigenschaft in den entsprechenden [**tsmf- \_ Unterstützungs \_ Daten \_ in**](tsmf-support-data-in.md) Structure übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="1259b-112">This must match the **guidMfSession** property in the corresponding [**TSMF\_SUPPORT\_DATA\_IN**](tsmf-support-data-in.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1259b-113">**numentries**</span><span class="sxs-lookup"><span data-stu-id="1259b-113">**numEntries**</span></span>
</dt> <dd>

<span data-ttu-id="1259b-114">Die Anzahl der Strukturen in den Daten variabler Länge.</span><span class="sxs-lookup"><span data-stu-id="1259b-114">The number of structures in the variable length data.</span></span>

</dd> <dt>

<span data-ttu-id="1259b-115">**...**</span><span class="sxs-lookup"><span data-stu-id="1259b-115">**...**</span></span>
</dt> <dd>

<span data-ttu-id="1259b-116">Eine Variable Anzahl von Strukturen, die Daten im Medienformat enthalten.</span><span class="sxs-lookup"><span data-stu-id="1259b-116">A variable number of structures containing media format data.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1259b-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1259b-117">Requirements</span></span>



| <span data-ttu-id="1259b-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1259b-118">Requirement</span></span> | <span data-ttu-id="1259b-119">Wert</span><span class="sxs-lookup"><span data-stu-id="1259b-119">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="1259b-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1259b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1259b-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1259b-121">None supported</span></span><br/>         |
| <span data-ttu-id="1259b-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1259b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1259b-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1259b-123">Windows Server 2008 R2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1259b-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1259b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1259b-125">**QueryProperty**</span><span class="sxs-lookup"><span data-stu-id="1259b-125">**QueryProperty**</span></span>](/windows/desktop/api/Wtsprotocol/nf-wtsprotocol-iwrdsprotocolconnection-queryproperty)
</dt> <dt>

[<span data-ttu-id="1259b-126">**tsmf \_ unterstützt \_ nodedata \_**</span><span class="sxs-lookup"><span data-stu-id="1259b-126">**TSMF\_SUPPORT\_NODEDATA\_OUT**</span></span>](tsmf-support-nodedata-out.md)
</dt> </dl>

 

 





