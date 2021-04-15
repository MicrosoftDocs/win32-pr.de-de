---
title: Get-Funktionen
description: Die Get-Funktionen der Netzwerkverwaltung rufen Informationen zu einer Domäne ab. Sie können diese Funktionen auch aufrufen, um Informationen zu lokalen, globalen, Arbeitsstations-und Server Benutzerkonten abzurufen.
ms.assetid: 9c97420d-bc8a-42c9-b7ea-3d2ebc0034b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8da830e1b86d3de3359d3ed3627a8d392737569
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515854"
---
# <a name="get-functions"></a>Get-Funktionen

Die Get-Funktionen der Netzwerkverwaltung rufen Informationen zu einer Domäne ab. Sie können diese Funktionen auch aufrufen, um Informationen zu lokalen, globalen, Arbeitsstations-und Server Benutzerkonten abzurufen.

Die Get-Funktionen der Netzwerkverwaltung sind nachfolgend aufgeführt.



| Funktion                                                               | BESCHREIBUNG                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**Netgetanydcname**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetanydcname)                             | Gibt den Namen eines beliebigen Domänen Controllers für eine Domäne zurück, die direkt von einem angegebenen Server als vertrauenswürdig eingestuft wird.                                   |
| [**NetGetDCName**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdcname)                                   | Gibt den Namen des primären Domänen Controllers (PDC) für die angegebene Domäne zurück.                                                        |
| [**Netgetdisplayinformationindex**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgetdisplayinformationindex) | Gibt den Index des ersten Anzeige Informations Eintrags zurück, dessen Name mit einer angegebenen Zeichenfolge beginnt oder alphabetisch auf die Zeichenfolge folgt. |
| [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)       | Gibt Informationen zu Benutzern, Computern oder globalen Gruppenkonten zurück.                                                                             |



 

Die von der Funktion [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation) zurückgegebenen Informationen sind auf folgenden Ebenen verfügbar:

-   [**Netzwerk \_ Anzeige \_ Gruppe**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_group)
-   [**Netzwerk \_ Anzeige \_ Computer**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_machine)
-   [**Benutzer für Netzwerk \_ Anzeige \_**](/windows/desktop/api/Lmaccess/ns-lmaccess-net_display_user)

 

 




