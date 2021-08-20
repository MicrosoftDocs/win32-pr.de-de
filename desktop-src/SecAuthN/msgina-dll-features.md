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

Wenn Sie eine [*GINA*](../secgloss/g-gly.md) schreiben, um die GINA-Standard-DLL (MSGina.dll) von Microsoft zu ersetzen, sollten Sie einige oder alle GINA-Standardfunktionen bereitstellen. Im Folgenden finden Sie eine Liste der Standardfeatures und eine kurze Beschreibung ihrer Kontrolle.

> [!Note]  
> GINA-DLLs werden in Windows Vista ignoriert.

 

Registrierungsschlüsselwerte steuern die Verfügbarkeit oder das Verhalten vieler dieser GINA-Standardfeatures. Sofern nicht anders angegeben, gehören diese Schlüsselwerte zum Registrierungsschlüssel Winlogon und haben den \[ Werttyp REG \_ SZ \] . Der tatsächliche Pfad des [*Winlogon-Schlüssels*](../secgloss/w-gly.md) ist:

**\\HKEY \_ LOCAL MACHINE Software Microsoft Windows NT \_ \\ \\ \\ \\ CurrentVersion \\ Winlogon**

-   **Dialogfeld "Rechtliche Benachrichtigung"**

    An einigen Stellen ist es für alle Personen, die Zugriff auf eine Arbeitsstation haben, erlaubt, sich zu anmelden und mit der Arbeit zu beginnen, es sei denn, es gibt eine Benachrichtigung, die angibt, dass das System nur für autorisierte Benutzer gilt. Außerdem möchten viele Benutzer, dass vor der normalen Anmeldung unternehmensspezifische Meldungen angezeigt werden. Die Standard-GINA verwendet zwei Winlogon-Registrierungsschlüsselwerte, damit ein System Informationen vor der Anmeldung anzeigen kann. Wenn einer der Schlüsselwerte vorhanden ist und eine Zeichenfolge enthält, die nicht NULL ist, wird vor dem üblichen Willkommensbildschirm ein Dialogfeld rechtlicher Hinweis angezeigt. Diese Schlüsselwertnamen sind in der folgenden Tabelle aufgeführt.

    

    | Schlüsselwertname         | Inhalte                                                            |
    |------------------------|---------------------------------------------------------------------|
    | **LegalNoticeCaption** | Die Zeichenfolge, die als Beschriftung des Dialogfelds "Rechtliche Hinweise" angezeigt werden soll. |
    | **LegalNoticeText**    | Die Zeichenfolge, die als Meldung des Dialogfelds "Rechtliche Hinweise" angezeigt werden soll. |

    

     

-   **Anzeigen des Nachbenutzernamens**

    Standardmäßig wird auf dem Anmeldebildschirm der Name des letzten Benutzers angezeigt, der sich erfolgreich bei der Arbeitsstation anmeldet. Dieses Feature wird durch den **Registrierungsschlüsselwert DontDisplayLastUserName** gesteuert. Wenn dieser Schlüsselwert auf 1 festgelegt ist, wird der Benutzername nicht im Anmeldedialogfeld angezeigt.

