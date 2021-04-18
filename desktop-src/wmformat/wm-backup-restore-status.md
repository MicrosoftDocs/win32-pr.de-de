---
title: WM_BACKUP_RESTORE_STATUS Struktur (wmdrmsdk. h)
description: Die Status Struktur der WM- \_ Sicherungs \_ Wiederherstellung \_ enthält Informationen zu einem ausstehenden Lizenz Sicherungs-oder Wiederherstellungs Vorgang.
ms.assetid: 74e94bc6-376b-4848-a9f9-11c9cb4005f2
keywords:
- WM_BACKUP_RESTORE_STATUS Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- WM_BACKUP_RESTORE_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476cd4ddab42ec9f8f44ff51b492bd3913824cf7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365730"
---
# <a name="wm_backup_restore_status-structure"></a><span data-ttu-id="ddd72-105">Status Struktur der WM- \_ Sicherungs \_ Wiederherstellung \_</span><span class="sxs-lookup"><span data-stu-id="ddd72-105">WM\_BACKUP\_RESTORE\_STATUS structure</span></span>

<span data-ttu-id="ddd72-106">Die **Status Struktur der WM- \_ Sicherungs \_ Wiederherstellung \_** enthält Informationen zu einem ausstehenden Lizenz Sicherungs-oder Wiederherstellungs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="ddd72-106">The **WM\_BACKUP\_RESTORE\_STATUS** structure holds information about a pending license backup or restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddd72-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddd72-107">Syntax</span></span>


```C++
typedef struct WM_BACKUP_RESTORE_STATUS {
  MSDRM_STATUS eStatus;
  BSTR         bstrError;
} ;
```



## <a name="members"></a><span data-ttu-id="ddd72-108">Member</span><span class="sxs-lookup"><span data-stu-id="ddd72-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ddd72-109">**estatus**</span><span class="sxs-lookup"><span data-stu-id="ddd72-109">**eStatus**</span></span>
</dt> <dd>

<span data-ttu-id="ddd72-110">Member der [**msdrm- \_ statusenumeration**](msdrm-status.md) , die den Status angibt.</span><span class="sxs-lookup"><span data-stu-id="ddd72-110">Member of the [**MSDRM\_STATUS**](msdrm-status.md) enumeration specifying the status.</span></span>

</dd> <dt>

<span data-ttu-id="ddd72-111">**bstrauerror**</span><span class="sxs-lookup"><span data-stu-id="ddd72-111">**bstrError**</span></span>
</dt> <dd>

<span data-ttu-id="ddd72-112">Zeichenfolge, die den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="ddd72-112">String containing the error.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ddd72-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ddd72-113">Remarks</span></span>

<span data-ttu-id="ddd72-114">Diese Struktur wird empfangen, wenn Sie die [**iwmdrmlicencbackuprestorestatus:: GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ddd72-114">This structure is received when you call the [**IWMDRMLicenseBackupRestoreStatus::GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) method.</span></span> <span data-ttu-id="ddd72-115">Sie enthält den Status des ausstehenden Sicherungs-oder Wiederherstellungs Vorgangs zum Zeitpunkt des Aufrufens.</span><span class="sxs-lookup"><span data-stu-id="ddd72-115">It contains the status of the pending backup or restore operation at the time of the call.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddd72-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ddd72-116">Requirements</span></span>



| <span data-ttu-id="ddd72-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ddd72-117">Requirement</span></span> | <span data-ttu-id="ddd72-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ddd72-118">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ddd72-119">Header</span><span class="sxs-lookup"><span data-stu-id="ddd72-119">Header</span></span><br/> | <dl> <span data-ttu-id="ddd72-120"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddd72-120"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddd72-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ddd72-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddd72-122">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="ddd72-122">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





