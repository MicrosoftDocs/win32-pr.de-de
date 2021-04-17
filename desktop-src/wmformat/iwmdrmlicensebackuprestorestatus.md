---
title: Iwmdrmlicentbackuprestorestatus-Schnittstelle
description: Die iwmdrmlicenlbackuprestorestatus-Schnittstelle bietet eine Methode zum Abrufen detaillierter Statusinformationen zu einer Lizenz Sicherung oder eines Wiederherstellungs Vorgangs. Diese Schnittstelle wird mit während der Sicherungs-und Wiederherstellungs Vorgängen generierten Status Ereignissen bereitgestellt.
ms.assetid: fbcd059f-13d9-4edb-8946-b55c9da6dca4
keywords:
- Iwmdrmlicenabbackuprestorestatus-Schnittstelle Windows Media-Format
- Iwmdrmlicenabbackuprestorestatus-Schnittstelle Windows Media-Format, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9db5d95daab78a506a3cc994fb9dd22153d0907
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315993"
---
# <a name="iwmdrmlicensebackuprestorestatus-interface"></a><span data-ttu-id="c4cc3-105">Iwmdrmlicentbackuprestorestatus-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="c4cc3-105">IWMDRMLicenseBackupRestoreStatus interface</span></span>

<span data-ttu-id="c4cc3-106">Die **iwmdrmlicenlbackuprestorestatus** -Schnittstelle bietet eine Methode zum Abrufen detaillierter Statusinformationen zu einer Lizenz Sicherung oder eines Wiederherstellungs Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="c4cc3-106">The **IWMDRMLicenseBackupRestoreStatus** interface provides a method to retrieve detailed status information about a license backup or restore operation.</span></span>

<span data-ttu-id="c4cc3-107">Diese Schnittstelle wird mit während der Sicherungs-und Wiederherstellungs Vorgängen generierten Status Ereignissen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c4cc3-107">This interface is delivered with progress events generated during license backup and restore operations.</span></span> <span data-ttu-id="c4cc3-108">Während der Lizenz Sicherung werden mehrere **mewmdrmlicenlbackupprogress** -Ereignisse generiert, von denen jede über eine zugehörige Instanz dieser Schnittstelle verfügt.</span><span class="sxs-lookup"><span data-stu-id="c4cc3-108">Several **MEWMDRMLicenseBackupProgress** events are generated during license backup, each of which has an accompanying instance of this interface.</span></span> <span data-ttu-id="c4cc3-109">Das gleiche gilt für **mewmdrmlicenserestoreprogress** -Ereignisse, die während der Wiederherstellung der Lizenz generiert werden.</span><span class="sxs-lookup"><span data-stu-id="c4cc3-109">The same is true of **MEWMDRMLicenseRestoreProgress** events, which are generated during license restoration.</span></span>

<span data-ttu-id="c4cc3-110">Wenn Sie einen Zeiger auf eine Instanz der **iwmdrmlicencbackuprestorestatus** -Schnittstelle abrufen möchten, müssen Sie zuerst die **imfmediaevent:: GetValue** -Methode des Progress-Ereignisses aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c4cc3-110">To retrieve a pointer to an instance of the **IWMDRMLicenseBackupRestoreStatus** interface, you must first call the **IMFMediaEvent::GetValue** method of the progress event.</span></span> <span data-ttu-id="c4cc3-111">Der Wert, den Sie aus dem Ereignis abrufen, ist ein Zeiger auf die **IUnknown** -Schnittstelle des Objekts, das die **iwmdrmlicensebackuprestorestatus** -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="c4cc3-111">The value you retrieve from the event is a pointer to the **IUnknown** interface of the object that implements the **IWMDRMLicenseBackupRestoreStatus** interface.</span></span>

## <a name="members"></a><span data-ttu-id="c4cc3-112">Member</span><span class="sxs-lookup"><span data-stu-id="c4cc3-112">Members</span></span>

<span data-ttu-id="c4cc3-113">Die **iwmdrmlicen* backuprestorestatus*\* -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c4cc3-113">The **IWMDRMLicenseBackupRestoreStatus** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c4cc3-114">**Iwmdrmlicentarbackuprestorestatus** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c4cc3-114">**IWMDRMLicenseBackupRestoreStatus** also has these types of members:</span></span>

-   [<span data-ttu-id="c4cc3-115">Methoden</span><span class="sxs-lookup"><span data-stu-id="c4cc3-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c4cc3-116">Methoden</span><span class="sxs-lookup"><span data-stu-id="c4cc3-116">Methods</span></span>

<span data-ttu-id="c4cc3-117">Die **iwmdrmlicentbackuprestorestatus** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="c4cc3-117">The **IWMDRMLicenseBackupRestoreStatus** interface has these methods.</span></span>



| <span data-ttu-id="c4cc3-118">Methode</span><span class="sxs-lookup"><span data-stu-id="c4cc3-118">Method</span></span>                                                          | <span data-ttu-id="c4cc3-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c4cc3-119">Description</span></span>                                                                                   |
|:----------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c4cc3-120">**GetStatus**</span><span class="sxs-lookup"><span data-stu-id="c4cc3-120">**GetStatus**</span></span>](iwmdrmlicensebackuprestorestatus-getstatus.md) | <span data-ttu-id="c4cc3-121">Ruft detaillierte Statusinformationen zu einer Lizenz Sicherung oder einem Wiederherstellungs Vorgang ab.</span><span class="sxs-lookup"><span data-stu-id="c4cc3-121">Retrieves detailed status information about a license backup or restore operation.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="c4cc3-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4cc3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4cc3-123">**Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="c4cc3-123">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

