---
description: Ein Anforderer sollte nur dann einen bestimmten Anbieter auswählen, wenn er einige Informationen zu den verfügbaren Anbietern enthält.
ms.assetid: 1a3bc938-2754-4fa2-bd7f-e9b3e876bf6c
title: Auswählen von Anbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39435f8f34091ccef51a6cce85b2c596f0c687d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131256"
---
# <a name="selecting-providers"></a><span data-ttu-id="8cfdb-103">Auswählen von Anbietern</span><span class="sxs-lookup"><span data-stu-id="8cfdb-103">Selecting Providers</span></span>

<span data-ttu-id="8cfdb-104">Ein Anforderer sollte nur dann einen bestimmten Anbieter auswählen, wenn er einige Informationen zu den verfügbaren Anbietern enthält.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-104">A requester should select a specific provider only if it has some information about the providers available.</span></span>

<span data-ttu-id="8cfdb-105">Da dies in der Regel nicht der Fall ist, wird empfohlen, dass eine Anforderer die GUID \_ null als Anbieter-ID für [**IVssBackupComponents:: addtosnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)bereitstellt, wodurch das System einen Anbieter nach folgendem Algorithmus auswählen kann:</span><span class="sxs-lookup"><span data-stu-id="8cfdb-105">Because this will not generally be the case, it is recommended that a requester supply GUID\_NULL as a provider ID to [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset), which allows the system to choose a provider according to the following algorithm:</span></span>

1.  <span data-ttu-id="8cfdb-106">Wenn ein Hardware Anbieter verfügbar ist, der das angegebene Volume unterstützt, wird er ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-106">If a hardware provider that supports the given volume is available, it is selected.</span></span>
2.  <span data-ttu-id="8cfdb-107">Wenn kein Hardware Anbieter verfügbar ist, wird ein beliebiger Softwareanbieter ausgewählt, der für das jeweilige Volume spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-107">If no hardware provider is available, then if any software provider specific to the given volume is available, it is selected.</span></span>
3.  <span data-ttu-id="8cfdb-108">Wenn kein Hardware Anbieter und kein Softwareanbieter für die Volumes verfügbar ist, wird der Systemanbieter ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-108">If no hardware provider and no software provider specific to the volumes is available, the system provider is selected.</span></span>

<span data-ttu-id="8cfdb-109">Allerdings kann ein Anforderer mithilfe von [**IVssBackupComponents:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query)Informationen zu verfügbaren Anbietern abrufen.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-109">However, a requester can obtain information about available providers by using [**IVssBackupComponents::Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).</span></span> <span data-ttu-id="8cfdb-110">Mit diesen Informationen und nur dann, wenn die Sicherungs Anwendung ein gutes Verständnis der verschiedenen Anbieter hat, kann ein Anforderer eine gültige Anbieter-ID für [**IVssBackupComponents:: addtosnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset)angeben.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-110">With this information, and only if the backup application has a good understanding of the various providers, a requester can supply a valid provider ID to [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset).</span></span>

<span data-ttu-id="8cfdb-111">Beachten Sie, dass alle Volumes nicht denselben Anbieter aufweisen müssen.</span><span class="sxs-lookup"><span data-stu-id="8cfdb-111">Note that all volumes do not need to have the same provider.</span></span>

 

 



