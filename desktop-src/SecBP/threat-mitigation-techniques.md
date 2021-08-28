---
description: Es gibt eine Reihe von Techniken zur Bedrohungsminderung, mit denen Sie Kennwörter besser schützen können.
ms.assetid: b2442579-e559-4053-869f-9d96e4db202e
title: Techniken zur Bedrohungsminderung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 315a79ec1db48a16de858d655bd1550fa1458720
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482446"
---
# <a name="threat-mitigation-techniques"></a>Techniken zur Bedrohungsminderung

Es gibt eine Reihe von Techniken zur Bedrohungsminderung, mit denen Sie Kennwörter besser schützen können. Diese Techniken werden mit einer oder mehreren der folgenden vier primären Technologien implementiert.



| Technologie                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cryptoapi                       | CryptoAPI bietet eine Reihe von Funktionen, mit denen Sie kryptografische Routinen auf Zielentitäten anwenden können. CryptoAPI kann Hashes, Digests, Verschlüsselung und Entschlüsselung bereitstellen, um die primäre Funktionalität zu nennen. CryptoAPI verfügt auch über weitere Features. Weitere Informationen zur Kryptografie und zur CryptoAPI finden Sie unter [Cryptography Essentials](/windows/desktop/SecCrypto/cryptography-essentials).           |
| Zugriffssteuerungslisten            | Eine [*Zugriffssteuerungsliste (Access Control List,*](/windows/desktop/SecGloss/a-gly) ACL) ist eine Liste von Sicherheitsschutzfunktionen, die für ein Objekt gelten. Ein Objekt kann eine Datei, ein Prozess, ein Ereignis oder ein anderes Objekt sein, das über einen Sicherheitsdeskriptor verfügt. Weitere Informationen zu ACLs finden Sie unter [Access Control Listen](/windows/desktop/SecAuthZ/access-control-lists) (ACLs). |
| Datenschutz-API             | Die Datenschutz-API (Data Protection API, DPAPI) stellt die folgenden vier Funktionen bereit, die Sie zum Verschlüsseln und Entschlüsseln vertraulicher Daten verwenden: [**CryptProtectData,**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata) [**CryptUnprotectData,**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata) [**CryptProtectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory)und [**CryptUnprotectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory).                  |
| Gespeicherte Benutzernamen und Kennwörter | Storage Funktionalität, die die Verarbeitung von Benutzerkennwörtern und anderen Anmeldeinformationen wie privaten Schlüsseln vereinfacht, konsistenter und sicherer macht. Weitere Informationen zu dieser Funktionalität finden Sie unter [**CredUIPromptForCredentials**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa).                                                                                                         |



 

Diese Technologien sind nicht auf allen Betriebssystemen verfügbar. Daher hängt das Ausmaß, in dem die Sicherheit verbessert werden kann, davon ab, welche Betriebssysteme beteiligt sind. Hier sind die Technologien, die in den einzelnen Betriebssystemen verfügbar sind.


| Betriebssystem | Technologie | 
|------------------|------------|
| Windows Server 2003 und Windows XP | <ul><li>Cryptoapi</li><li>Zugriffssteuerungslisten</li><li>Datenschutz-API</li><li>Gespeicherte Benutzernamen und Kennwörter</li></ul> | 
| Windows 2000 | <ul><li>Cryptoapi</li><li>Zugriffssteuerungslisten</li><li><a href="/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata"><strong>CryptProtectData</strong></a></li><li><a href="/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata"><strong>CryptUnprotectData</strong></a></li></ul> | 




 

Bei den folgenden Techniken zur Bedrohungsminderung wird mindestens eine der vier Technologien verwendet. Techniken, die die Verwendung von Technologien erfordern, die nicht im Betriebssystem enthalten sind, können nicht verwendet werden.

## <a name="getting-passwords-from-the-user"></a>Abrufen von Kennwörtern vom Benutzer

Wenn Sie dem Benutzer erlauben, ein Kennwort einzurichten, erzwingen Sie die Verwendung sicherer Kennwörter. Beispielsweise müssen Kennwörter mindestens acht Zeichen lang sein. Kennwörter müssen auch Groß- und Kleinbuchstaben, Zahlen und andere Tastaturzeichen wie das Dollarzeichen ($), das Ausrufezeichen (!) oder größer als (>) enthalten.

Nachdem Sie ein Kennwort erhalten haben, verwenden Sie es schnell (mit so wenig Code wie möglich), und löschen Sie dann alle Spuren des Kennworts. Dies minimiert die Zeit, die einem Eindringling zum "Abfangen" des Kennworts zur Verfügung steht. Der Vergleich mit dieser Technik ist die Häufigkeit, mit der das Kennwort vom Benutzer abgerufen werden muss. das Prinzip sollte jedoch nach Möglichkeit angewendet werden. Informationen zum ordnungsgemäßen Abrufen von Kennwörtern finden Sie unter [Fragen des Benutzers nach Anmeldeinformationen.](asking-the-user-for-credentials.md)

Vermeiden Sie die Bereitstellung von Optionen für die Benutzeroberfläche "Kennwort speichern". Häufig fordern Benutzer diese Option an. Wenn Sie es angeben müssen, stellen Sie mindestens sicher, dass das Kennwort sicher gespeichert wird. Weitere Informationen finden Sie weiter unten in diesem Thema im Abschnitt Speichern von Kennwörtern.

Beschränken Sie die Kennworteingabeversuche. Sperren Sie den Benutzer nach einer bestimmten Anzahl von Versuchen ohne Erfolg für einen bestimmten Zeitraum. Verlängern Sie optional die Antwortzeit für jeden Versuch über einen Höchstwert. Diese Technik zielt darauf ab, einen Schätzangriff zu vereigen.

## <a name="storing-passwords"></a>Speichern von Kennwörtern

Speichern Sie Kennwörter niemals in Klartext (unverschlüsselt). Das Verschlüsseln von Kennwörtern erhöht die Sicherheit erheblich. Informationen zum Speichern verschlüsselter Kennwörter finden Sie unter [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata). Informationen zum Verschlüsseln von Kennwörtern im Arbeitsspeicher finden Sie unter [**CryptProtectMemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory). Store Kennwörter an so wenigen Stellen wie möglich. Je mehr Stellen ein Kennwort gespeichert wird, desto größer ist die Wahrscheinlichkeit, dass ein Eindringling es findet. Speichern Sie Kennwörter niemals auf einer Webseite oder in einer webbasierten Datei. Das Speichern von Kennwörtern auf einer Webseite oder in einer webbasierten Datei ermöglicht eine einfache Kompromittierung.

Nachdem Sie ein Kennwort verschlüsselt und gespeichert haben, verwenden Sie sichere ACLs, um den Zugriff auf die Datei zu beschränken. Alternativ können Sie Kennwörter und Verschlüsselungsschlüssel auf Wechselmedien speichern. Das Speichern von Kennwörtern und Verschlüsselungsschlüsseln auf einem Wechselmedium, z. B. einer Smartcard, hilft bei der Erstellung eines sichereren Systems. Nachdem ein Kennwort für eine bestimmte Sitzung abgerufen wurde, kann die Karte entfernt werden, wodurch die Möglichkeit beseitigt wird, dass ein Eindringling Darauf zugreifen kann.

 

 
