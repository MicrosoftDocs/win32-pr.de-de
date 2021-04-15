---
description: 'Die Erweiterungs-Snap-in-Erweiterung hat keine Möglichkeit, die Sicherheitsdatenbank direkt abzufragen, um Informationen abzurufen. Stattdessen müssen diese Informationen aus den Sicherheitskonfigurations-Snap-Ins mithilfe von "iscesvsintachmentdata:: GetData" abgefragt werden.'
ms.assetid: 1171beed-5b28-4f31-b33f-533e3c631b0d
title: Daten aus den Konfigurations-Snap-Ins erhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c888cef92a354f73f01e87fca12cee2567dab48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529639"
---
# <a name="getting-data-from-the-configuration-snap-ins"></a><span data-ttu-id="55543-104">Daten aus den Konfigurations-Snap-Ins erhalten</span><span class="sxs-lookup"><span data-stu-id="55543-104">Getting Data from the Configuration Snap-ins</span></span>

<span data-ttu-id="55543-105">Die Erweiterungs-Snap-in-Erweiterung hat keine Möglichkeit, die Sicherheitsdatenbank direkt abzufragen, um Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="55543-105">The attachment snap-in extension has no way to directly query the security database to retrieve information.</span></span> <span data-ttu-id="55543-106">Stattdessen müssen diese Informationen aus den Sicherheitskonfigurations-Snap-Ins mithilfe von " [**iscesvsintachmentdata:: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata)" abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="55543-106">Instead, it must query this information from the Security Configuration snap-ins using [**ISceSvcAttachmentData::GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).</span></span>

<span data-ttu-id="55543-107">Das Anlagen-Snap-in kann alle Daten abrufen, wenn Sie sich selbst initialisieren, oder es kann Informationen abrufen, wenn der Knoten geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="55543-107">The attachment snap-in can retrieve all of the data when it initializes itself, or it can retrieve information when its node is opened.</span></span>

> [!Note]  
> <span data-ttu-id="55543-108">Sie müssen die [**iscesvsintachmentdata:: FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-freebuffer) -Methode verwenden, um den von der Sicherheitskonfigurations-Snap-in-Methode " [**iscesvasetachmentdata:: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata)" zugeordneten Puffer freizugeben.</span><span class="sxs-lookup"><span data-stu-id="55543-108">You must use the [**ISceSvcAttachmentData::FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-freebuffer) method to free the buffer allocated by the Security Configuration snap-in method [**ISceSvcAttachmentData::GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata).</span></span>

 

 

 



