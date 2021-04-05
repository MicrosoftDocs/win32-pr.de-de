---
title: Itssbtaskinfo-Eigenschaften
description: Die itssbtaskinfo-Schnittstelle macht die folgenden Eigenschaften verfügbar.
ms.assetid: 402B8502-DE17-440B-867D-45922582C30E
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c0e4c8fefc2e443778b2ce177e61a314a3e0ef9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718282"
---
# <a name="itssbtaskinfo-properties"></a><span data-ttu-id="4f01f-103">Itssbtaskinfo-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="4f01f-103">ITsSbTaskInfo Properties</span></span>

<span data-ttu-id="4f01f-104">Die [**itssbtaskinfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo) -Schnittstelle macht die folgenden Eigenschaften verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4f01f-104">The [**ITsSbTaskInfo**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo) interface exposes the following properties.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4f01f-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="4f01f-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="4f01f-106">**Context-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="4f01f-106">**Context property**</span></span>](itssbtaskinfo-context.md)
</dt> <dd>

<span data-ttu-id="4f01f-107">Ruft die dem Task zugeordneten Kontext Bytes ab.</span><span class="sxs-lookup"><span data-stu-id="4f01f-107">Retrieves the context bytes associated with the task.</span></span>

</dd> <dt>

[<span data-ttu-id="4f01f-108">**Stichtag (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="4f01f-108">**Deadline property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_deadline)
</dt> <dd>

<span data-ttu-id="4f01f-109">Ruft den Zeitpunkt ab, zu dem die Aufgabe initiiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="4f01f-109">Retrieves the time by which the task must be initiated.</span></span> <span data-ttu-id="4f01f-110">Hiermit werden Patches priorisiert.</span><span class="sxs-lookup"><span data-stu-id="4f01f-110">This is used to prioritize patches.</span></span> <span data-ttu-id="4f01f-111">Der Patch mit dem frühesten Stichtag wird zuerst initiiert.</span><span class="sxs-lookup"><span data-stu-id="4f01f-111">The patch with the earliest deadline will get initiated first.</span></span>

</dd> <dt>

[<span data-ttu-id="4f01f-112">**EndTime (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="4f01f-112">**EndTime property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_endtime)
</dt> <dd>

<span data-ttu-id="4f01f-113">Ruft den letzten Zeitpunkt ab, zu dem der Task-Agent den Task starten kann.</span><span class="sxs-lookup"><span data-stu-id="4f01f-113">Retrieves the latest time the task agent can start the task.</span></span>

</dd> <dt>

[<span data-ttu-id="4f01f-114">**Eigenschaft Bezeichner**</span><span class="sxs-lookup"><span data-stu-id="4f01f-114">**Identifier property**</span></span>](itssbtaskinfo-identifier.md)
</dt> <dd>

<span data-ttu-id="4f01f-115">Ruft eine GUID ab, die vom Task-Agent als eindeutiger Bezeichner verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4f01f-115">Retrieves a GUID that is used as a unique identifier by the task agent.</span></span>

</dd> <dt>

[<span data-ttu-id="4f01f-116">**Bezeichnung (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="4f01f-116">**Label property**</span></span>](itssbtaskinfo-label.md)
</dt> <dd>

<span data-ttu-id="4f01f-117">Ruft die Bezeichnung ab, die den Zweck der Aufgabe beschreibt.</span><span class="sxs-lookup"><span data-stu-id="4f01f-117">Retrieves the label that describes the purpose of the task.</span></span>

</dd> <dt>

[<span data-ttu-id="4f01f-118">**Plugin-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="4f01f-118">**Plugin property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_plugin)
</dt> <dd>

<span data-ttu-id="4f01f-119">Ruft den anzeigen amen des Task-Agents ab.</span><span class="sxs-lookup"><span data-stu-id="4f01f-119">Retrieves the display name of the task agent.</span></span>

</dd> <dt>

[<span data-ttu-id="4f01f-120">**StartTime (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="4f01f-120">**StartTime property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_starttime)
</dt> <dd>

<span data-ttu-id="4f01f-121">Ruft den frühesten Zeitpunkt ab, zu dem der Task-Agent den Task starten kann.</span><span class="sxs-lookup"><span data-stu-id="4f01f-121">Retrieves the earliest time the task agent can start the task.</span></span>

</dd> <dt>

[<span data-ttu-id="4f01f-122">**Status (Eigenschaft)**</span><span class="sxs-lookup"><span data-stu-id="4f01f-122">**Status property**</span></span>](itssbtaskinfo-status.md)
</dt> <dd>

<span data-ttu-id="4f01f-123">Ruft einen RDV-aufgabenstatusenumerationswert ab, der den Zustand der Aufgabe darstellt. [**\_ \_**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status)</span><span class="sxs-lookup"><span data-stu-id="4f01f-123">Retrieves an [**RDV\_TASK\_STATUS**](/windows/desktop/api/SessDirPublicTypes/ne-sessdirpublictypes-rdv_task_status) enumeration value that represents the state of the task.</span></span>

</dd> <dt>

[<span data-ttu-id="4f01f-124">**TargetID-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="4f01f-124">**TargetId property**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskinfo-get_targetid)
</dt> <dd>

<span data-ttu-id="4f01f-125">Ruft den Ziel Bezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="4f01f-125">Retrieves the target identifier.</span></span>

</dd> </dl>

 

 




