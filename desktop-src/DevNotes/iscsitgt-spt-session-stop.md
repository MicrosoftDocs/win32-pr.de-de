---
description: Wird mit IOCTL \_ SCSI \_ Miniport ioctl und dem ctlcode \_ iscsitgt \_ SPT \_ Session \_ End (0x101)-Steuerungs Code verwendet, um eine Sitzung zu beenden.
ms.assetid: 74DAA560-A5BA-475C-AA36-7E6F0EA82EFE
title: ISCSITGT_SPT_SESSION_STOP Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCSITGT_SPT_SESSION_STOP
api_type:
- NA
api_location: ''
ms.openlocfilehash: e4501fbe2d1bbf884448d6b6a9476ee4782d3da7
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "103869672"
---
# <a name="iscsitgt_spt_session_stop-structure"></a><span data-ttu-id="6949a-103">Struktur der iscsitgt \_ SPT- \_ Sitzungs \_ Beendigung</span><span class="sxs-lookup"><span data-stu-id="6949a-103">ISCSITGT\_SPT\_SESSION\_STOP structure</span></span>

<span data-ttu-id="6949a-104">\[Die folgende Struktur ist für die Verwendung in Windows Server 2012 R2 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6949a-104">\[The following structure is available for use in Windows Server 2012 R2.</span></span> <span data-ttu-id="6949a-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="6949a-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="6949a-106">Wird mit [**IOCTL \_ SCSI \_ Miniport**](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_miniport) ioctl und dem ctlcode \_ iscsitgt \_ SPT \_ Session \_ End (0x101)-Steuerungs Code verwendet, um eine Sitzung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="6949a-106">Used with the [**IOCTL\_SCSI\_MINIPORT**](/windows-hardware/drivers/ddi/ntddscsi/ni-ntddscsi-ioctl_scsi_miniport) IOCTL and the CTLCODE\_ISCSITGT\_SPT\_SESSION\_END (0x101) control code to stop a session.</span></span>

## <a name="syntax"></a><span data-ttu-id="6949a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6949a-107">Syntax</span></span>


```C++
typedef struct _ISCSITGT_SPT_SESSION_STOP {
  SRB_IO_CONTROL Header;
  SESSION_COOKIE ITNexusHandle;
} ISCSITGT_SPT_SESSION_STOP, *PISCSITGT_SPT_SESSION_STOP;
```



## <a name="members"></a><span data-ttu-id="6949a-108">Member</span><span class="sxs-lookup"><span data-stu-id="6949a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="6949a-109">**Header**</span><span class="sxs-lookup"><span data-stu-id="6949a-109">**Header**</span></span>
</dt> <dd>

<span data-ttu-id="6949a-110">Obligatorischer Header.</span><span class="sxs-lookup"><span data-stu-id="6949a-110">Mandatory header.</span></span>

</dd> <dt>

<span data-ttu-id="6949a-111">**Itnexushandle**</span><span class="sxs-lookup"><span data-stu-id="6949a-111">**ITNexusHandle**</span></span>
</dt> <dd>

<span data-ttu-id="6949a-112">Ein undurchsichtiges handle, das eine Sitzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="6949a-112">An opaque handle representing a session.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6949a-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6949a-113">Requirements</span></span>



| <span data-ttu-id="6949a-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6949a-114">Requirement</span></span> | <span data-ttu-id="6949a-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6949a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="6949a-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6949a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6949a-117">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6949a-117">None supported</span></span><br/>                               |
| <span data-ttu-id="6949a-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6949a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6949a-119">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6949a-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6949a-120">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="6949a-120">End of client support</span></span><br/>    | <span data-ttu-id="6949a-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="6949a-121">None supported</span></span><br/>                               |
| <span data-ttu-id="6949a-122">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="6949a-122">End of server support</span></span><br/>    | <span data-ttu-id="6949a-123">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="6949a-123">Windows Server 2012 R2</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="6949a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6949a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6949a-125">iSCSI-Ziel-Pass-Through</span><span class="sxs-lookup"><span data-stu-id="6949a-125">iSCSI Target Pass-Through</span></span>](/powershell/module/iscsi)
</dt> <dt>

[<span data-ttu-id="6949a-126">**SRB \_ IO- \_ Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="6949a-126">**SRB\_IO\_CONTROL**</span></span>](/windows-hardware/drivers/ddi/ntddscsi/ns-ntddscsi-_srb_io_control)
</dt> </dl>

 

 
