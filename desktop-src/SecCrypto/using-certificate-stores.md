---
description: CAPICOM verwendet digitale Zertifikate, um Signaturen zu erstellen, Sitzungs Verschlüsselungsschlüssel zu verschlüsseln, wenn eingehüllte Nachrichten erstellt werden, und verschlüsselte Sitzungsschlüssel zu entschlüsseln, wenn eine eingeschlossene Nachricht empfangen wird.
ms.assetid: 018fc41a-19fd-4e4c-bfed-e0215afb5150
title: Verwenden von Zertifikat speichern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682068ba8f2f88d0fedabeef7ccee676f092e52e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347251"
---
# <a name="using-certificate-stores"></a>Verwenden von Zertifikat speichern

\[CAPICOM ist eine nur-32-Bit-Komponente, die für die Verwendung in den folgenden Betriebssystemen verfügbar ist: Windows Server 2008, Windows Vista und Windows XP. Verwenden Sie stattdessen die .NET Framework, um Sicherheitsfunktionen zu implementieren. Weitere Informationen finden Sie unter [Alternativen zur Verwendung von CAPICOM](alternatives-to-using-capicom.md).\]

CAPICOM verwendet [*digitale Zertifikate*](../secgloss/d-gly.md) , um Signaturen zu erstellen, Sitzungs Verschlüsselungsschlüssel zu verschlüsseln, wenn eingehüllte Nachrichten erstellt werden, und verschlüsselte Sitzungsschlüssel zu entschlüsseln, wenn eine eingeschlossene Nachricht empfangen wird. Standardmäßig verwendet CAPICOM Zertifikate im My-Speicher, die über einen zugeordneten privaten Schlüssel für die Erstellung [*digitaler Signaturen*](../secgloss/d-gly.md) und das Entschlüsseln von Sitzungs Schlüsseln verfügen. In den meisten Fällen muss eine Anwendung niemals einen Zertifikat Speicher öffnen oder anderweitig direkt bearbeiten.

Anwendungen, die eingeschlossene Nachrichten erstellen, verwenden jedoch den [*öffentlichen Schlüssel*](../secgloss/p-gly.md) für jeden beabsichtigten Empfänger einer eingeschlossenen Nachricht. Diese Schlüssel werden aus den Zertifikaten der vorgesehenen Empfänger abgerufen. Daher werden die Zertifikate dieser Empfänger in einem Zertifikat Speicher gesammelt, um eingeschlossene Nachrichten für eine Gruppe beabsichtigter Empfänger zu erstellen.

In der folgenden Tabelle sind die Standard Zertifikat Speicher aufgelistet, die normalerweise auf einer Benutzer Station gespeichert sind.



| Speicher        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                 |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| My           | Enthält persönliche Zertifikate. Diesen Zertifikaten wird normalerweise ein privater Schlüssel zugeordnet.                                                                                                                                                                                                                                                                             |
| Andere Personen | Enthält die Zertifikate der Benutzer, an die der Benutzer normalerweise eingeschlossene Nachrichten sendet oder von denen signierte Nachrichten empfangen werden.                                                                                                                                                                                                                                                     |
| ZS und Stamm  | Enthält die [*Zertifikate*](../secgloss/r-gly.md) der Zertifizierungsstellen, denen der Benutzer vertraut, um Zertifikate für andere auszustellen. Zertifikate in diesen speichern werden normalerweise mit dem Betriebssystem oder dem Netzwerkadministrator des Benutzers bereitgestellt. Zertifikate im Stamm Speicher sind in der Regel selbst signiert. |



 

Zusätzliche CAPICOM \_ \_ -Speicher für aktuelle Benutzer können erstellt, geöffnet und persistent gespeichert werden, indem ein anderer Speicher Name als Zeichenfolge gegeben wird. Wenn kein Speicher mit diesem Namen vorhanden ist, wird ein leerer Speicher erstellt und geöffnet. Wenn ein Speicher vorhanden ist, wird er geöffnet, und alle derzeit im Speicher gespeicherten Zertifikate werden zur Verfügung gestellt.

In den folgenden Abschnitten sind Beispiele für Zertifikat Speicher Tasks aufgeführt:

-   [Öffnen des Active Directory Stores und Abrufen von Zertifikaten](opening-the-active-directory-store-and-retrieving-certificates.md)
-   [Hinzufügen von Zertifikaten zu einem Zertifikat Speicher](adding-certificates-to-a-certificate-store.md)
-   [Verwenden von speichern an unterschiedlichen Standorten](using-stores-in-different-locations.md)
-   [Sammeln und Überprüfen von Zertifikaten](collecting-and-verifying-certificates.md)

 

 
