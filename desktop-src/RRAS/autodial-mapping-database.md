---
title: AutoDial-Daten Bank Zuordnung
description: Die AutoDial-Zuordnungs Datenbank ordnet Netzwerkadressen RAS-Telefonbucheinträgen zu.
ms.assetid: 4589d1e5-eec3-46ac-a10f-f20ae9f7b543
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511f15f98848559a892e8c20e766d47a07780fbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858294"
---
# <a name="autodial-mapping-database"></a>AutoDial-Daten Bank Zuordnung

Die AutoDial-Zuordnungs Datenbank ordnet Netzwerkadressen RAS-Telefonbucheinträgen zu. Die Datenbank kann IP-Adressen (z. b. "172.21.167.35"), Internet Hostnamen (z. b. "www.Microsoft.com") oder NetBIOS-Namen (z. b. "products1") enthalten. Die jeder Adresse in der AutoDial-Datenbank zugeordnet ist, ist ein Satz von mindestens einem [**rasauydialentry-Eintrag**](/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)) . Jeder dieser Einträge gibt einen Telefonbucheintrag an, den RAS für das Herstellen einer Verbindung mit der Adresse von einem bestimmten Standort der Telefonieschnittstelle (Application Programming Interface, TAPI) wählen kann. Weitere Informationen zu TAPI-Wähl Positionen finden Sie in der TAPI-Dokumentation.

AutoDial erstellt in zwei Situationen automatisch Einträge in der AutoDial-Mapping-Datenbank:

-   Wenn ein Verbindungsversuch mit einer Netzwerkadresse fehlschlägt

    Wenn es in der Zuordnungsdatenbank keinen Eintrag für die Adresse gibt und der Computer weder direkt noch über RAS mit einem Netzwerk verbunden ist, wird der Benutzer von AutoDial aufgefordert, die Informationen anzugeben, die zum Herstellen einer DFÜ-Verbindung erforderlich sind. Wenn der Benutzer die Informationen bereitstellt und der DFÜ-Verbindungsvorgang erfolgreich ist, speichert AutoDial die Informationen in der Mapping-Datenbank.

-   Wenn der Computer über RAS mit einem Netzwerk verbunden ist

    Wenn der Benutzer eine Verbindung mit einer Netzwerkadresse herstellt, erstellt AutoDial einen Eintrag in der Datenbank. Der Eintrag ordnet die Netzwerkadresse dem Telefonbucheintrag zu, der zum Herstellen der RAS-Verbindung verwendet wurde.

Sie können die Funktion " [**rassetautdialaddress**](/windows/desktop/api/Ras/nf-ras-rassetautodialaddressa) " verwenden, um der AutoDial-Zuordnungs Datenbank eine Adresse hinzuzufügen, eine Adresse aus der Datenbank zu löschen oder die AutoDial-Einträge zu ändern, die einer vorhandenen Adresse in der Datenbank zugeordnet sind. Mithilfe der Funktion " [**rasgetautodialaddress**](/windows/desktop/api/Ras/nf-ras-rasgetautodialaddressa) " können Sie die AutoDial-Einträge abrufen, die einer angegebenen Netzwerkadresse in der AutoDial-Mapping-Datenbank zugeordnet sind. Die Funktion " [**rasenumschlag autodialadressen**](/windows/desktop/api/Ras/nf-ras-rasenumautodialaddressesa) " gibt eine Liste aller Adressen in der AutoDial-Mapping-Datenbank zurück.

 

 