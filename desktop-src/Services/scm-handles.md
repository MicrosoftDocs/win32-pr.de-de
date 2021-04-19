---
description: Der SCM unterstützt handle-Typen, um den Zugriff auf die folgenden Objekte zuzulassen.
ms.assetid: 5ffdd1a9-1a66-4fc4-b35d-4f744bae4897
title: SCM-Handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c8a84fb09dbc95f3e1b5f5cee432de616f5ff6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366182"
---
# <a name="scm-handles"></a>SCM-Handles

Der SCM unterstützt handle-Typen, um den Zugriff auf die folgenden Objekte zuzulassen.

-   Die Datenbank der installierten Dienste.
-   Ein-Dienst.
-   Die Datenbanksperre.

Ein scmanager-Objekt stellt die Datenbank der installierten Dienste dar. Es handelt sich um ein Container Objekt, das Dienst Objekte enthält. Die [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) -Funktion gibt ein Handle für ein scmanager-Objekt auf einem angegebenen Computer zurück. Dieses Handle wird beim Installieren, löschen, öffnen und Auflisten von Diensten sowie beim Sperren der Dienst Datenbank verwendet.

Ein Dienst Objekt stellt einen installierten Dienst dar. Die Funktionen [**"-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) " und " [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) " geben Handles an installierte Dienste zurück.

Die Funktionen " [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)", " [**forateservice**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)" und " [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) " können unterschiedliche Typen von Zugriff auf scmanager-und Dienst Objekte anfordern. Der angeforderte Zugriff wird abhängig vom Zugriffs Token des aufrufenden Prozesses und der Sicherheits Beschreibung, die dem scmanager-oder Dienst Objekt zugeordnet ist, gewährt oder verweigert.

Die [**closeservicehandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle) -Funktion schließt Handles zu scmanager-und Dienst Objekten. Wenn Sie diese Handles nicht mehr benötigen, sollten Sie Sie schließen.

 

 



