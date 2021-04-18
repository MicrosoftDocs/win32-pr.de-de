---
description: 'Während eines Wiederherstellungs Vorgangs kann der Anforderer die IVssBackupComponents:: abtrestorestate-Methode verwenden, um den Typ des laufenden Wiederherstellungs Vorgangs zu definieren.'
ms.assetid: f6bf1979-7604-450f-8988-2a17da6b82d7
title: VSS-Wiederherstellungs Status
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97581d33f5695890ba83e87c6f6155a9e7f92f78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368083"
---
# <a name="vss-restore-state"></a><span data-ttu-id="c0422-103">VSS-Wiederherstellungs Status</span><span class="sxs-lookup"><span data-stu-id="c0422-103">VSS Restore State</span></span>

<span data-ttu-id="c0422-104">Während eines Wiederherstellungs Vorgangs kann der Anforderer die [**IVssBackupComponents:: abtrestorestate**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate) -Methode verwenden, um den Typ des laufenden Wiederherstellungs Vorgangs zu definieren.</span><span class="sxs-lookup"><span data-stu-id="c0422-104">During a restore operation, the requester can use the [**IVssBackupComponents::SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate) method to define the type of restore operation in progress.</span></span> <span data-ttu-id="c0422-105">Bei den meisten Wiederherstellungs Vorgängen muss der Standard Wiederherstellungstyp (VSS \_ rtype nicht definiert) jedoch nicht überschrieben werden \_ .</span><span class="sxs-lookup"><span data-stu-id="c0422-105">However, most restore operations will not need to override the default restore type (VSS\_RTYPE\_UNDEFINED).</span></span> <span data-ttu-id="c0422-106">Writer sollten diesen wiederherungstyp so behandeln, als wäre er VSS \_ rtype \_ by \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="c0422-106">Writers should treat this restore type as if it were VSS\_RTYPE\_BY\_COPY.</span></span> <span data-ttu-id="c0422-107">Weitere Informationen zu den Werten des Wiederherstellungs Typs finden Sie in der Enumeration des [**VSS- \_ Wiederherstellungs \_ Typs**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) .</span><span class="sxs-lookup"><span data-stu-id="c0422-107">For more information about restore type values, see the [**VSS\_RESTORE\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) enumeration.</span></span>

 

 



