---
description: Es gibt eine Reihe von Techniken zur Bedrohungsminderung, die Sie verwenden können, um Kenn Wörter besser zu schützen.
ms.assetid: b2442579-e559-4053-869f-9d96e4db202e
title: Techniken zur Bedrohungsminderung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 435ec2b8db3a634ea93ce77d585038909056c7d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867800"
---
# <a name="threat-mitigation-techniques"></a>Techniken zur Bedrohungsminderung

Es gibt eine Reihe von Techniken zur Bedrohungsminderung, die Sie verwenden können, um Kenn Wörter besser zu schützen. Diese Techniken werden mithilfe einer oder mehrerer der folgenden vier primären Technologien implementiert.



| Technologie                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CryptoAPI                       | CryptoAPI bietet eine Reihe von Funktionen, mit deren Hilfe Sie kryptografieroutinen auf Ziel Entitäten anwenden können. CryptoAPI kann Hashes, Digests, Verschlüsselung und Entschlüsselung bereitstellen, um die primäre Funktionalität zu erwähnen. CryptoAPI weist auch andere Funktionen auf. Informationen zur Kryptografie und der kryptografieapi finden Sie unter [Kryptografie Essentials](/windows/desktop/SecCrypto/cryptography-essentials).           |
| Zugriffssteuerungslisten            | Eine [*Zugriffs Steuerungs Liste (Access Control List*](/windows/desktop/SecGloss/a-gly) , ACL) ist eine Liste von Sicherheitsmaßnahmen, die für ein Objekt gelten. Bei einem Objekt kann es sich um eine Datei, einen Prozess, ein Ereignis oder eine beliebige andere Person mit einem Sicherheits Deskriptor handeln. Weitere Informationen zu ACLs finden Sie unter [Access Control Listen](/windows/desktop/SecAuthZ/access-control-lists) (ACLs). |
| Datenschutz-API             | Die Datenschutz-API (Data Protection API, DPAPI) stellt die folgenden vier Funktionen bereit, mit denen Sie sensible Daten verschlüsseln und entschlüsseln können: [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata), [**CryptUnprotectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata), [**cryptprotectmemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory)und [**cryptunprotectmemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory).                  |
| Gespeicherte Benutzernamen und Kenn Wörter | Speicherfunktionen, die die Handhabung von Benutzer Kennwörtern und anderen Anmelde Informationen, wie z. b. private Schlüssel, vereinfachen, konsistentere und sicherer machen. Weitere Informationen zu dieser Funktion finden Sie unter " [**kreduipromptforanmelde**](/windows/desktop/api/wincred/nf-wincred-creduipromptforcredentialsa)Informationen".                                                                                                         |



 

Diese Technologien sind nicht auf allen Betriebssystemen verfügbar. Daher ist der Umfang, in dem die Sicherheit verbessert werden kann, abhängig davon, welche Betriebssysteme beteiligt sind. Im folgenden finden Sie die Technologien, die in jedem Betriebssystem verfügbar sind.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Betriebssystem</th>
<th>Technologie</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Server 2003 und Windows XP</td>
<td><ul>
<li>CryptoAPI</li>
<li>Zugriffssteuerungslisten</li>
<li>Datenschutz-API</li>
<li>Gespeicherte Benutzernamen und Kenn Wörter</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows 2000</td>
<td><ul>
<li>CryptoAPI</li>
<li>Zugriffssteuerungslisten</li>
<li><a href="/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata"><strong>CryptProtectData</strong></a></li>
<li><a href="/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectdata"><strong>CryptUnprotectData</strong></a></li>
</ul></td>
</tr>
</tbody>
</table>



 

Bei den folgenden Verfahren zur Bedrohungsminderung wird eine oder mehrere der vier Technologien verwendet. Techniken, die die Verwendung von Technologien erfordern, die nicht im Betriebssystem enthalten sind, können nicht verwendet werden.

