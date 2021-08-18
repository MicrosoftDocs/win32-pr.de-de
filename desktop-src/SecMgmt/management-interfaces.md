---
description: Listet die Schnittstellen auf, die von der Anlagen-Engine bereitgestellt werden.
ms.assetid: 451587bd-a7ab-446b-b647-be98de251915
title: Sicherheitsverwaltungsschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6adc6cbaa24be46508e2a4f72181c96d4ccb65e589fdad95808c65a57262b73b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894327"
---
# <a name="security-management-interfaces"></a>Sicherheitsverwaltungsschnittstellen

Dieser Abschnitt enthält Referenzseiten für die folgenden Schnittstellengruppen:

-   [Schnittstellen der Anlagen-Engine](#attachment-engine-interfaces)

## <a name="attachment-engine-interfaces"></a>Schnittstellen der Anlagen-Engine



| Schnittstelle                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)               | Ruft Konfigurations- und Analysedaten zu einem angegebenen Sicherheitsdienst aus den Sicherheitskonfigurations-Snap-Ins ab. Die Sicherheitskonfigurations-Snap-Ins machen diese Schnittstelle verfügbar, die die Erweiterungen des Anlagen-Snap-Ins aufrufen, um Konfigurations- oder Analyseinformationen abzufragen.                                                 |
| [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) | Ruft geänderte Konfigurations- oder Analyseinformationen aus einem Anlagen-Snap-In ab. Die Sicherheitskonfigurations-Snap-Ins rufen diese Schnittstelle auf, um alle geänderten Informationen aus der Erweiterung für das Anfüge-Snap-In abzurufen. Das Sicherheitskonfigurations-Snap-In speichert diese Daten dann entsprechend in der Sicherheitsdatenbank. |



 

Weitere Informationen zu den COM-Schnittstellen, die von Snap-In-Erweiterungen implementiert werden müssen, finden Sie in der [Microsoft Management Console-Dokumentation.](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page)

 

 
