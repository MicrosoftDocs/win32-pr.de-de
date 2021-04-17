---
title: Voraussetzungen für das Installieren einer Schema Erweiterung
description: Um das Schema zu ändern, stellen Sie sicher, dass Sie über die folgenden Rechte verfügen und über die folgenden Informationen verfügen. Sie müssen über ausreichende Rechte verfügen, um das Schema zu ändern.
ms.assetid: f7795eac-2b95-4b6c-a2f5-8728316059ab
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 275f468df54b9ced3dcca0648e4cc3602ab71422
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104314374"
---
# <a name="prerequisites-for-installing-a-schema-extension"></a>Voraussetzungen für das Installieren einer Schema Erweiterung

Um das Schema zu ändern, stellen Sie sicher, dass Sie über die folgenden Rechte verfügen und die folgenden Informationen beachten:

-   Sie müssen über ausreichende Rechte verfügen, um das Schema zu ändern. Das Schema enthält alle Daten Definitionen für Active Directory Domain Services für das gesamte Unternehmen. Um das Schema zu aktualisieren, muss ein Benutzer Mitglied der Gruppe "Schema Administratoren" sein, oder es muss die Berechtigung zum Aktualisieren des Schemas delegiert worden sein.
-   Schema Änderungen können nur am Schema Master vorgenommen werden. Weitere Informationen finden Sie unter [Erkennen des Schema Masters](detecting-the-schema-master.md).
-   Der Schema Master muss beschreibbar sein. Das heißt, die Sicherheits intersperre in der Registrierung muss entfernt werden. Weitere Informationen finden Sie unter [Aktivieren von Schema Änderungen am Schema Master](enabling-schema-changes-at-the-schema-master.md).
-   Weitere Informationen zum Überprüfen, ob der Schema Master geändert werden kann, und zum Ändern der Einstellungen finden Sie unter "XADM: nicht zum Aktualisieren des Schemas auf dem Schema Besitzer" in der Hilfe-und Support Knowledge Base unter [https://support.microsoft.com/kb/261231](https://support.microsoft.com/kb/261231) .

 

 