## <a name="getting-passwords-from-the-user"></a>Kenn Wörter werden vom Benutzer erhalten.

Wenn Sie dem Benutzer das Einrichten eines Kennworts gestatten, erzwingen Sie die Verwendung sicherer Kenn Wörter. Fordern Sie z. b. an, dass Kenn Wörter eine minimale Länge haben, z. b. acht Zeichen. Kenn Wörter sollten auch groß-und Kleinbuchstaben, Ziffern und andere Tastatur Zeichen, wie z. b. das Dollarzeichen ($), Ausrufezeichen (!) oder größer als (>) einschließen müssen.

Nachdem Sie ein Kennwort erhalten haben, verwenden Sie es schnell (indem Sie so wenig Code wie möglich verwenden), und löschen Sie dann alle Überbleibsel des Kennworts. Dies minimiert die Zeit, die einem Eindring Dienst zum "Trap" des Kennworts zur Verfügung steht. Der Kompromiss bei dieser Technik ist die Häufigkeit, mit der das Kennwort vom Benutzer abgerufen werden muss. Das Prinzip sollte jedoch immer verwendet werden, wenn es möglich ist. Informationen dazu, wie Sie Kenn Wörter ordnungsgemäß abrufen, finden Sie unter [anfordern von Anmelde Informationen für den Benutzer](asking-the-user-for-credentials.md).

Vermeiden Sie die Angabe der Benutzeroberflächen Optionen "Kennwort speichern". Häufig fordern Benutzer diese Option an. Wenn Sie ihn bereitstellen müssen, sollten Sie mindestens sicherstellen, dass das Kennwort auf sichere Weise gespeichert wird. Weitere Informationen finden Sie im Abschnitt Speichern von Kenn Wörtern weiter unten in diesem Thema.

Kenn Wort Eingabe Versuche begrenzen. Sperren Sie den Benutzer nach einer bestimmten Anzahl von versuchen ohne Erfolg für eine bestimmte Zeitspanne. Optional können Sie die Antwortzeit für jeden Wiederholungs Vorgang auf einen maximalen Wert verlängern. Dieses Verfahren zielt darauf ab, einen Angriff zu besiegen.

## <a name="storing-passwords"></a>Speichern von Kenn Wörtern

Speichern Sie Kenn Wörter niemals im Klartext (unverschlüsselt). Das Verschlüsseln von Kenn Wörtern erhöht die Sicherheit erheblich. Informationen zum Speichern verschlüsselter Kenn Wörter finden Sie unter [**CryptProtectData**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectdata). Weitere Informationen zum Verschlüsseln von Kenn Wörtern im Speicher finden Sie unter [**cryptprotectmemory**](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory). Speichern Sie die Kenn Wörter an möglichst wenigen Stellen. Umso mehr stellen ein Kennwort gespeichert, desto größer ist die Wahrscheinlichkeit, dass ein Angreifer es finden kann. Speichern Sie niemals Kenn Wörter auf einer Webseite oder in einer webbasierten Datei. Durch das Speichern von Kenn Wörtern auf einer Webseite oder in einer webbasierten Datei können Sie problemlos kompromittiert werden.

Nachdem Sie ein Kennwort verschlüsselt und gespeichert haben, verwenden Sie sichere ACLs, um den Zugriff auf die Datei einzuschränken. Alternativ können Sie Kenn Wörter und Verschlüsselungsschlüssel auf Wechselmedien speichern. Das Speichern von Kenn Wörtern und Verschlüsselungsschlüsseln auf einem Wechselmedium, z. b. eine Smartcard, trägt dazu bei, ein sicheres System zu erstellen. Nachdem ein Kennwort für eine bestimmte Sitzung abgerufen wurde, kann die Karte entfernt werden, wodurch die Wahrscheinlichkeit entfernt wird, dass ein Angreifer darauf zugreifen kann.

 

 
