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
# <a name="getting-data-from-the-configuration-snap-ins"></a>Daten aus den Konfigurations-Snap-Ins erhalten

Die Erweiterungs-Snap-in-Erweiterung hat keine Möglichkeit, die Sicherheitsdatenbank direkt abzufragen, um Informationen abzurufen. Stattdessen müssen diese Informationen aus den Sicherheitskonfigurations-Snap-Ins mithilfe von " [**iscesvsintachmentdata:: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata)" abgefragt werden.

Das Anlagen-Snap-in kann alle Daten abrufen, wenn Sie sich selbst initialisieren, oder es kann Informationen abrufen, wenn der Knoten geöffnet wird.

> [!Note]  
> Sie müssen die [**iscesvsintachmentdata:: FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-freebuffer) -Methode verwenden, um den von der Sicherheitskonfigurations-Snap-in-Methode " [**iscesvasetachmentdata:: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata)" zugeordneten Puffer freizugeben.

 

 

 



