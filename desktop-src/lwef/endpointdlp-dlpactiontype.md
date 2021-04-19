---
description: Gibt den Aktionstyp eines Endpunktvorgangs zur Verhinderung von Datenverlust (Data Loss Prevention, DLP) an.
title: DlpActionType-Enumeration (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpActionType
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 7900e79536cc9ac45037e205962a563bcde8878a
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495774"
---
# <a name="dlpactiontype-enumeration"></a><span data-ttu-id="11221-103">DlpActionType-Enumeration</span><span class="sxs-lookup"><span data-stu-id="11221-103">DlpActionType enumeration</span></span>

<span data-ttu-id="11221-104">Gibt den Aktionstyp eines Endpunktvorgangs zur Verhinderung von Datenverlust (Data Loss Prevention, DLP) an.</span><span class="sxs-lookup"><span data-stu-id="11221-104">Specifies the action type of an endpoint Data Loss Prevention (DLP) operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="11221-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="11221-105">Syntax</span></span>


```C++
typedef enum  
{
    DlpActionTypeCopyToRemovableMedia = 0,
    DlpActionTypeCopyToNetworkShare = 1,
    DlpActionTypeCopyToClipboard = 2,
    DlpActionTypePrint = 3,
    DlpActionTypeScreenClip = 4,
    DlpActionTypeAccessByUnallowedApp = 5,
    DlpActionTypeCloudAppEgress = 6,
    DlpActionTypeAccessByBluetoothApp = 7,
    DlpActionTypeAccessByRDPApp = 8,
    DlpActionTypeCount = 9
} DlpActionType;
```


## <a name="constants"></a><span data-ttu-id="11221-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="11221-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="11221-107">*DlpActionTypeCopyToRemovableMedia*</span><span class="sxs-lookup"><span data-stu-id="11221-107">*DlpActionTypeCopyToRemovableMedia*</span></span>
</dt> <dd>

<span data-ttu-id="11221-108">Ein Kopiervorgang auf Wechselmedien.</span><span class="sxs-lookup"><span data-stu-id="11221-108">A copy operation to removable media.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="11221-109">*DlpActionTypeCopyToNetworkShare*</span><span class="sxs-lookup"><span data-stu-id="11221-109">*DlpActionTypeCopyToNetworkShare*</span></span>
</dt> <dd>

<span data-ttu-id="11221-110">Ein Kopiervorgang in einen freigegebenen Netzwerkordner.</span><span class="sxs-lookup"><span data-stu-id="11221-110">A copy operation to a shared network folder.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="11221-111">*DlpActionTypeCopyToClipboard*</span><span class="sxs-lookup"><span data-stu-id="11221-111">*DlpActionTypeCopyToClipboard*</span></span>
</dt> <dd>

<span data-ttu-id="11221-112">Ein Kopiervorgang in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="11221-112">A copy operation to the clipboard.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="11221-113">*DlpActionTypePrint*</span><span class="sxs-lookup"><span data-stu-id="11221-113">*DlpActionTypePrint*</span></span>
</dt> <dd>

<span data-ttu-id="11221-114">Ein Druckvorgang.</span><span class="sxs-lookup"><span data-stu-id="11221-114">A print operation.</span></span>

</dd> </dl>


<dl> <dt>

<span data-ttu-id="11221-115">*DlpActionTypeScreenClip*</span><span class="sxs-lookup"><span data-stu-id="11221-115">*DlpActionTypeScreenClip*</span></span>
</dt> <dd>

<span data-ttu-id="11221-116">Ein Bildschirmaufnahmevorgang.</span><span class="sxs-lookup"><span data-stu-id="11221-116">A screen capture operation.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="11221-117">*DlpActionTypeAccessByUnallowedApp*</span><span class="sxs-lookup"><span data-stu-id="11221-117">*DlpActionTypeAccessByUnallowedApp*</span></span>
</dt> <dd>

<span data-ttu-id="11221-118">Ein Vorgang, der von einer nicht zulässigen App ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="11221-118">An operation performed by an unallowed app.</span></span>

</dd> </dl>


<dl> <dt>

<span data-ttu-id="11221-119">*DlpActionTypeCloudAppEgress*</span><span class="sxs-lookup"><span data-stu-id="11221-119">*DlpActionTypeCloudAppEgress*</span></span>
</dt> <dd>

<span data-ttu-id="11221-120">Ein Vorgang, der auf einen Cloudstandort ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="11221-120">An operation targeted to a cloud location.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="11221-121">*DlpActionTypeAccessByBluetoothApp*</span><span class="sxs-lookup"><span data-stu-id="11221-121">*DlpActionTypeAccessByBluetoothApp*</span></span>
</dt> <dd>

<span data-ttu-id="11221-122">Ein Vorgang, der den Zugriff über eine Bluetooth-App umfasst.</span><span class="sxs-lookup"><span data-stu-id="11221-122">An operation that includes access by a bluetooth app.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="11221-123">*DlpActionTypeAccessByRDPApp*</span><span class="sxs-lookup"><span data-stu-id="11221-123">*DlpActionTypeAccessByRDPApp*</span></span>
</dt> <dd>

<span data-ttu-id="11221-124">Ein Vorgang, der den Zugriff über einen Remotedesktop umfasst.</span><span class="sxs-lookup"><span data-stu-id="11221-124">An operation that includes access by a remote desktop.</span></span>

</dd> </dl>

<dl> <dt>

<span data-ttu-id="11221-125">*DlpActionTypeCount*</span><span class="sxs-lookup"><span data-stu-id="11221-125">*DlpActionTypeCount*</span></span>
</dt> <dd>

<span data-ttu-id="11221-126">Der Höchstwert der Enumeration.</span><span class="sxs-lookup"><span data-stu-id="11221-126">The maximum value of the enumeration.</span></span>

</dd> </dl>
 

## <a name="remarks"></a><span data-ttu-id="11221-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="11221-127">Remarks</span></span>

<span data-ttu-id="11221-128">Werte aus dieser Enumeration werden von der [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="11221-128">Values from this enumeration are used by the [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="11221-129">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="11221-129">Requirements</span></span>



| <span data-ttu-id="11221-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11221-130">Requirement</span></span>          |    <span data-ttu-id="11221-131">Wert</span><span class="sxs-lookup"><span data-stu-id="11221-131">Value</span></span>                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="11221-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11221-132">Minimum supported client</span></span><br/> | <span data-ttu-id="11221-133">Windows 10, Version 1809 (10.0; Build 17763)</span><span class="sxs-lookup"><span data-stu-id="11221-133">Windows 10, version 1809 (10.0; Build 17763)</span></span>           |

