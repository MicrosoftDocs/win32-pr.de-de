---
description: Active Directory stellt die Konto Datenbank bereit, die der Schlüsselverteilungscenter (KDC) zum Abrufen von Informationen zu Sicherheits Prinzipale in der Domäne verwendet.
ms.assetid: 560ef22c-dd4f-49f8-9e15-a45dbf17df01
title: Konto Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0713d8f7b4336f43172fcd5cda18aa9d25c702fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959921"
---
# <a name="account-database"></a>Konto Datenbank

Active Directory stellt die Konto Datenbank bereit, die der [*Schlüsselverteilungscenter*](/windows/desktop/SecGloss/k-gly) (KDC) zum Abrufen von Informationen zu [*Sicherheits Prinzipale*](/windows/desktop/SecGloss/s-gly) in der Domäne verwendet. Jeder Prinzipal wird durch ein Konto Objekt im Verzeichnis dargestellt. Der [*Verschlüsselungs*](/windows/desktop/SecGloss/e-gly) Schlüssel, der für die Kommunikation mit einem Benutzer, einem Computer oder einem Dienst verwendet wird, wird als Attribut des Konto Objekts dieses Sicherheits Prinzipals gespeichert.

Nur Domänen Controller sind Active Directory Server. Jeder Domänen Controller speichert eine beschreibbare Kopie des Verzeichnisses, sodass Konten erstellt, Kenn Wörter zurückgesetzt und die Gruppenmitgliedschaft auf einem beliebigen Domänen Controller geändert werden kann. An einem Replikat des Verzeichnisses vorgenommene Änderungen werden automatisch an alle anderen Replikate weitergegeben. Windows repliziert den Informationsspeicher für die Active Directory mithilfe eines proprietären Replikations Protokolls mit mehreren Mastern, das eine sichere Remote Prozedur Aufrufe zwischen Replikations Partnern verwendet. Für die Verbindung wird das [*Kerberos-Authentifizierungsprotokoll*](/windows/desktop/SecGloss/k-gly) verwendet, um die gegenseitige [*Authentifizierung*](/windows/desktop/SecGloss/a-gly) und Verschlüsselung bereitzustellen.

Die physische Speicherung von Kontodaten wird vom [Verzeichnis System-Agent](/windows/desktop/AD/directory-system-agent)verwaltet, einem geschützten Prozess, der mit der [*lokalen Sicherheits Autorität (Local Security Authority*](/windows/desktop/SecGloss/l-gly) , LSA) auf dem Domänen Controller integriert ist. Clients des Verzeichnis Dienstanbieter erhalten nie direkten Zugriff auf den Datenspeicher. Jeder Client, der Zugriff auf Verzeichnisinformationen wünscht, muss eine Verbindung mit dem Verzeichnis System-Agent herstellen und anschließend Verzeichnisobjekte und deren Attribute suchen, lesen und schreiben.

Anforderungen für den Zugriff auf ein Objekt oder Attribut im Verzeichnis können von Windows-Zugriffs Steuerungsmechanismen überprüft werden. Wie Datei-und Ordner Objekte im NTFS-Dateisystem werden Objekte in der Active Directory durch [*Zugriffs Steuerungs Listen (Access Control Lists*](/windows/desktop/SecGloss/a-gly) , ACLs) geschützt, die angeben, wer auf das Objekt zugreifen kann und auf welche Weise. Im Gegensatz zu Dateien und Ordnern haben Active Directory Objekte jedoch für jedes ihrer Attribute eine ACL. Daher können Attribute für vertrauliche Kontoinformationen durch restriktivere Berechtigungen geschützt werden, als diejenigen, die anderen Attributen des Kontos erteilt wurden.

Die sensibelsten Informationen zu einem Konto sind natürlich sein Kennwort. Obwohl das Password-Attribut eines Account-Objekts einen Verschlüsselungsschlüssel speichert, der von einem Kennwort abgeleitet ist, aber nicht das Kennwort selbst, ist dieser Schlüssel für einen Eindring Dienst ebenso nützlich. Daher wird der Zugriff auf das Password-Attribut eines Account-Objekts nur dem Kontoinhaber erteilt, niemals an andere Personen, nicht sogar an Administratoren. Nur Prozesse mit vertrauenswürdigem Computing-Basis Privileg – Prozesse, die im Sicherheits [*Kontext*](/windows/desktop/SecGloss/c-gly) der LSA ausgeführt werden – dürfen Kenn Wort Informationen lesen oder ändern.

Um einen Offline Angriff durch eine Person mit Zugriff auf das Sicherungs Band eines Domänen Controllers zu verhindern, wird das Kenn Wort Attribut eines Konto Objekts durch eine zweite Verschlüsselung mit einem Systemschlüssel weiter geschützt. Dieser Verschlüsselungsschlüssel kann auf einem Wechsel Datenträger gespeichert werden, sodass er separat geschützt werden kann, oder er kann auf dem Domänen Controller gespeichert, aber durch einen Zerstreuung Mechanismus geschützt werden. Administratoren haben die Möglichkeit, zu entscheiden, wo der Systemschlüssel gespeichert wird und welche der verschiedenen Algorithmen zum Verschlüsseln von Kenn Wort Attributen verwendet werden.

 

 