-   **Automatische Anmeldung**

    Dieses Feature ermöglicht es einem System, sich bei jedem Start des Systems automatisch bei einem Benutzer zu anmelden, indem es Standardinformationen verwendet und das Anmeldefeld STRG+ALT+ENTF deaktiviert.

    Dieses Feature verwendet die folgenden Werte des Winlogon-Schlüssels.

    

    | Wert                 | Inhalte                                           |
    |-----------------------|----------------------------------------------------|
    | **AutoAdminLogon**    | 1                                                  |
    | **AutoLogonCount**    | Gibt an, wie oft eine automatische Anmeldung erfolgt.       |
    | **DefaultUserName**   | Der Name des Benutzerkontos                       |
    | **DefaultDomainName** | Der Name der Domäne, in der sich das Benutzerkonto befindet. |

    

     

    Wenn der **AutoAdminLogon-Schlüsselwert** vorhanden ist und einen Schlüssel enthält und der **AutoLogonCount-Schlüsselwert** nicht vorhanden ist, erfolgt jedes Mal eine automatische Anmeldung, wenn sich der aktuelle Benutzer abmelden oder das System neu gestartet wird. Das Konto, das angemeldet wird, wird mithilfe der **Schlüsselwerte DefaultUserName** **und DefaultDomainName** angegeben. Das Kennwort für das Konto kann auf zwei Arten angegeben werden. Bei Computern, auf denen eines der Betriebssysteme Windows Server 2003 oder Windows XP ausgeführt wird, sollte das Kennwort mithilfe der [**LsaStorePrivateData-Funktion**](/windows/win32/api/ntsecapi/nf-ntsecapi-lsastoreprivatedata) als Geheimnis gespeichert werden. Weitere Informationen finden Sie unter [Schützen des Kennworts für die automatische Anmeldung.](protecting-the-automatic-logon-password.md) Die andere Möglichkeit, das Kennwort zu speichern, ist in Klartext im **DefaultPassword-Eintrag** des Winlogon-Schlüssels. Aus Sicherheitsgründen sollte diese Technik vermieden werden. Wenn Sie das Kennwort mithilfe der **LsaStorePrivateData-Funktion** speichern, geben Sie keinen **DefaultPassword-Eintrag** im Winlogon-Schlüssel an.

    Wenn der **AutoAdminLogon-Schlüsselwert** vorhanden ist und einen Schlüssel enthält, und wenn der **AutoLogonCount-Schlüsselwert** vorhanden ist und nicht 0 (null) ist, bestimmt **AutoLogonCount** die Anzahl der automatischen Anmeldungen, die auftreten. Bei jedem Neustart des Systems wird der **Wert von AutoLogonCount** um eins dekrementiert, bis er 0 (null) erreicht. Wenn **AutoLogonCount** null erreicht, wird kein Konto automatisch angemeldet, der **AutoLogonCount-Schlüsselwert** und der **DefaultPassword-Schlüsselwert,** sofern er verwendet wird, werden aus der Registrierung gelöscht, und **AutoAdminLogon** wird auf 0 (null) festgelegt.

    Es gibt einen zusätzlichen Nachteil bei der Verwendung von **AutoAdminLogon:** Standardmäßig überprüft MSGina.dll den Status der UMSCHALTTASTE, wenn **AutoAdminLogon** eins ist. Wenn die UMSCHALTTASTE während des Startvorgangs zurück gehalten wird, ignoriert MSGina.dll den **Schlüsselwert AutoAdminLogon** und fordert den Benutzer interaktiv zur Eingabe von Identifikations- und Authentifizierungsinformationen auf. Dies ist ein nützliches Feature beim Debuggen einer dedizierten Anwendung. Um die Bedeutung der UMSCHALTTASTE zu deaktivieren, legen Sie **den IgnoreShiftOverride-Schlüsselwert** auf 1 fest.

-   **Nicht authentifiziertes Herunterfahren zulassen**

    Sie können die [*Standard-GINA so*](../secgloss/g-gly.md) konfigurieren, dass eine **Schaltfläche Herunterfahren** in das Anmeldedialogfeld eingeschaltet wird. Dadurch können Benutzer das System herunterfahren, ohne sich zuerst anmelden zu müssen. Der folgende Schlüsselwert steuert, ob diese Schaltfläche enthalten ist.

    

    | Wert                    | Beschreibung                                           |
    |--------------------------|-------------------------------------------------------|
    | **ShutdownWithoutLogon** | Eine , die die Schaltfläche enthält; 0 (null), um die Schaltfläche auszuschließen |

    

     

-   **Userinit.exe Aktivierung**

    Userinit.exe ist eine Anwendung, die von einem MSGina.dll ausgeführt wird, wenn sich der Benutzer angemeldet hat. Sie wird im Kontext des neu angemeldeten [*Benutzers*](../secgloss/c-gly.md) und auf dem Anwendungsdesktop ausgeführt. Der Zweck besteht in der Einrichtung der Umgebung des Benutzers, einschließlich der Wiederherstellung von Netzwerkverwendungszwecken, dem Einrichten von Profileinstellungen wie Schriftarten und Bildschirmfarben und dem Ausführen von Anmeldeskripts. Nach Abschluss dieser Aufgaben führt Userinit.exe die Benutzershellprogramme aus. Die Shellprogramme erben die Umgebung, die Userinit.exe einrichten. Die spezifischen Shellprogramme, Userinit.exe ausgeführt werden,  werden im Shell-Schlüsselwert unter dem Registrierungsschlüssel Winlogon gespeichert.

    Der  Shell-Schlüsselwert kann eine durch Komma getrennte Liste der auszuführenden Programme enthalten. Windows Der Explorer ist das Standardshellprogramm und wird ausgeführt, wenn der Wert des **Shellschlüssels** NULL ist oder nicht vorhanden ist. Standardmäßig wird Windows-Explorer aufgeführt.

-   **Sicherheitsoptionen für angemeldete Benutzer**

    Wenn ein Benutzer bei der [](../secgloss/s-gly.md) Anmeldung in eine Sichere Aufmerksamkeitssequenz (SAS) eintritt, wird dem Benutzer ein Bildschirm mit Sicherheitsoptionen angezeigt. Unter den aufgeführten Optionen sind:

    -   Fahren Sie das System herunter.
    -   Melden Sie sich ab.
    -   Ändern Sie das Kennwort.
    -   Wechseln Sie zur Aufgabenliste.
    -   Sperren Sie die Arbeitsstation.

    Eine Ersatz-GINA kann ähnliche Optionen bereitstellen, wenn ein SAS-Ereignis empfangen wird, während ein Benutzer angemeldet ist.

 

 
