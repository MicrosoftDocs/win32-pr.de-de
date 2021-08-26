---
title: AutoDial Connection Operations
description: Wenn beim Versuch, eine Verbindung mit einer Netzwerkadresse herzustellen, ein Fehler auftritt, weil der Host nicht erreicht werden kann, durchsucht das System die AutoDial-Zuordnungsdatenbank nach der Adresse.
ms.assetid: 343ee69e-1ff5-4107-9ddb-4245c3b4a54d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef0f65f62121d631dcf035e641c9d0d4d89850d7673e1c47b82ff4a4889dff49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030500"
---
# <a name="autodial-connection-operations"></a>AutoDial Connection Operations

Wenn beim Versuch, eine Verbindung mit einer Netzwerkadresse herzustellen, ein Fehler auftritt, weil der Host nicht erreicht werden kann, durchsucht das System die AutoDial-Zuordnungsdatenbank nach der Adresse. Wenn sich die Adresse in der Datenbank befindet, initiiert das System einen autodialen Vorgang für [**RASAUTODIALENTRY**](/previous-versions/windows/desktop/legacy/aa376721(v=vs.85)), sofern vorhanden, der dem lokalen TAPI-Wählpfad entspricht.

Die RAS-API stellt Funktionen bereit, mit denen Sie AutoDial-Parameter zum Steuern von AutoDial-Verbindungen festlegen und abfragen können. Sie können die [**RasSetAutodialEnable-Funktion**](/windows/desktop/api/Ras/nf-ras-rassetautodialenablea) aufrufen, um die AutoDial-Funktion für einen angegebenen TAPI-Wählort zu aktivieren oder zu deaktivieren. Die [**RasGetAutodialEnable-Funktion**](/windows/desktop/api/Ras/nf-ras-rasgetautodialenablea) gibt an, ob die AutoDial-Funktion für einen angegebenen TAPI-Wählort aktiviert ist. Weitere Informationen zu TAPI-Wählorten finden Sie in der TAPI-Dokumentation. Sie können die [**RasSetAutodialParam-Funktion**](/windows/desktop/api/Ras/nf-ras-rassetautodialparama) aufrufen, um andere AutoDial-Verbindungsparameter festzulegen. Beispielsweise können Sie AutoDial-Verbindungen für die aktuelle Anmeldesitzung deaktivieren. Rufen Sie die [**RasGetAutodialParam-Funktion**](/windows/desktop/api/Ras/nf-ras-rasgetautodialparama) auf, um den aktuellen Wert der AutoDial-Verbindungsparameter zu bestimmen.

Das System stellt eine Standardbenutzeroberfläche für AutoDial Dialing-Vorgänge bereit. Sie können jedoch eine AutoDial-DLL (Dynamic Link Library) erstellen, um eine benutzerdefinierte Benutzeroberfläche für AutoDial Dialing-Vorgänge mit angegebenen Telefonbucheinträgen bereitzustellen. Ihre autodiale DLL muss sowohl eine ANSI- als auch eine Unicode-Version eines [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca) AutoDial-Handlers exportieren.

Um Ihren benutzerdefinierten AutoDial-Handler für einen Telefonbucheintrag zu aktivieren, rufen Sie die [**RasSetEntryProperties-Funktion**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) auf, um die Eigenschaften für diesen Eintrag festzulegen. Die an **RasSetEntryProperties** übergebenen **szAutodialDll-** und **szAutodialFunc-Member** der [**RASENTRY-Struktur**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) geben den Namen Ihrer AutoDial-DLL und den Namen Ihrer [**RASADFunc-Funktion**](/windows/desktop/api/Ras/nc-ras-rasadfunca) an, mit Ausnahme des Suffixes "A" oder "W".

Wenn das System einen AutoDial-Vorgang für einen Telefonbucheintrag mit einem benutzerdefinierten AutoDial-Handler startet, ruft es den angegebenen [**RASADFunc auf.**](/windows/desktop/api/Ras/nc-ras-rasadfunca) Die **RASADFunc-Funktion** empfängt einen Zeiger auf eine [**RASADPARAMS-Struktur,**](/previous-versions/windows/desktop/legacy/aa376719(v=vs.85)) die den Speicherort und das übergeordnete Fenster für das Fenster Ihrer Benutzeroberfläche angibt. **RasadFunc** kann einen Thread starten, um den benutzerdefinierten Wählvorgang auszuführen. Die **RASADFunc-Funktion** gibt **TRUE** zurück, um anzugeben, dass sie die Wählfunktion übernommen hat, oder **FALSE,** um dem System das Wählen zu ermöglichen. Ihr benutzerdefinierter Wählvorgang muss die [**RasDial-Funktion**](/windows/desktop/api/Ras/nf-ras-rasdiala) verwenden, um die tatsächliche Wählfunktion durchzuführen. Wenn der Wählvorgang abgeschlossen wurde, gibt der benutzerdefinierte Wählvorgang einen Erfolg oder Fehler an, indem die Variable festgelegt wird, auf die der *lpdwRetCode-Parameter* verweist, der an [**RASADFunc**](/windows/desktop/api/Ras/nc-ras-rasadfunca)übergeben wird.

 

 