---
description: Die Snap-In-Erweiterung muss den Benutzern die aktuellen Konfigurations- und Analyseinformationen anzeigen.
ms.assetid: 503bc283-c1cd-4258-a27e-4046553882fa
title: Anzeigen von Konfigurations- und Analyseinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d33971f413058279aa840db4a61e529eb25ee7f317145a66bcb4474142a35c76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894783"
---
# <a name="displaying-configuration-and-analysis-information"></a>Anzeigen von Konfigurations- und Analyseinformationen

Die Snap-In-Erweiterung muss den Benutzern die aktuellen Konfigurations- und Analyseinformationen anzeigen.

Um Informationen anzuzeigen, muss der Erweiterungsknoten des Snap-Ins für Anlagen die Sicherheitskonfigurations-Snap-Ins mithilfe des Knotens Dienste erweitern. Der Knoten Dienste ist das MMC-Snap-In, das auf dem System installierte Dienste verwaltet.

Die Knotentypen, die erweitert werden können, lauten wie folgt:

-   Configuration Services NodeType={24a7f717-1f0c-11d1-affb-00c04fb984f9}
-   Inspection Services NodeType={678050c7-1ff8-11d1-affb-00c04fb984f9}

Wenn der Knoten Dienste erweitert wird, benachrichtigt die MMC alle registrierten Snap-In-Erweiterungen. Jedes Anlagen-Snap-In sollte sich selbst unter dem Knoten Dienste einfügen und die folgenden Aufgaben ausführen:

-   Rufen **Sie QueryInterface auf,** um einen Zeiger auf die [**ISceSvcAttachmentData-Schnittstelle**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) zu erhalten, die von den Sicherheitskonfigurations-Snap-Ins verfügbar gemacht wird.
-   Rufen [**Sie ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) auf, um die Sicherheitskonfigurations-Snap-Ins darüber zu informieren, dass die Snap-In-Erweiterung geladen wird, und um einen Kontext für die Kommunikation zu erstellen.
-   Rufen [**Sie ISceSvcAttachmentData::GetData auf,**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata) um Konfigurationsinformationen aus der Datenbank abzurufen. Dieser Schritt kann entweder ausgeführt werden, wenn die Snap-In-Erweiterung sich selbst initialisiert oder wenn der Benutzer seinen Knoten öffnet.

Weitere Informationen finden Sie unter [Adding an Attachment Snap-in Extension Node](adding-an-attachment-snap-in-extension-node.md).

 

 



