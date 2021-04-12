---
title: AutoDial-Verbindungs Vorgänge
description: Wenn der Versuch, eine Verbindung mit einer Netzwerkadresse herzustellen, fehlschlägt, weil der Host nicht erreicht werden kann, durchsucht das System die AutoDial-Zuordnungsdatenbank nach der Adresse.
ms.assetid: 343ee69e-1ff5-4107-9ddb-4245c3b4a54d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 150fa8542d1724be9d60f997db7952d6df387b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390411"
---
# <a name="autodial-connection-operations"></a>AutoDial-Verbindungs Vorgänge

Wenn der Versuch, eine Verbindung mit einer Netzwerkadresse herzustellen, fehlschlägt, weil der Host nicht erreicht werden kann, durchsucht das System die AutoDial-Zuordnungsdatenbank nach der Adresse. Wenn sich die Adresse in der Datenbank befindet, initiiert das System ggf. einen AutoDial-Vorgang für den [**rasauydialentry**](/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)), der dem lokalen TAPI-Wähl Speicherort entspricht.

Die RAS-API stellt Funktionen bereit, mit denen Sie AutoDial-Parameter festlegen und Abfragen können, mit denen AutoDial-Verbindungen gesteuert werden. Sie können die [**rassetaudedialenable**](/windows/desktop/api/Ras/nf-ras-rassetautodialenablea) -Funktion zum Aktivieren oder Deaktivieren der AutoDial-Funktion für einen angegebenen TAPI-wählspeicherort abrufen. Die Funktion " [**rasgetautodialenable**](/windows/desktop/api/Ras/nf-ras-rasgetautodialenablea) " gibt an, ob das AutoDial-Feature für einen angegebenen TAPI-Wähl Speicherort aktiviert ist. Weitere Informationen zu TAPI-Wähl Positionen finden Sie in der TAPI-Dokumentation. Sie können die [**rassetautodialparam**](/windows/desktop/api/Ras/nf-ras-rassetautodialparama) -Funktion zum Festlegen anderer AutoDial-Verbindungsparameter aufruft. Beispielsweise können Sie AutoDial-Verbindungen für die aktuelle Anmelde Sitzung deaktivieren. Aufrufen der Funktion " [**rasgetautodialparam**](/windows/desktop/api/Ras/nf-ras-rasgetautodialparama) ", um den aktuellen Wert der AutoDial-Verbindungsparameter zu ermitteln.

Das System stellt eine Standardbenutzer Oberfläche für AutoDial-Wähl Vorgänge bereit. Sie können jedoch eine AutoDial Dynamic Link Library (dll) erstellen, um eine benutzerdefinierte Benutzeroberfläche für AutoDial-Wahl Vorgänge bereitzustellen, die die angegebenen Telefonbucheinträge einschließen. Die AutoDial-dll muss sowohl eine ANSI-als auch eine Unicode-Version eines [**rasadfunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca) -AutoDial-Handlers exportieren.

Um Ihren benutzerdefinierten AutoDial-Handler für einen Telefonbucheintrag zu aktivieren, rufen Sie die [**rassetentryproperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) -Funktion auf, um die Eigenschaften für diesen Eintrag festzulegen. Die Elemente **szautodialdll** und **szautodialfunc** der [**rasentry**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) -Struktur, die an **rassetentryproperties** übergebenen werden, geben den Namen Ihrer AutoDial-dll und den Namen der [**rasadfunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca) -Funktion an, ausgenommen das Suffix "A" oder "W".

Wenn das System einen AutoDial-Vorgang für einen Telefonbucheintrag mit einem benutzerdefinierten AutoDial-Handler startet, ruft er den angegebenen [**rasadfunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca)auf. Die **rasadfunc** -Funktion empfängt einen Zeiger auf eine [**rasadpara AMS**](/previous-versions/windows/desktop/legacy/aa376719(v=vs.85)) -Struktur, die die Position und das übergeordnete Fenster für das Fenster ihrer Benutzeroberfläche angibt. Der **rasadfunc** kann einen Thread starten, um den benutzerdefinierten Wahlvorgang auszuführen. Die **rasadfunc** -Funktion gibt **true** zurück, um anzugeben, dass die Wähl Vorgänge übernommen wurden, oder **false** , um dem System das Durchführen der Wahl zu gestatten. Der benutzerdefinierte Wahlvorgang muss die Funktion " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " verwenden, um die tatsächliche Wahl durchzuführen. Wenn der Wahlvorgang abgeschlossen wurde, gibt der benutzerdefinierte Wahlvorgang Erfolg oder Fehler an, indem die Variable festgelegt wird, auf die der *lpdwretcode* -Parameter verweist, der an [**rasadfunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca)übergeben wird.

 

 