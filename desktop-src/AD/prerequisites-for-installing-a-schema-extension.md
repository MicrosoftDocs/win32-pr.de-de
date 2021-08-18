---
title: Voraussetzungen für die Installation einer Schemaerweiterung
description: Um das Schema zu ändern, stellen Sie sicher, dass Sie über die folgenden Rechte verfügen und die folgenden Informationen kennen. Sie müssen über ausreichende Rechte zum Ändern des Schemas verfügen.
ms.assetid: f7795eac-2b95-4b6c-a2f5-8728316059ab
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78af50626d452c8e26cbf1e7d33addfcea4f854cd2b40b0860bb98c783044748
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185302"
---
# <a name="prerequisites-for-installing-a-schema-extension"></a>Voraussetzungen für die Installation einer Schemaerweiterung

Um das Schema zu ändern, stellen Sie sicher, dass Sie über die folgenden Rechte verfügen und die folgenden Informationen kennen:

-   Sie müssen über ausreichende Rechte zum Ändern des Schemas verfügen. Das Schema enthält alle Datendefinitionen für Active Directory Domain Services für das gesamte Unternehmen. Zum Aktualisieren des Schemas muss ein Benutzer Mitglied der Gruppe Schemaadministratoren sein oder die Rechte zum Aktualisieren des Schemas delegiert worden sein.
-   Schemaänderungen können nur am Schemamaster vorgenommen werden. Weitere Informationen finden Sie unter [Erkennen des Schemamasters.](detecting-the-schema-master.md)
-   Der Schemamaster muss beschreibbar sein. Das heißt, der Sicherheitsinlock in der Registrierung muss entfernt werden. Weitere Informationen finden Sie unter [Aktivieren von Schemaänderungen im Schemamaster.](enabling-schema-changes-at-the-schema-master.md)
-   Weitere Informationen zum Überprüfen, ob der Schemamaster geändert werden kann, und zum Ändern der Einstellungen finden Sie unter "XADM: Das Schema für den Schemabesitzer kann nicht aktualisiert werden" im Hilfe- und Knowledge Base unter [https://support.microsoft.com/kb/261231](https://support.microsoft.com/kb/261231) .

 

 




