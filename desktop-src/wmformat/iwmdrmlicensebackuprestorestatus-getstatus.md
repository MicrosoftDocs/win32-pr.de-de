---
title: Iwmdrmlicencbackuprestorestatus-Methode (wmdrmsdk. h)
description: Mit der GetStatus-Methode werden detaillierte Statusinformationen zu einer Lizenz Sicherung oder einem Wiederherstellungs Vorgang abgerufen.
ms.assetid: 1a695baf-0971-4dbf-90fa-1b10178a3348
keywords:
- GetStatus-Methode Windows Media-Format
- GetStatus-Methode Windows Media-Format, iwmdrmlicenabbackuprestorestatus-Schnittstelle
- Iwmdrmlicencbackuprestorestatus-Schnittstelle Windows Media-Format, GetStatus-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus.GetStatus
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3373e71bcae9dc1054e97e8b758ac72389b9a712
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367788"
---
# <a name="iwmdrmlicensebackuprestorestatusgetstatus-method"></a><span data-ttu-id="69566-106">Iwmdrmlicencbackuprestorestatus:: GetStatus-Methode</span><span class="sxs-lookup"><span data-stu-id="69566-106">IWMDRMLicenseBackupRestoreStatus::GetStatus method</span></span>

<span data-ttu-id="69566-107">Mit der **GetStatus** -Methode werden detaillierte Statusinformationen zu einer Lizenz Sicherung oder einem Wiederherstellungs Vorgang abgerufen.</span><span class="sxs-lookup"><span data-stu-id="69566-107">The **GetStatus** method retrieves detailed status information about a license backup or restore operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="69566-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="69566-108">Syntax</span></span>


```C++
HRESULT GetStatus(
  [out] WM_BACKUP_RESTORE_STATUS *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="69566-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="69566-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69566-110">*pstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="69566-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="69566-111">Zeiger auf eine [**Status Struktur der WM- \_ Sicherungs \_ Wiederherstellung \_**](wm-backup-restore-status.md) , die die Statusinformationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="69566-111">Pointer to a [**WM\_BACKUP\_RESTORE\_STATUS**](wm-backup-restore-status.md) structure that receives the status information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69566-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69566-112">Return value</span></span>

<span data-ttu-id="69566-113">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="69566-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="69566-114">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="69566-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="69566-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="69566-115">Return code</span></span>                                                                          | <span data-ttu-id="69566-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69566-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="69566-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="69566-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="69566-118">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="69566-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="69566-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69566-119">Remarks</span></span>

<span data-ttu-id="69566-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="69566-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="69566-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69566-121">Requirements</span></span>



| <span data-ttu-id="69566-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69566-122">Requirement</span></span> | <span data-ttu-id="69566-123">Wert</span><span class="sxs-lookup"><span data-stu-id="69566-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69566-124">Header</span><span class="sxs-lookup"><span data-stu-id="69566-124">Header</span></span><br/>  | <dl> <span data-ttu-id="69566-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="69566-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="69566-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="69566-126">Library</span></span><br/> | <dl> <span data-ttu-id="69566-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="69566-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69566-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69566-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69566-129">**Iwmdrmlicentbackuprestorestatus-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="69566-129">**IWMDRMLicenseBackupRestoreStatus Interface**</span></span>](iwmdrmlicensebackuprestorestatus.md)
</dt> </dl>

 

 





