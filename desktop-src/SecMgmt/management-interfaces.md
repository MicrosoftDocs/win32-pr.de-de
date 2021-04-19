---
description: Listet die von der Anlage-Engine bereitgestellten Schnittstellen auf.
ms.assetid: 451587bd-a7ab-446b-b647-be98de251915
title: Sicherheits Verwaltungs Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b3a205757a3bf324a5308a5f6fbc3d63374b4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373243"
---
# <a name="security-management-interfaces"></a>Sicherheits Verwaltungs Schnittstellen

Dieser Abschnitt enthält Referenzseiten für die folgenden Gruppen von Schnittstellen:

-   [Schnittstellen des Anlagen Moduls](#attachment-engine-interfaces)

## <a name="attachment-engine-interfaces"></a>Schnittstellen des Anlagen Moduls



| Schnittstelle                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iscesvstreamtachmentdata**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)               | Ruft Konfigurations-und Analysedaten zu einem angegebenen Sicherheitsdienst aus den Snap-Ins für die Sicherheitskonfiguration ab. Die Sicherheitskonfigurations-Snap-Ins machen diese Schnittstelle verfügbar, welche Anlagen-Snap-in-Erweiterungen zum Abfragen von Konfigurations-oder Analyse Informationen aufruft.                                                 |
| [**Iscesvplattachmentpersistinfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) | Ruft geänderte Konfigurations-oder Analyse Informationen von einem Anlage-Snap-in ab. Mithilfe der Sicherheitskonfigurations-Snap-Ins wird diese Schnittstelle aufgerufen, um geänderte Informationen aus der Erweiterungs-Snap-in-Erweiterung abzurufen. Das Sicherheitskonfigurations-Snap-in speichert diese Daten dann entsprechend in der Sicherheitsdatenbank. |



 

Weitere Informationen zu den COM-Schnittstellen, die von Snap-in-Erweiterungen implementiert werden müssen, finden Sie in der Dokumentation zu [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) .

 

 
