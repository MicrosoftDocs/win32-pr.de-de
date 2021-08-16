---
description: Wenn Sie eine GINA schreiben, um die GINA-Standard-DLL (MSGina.dll) von Microsoft zu ersetzen, sollten Sie einige oder alle GINA-Standardfunktionen bereitstellen.
ms.assetid: cd2ce7b7-6167-4451-9f6e-881676a2145c
title: MSGina.dll Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2acf5d1e7e9dccf9581b27ea2fef3deb1c2c8aa218a1b0a711b7015134e1d2d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117786749"
---
# <a name="msginadll-features"></a>MSGina.dll Features

Wenn Sie eine [*GINA*](../secgloss/g-gly.md) schreiben, um die GINA-Standard-DLL (MSGina.dll) von Microsoft zu ersetzen, sollten Sie einige oder alle GINA-Standardfunktionen bereitstellen. Es folgt eine Liste der Standardfeatures und eine kurze Beschreibung, wie sie gesteuert werden.

> [!Note]  
> GINA-DLLs werden in Windows Vista ignoriert.

 

Registrierungsschlüsselwerte steuern die Verfügbarkeit oder das Verhalten vieler dieser GINA-Standardfeatures. Sofern nicht anders angegeben, gehören diese Schlüsselwerte zum Winlogon-Registrierungsschlüssel und weisen den Werttyp \[ REG \_ SZ \] auf. Der tatsächliche Pfad des [*Winlogon-Schlüssels*](../secgloss/w-gly.md) lautet:

**\\HKEY \_ LOCAL MACHINE Software Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ Winlogon**

-   **Rechtliche Benachrichtigung (Dialogfeld)**

    An einigen Stellen ist es zulässig, dass sich jeder Benutzer, der Zugriff auf eine Arbeitsstation hat, anmeldet und mit der Arbeit beginnt, es sei denn, es gibt eine Benachrichtigung, die angibt, dass das System nur für autorisierte Benutzer vorgesehen ist. Darüber hinaus möchten viele Benutzer, dass unternehmensspezifische Nachrichten vor der normalen Anmeldung angezeigt werden. Die GINA standard verwendet zwei Winlogon-Registrierungsschlüsselwerte, um einem System das Anzeigen von Informationen vor der Anmeldung zu ermöglichen. Wenn einer der Schlüsselwerte vorhanden ist und eine Zeichenfolge ungleich NULL enthält, wird vor dem üblichen Willkommensbildschirm ein Dialogfeld Rechtliche Hinweise angezeigt. Diese Schlüsselwertnamen werden in der folgenden Tabelle angezeigt.

    

    | Schlüsselwertname         | Inhalte                                                            |
    |------------------------|---------------------------------------------------------------------|
    | **LegalNoticeCaption** | Die Zeichenfolge, die als Beschriftung des Dialogfelds "Rechtliche Hinweise" angezeigt werden soll. |
    | **LegalNoticeText**    | Die Zeichenfolge, die als Meldung des Dialogfelds "Rechtliche Hinweise" angezeigt werden soll. |

    

     

-   **Anzeigen des Nachbenutzernamens**

    Standardmäßig wird auf dem Anmeldebildschirm der Name des letzten Benutzers angezeigt, der sich erfolgreich bei der Arbeitsstation anmelden soll. Dieses Feature wird durch den Registrierungsschlüsselwert **DontDisplayLastUserName** gesteuert. Wenn dieser Schlüsselwert auf 1 festgelegt ist, wird der Benutzername nicht im Anmeldedialogfeld angezeigt.

