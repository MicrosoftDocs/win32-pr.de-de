---
description: Sie können eine Sicherheits Beschreibung für eine Named Pipe angeben, wenn Sie die Funktion "up-amedpipe" aufrufen. Der Sicherheits Deskriptor steuert den Zugriff auf Client-und Server Enden der Named Pipe.
ms.assetid: f9ea97c9-9a97-4083-82d8-29ffb8be5a77
title: Sicherheit und Zugriffsrechte für benannte Pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11cada606d8197ac2f64943aa742bbfd614fa4ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356201"
---
# <a name="named-pipe-security-and-access-rights"></a>Sicherheit und Zugriffsrechte für benannte Pipe

Mithilfe der Windows-Sicherheit können Sie den Zugriff auf Named Pipes steuern. Weitere Informationen zur Sicherheit finden Sie unter [Zugriffs Steuerungsmodell](/windows/desktop/SecAuthZ/access-control-model).

Sie können eine [Sicherheits Beschreibung](/windows/desktop/SecAuthZ/security-descriptors) für eine Named Pipe angeben, wenn Sie die Funktion "up- [**amedpipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) " aufrufen. Der Sicherheits Deskriptor steuert den Zugriff auf Client-und Server Enden der Named Pipe. Wenn Sie **null** angeben, erhält der Named Pipe eine Standard Sicherheits Beschreibung. Die ACLs in der Standard Sicherheits Beschreibung für eine Named Pipe gewähren dem Konto "LocalSystem", den Administratoren und dem Ersteller des Erstellers volle Kontrolle. Außerdem erteilen Sie den Mitgliedern der Gruppe Jeder und des anonymen Kontos Lesezugriff.

Um die Sicherheits Beschreibung eines Named Pipe abzurufen, rufen Sie die [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) -Funktion auf. Um die Sicherheits Beschreibung einer Named Pipe zu ändern, müssen Sie die Funktion [**setsecurityinfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) aufrufen.

Wenn ein Thread "up" aufruft, um ein Handle für das Server Ende einer vorhandenen [**Named Pipe zu öffnen**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) , führt das System eine Zugriffs Überprüfung durch, bevor das Handle zurückgegeben wird. Die Zugriffs Überprüfung vergleicht das Zugriffs Token des Threads und die angeforderten [Zugriffsrechte](/windows/desktop/SecAuthZ/access-rights-and-access-masks) mit der DACL in der Sicherheits Beschreibung des Named Pipe. Zusätzlich zu den angeforderten Zugriffsrechten muss die DACL zulassen, dass die aufrufenden Thread Datei den \_ \_ \_ Zugriff auf die Named Pipe der Pipe-Instanz ermöglicht.

Wenn ein Client die Funktion "up [**" oder "**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) [**callnamedpipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) " aufruft, um eine Verbindung mit dem Client Ende einer Named Pipe herzustellen, führt das System auf ähnliche Weise eine Zugriffs Überprüfung aus, bevor der Zugriff auf den Client gewährt wird.

Das Handle, das von der Funktion " [**roatamedpipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) " zurückgegeben wird, verfügt immer über Synchronisierungs Er verfügt auch \_ über generische Lese-, generische \_ Schreibvorgänge oder beides, je nach dem Öffnungs Modus der Pipe. Im folgenden finden Sie die Zugriffsrechte für jeden geöffneten Modus.



| Öffnungs Modus                           | Zugriffsrechte                                              |
|-------------------------------------|------------------------------------------------------------|
| \_Pipezugriffsduplex \_ (0x00000003)   | Generischer Dateityp \_ \_ lesen, generischer Dateityp \_ \_ schreiben und synchronisieren |
| Pipe- \_ Zugriff eingehend \_ (0x00000001)  | \_Dateigenerisch \_ Lesen und synchronisieren                        |
| Ausgehende Pipe- \_ Zugriff \_ (0x00000002) | \_Allgemeines \_ schreiben und Synchronisieren von Dateien                       |



 

Der \_ generische Datei \_ Lesezugriff für ein Named Pipe kombiniert die Rechte zum Lesen von Daten aus der Pipe, zum Lesen von Pipe-Attributen, zum Lesen erweiterter Attribute und zum Lesen der DACL der Pipe.

\_Der generische Datei \_ Schreibzugriff für eine Named Pipe kombiniert die Rechte zum Schreiben von Daten in die Pipe, zum Anfügen von Daten an die Pipe, zum Schreiben von Pipe-Attributen, zum Schreiben erweiterter Attribute und zum Lesen der DACL der Pipe. Da \_ \_ die Datei Daten \_ Anfügen und \_ die Pipe-Pipeline \_ Instanz die gleiche Definition aufweisen, wird durch die Datei \_ generischer \_ Schreibvorgang die Berechtigung zum Erstellen der Pipe ermöglicht. Um dieses Problem zu vermeiden, verwenden Sie die einzelnen Rechte anstelle der Verwendung des generischen Schreibzugriffs auf die Datei \_ \_ .

Sie können das Zugriffs \_ System \_ -Sicherheits Zugriffsrecht für ein Named Pipe Objekt anfordern, wenn Sie die SACL des Objekts lesen oder schreiben möchten. Weitere Informationen finden Sie unter [Zugriffs Steuerungs Listen (Access Control Lists, ACLs)](/windows/desktop/SecAuthZ/access-control-lists) und [SACL-Zugriffsrecht](/windows/desktop/SecAuthZ/sacl-access-right).

Um zu verhindern, dass Remote Benutzer oder Benutzer in einer anderen Terminaldienste-Sitzung auf eine Named Pipe zugreifen, verwenden Sie die Anmelde-SID für die DACL für die Pipe. Die Anmelde-SID wird auch bei der "Run-as"-Anmeldung verwendet. Dies ist die SID, mit der der Objekt Namespace pro Sitzung geschützt wird. Weitere Informationen finden Sie unter " [erhalten der Anmelde-SID" in C++](/previous-versions//aa446670(v=vs.85)).

 

 
