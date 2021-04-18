---
description: Die Erweiterung des Erweiterungs-Snap-Ins muss dem Benutzer die Möglichkeit geben, Konfigurationsinformationen zum Dienst zu ändern.
ms.assetid: fb36fcce-5a69-49cd-8cd3-b0b048f2f566
title: Ändern von Konfigurationsinformationen in der Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6158d76d0f5114bd2d7b483e0af3d00f8f2439
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352482"
---
# <a name="modifying-configuration-information-in-the-user-interface"></a><span data-ttu-id="43636-103">Ändern von Konfigurationsinformationen in der Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="43636-103">Modifying Configuration Information in the User Interface</span></span>

<span data-ttu-id="43636-104">Die Erweiterung des Erweiterungs-Snap-Ins muss dem Benutzer die Möglichkeit geben, Konfigurationsinformationen zum Dienst zu ändern.</span><span class="sxs-lookup"><span data-stu-id="43636-104">An attachment snap-in extension must allow the user to modify configuration information about the service.</span></span> <span data-ttu-id="43636-105">Die geänderten Informationen sollten von der Erweiterungs-Snap-in-Erweiterung gespeichert werden, bis das Sicherheitskonfigurations-Snap-in Methoden der [**iscesvplattachmentpersistinfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) -Schnittstelle aufruft, um die Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="43636-105">The modified information should be stored by the attachment snap-in extension until the Security Configuration snap-in calls methods of the [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) interface to retrieve the information.</span></span>

<span data-ttu-id="43636-106">Um Speicher Verluste zu vermeiden, können Sie von der Snap-in-Erweiterung zugeordnete Arbeitsspeicher freigeben, indem Sie [**iscesvplattachmentpersistinfo:: FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentpersistinfo-freebuffer)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="43636-106">To avoid memory leaks, free memory allocated by the snap-in extension by calling [**ISceSvcAttachmentPersistInfo::FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentpersistinfo-freebuffer).</span></span>

 

 



