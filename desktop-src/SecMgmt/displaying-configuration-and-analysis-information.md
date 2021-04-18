---
description: In Ihrer Snap-in-Erweiterung müssen die aktuellen Konfigurations-und Analyse Informationen für die Benutzer angezeigt werden.
ms.assetid: 503bc283-c1cd-4258-a27e-4046553882fa
title: Anzeigen von Konfigurations-und Analyse Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc2f0d598ced5f789d9b417d79df591a71f82ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357927"
---
# <a name="displaying-configuration-and-analysis-information"></a>Anzeigen von Konfigurations-und Analyse Informationen

In Ihrer Snap-in-Erweiterung müssen die aktuellen Konfigurations-und Analyse Informationen für die Benutzer angezeigt werden.

Zum Anzeigen von Informationen muss der Erweiterungs Knoten "Anlagen-Snap-in" die Sicherheitskonfigurations-Snap-Ins mithilfe des Knotens "Dienste" erweitern. Der Knoten Dienste ist das MMC-Snap-in, mit dem die auf dem System installierten Dienste verwaltet werden.

Die Knoten Typen, die erweitert werden können, lauten wie folgt:

-   Konfigurations Dienste NodeType = {24a7f 717-1F-c-11d1-affb-00c04tb984f 9}
-   Inspektionsdienste NodeType = {678050c7-1ff8-11d1-affb-00C04FB984F9}

Wenn der Knoten Dienste erweitert wird, benachrichtigt die MMC alle registrierten Snap-in-Erweiterungen. Jedes Anlage-Snap-in sollte sich selbst unter dem Knoten Dienste einfügen und die folgenden Aufgaben ausführen:

-   Ruft **QueryInterface** auf, um einen Zeiger auf die [**iscesvcalltachmentdata**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) -Schnittstelle abzurufen, die von den Sicherheitskonfigurations-Snap-Ins verfügbar gemacht wird.
-   Wenden Sie [**iscesvcalltachmentdata:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) an, um die Sicherheitskonfigurations-Snap-Ins zu informieren, dass die Snap-in-Erweiterung geladen ist, und um einen Kontext für die Kommunikation zu erstellen.
-   Rufen Sie [**iscesvasetachmentdata:: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata) auf, um Konfigurationsinformationen aus der Datenbank abzurufen. Dieser Schritt kann entweder ausgeführt werden, wenn die Snap-in-Erweiterung selbst initialisiert wird oder wenn der Benutzer den Knoten öffnet.

Weitere Informationen finden Sie unter [Hinzufügen eines Erweiterungs Knotens für einen Anlagen-Snap-in](adding-an-attachment-snap-in-extension-node.md).

 

 



