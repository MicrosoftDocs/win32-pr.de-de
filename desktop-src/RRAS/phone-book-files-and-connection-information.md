---
title: Phone-Book von Dateien und Verbindungsinformationen
description: Ein rasdial-Befehl muss die Informationen angeben, die der RAS-Verbindungs-Manager benötigt, um die Verbindung herzustellen.
ms.assetid: bc3885a4-3c1e-47bc-b622-072b33ac3b51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d352772eec057edd6ab8c9f53640c50ea0fc73
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102135"
---
# <a name="phone-book-files-and-connection-information"></a>Phone-Book von Dateien und Verbindungsinformationen

Ein [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) -Befehl muss die Informationen angeben, die der RAS-Verbindungs-Manager benötigt, um die Verbindung herzustellen. In der Regel stellt der **rasdial** -Anruf die Verbindungsinformationen bereit, indem er einen Telefonbucheintrag angibt. Zu den Verbindungsinformationen in einem Telefonbucheintrag zählen Telefonnummern, Bit/s-Raten, [Informationen zur Benutzerauthentifizierung](user-authentication-information.md)und [andere Verbindungsinformationen](other-connection-information.md).

Ein RAS-Client verwendet die Parameter der Funktion " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) ", um eine Telefonbuchdatei und einen Eintrag in dieser Datei anzugeben. Der *lpszphonebookpath* -Parameter kann den Namen einer Telefonbuchdatei angeben, oder er kann **null** sein, um anzugeben, dass die standardmäßige Telefonbuchdatei verwendet werden soll. Der *lprasdialparameams* -Parameter verweist auf eine [**rasdialbiams**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) -Struktur, die den Namen des zu verwendenden Telefonbucheintrags angibt.

Zum Anzeigen einer Liste von Telefonbucheinträgen, von denen der Benutzer eine Verbindung auswählen kann, kann ein RAS-Client die Funktion " [**RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa) " aufrufen, um die Einträge in einer Telefonbuchdatei aufzulisten.

Um eine Verbindung herzustellen, ohne einen Telefonbucheintrag zu verwenden, kann der Befehl " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " eine leere Zeichenfolge für den **szentryname** -Member der " [**rasdialparameams**](/previous-versions/windows/desktop/legacy/aa377238(v=vs.85)) "-Struktur angeben. Der " **rasdialparser. szphonenumber** "-Member muss die aufzurufende Zahl enthalten. In diesem Fall verwendet der RAS-Verbindungs-Manager den ersten verfügbaren Modemanschluss und die Standardwerte für alle anderen Einstellungen.

 

 