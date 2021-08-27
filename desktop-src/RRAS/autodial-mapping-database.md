---
title: AutoDial Mapping Database
description: Die AutoDial-Zuordnungsdatenbank ordnet Netzwerkadressen RAS-Telefonbucheinträgen zu.
ms.assetid: 4589d1e5-eec3-46ac-a10f-f20ae9f7b543
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e89bd065a136492281adb3424636a8820c76c76bf6867e70db75aecfa0f345d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036720"
---
# <a name="autodial-mapping-database"></a>AutoDial Mapping Database

Die AutoDial-Zuordnungsdatenbank ordnet Netzwerkadressen RAS-Telefonbucheinträgen zu. Die Datenbank kann IP-Adressen (z.B. "172.21.167.35"), Internethostnamen (z.B. "www.microsoft.com") oder NetBIOS-Namen (z.B. "products1") enthalten. Jeder Adresse in der AutoDial-Datenbank ist ein Satz von mindestens einem [**RASAUTODIALENTRY-Eintrag**](/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)) zugeordnet. Jeder dieser Einträge gibt einen Telefonbucheintrag an, den RAS wählen kann, um eine Verbindung mit der Adresse von einem bestimmten TAPI-Wählstandort (Phone Application Programming Interface) herzustellen. Weitere Informationen zu TAPI-Wählorten finden Sie in der TAPI-Dokumentation.

AutoDial erstellt in zwei Situationen automatisch Einträge in der AutoDial-Zuordnungsdatenbank:

-   Beim Versuch, eine Verbindung mit einer Netzwerkadresse herzustellen, tritt ein Fehler auf.

    Wenn es keinen Eintrag für die Adresse in der Zuordnungsdatenbank gibt und der Computer weder direkt noch über RAS mit einem Netzwerk verbunden ist, fordert AutoDial den Benutzer auf, die informationen anzugeben, die zum Herstellen einer DFÜ-Verbindung erforderlich sind. Wenn der Benutzer die Informationen bereitstellt und die DFÜ-Verbindung erfolgreich ist, speichert AutoDial die Informationen in der Zuordnungsdatenbank.

-   Wenn der Computer über RAS mit einem Netzwerk verbunden ist

    Wenn der Benutzer eine Verbindung mit einer Netzwerkadresse herstellt, erstellt AutoDial einen Eintrag in der Datenbank. Der Eintrag ordnet die Netzwerkadresse dem Telefonbucheintrag zu, der zum Herstellen der RAS-Verbindung verwendet wurde.

Sie können die [**RasSetAutodialAddress-Funktion**](/windows/desktop/api/Ras/nf-ras-rassetautodialaddressa) verwenden, um der AutoDial-Zuordnungsdatenbank eine Adresse hinzuzufügen, eine Adresse aus der Datenbank zu löschen oder die AutoDial-Einträge zu ändern, die einer vorhandenen Adresse in der Datenbank zugeordnet sind. Sie können die [**RasGetAutodialAddress-Funktion**](/windows/desktop/api/Ras/nf-ras-rasgetautodialaddressa) verwenden, um die AutoDial-Einträge abzurufen, die einer angegebenen Netzwerkadresse in der AutoDial-Zuordnungsdatenbank zugeordnet sind. Die [**RasEnumAutodialAddresses-Funktion**](/windows/desktop/api/Ras/nf-ras-rasenumautodialaddressesa) gibt eine Liste aller Adressen in der AutoDial-Zuordnungsdatenbank zurück.

 

 