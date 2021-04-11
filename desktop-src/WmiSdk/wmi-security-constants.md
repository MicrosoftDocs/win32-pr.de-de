---
description: WMI prüft die Zugriffsrechte für Anwendungen und Skripts.
ms.assetid: f6808f50-a1fd-434f-8a42-efa3afbe7871
ms.tgt_platform: multiple
title: WMI-Sicherheits Konstanten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d360aa57c12c958db95c4b94f2b06327a3f70dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218165"
---
# <a name="wmi-security-constants"></a>WMI-Sicherheits Konstanten

WMI prüft die Zugriffsrechte für Anwendungen und Skripts für Objekte wie WMI-Namespaces, Drucker, Dienste, DCOM-Anwendungen, Dateien, Freigaben und andere Sicherungs fähige Objekte. Der Zugriff auf diese Sicherungs fähigen Objekte wird durch Zugriffs Steuerungs Einträge (Access Control Entries, ACE) gesteuert. Jeder ACE enthält Listen, die festlegen, auf welche Gruppen oder Benutzer zugegriffen werden soll. Weitere Informationen zu Sicherheits-und Zugriffs Steuerungs Listen (ACLs, DACLs oder SACLs) finden Sie unter [Access Control Listen (ACLs)](/windows/desktop/SecAuthZ/access-control-lists) und [Sicherheits Deskriptoren](/windows/desktop/SecAuthZ/security-descriptors).

Viele Anbieter Methoden in WMI, die Sicherungs fähige Objekte betreffen, erfordern, dass der Administrator bestimmte Berechtigungen aktiviert. Welche Version der Berechtigung Sie verwenden, hängt von der Programmiersprache ab, wie in [**Berechtigungs Konstanten**](privilege-constants.md)gezeigt.

Die Sicherheits Konstanten werden in den folgenden Themen definiert:

-   [**Ereignis Sicherheits Konstanten**](event-security-constants.md)
-   [**Datei-und Verzeichniszugriffs Rechte-Konstanten**](file-and-directory-access-rights-constants.md)
-   [**Namespace-Zugriffsrechte Konstanten**](namespace-access-rights-constants.md)
-   [**Namespace-ACE-Flag-Konstanten**](namespace-ace-flag-constants.md)
-   [**Namespace-ACE-Typkonstanten**](namespace-ace-type-constants.md)
-   [**Berechtigungs Konstanten**](privilege-constants.md)

 

 