-   **Automatische Anmeldung**

    Dieses Feature ermöglicht es einem System, sich automatisch bei jedem Systemstart anzumelden, indem Standardinformationen verwendet und das Feld STRG+ALT+ENTF-Anmeldung deaktiviert wird.

    Dieses Feature verwendet die folgenden Werte des Winlogon-Schlüssels.

    

    | Wert                 | Inhalte                                           |
    |-----------------------|----------------------------------------------------|
    | **AutoAdminLogon**    | 1                                                  |
    | **AutoLogonCount**    | Gibt an, wie oft eine automatische Anmeldung erfolgen soll       |
    | **DefaultUserName**   | Der Name des Benutzerkontos.                       |
    | **DefaultDomainName** | Der Name der Domäne, in der sich das Benutzerkonto befindet. |

    

     

    Wenn der **AutoAdminLogon-Schlüsselwert** vorhanden ist und einen Schlüssel enthält und der **Schlüsselwert AutoLogonCount** nicht vorhanden ist, erfolgt jedes Mal eine automatische Anmeldung, wenn sich der aktuelle Benutzer abmeldet oder das System neu gestartet wird. Das Konto, bei dem die Anmeldung erfolgt, wird mithilfe der Schlüsselwerte **DefaultUserName** und **DefaultDomainName** angegeben. Das Kennwort für das Konto kann auf zwei Arten angegeben werden. Bei Computern, auf denen eines der Betriebssysteme Windows Server 2003 oder Windows XP ausgeführt wird, sollte das Kennwort mithilfe der [**LsaStorePrivateData-Funktion**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) als Geheimnis gespeichert werden. Weitere Informationen finden Sie unter [Schützen des Kennworts für die automatische Anmeldung.](protecting-the-automatic-logon-password.md) Die andere Möglichkeit zum Speichern des Kennworts ist der Klartext im **DefaultPassword-Eintrag** des Winlogon-Schlüssels. Aus Sicherheitsgründen sollte diese Technik vermieden werden. Wenn Sie das Kennwort mit der **LsaStorePrivateData-Funktion** speichern, geben Sie keinen **DefaultPassword-Eintrag** im Winlogon-Schlüssel an.

    Wenn der **AutoAdminLogon-Schlüsselwert** vorhanden ist und einen Wert enthält, und wenn der **AutoLogonCount-Schlüsselwert** vorhanden ist und nicht 0 (null) ist, bestimmt **AutoLogonCount** die Anzahl der automatischen Anmeldungen, die auftreten. Bei jedem Neustart des Systems wird der Wert von **AutoLogonCount** um eins dekrementiert, bis er 0 (null) erreicht. Wenn **AutoLogonCount** 0 (null) erreicht, wird kein Konto automatisch angemeldet, der **AutoLogonCount-Schlüsselwert** und **der DefaultPassword-Schlüsselwert** werden bei Verwendung aus der Registrierung gelöscht, und **AutoAdminLogon** wird auf 0 (null) festgelegt.

    Bei der Verwendung von **AutoAdminLogon** gibt es einen zusätzlichen Nachteil: Standardmäßig überprüft MSGina.dll den Zustand des UMSCHALTTASTENs, wenn **AutoAdminLogon** eins ist. Wenn die UMSCHALTTASTE während des Startvorgangs gedrückt gehalten wird, ignoriert MSGina.dll den Schlüsselwert **AutoAdminLogon** und fordert den Benutzer interaktiv zur Identifizierung und Authentifizierung auf. Dies ist ein nützliches Feature beim Debuggen einer dedizierten Anwendung. Um die Bedeutung der UMSCHALTTASTE zu deaktivieren, legen Sie den Schlüsselwert **IgnoreShiftOverride** auf 1 fest.

-   **Nicht authentifiziertes Herunterfahren zulassen**

    Sie können die [*GINA-Standardeinstellung*](../secgloss/g-gly.md) so konfigurieren, dass sie eine Schaltfläche **Herunterfahren** in das Anmeldedialogfeld einschließt. Dadurch können Benutzer das System herunterfahren, ohne sich zuerst anzumelden. Der folgende Schlüsselwert steuert, ob diese Schaltfläche enthalten ist.

    

    | Wert                    | BESCHREIBUNG                                           |
    |--------------------------|-------------------------------------------------------|
    | **ShutdownWithoutLogon** | Eine , die die Schaltfläche einschließen soll. 0 (null), um die Schaltfläche auszuschließen |

    

     

-   **Userinit.exe Aktivierung**

    Userinit.exe ist eine Anwendung, die von MSGina.dll ausgeführt wird, wenn sich der Benutzer angemeldet hat. Sie wird im [*Kontext*](../secgloss/c-gly.md) des neu angemeldeten Benutzers und auf dem Anwendungsdesktop ausgeführt. Der Zweck besteht darin, die Umgebung des Benutzers einzurichten, einschließlich der Wiederherstellung von Netzwerkverwendungen, dem Einrichten von Profileinstellungen wie Schriftarten und Bildschirmfarben und dem Ausführen von Anmeldeskripts. Nach Abschluss dieser Aufgaben führt Userinit.exe die Benutzershellprogramme aus. Die Shellprogramme erben die Umgebung, die Userinit.exe eingerichtet wurde. Die spezifischen Shellprogramme, die Userinit.exe ausgeführt werden, werden im **Shellschlüsselwert** unter dem Winlogon-Registrierungsschlüssel gespeichert.

    Der  Shell-Schlüsselwert kann eine durch Kommas getrennte Liste der auszuführenden Programme enthalten. Windows Der Explorer ist das Standardshellprogramm und wird ausgeführt, wenn der **Shellschlüsselwert** NULL ist oder nicht vorhanden ist. Standardmäßig ist Windows Explorer aufgeführt.

-   **Sicherheitsoptionen für angemeldete Benutzer**

    Wenn ein Benutzer bei der Anmeldung eine [*Sichere Aufmerksamkeitssequenz (Secure Attention Sequence,*](../secgloss/s-gly.md) SAS) eingibt, wird dem Benutzer ein Bildschirm mit Sicherheitsoptionen angezeigt. Zu den aufgeführten Optionen gehören:

    -   Fahren Sie das System herunter.
    -   Melden Sie sich ab.
    -   Ändern Sie das Kennwort.
    -   Wechseln Sie zur Aufgabenliste.
    -   Sperren Sie die Arbeitsstation.

    Eine Ersatz-GINA kann ähnliche Optionen bereitstellen, wenn ein SAS-Ereignis empfangen wird, während ein Benutzer angemeldet ist.

 

 
