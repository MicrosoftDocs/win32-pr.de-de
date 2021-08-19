---
description: CAPICOM verwendet digitale Zertifikate zum Erstellen von Signaturen, Verschlüsseln von Sitzungsverschlüsselungsschlüsseln beim Erstellen umhumschlagener Nachrichten und Entschlüsseln verschlüsselter Sitzungsschlüssel, wenn eine umhumhierte Nachricht empfangen wird.
ms.assetid: 018fc41a-19fd-4e4c-bfed-e0215afb5150
title: Verwenden von Zertifikatspeichern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f687286d40e64e590079d872a0134742d552b66a9926a1febeb5c42ae2ad7566
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971612"
---
# <a name="using-certificate-stores"></a>Verwenden von Zertifikatspeichern

\[CAPICOM ist eine 32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfeatures zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]

CAPICOM verwendet digitale Zertifikate zum Erstellen von Signaturen, Verschlüsseln von [*Sitzungsverschlüsselungsschlüsseln*](../secgloss/d-gly.md) beim Erstellen umhumschlagener Nachrichten und Entschlüsseln verschlüsselter Sitzungsschlüssel, wenn eine umhumhierte Nachricht empfangen wird. Standardmäßig verwendet CAPICOM Zertifikate im Speicher "My", die [](../secgloss/d-gly.md) über einen zugeordneten privaten Schlüssel für die Erstellung digitaler Signaturen und die Entschlüsselung von Sitzungsschlüsseln verfügen. In den meisten Fällen muss eine Anwendung niemals einen Zertifikatspeicher öffnen oder anderweitig direkt behandeln.

Anwendungen, die umhumschlagte Nachrichten erstellen, verwenden jedoch den [*öffentlichen Schlüssel*](../secgloss/p-gly.md) jedes beabsichtigten Empfängers einer umschlagten Nachricht. Diese Schlüssel werden aus den Zertifikaten der vorgesehenen Empfänger abgerufen. Daher werden die Zertifikate dieser Empfänger in einem Zertifikatspeicher gesammelt, um umhumhierte Nachrichten für eine Gruppe vorgesehener Empfänger zu erstellen.

In der folgenden Tabelle sind die Standardzertifikatspeicher aufgeführt, die normalerweise auf einer Benutzerstation gespeichert werden.



| Speicher        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| My           | Enthält persönliche Zertifikate. Diesen Zertifikaten wird in der Regel ein privater Schlüssel zugeordnet.                                                                                                                                                                                                                                                                             |
| Andere Personen | Enthält die Zertifikate der Zertifikate, an die der Benutzer normalerweise umschlagte Nachrichten sendet oder von denen signierte Nachrichten empfangen werden.                                                                                                                                                                                                                                                     |
| Ca und Root  | Enthält die [*Zertifikate von Zertifizierungsstellen,*](../secgloss/r-gly.md) denen der Benutzer vertraut, um Anderen Zertifikate ausstellen zu können. Zertifikate in diesen Speichern werden normalerweise mit dem Betriebssystem oder vom Netzwerkadministrator des Benutzers bereitgestellt. Zertifikate im Stammspeicher sind in der Regel selbstsigniert. |



 

Zusätzliche CAPICOM CURRENT USER-Speicher können erstellt, geöffnet und beibehalten werden, indem ein anderer \_ \_ Geschäftsname als Zeichenfolge übergeben wird. Wenn kein Speicher mit diesem Namen vorhanden ist, wird ein leerer Speicher erstellt und geöffnet. Wenn ein Speicher vorhanden ist, wird er geöffnet, und alle zertifikate, die sich derzeit im Speicher befinden, werden verfügbar gemacht.

Die folgenden Abschnitte zeigen Beispiele für Zertifikatspeicheraufgaben:

-   [Öffnen der Active Directory-Store und Abrufen von Zertifikaten](opening-the-active-directory-store-and-retrieving-certificates.md)
-   [Hinzufügen von Zertifikaten zu einem Store](adding-certificates-to-a-certificate-store.md)
-   [Verwenden von Speichern an unterschiedlichen Standorten](using-stores-in-different-locations.md)
-   [Sammeln und Überprüfen von Zertifikaten](collecting-and-verifying-certificates.md)

 

 
