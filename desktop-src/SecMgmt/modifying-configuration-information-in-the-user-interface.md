---
description: Eine Anfüge-Snap-In-Erweiterung muss es dem Benutzer ermöglichen, Konfigurationsinformationen zum Dienst zu ändern.
ms.assetid: fb36fcce-5a69-49cd-8cd3-b0b048f2f566
title: Ändern von Konfigurationsinformationen im Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 414e2ab1475ec1c3241d60b96d182a522c299a9f5cf6134f50339c2088c99d9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119005118"
---
# <a name="modifying-configuration-information-in-the-user-interface"></a>Ändern von Konfigurationsinformationen im Benutzeroberfläche

Eine Anfüge-Snap-In-Erweiterung muss es dem Benutzer ermöglichen, Konfigurationsinformationen zum Dienst zu ändern. Die geänderten Informationen sollten von der Erweiterung des Anfüge-Snap-Ins gespeichert werden, bis das Sicherheitskonfigurations-Snap-In Methoden der [**ISceSvcAttachmentPersistInfo-Schnittstelle**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) aufruft, um die Informationen abzurufen.

Um Speicherverluste zu vermeiden, können Sie den von der Snap-In-Erweiterung belegten Arbeitsspeicher freigeben, indem [**Sie ISceSvcAttachmentPersistInfo::FreeBuffer**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentpersistinfo-freebuffer)aufrufen.

 

 



