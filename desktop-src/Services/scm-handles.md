---
description: Der SCM unterstützt Handletypen, um den Zugriff auf die folgenden Objekte zuzulassen.
ms.assetid: 5ffdd1a9-1a66-4fc4-b35d-4f744bae4897
title: SCM-Handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6830063e57b2135c32bf01b4fdc0b4cf6207de32198d9f88d97667f4b403fe2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889188"
---
# <a name="scm-handles"></a>SCM-Handles

Der SCM unterstützt Handletypen, um den Zugriff auf die folgenden Objekte zuzulassen.

-   Die Datenbank der installierten Dienste.
-   Ein Dienst.
-   Die Datenbanksperre.

Ein SCManager-Objekt stellt die Datenbank der installierten Dienste dar. Es handelt sich um ein Containerobjekt, das Dienstobjekte enthält. Die [**OpenSCManager-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) gibt ein Handle für ein SCManager-Objekt auf einem angegebenen Computer zurück. Dieses Handle wird beim Installieren, Löschen, Öffnen und Aufzählen von Diensten und beim Sperren der Dienstdatenbank verwendet.

Ein Dienstobjekt stellt einen installierten Dienst dar. Die Funktionen [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) und [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) geben Handles an installierte Dienste zurück.

Die Funktionen [**OpenSCManager,**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)und [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) können unterschiedliche Zugriffstypen auf SCManager- und Dienstobjekte anfordern. Der angeforderte Zugriff wird abhängig vom Zugriffstoken des aufrufenden Prozesses und dem Sicherheitsdeskriptor gewährt oder verweigert, der dem SCManager- oder Dienstobjekt zugeordnet ist.

Die [**CloseServiceHandle-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle) schließt Handles für SCManager- und Dienstobjekte. Wenn Sie diese Handles nicht mehr benötigen, schließen Sie sie unbedingt.

 

 



