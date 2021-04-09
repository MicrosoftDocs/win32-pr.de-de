---
description: Wenn Sie eine Gina schreiben, um die Microsoft Standard Gina DLL (MSGina.dll) zu ersetzen, können Sie einige oder alle der standardmäßigen Gina-Funktionalität bereitstellen.
ms.assetid: cd2ce7b7-6167-4451-9f6e-881676a2145c
title: MSGina.dll Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51833ab92e47dad01c13df004797e3ab3552b09a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867255"
---
# <a name="msginadll-features"></a>MSGina.dll Features

Wenn Sie eine [*Gina*](../secgloss/g-gly.md) schreiben, um die Microsoft Standard Gina DLL (MSGina.dll) zu ersetzen, können Sie einige oder alle der standardmäßigen Gina-Funktionalität bereitstellen. Im folgenden finden Sie eine Liste der Standard Features und eine kurze Beschreibung ihrer Kontrolle.

> [!Note]  
> Gina-DLLs werden in Windows Vista ignoriert.

 

Registrierungsschlüssel Werte steuern die Verfügbarkeit oder das Verhalten vieler dieser Standard-Gina-Features. Sofern nicht anders angegeben, gehören diese Schlüsselwerte zum Registrierungsschlüssel Winlogon und haben den Werttyp \[ reg \_ SZ \] . Der tatsächliche Pfad des [*Winlogon*](../secgloss/w-gly.md) -Schlüssels lautet:

**\\HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Winlogon**

-   **Dialog Feld "rechtliche Benachrichtigung"**

    An manchen Stellen ist es für alle Benutzer zulässig, die Zugriff auf eine Arbeitsstation haben, um sich anzumelden und mit der Arbeit zu beginnen, es sei denn, es gibt eine Benachrichtigung, die angibt, dass das System nur autorisierten Benutzern entspricht. Viele Benutzer wünschen sich außerdem, dass unternehmensspezifische Meldungen vor der normalen Anmeldung angezeigt werden. Der Standard Gina verwendet zwei Winlogon-Registrierungsschlüssel Werte, damit ein System vor der Anmeldung Informationen anzeigen kann. Wenn ein Schlüsselwert vorhanden ist und eine Zeichenfolge ungleich NULL enthält, wird vor der herkömmlichen Willkommensseite ein Rechtshinweis Dialogfeld angezeigt. Diese Namen der Schlüsselwerte sind in der folgenden Tabelle aufgeführt.

    

    | Schlüsselwert Name         | Inhalte                                                            |
    |------------------------|---------------------------------------------------------------------|
    | **LegalNoticeCaption** | Die Zeichenfolge, die als Beschriftung des Dialog Felds rechtliche Hinweise angezeigt werden soll. |
    | **Legalnotiz-Text**    | Die Zeichenfolge, die als Meldung des Dialog Felds rechtliche Hinweise angezeigt werden soll. |

    

     

-   **Letzten Benutzernamen anzeigen**

    Der Anmeldebildschirm zeigt standardmäßig den Namen des letzten Benutzers an, um sich erfolgreich bei der Arbeitsstation anzumelden. Diese Funktion wird durch den Registrierungsschlüssel Wert " **DontDisplayLastUserName** " gesteuert. Wenn dieser Schlüsselwert auf 1 festgelegt ist, wird der Benutzername nicht im Anmelde Dialogfeld angezeigt.

