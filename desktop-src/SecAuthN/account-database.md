---
description: Active Directory stellt die Kontodatenbank zur Verfügung, die vom Schlüsselverteilungscenter (KDC) verwendet wird, um Informationen zu Sicherheitsprinzipals in der Domäne zu erhalten.
ms.assetid: 560ef22c-dd4f-49f8-9e15-a45dbf17df01
title: Kontodatenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4d5e41c959a8c546ef36a5e4014b14ffc949e1670e2b32b199a8c9368bfbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141593"
---
# <a name="account-database"></a>Kontodatenbank

Active Directory stellt die [](/windows/desktop/SecGloss/k-gly) Kontodatenbank zur Verfügung, die vom Schlüsselverteilungscenter (KDC) verwendet wird, um Informationen über Sicherheitsprinzipale [*in*](/windows/desktop/SecGloss/s-gly) der Domäne zu erhalten. Jeder Prinzipal wird durch ein Kontoobjekt im Verzeichnis dargestellt. Der [*Verschlüsselungsschlüssel,*](/windows/desktop/SecGloss/e-gly) der für die Kommunikation mit einem Benutzer, Computer oder Dienst verwendet wird, wird als Attribut des Kontoobjekts dieses Sicherheitsprinzipals gespeichert.

Nur Domänencontroller sind Active Directory-Server. Jeder Domänencontroller speichert eine beschreibbare Kopie des Verzeichnisses, sodass Konten erstellt, Kennwörter zurückgesetzt und gruppenmitgliedschaften auf jedem Domänencontroller geändert werden können. Änderungen, die an einem Replikat des Verzeichnisses vorgenommen werden, werden automatisch an alle anderen Replikate propagiert. Windows repliziert den Informationsspeicher für Active Directory mithilfe eines proprietären Replikationsprotokolls mit mehreren Mastern, das eine sichere Remoteprozeduraufrufverbindung zwischen Replikationspartnern verwendet. Die Verbindung verwendet das [*Kerberos-Authentifizierungsprotokoll,*](/windows/desktop/SecGloss/k-gly) um gegenseitige [*Authentifizierung und*](/windows/desktop/SecGloss/a-gly) Verschlüsselung bereitzustellen.

Die physische Speicherung von Kontodaten wird vom [Verzeichnissystem-Agent](/windows/desktop/AD/directory-system-agent)verwaltet. Dabei handelt es sich um einen geschützten Prozess, der in die lokale Sicherheitsstelle [*(Local Security Authority,*](/windows/desktop/SecGloss/l-gly) LSA) auf dem Domänencontroller integriert ist. Clients des Verzeichnisdiensts erhalten nie direkten Zugriff auf den Datenspeicher. Jeder Client, der Zugriff auf Verzeichnisinformationen möchte, muss eine Verbindung mit dem Verzeichnissystem-Agent herstellen und dann verzeichnisobjekte und deren Attribute suchen, lesen und schreiben.

Anforderungen für den Zugriff auf ein Objekt oder Attribut im Verzeichnis unterliegen einer Überprüfung durch Windows Zugriffssteuerungsmechanismen. Wie Datei- und Ordnerobjekte im NTFS-Dateisystem werden Objekte in Active Directory durch Zugriffssteuerungslisten (Access [*Control*](/windows/desktop/SecGloss/a-gly) Lists, ACLs) geschützt, die angeben, wer auf das Objekt zugreifen kann und auf welche Weise. Im Gegensatz zu Dateien und Ordnern verfügen Active Directory-Objekte jedoch über eine ACL für jedes ihrer Attribute. Daher können Attribute für vertrauliche Kontoinformationen durch restriktivere Berechtigungen geschützt werden als für andere Attribute des Kontos.

Die vertraulichsten Informationen zu einem Konto sind natürlich sein Kennwort. Obwohl das Kennwortattribut eines Kontoobjekts einen von einem Kennwort abgeleiteten Verschlüsselungsschlüssel speichert, nicht das Kennwort selbst, ist dieser Schlüssel für ein Eindringling genauso nützlich. Daher wird der Zugriff auf das Kennwortattribut eines Kontoobjekts nur für den Kontoinhaber gewährt, niemals für andere Personen, nicht einmal für Administratoren. Nur Prozesse mit Trusted Computing Base-Berechtigungen [](/windows/desktop/SecGloss/c-gly) – Prozesse, die im Sicherheitskontext des LSA ausgeführt werden – dürfen Kennwortinformationen lesen oder ändern.

Um einen Offlineangriff durch eine Person mit Zugriff auf das Sicherungsband eines Domänencontrollers zu verhindern, wird das Kennwortattribut eines Kontoobjekts durch eine zweite Verschlüsselung mithilfe eines Systemschlüssels weiter geschützt. Dieser Verschlüsselungsschlüssel kann auf Wechselmedien gespeichert werden, sodass er separat geschützt werden kann, oder er kann auf dem Domänencontroller gespeichert, aber durch einen Verteilungsmechanismus geschützt werden. Administratoren können auswählen, wo der Systemschlüssel gespeichert wird und welcher von mehreren Algorithmen zum Verschlüsseln von Kennwortattributen verwendet wird.

 

 
