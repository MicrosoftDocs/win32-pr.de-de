---
description: Jede MIB-Objektdefinition enthält entweder eine Access (SNMPv1)-oder eine Max-Access (SNMPv2C)-Klausel, die die Zugriffsrechte für das Objekt definiert.
ms.assetid: c3b8d65b-c1ca-4131-baf4-1aab54451180
ms.tgt_platform: multiple
title: Access-und Max-Access-Klauseln
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37084a25a48c874866774b990a70e1332e730103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363248"
---
# <a name="access-and-max-access-clauses"></a><span data-ttu-id="428ec-103">Access-und Max-Access-Klauseln</span><span class="sxs-lookup"><span data-stu-id="428ec-103">ACCESS and MAX-ACCESS Clauses</span></span>

<span data-ttu-id="428ec-104">Jede MIB-Objektdefinition enthält entweder eine Access (SNMPv1)-oder eine Max-Access (SNMPv2C)-Klausel, die die Zugriffsrechte für das Objekt definiert.</span><span class="sxs-lookup"><span data-stu-id="428ec-104">Each MIB object definition contains either an ACCESS (SNMPv1) or MAX-ACCESS (SNMPv2C) clause that defines the access rights to the object.</span></span>

> [!Note]  
> <span data-ttu-id="428ec-105">Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="428ec-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="428ec-106">In der folgenden Tabelle ist die Zuordnung der SNMPv1 Access-Klausel aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="428ec-106">The following table lists the mapping of the SNMPv1 ACCESS clause.</span></span>



| <span data-ttu-id="428ec-107">MIB-Zugriffs Klausel</span><span class="sxs-lookup"><span data-stu-id="428ec-107">MIB ACCESS clause</span></span> | <span data-ttu-id="428ec-108">CIM Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="428ec-108">CIM qualifier</span></span>       |
|-------------------|---------------------|
| <span data-ttu-id="428ec-109">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="428ec-109">read-only</span></span>         | <span data-ttu-id="428ec-110">**Lesen**</span><span class="sxs-lookup"><span data-stu-id="428ec-110">**Read**</span></span>            |
| <span data-ttu-id="428ec-111">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="428ec-111">read-write</span></span>        | <span data-ttu-id="428ec-112">**Lesen**, **Schreiben**</span><span class="sxs-lookup"><span data-stu-id="428ec-112">**Read**, **Write**</span></span> |
| <span data-ttu-id="428ec-113">Lesegeschützte</span><span class="sxs-lookup"><span data-stu-id="428ec-113">write-only</span></span>        | <span data-ttu-id="428ec-114">**Schreiben**</span><span class="sxs-lookup"><span data-stu-id="428ec-114">**Write**</span></span>           |
| <span data-ttu-id="428ec-115">nicht zugänglich</span><span class="sxs-lookup"><span data-stu-id="428ec-115">not-accessible</span></span>    | <span data-ttu-id="428ec-116">**Nicht \_ zugänglich**</span><span class="sxs-lookup"><span data-stu-id="428ec-116">**Not\_Accessible**</span></span> |



 

<span data-ttu-id="428ec-117">In der folgenden Tabelle ist die Zuordnung der SNMPv2C Max-Access-Klausel aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="428ec-117">The following table lists the mapping of the SNMPv2C MAX-ACCESS clause.</span></span>



| <span data-ttu-id="428ec-118">MIB-Access-Klausel</span><span class="sxs-lookup"><span data-stu-id="428ec-118">MIB-ACCESS clause</span></span>     | <span data-ttu-id="428ec-119">CIM Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="428ec-119">CIM qualifier</span></span>       |
|-----------------------|---------------------|
| <span data-ttu-id="428ec-120">schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="428ec-120">read-only</span></span>             | <span data-ttu-id="428ec-121">**Lesen**</span><span class="sxs-lookup"><span data-stu-id="428ec-121">**Read**</span></span>            |
| <span data-ttu-id="428ec-122">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="428ec-122">read-write</span></span>            | <span data-ttu-id="428ec-123">**Lesen**, **Schreiben**</span><span class="sxs-lookup"><span data-stu-id="428ec-123">**Read**, **Write**</span></span> |
| <span data-ttu-id="428ec-124">Lesen/Erstellen</span><span class="sxs-lookup"><span data-stu-id="428ec-124">read-create</span></span>           | <span data-ttu-id="428ec-125">**Lesen**</span><span class="sxs-lookup"><span data-stu-id="428ec-125">**Read**</span></span>            |
| <span data-ttu-id="428ec-126">Zugriff für Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="428ec-126">accessible-for-notify</span></span> | <span data-ttu-id="428ec-127">**Nicht \_ zugänglich**</span><span class="sxs-lookup"><span data-stu-id="428ec-127">**Not\_Accessible**</span></span> |
| <span data-ttu-id="428ec-128">nicht zugänglich</span><span class="sxs-lookup"><span data-stu-id="428ec-128">not-accessible</span></span>        | <span data-ttu-id="428ec-129">**Nicht \_ zugänglich**</span><span class="sxs-lookup"><span data-stu-id="428ec-129">**Not\_Accessible**</span></span> |



 

<span data-ttu-id="428ec-130">Wenn ein MIB-Objekt nicht zugreifbar zugeordnet ist und keine Schlüssel gebundene Eigenschaft der Klasse ist, gibt es keine Zuordnung des MIB-Objekts selbst.</span><span class="sxs-lookup"><span data-stu-id="428ec-130">When a MIB object maps to not-accessible and is not a keyed property of the class, there is no mapping of the MIB object itself.</span></span>

 

 



