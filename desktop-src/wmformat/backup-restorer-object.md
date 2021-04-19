---
title: Backup Restorer-Objekt
description: Backup Restorer-Objekt
ms.assetid: 83ce28c0-fd17-46ff-94c0-d28124a0e56a
keywords:
- Windows Media-Format-SDK, Backup Restorer Objects
- Advanced Systems Format (ASF), Backup Restorer Objects
- ASF (Advanced Systems Format), Backup Restorer Objects
- Objekte, Backup Restorer Objects
- Backup Restorer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d08e8bec9bb7bbc2a45fbf632e69d230a2536633
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106338043"
---
# <a name="backup-restorer-object"></a><span data-ttu-id="11e12-108">Backup Restorer-Objekt</span><span class="sxs-lookup"><span data-stu-id="11e12-108">Backup Restorer Object</span></span>

<span data-ttu-id="11e12-109">Der Backup Restorer bietet Schnittstellen zum Sichern von Lizenzen, in der Regel auf Wechselmedien und zum anschließenden Wiederherstellen dieser Lizenzen auf einem neuen Computer.</span><span class="sxs-lookup"><span data-stu-id="11e12-109">The backup restorer provides interfaces to handle backing up licenses, typically onto removable media, and then restoring those licenses onto a new computer.</span></span>

<span data-ttu-id="11e12-110">Das Backup Restorer-Objekt wird von der [**wmkreatebackuprestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) -Funktion erstellt, mit der ein Zeiger auf eine [**iwmlicensebackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) -Schnittstelle festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="11e12-110">The backup restorer object is created by the [**WMCreateBackupRestorer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatebackuprestorer) function, which sets a pointer to an [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) interface.</span></span> <span data-ttu-id="11e12-111">Die anderen Schnittstellen des Backup Restorer-Objekts können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="11e12-111">The other interfaces of the backup restorer object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="11e12-112">Die folgenden Schnittstellen werden vom Backup Restorer-Objekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="11e12-112">The following interfaces are supported by the backup restorer object.</span></span>



| <span data-ttu-id="11e12-113">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="11e12-113">Interface</span></span>                                              | <span data-ttu-id="11e12-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11e12-114">Description</span></span>                                                                                                                                               |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11e12-115">**Iwmbackuprestore-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="11e12-115">**IWMBackupRestoreProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbackuprestoreprops) | <span data-ttu-id="11e12-116">Legt die Eigenschaften fest, die von den Schnittstellen [**iwmlicensebackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) und [**iwmlicenserestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) benötigt werden, oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="11e12-116">Sets and retrieves properties required by the [**IWMLicenseBackup**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup) and [**IWMLicenseRestore**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore) interfaces.</span></span> |
| [<span data-ttu-id="11e12-117">**Iwmlicenlbackup**</span><span class="sxs-lookup"><span data-stu-id="11e12-117">**IWMLicenseBackup**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicensebackup)           | <span data-ttu-id="11e12-118">Sichert Lizenzen, in der Regel, damit Sie auf einem anderen Computer wieder hergestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="11e12-118">Backs up licenses, typically so that they can be restored onto another computer.</span></span>                                                                          |
| [<span data-ttu-id="11e12-119">**Iwmlicenserestore**</span><span class="sxs-lookup"><span data-stu-id="11e12-119">**IWMLicenseRestore**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlicenserestore)         | <span data-ttu-id="11e12-120">Stellt Lizenzen wieder her.</span><span class="sxs-lookup"><span data-stu-id="11e12-120">Restores licenses.</span></span>                                                                                                                                        |



 

<span data-ttu-id="11e12-121">Die folgende Rückruf Schnittstelle muss von der Anwendung implementiert werden, damit das Backup Restorer-Objekt verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="11e12-121">The following callback interface must be implemented by the application in order to use the backup restorer object.</span></span>



| <span data-ttu-id="11e12-122">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="11e12-122">Interface</span></span>                                      | <span data-ttu-id="11e12-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11e12-123">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="11e12-124">**Iwmstatus Callback**</span><span class="sxs-lookup"><span data-stu-id="11e12-124">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="11e12-125">Empfängt Statusmeldungen von Prozessen, die in einem separaten Thread ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="11e12-125">Receives status messages from processes that execute in a separate thread.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="11e12-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="11e12-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11e12-127">**Sichern und Wiederherstellen von Lizenzen**</span><span class="sxs-lookup"><span data-stu-id="11e12-127">**Backing Up and Restoring Licenses**</span></span>](backing-up-and-restoring-licenses.md)
</dt> <dt>

[<span data-ttu-id="11e12-128">**Objekte**</span><span class="sxs-lookup"><span data-stu-id="11e12-128">**Objects**</span></span>](objects.md)
</dt> </dl>

 

 