-   **Automatische Anmeldung**

    Diese Funktion ermöglicht es einem System, sich bei jedem Start des Systems automatisch anzumelden, indem Standardinformationen verwendet und das Anmeldefeld STRG + ALT + ENTF deaktiviert wird.

    Diese Funktion verwendet die folgenden Werte für den Winlogon-Schlüssel.

    

    | Wert                 | Inhalte                                           |
    |-----------------------|----------------------------------------------------|
    | **AutoAdminLogon**    | 1                                                  |
    | **AutoLogonCount**    | Gibt an, wie oft eine automatische Anmeldung durchzuführen ist.       |
    | **DefaultUserName**   | Der Name des Benutzerkontos.                       |
    | **Defaultdomain Name** | Der Name der Domäne, in der sich das Benutzerkonto befindet. |

    

     

    Wenn der **AutoAdminLogon** -Schlüsselwert vorhanden ist und einen enthält und der Wert für den **AutoLogonCount** -Schlüssel nicht vorhanden ist, wird jedes Mal eine automatische Anmeldung durchführt, wenn der aktuelle Benutzer sich abmeldet oder das System neu gestartet wird. Das Konto, bei dem die Anmeldung erfolgt, wird mit den Schlüsselwerten **DefaultUserName** und **DefaultDomainName** angegeben. Das Kennwort für das Konto kann auf zwei Arten angegeben werden. Bei Computern, auf denen eines der Windows Server 2003-oder Windows XP-Betriebssysteme ausgeführt wird, sollte das Kennwort mithilfe der [**lsastoreprivatedata**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) -Funktion als geheimer Schlüssel gespeichert werden. Weitere Informationen finden Sie unter [Schützen des Kennworts für die automatische Anmeldung](protecting-the-automatic-logon-password.md). Die andere Möglichkeit, das Kennwort zu speichern, ist im **DefaultPassword** -Eintrag des Winlogon-Schlüssels Klartext. aus Sicherheitsgründen sollte diese Technik vermieden werden. Wenn Sie das Kennwort mit der **lsastoreprivatedata** -Funktion speichern, geben Sie keinen **DefaultPassword** -Eintrag im Winlogon-Schlüssel an.

    Wenn der **AutoAdminLogon** -Schlüsselwert vorhanden ist und einen enthält und wenn der Schlüsselwert " **AutoLogonCount** " vorhanden und nicht NULL ist, bestimmt " **AutoLogonCount** " die Anzahl der auftretenden automatischen Anmeldungen. Jedes Mal, wenn das System neu gestartet wird, wird der Wert von " **AutoLogonCount** " um 1 dekrementiert, bis Null erreicht wird. Wenn die Funktion " **AutoLogonCount** " den Wert Null erreicht, wird kein Konto automatisch angemeldet, der Schlüsselwert " **AutoLogonCount** " und der **DefaultPassword** -Schlüsselwert, falls verwendet, aus der Registrierung gelöscht und " **AutoAdminLogon** " auf 0 (null) festgelegt.

    Es gibt einen zusätzlichen Nachteil bei der Verwendung von **AutoAdminLogon**: standardmäßig MSGina.dll den Status der Umschalttaste überprüft, wenn **AutoAdminLogon** eine solche ist. Wenn die UMSCHALTTASTE während des Startvorgangs gedrückt gehalten wird, ignoriert MSGina.dll den **AutoAdminLogon** -Schlüsselwert und fordert den Benutzer zur interaktiven Identifizierung und Authentifizierung auf. Dies ist ein nützliches Feature, wenn Sie eine dedizierte Anwendung debuggen. Um die Bedeutung der Umschalttaste zu deaktivieren, legen Sie den **ignoreshiftoverride** -Schlüsselwert auf 1 fest.

-   **Nicht authentifiziertes Herunterfahren zulassen**

    Sie können die Standard- [*Gina*](../secgloss/g-gly.md) so konfigurieren, dass die Schaltfläche **herunter** fahren im Anmelde Dialogfeld enthalten ist. Dadurch können Benutzer das System Herunterfahren, ohne sich zuerst anzumelden. Mit dem folgenden Schlüsselwert wird gesteuert, ob diese Schaltfläche eingeschlossen ist.

    

    | Wert                    | BESCHREIBUNG                                           |
    |--------------------------|-------------------------------------------------------|
    | **ShutdownWithoutLogon** | Eine, die die Schaltfläche einschließt. NULL, um die Schaltfläche auszuschließen. |

    

     

-   **Userinit.exe Aktivierung**

    Userinit.exe ist eine Anwendung, die von MSGina.dll ausgeführt wird, wenn sich der Benutzer angemeldet hat. Er wird im [*Kontext*](../secgloss/c-gly.md) des neu angemeldeten Benutzers und auf dem Anwendungs Desktop ausgeführt. Der Zweck besteht darin, die Umgebung des Benutzers einzurichten, einschließlich der Wiederherstellung der Netzwerk Verwendung, dem Einrichten von Profileinstellungen wie Schriftarten und Bildschirmfarben sowie der Ausführung von Anmelde Skripts. Nach Abschluss dieser Aufgaben führt Userinit.exe die benutzershellprogramme aus. Die Shellprogramme erben die Umgebung, die Userinit.exe einrichten. Die spezifischen Shellprogramme, die Userinit.exe ausgeführt werden, werden  im shellschlüsselwert unter dem Registrierungsschlüssel Winlogon gespeichert.

    Der **shellschlüsselwert** kann eine durch Trennzeichen getrennte Liste der auszuführenden Programme enthalten. Windows-Explorer ist das standardmäßige Shellprogramm und wird ausgeführt,  wenn der shellschlüsselwert NULL oder nicht vorhanden ist. Standardmäßig wird Windows-Explorer aufgelistet.

-   **Sicherheitsoptionen bei der Anmeldung**

    Wenn ein Benutzer bei der Anmeldung eine Sicherheits Ansicht ( [*Secure Attention Sequence*](../secgloss/s-gly.md) , SAS) eingibt, wird dem Benutzer ein Bildschirm mit den Sicherheitsoptionen angezeigt. Zu den aufgeführten Optionen gehören:

    -   Fahren Sie das System herunter.
    -   Melden Sie sich ab.
    -   Ändern Sie das Kennwort.
    -   Wechseln Sie zur Aufgabenliste.
    -   Sperren Sie die Arbeitsstation.

    Ein Ersatz-GINA kann ähnliche Optionen bereitstellen, wenn ein SAS-Ereignis empfangen wird, während ein Benutzer angemeldet ist.

 

 
