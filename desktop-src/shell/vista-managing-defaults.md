---
description: Dieses Thema bietet unabhängigen Softwareherstellern (Independent Software Vendors, ISVs) eine kurze Anleitung zu den Schritten, die zum Registrieren und Verwalten von Anwendungsstandardeinstellungen in Windows Vista und höher erforderlich sind. Links zu ausführlicheren Artikeln zu den themenbezogenen Abschnitten finden Sie hier.
ms.assetid: 649eb20d-07d3-4209-abff-45fc50f05631
title: Verwalten von Standardanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc146858d197b96229edda49ac2e7249db51bf4c
ms.sourcegitcommit: 4d639170c06864e47ef66b2cfe6ca3d07cce0b02
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109812825"
---
# <a name="managing-default-applications"></a>Verwalten von Standardanwendungen

Das Feature **Programmzugriff und Computerstandardeinstellungen** festlegen (SPAD) wurde Windows XP und neueren Versionen von Windows hinzugefügt, um die Standardwerte pro Computer zu verwalten. Zusätzlich zu SPAD wurde in Windows Vista das Konzept der Standardanwendungen pro Benutzer und das Element **Standardprogramme** in Systemsteuerung eingeführt.

> [!IMPORTANT]
> Dieses Thema gilt nicht für Windows 10. Die Funktionsweise von Standarddateizuordnungen hat sich in Windows 10 geändert. Weitere Informationen finden Sie im Abschnitt Änderungen an der Verarbeitung von **Standard-Apps durch Windows 10** in [diesem Beitrag](https://blogs.windows.com/windows-insider/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

Die Standardeinstellungen pro Benutzer gelten spezifisch für ein einzelnes Benutzerkonto auf dem System. Wenn die Standardeinstellungen pro Benutzer vorhanden sind, haben sie Vorrang vor den entsprechenden Computerstandardeinstellungen für dieses Konto. Ab Windows 8 ist das Erweiterbarkeitssystem für Dateityp- und Protokollstandarddaten streng benutzer- und computerspezifische Standardwerte werden ignoriert. SPAD wurde auch in Windows 8 geändert, um Standardwerte pro Benutzer festzulegen.

-   Auf Systemen, auf denen Versionen von Windows vor Windows 8 ausgeführt werden, erhält ein neu erstelltes Benutzerkonto computerspezifische Standardwerte, bis die Standardwerte pro Benutzer eingerichtet sind. In Windows Vista und höher können Benutzer das Element **Standardprogramme** in Systemsteuerung verwenden, um ihre Standardwerte pro Benutzer festzulegen oder zu ändern. Wenn eine Anwendung zum ersten Mal ausgeführt wird, können außerdem benutzerspezifische Standardwerte gemäß den Richtlinien festgelegt werden, die im Abschnitt Erste Ausführung der [Anwendung und Standardeinstellungen](#application-first-run-and-defaults) beschrieben sind.
-   Auf Systemen, auf denen Windows 8 ausgeführt wird, basiert ein neu erstelltes Benutzerkonto von Anfang an auf Benutzerstandardeinstellungen, und die Einstellung dieser Standardwerte bei der ersten Ausführung, wie im Abschnitt [Application First Run and Defaults (Erste Ausführung der Anwendung und Standardwerte)](#application-first-run-and-defaults) erläutert, wird nicht mehr unterstützt.

Eine Anwendung muss sowohl bei SPAD als auch bei der Standardprogrammfunktion registriert werden, um als Standardprogramm in Windows Vista und höher angeboten zu werden.

In diesem Thema erhalten unabhängige Softwarehersteller (INDEPENDENT Software Vendors, ISVs) eine Kurzanleitung zu den Schritten, die zum Registrieren und Verwalten von Anwendungseinstellungen in Windows Vista und höher erforderlich sind. Es werden Links zu detaillierteren Artikeln zu den einzelnen Abschnitten bereitgestellt.

-   [Standardprogrammelement in Systemsteuerung](#default-programs-item-in-control-panel)
-   [Festlegen der Standardeinstellungen für Programmzugriff und Computer](#set-program-access-and-computer-defaults)
    -   [Festlegen von Standardwerten in SPAD](#setting-defaults-in-spad)
    -   [Ausblenden des Zugriffs in SPAD](#hide-access-in-spad)
-   [Registrieren für Anwendungseinstiegspunkte](#registering-for-application-entry-points)
    -   [Öffnen mit](#open-with)
    -   [Startmenü und Schnellstart Leiste](#start-menu-and-quick-launch-bar)
-   [Anwendungsinstallation und Standardwerte](#application-installation-and-defaults)
-   [Anwendungsupgrades und -standardwerte](#application-upgrades-and-defaults)
-   [Erste Ausführung der Anwendung und Standardwerte](#application-first-run-and-defaults)
-   [Überprüfen der Standardwerte und Er nachfragen nach Benutzereinwilligung](#verifying-defaults-and-asking-for-user-consent)
-   [Tipps zur Anwendungskompatibilität](#application-compatibility-tips)
    -   [Vermeiden des Auslösens Per-User Virtualisierung](#avoid-triggering-per-user-virtualization)
    -   [Vermeiden von AppCompat-Warnungen oder -Blöcken im Programmkompatibilitäts-Assistenten](#avoid-appcompat-warnings-or-blocks-from-the-program-compatibility-assistant)
    -   [Unterstützung für frühere Windows-Betriebssystemversionen](#support-for-previous-windows-operating-system-versions)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="default-programs-item-in-control-panel"></a>Standardprogrammelement in Systemsteuerung

**Standardprogramme ist ein** in Windows Vista eingeführtes Feature, auf das sie direkt über das **Startmenü** sowie über Systemsteuerung. Sie bietet eine neue Infrastruktur, die mit Standardbenutzerberechtigungen (nicht mit erhöhten Rechten) arbeitet und Benutzern und Anwendungen die Verwaltung von Standardeinstellungen pro Benutzer ermöglicht. Für Benutzer bietet Standardprogramme eine einheitliche und leicht zugängliche Möglichkeit, Standardeinstellungen, Dateizuordnungen und Einstellungen für die automatische Wiedergabe für alle Anwendungen im System zu verwalten. Bei Anwendungen bietet die Verwendung des benutzerbezogenen Bereichs, der von den Standardprogramm-APIs bereitgestellt wird, die folgenden Vorteile:

-   **Keine Rechteerweiterung**

    Eine Anwendung muss ihre Berechtigungen nicht erhöhen, um Standardwerte zu beanspruchen.

-   **Gute Strecht**

    Auf einem Computer mit mehreren Benutzern kann jeder Benutzer verschiedene Standardanwendungen auswählen.

-   **Standardverwaltung**

    Standardprogramm-APIs bieten einen zuverlässigen und konsistenten Mechanismus, um den Standardstatus selbst zu überprüfen und verloren gegangene Einstellungen freizulegen, ohne direkt in die Registrierung schreiben zu müssen. Ab Windows 8 wird jedoch nicht empfohlen, dass Anwendungen den Standardstatus abfragen, da eine Anwendung die Standardeinstellungen nicht mehr ändern kann. Diese Änderungen können nur vom Benutzer vorgenommen werden.

Damit Ihre Anwendung Standardeinstellungen effektiv verwalten kann, müssen Sie Ihre Anwendung als potenzielles Standardprogramm registrieren. Ausführliche Informationen zum Registrieren und Verwenden der Standardprogramm-APIs finden Sie unter [Standardprogramme.](default-programs.md)

Standardprogramme bieten auch diese beiden Features:

-   **Wiederverwendbare Standardbenutzeroberfläche**

    Die Benutzeroberfläche der Programmstandardeinstellungen **(Standardprogramme festlegen)** und Dateizuordnungen **(Einem Programm einen Dateityp oder ein Protokoll zuordnen)** können wiederverwendet und innerhalb einer Anwendung aufgerufen werden. Dadurch können Anwendungen eine Standardbenutzerfreundlichkeit für die Verwaltung von Standardwerten bereitstellen, und ISVs müssen keine benutzerdefinierte oder gleichwertige Benutzeroberfläche entwickeln.

-   **Einbeziehen von URL- und Marketinginformationen**

    Im Rahmen der Seite **Standardprogramme festlegen** des Artikels **Standardprogramme** in Systemsteuerung kann eine Anwendung Marketinginformationen und einen Link zur Website des Anbieters bereitstellen. Diese URL wird vom Authenticode-Zertifikat abgeleitet, mit dem die Anwendung signiert wurde. Dadurch wird missbraucht und nicht autorisiertes Ersetzen dieses Links verhindert. Wenn eine Anwendung über ein Authenticode-Zertifikat verfügt, das eine eingebettete URL enthält, zeigt die Windows-Benutzeroberfläche diese eingebettete URL an. ISVs sollten dieses Feature nutzen, um Benutzer für Updates und andere Downloads auf ihre Website zu leitet.

## <a name="set-program-access-and-computer-defaults"></a>Festlegen der Standardeinstellungen für Programmzugriff und Computer

**Durch Festlegen von Programmzugriff und Computereinstellungen** (SPAD) können Administratoren computerweite Standardwerte verwalten, die von allen neuen Benutzern dieses Computers geerbt werden. Vor der Windows 8 ermöglichte SPAD Administratoren auch das Reparieren von Dateizuordnungen, wenn sie beschädigt werden, wenn Programme aus dem System entfernt wurden. Ab dem Windows 8 hat SPAD jedoch nur Auswirkungen auf benutzerspezifische Standardwerte.

Weitere Informationen zum Registrieren einer Anwendung in SPAD finden Sie unter Working [with Set Program Access and Computer Defaults (SPAD) und](cpl-setprogramaccess.md) Registering [Programs with Client Types](reg-middleware-apps.md). Spezifische Änderungen und neue Empfehlungen werden in den folgenden Abschnitten erläutert.

### <a name="setting-defaults-in-spad"></a>Festlegen von Standardwerten in SPAD

Die Standardwerte pro Benutzer überschreiben die Standardwerte pro Computer.

-   **Vor Windows 8:** Die in SPAD festgelegten Standardwerte (die pro Computer gelten) werden benutzern nicht angezeigt, wenn entsprechende Standardeinstellungen pro Benutzer festgelegt sind. Wenn ein Benutzer keine Standardeinstellung pro Benutzer festgelegt hat, verwendet das System die entsprechende Standardeinstellung des Computers. Neue Benutzerkonten auf einem Computer erben anfänglich die Standardeinstellungen des Computers. Wenn ein Benutzer eine Anwendung zum ersten Mal ausgeführt, sollte die Anwendung den Benutzer auffordern, seine benutzerspezifischen Standardwerte zu zuweisen. Weitere Informationen [finden Sie unter Application First Run (Erste Ausführung der Anwendung) und Defaults (Standardwerte).](#application-first-run-and-defaults)
-   **Ab Windows 8:** Alle Standardwerte gelten pro Benutzer, und alle Standardeinstellungen pro Computer werden ignoriert. Anwendungen können keine Standardoptionen mehr festlegen, sodass sie den Benutzer nicht durch die Zuweisung dieser Standardwerte gehen können.

Wenn eine anwendung vor Windows 8 set **as default** in SPAD implementiert, sollten die folgenden Richtlinien befolgt werden:

-   Anwendungen sollten nur Standardwerte auf Computerebene über SPAD beanspruchen.
-   Anwendungen sollten *keine* Benutzerstandardeinstellungen über SPAD beanspruchen.

Wenn eine Windows 8 Anwendung **Set as Default** in SPAD implementiert, müssen sie ihre Dateitypen und Protokolle unter [Standardprogramme](default-programs.md)mit dem gleichen Anwendungsnamen registrieren, der auch in SPAD verwendet wird. Dadurch kann eine Änderung in SPAD als Änderung im entsprechenden Standardprogrammeintrag für den aktuellen Benutzer widergespiegelt werden.

### <a name="hide-access-in-spad"></a>Ausblenden des Zugriffs in SPAD

Auf die Option "Zugriff ausblenden" für jede mögliche Standardeinstellung in SPAD kann auf zwei Arten zugegriffen werden:

-   Wählen Sie die **Nicht-Microsoft-Kategorie** der Standardwerte aus, wodurch der Zugriff auf alle Microsoft-Standardwerte entfernt wird.
-   Wählen Sie die Kategorie **Benutzerdefiniert** aus, und deaktivieren Sie das Kontrollkästchen **Zugriff auf dieses Programm aktivieren.**

Zuvor wurden bei einer dieser Aktionen alle Einstiegspunkte zu den entsprechenden Anwendungen auf dem System entfernt. Spezifische Richtlinien für diese Situation lauten, Verknüpfungen und Symbole aus den folgenden Speicherorten zu entfernen:

-   Power BI Desktop
-   Startmenü
-   Schnellstart-Leiste (nur Windows Vista und früher)
-   Benachrichtigungsbereich
-   Kontextmenüs
-   Ordnertaskband

Anbietern wird empfohlen, diese Richtlinien in der Rückruffunktion Zugriff ausblenden der Anwendung zu implementieren.

### <a name="alternate-hide-access-method-in-spad"></a>Alternative Methode zum Ausblenden des Zugriffs in SPAD

Bei einigen Legacyanwendungen ist eine vollständige Implementierung von Zugriff ausblenden möglicherweise nicht praktikabel. Eine alternative Methode, die den gleichen Effekt erzielt, vom Benutzer jedoch nicht leicht rückgängig gemacht werden kann, ist die Deinstallation der Anwendung. Im Folgenden werden das Beispielverhalten und der Beispielcode für die Implementierung veranschaulicht.

Die empfohlene Benutzeroberfläche für diese Alternative sieht wie folgt aus:

-   Wenn der Benutzer das Feld **Zugriff auf dieses Programm** aktivieren in SPAD löscht, wird die folgende Benutzeroberfläche angezeigt.

    ![Vista-Dialogfeld zum Ausblenden des Zugriffs auf das Programm](images/hideaccessvista.png)

-   Wenn der Benutzer auf  **OK klickt,** wird das Element Programme und Features in Systemsteuerung angezeigt, damit der Benutzer die Anwendung deinstallieren kann.
-   Windows XP-Benutzern sollte das folgende Dialogfeld angezeigt werden.

    ![Dialogfeld "Windows XP" zum Ausblenden des Zugriffs auf das Programm](images/hideaccessxp.png)

-   Wenn der Windows XP-Benutzer  auf **OK klickt,** wird das Element Programme hinzufügen oder entfernen in Systemsteuerung angezeigt, damit der Benutzer die Anwendung deinstallieren kann.

Der folgende Code bietet eine wiederverwendbare Implementierung für das Feature Zugriff ausblenden, wie zuvor beschrieben. Sie kann unter Windows XP, Windows Vista und Windows 7 verwendet werden.


```
#include <windows.h>
#include <shlwapi.h>
#include <strsafe.h>

PCWSTR c_pszMessage1 = L"To hide access to this program, you need to uninstall it by ";
PCWSTR c_pszMessage2 = L"using\n%s in Control Panel.\n\nWould you like to start %s?";
PCWSTR c_pszApplicationName  = L"Sample App";

int _tmain(int argc, WCHAR* argv[])
{
    OSVERSIONINFO version;
    version.dwOSVersionInfoSize = sizeof(version);

    if (GetVersionEx(&version))
    {
        PCWSTR pszCPLName = NULL;

        if (version.dwMajorVersion >= 6)
        {
            // Windows Vista and later
            pszCPLName = L"Programs and Features";
        }
        else if (version.dwMajorVersion == 5 &&
                 version.dwMinorVersion == 1)
        {
            // XP
            pszCPLName = L"Add/Remove Programs";
        }

        if (pszCPLName != NULL)
        {
            WCHAR szMessage[256], szScratch[256];
            if (SUCCEEDED(StringCchPrintf(szScratch, 
                                          ARRAYSIZE(szScratch), 
                                          c_pszMessage2, 
                                          pszCPLName, 
                                          pszCPLName)))
            {
                if (SUCCEEDED(StringCchCopy(szMessage, 
                                            ARRAYSIZE(szMessage), 
                                            c_pszMessage1)))
                {
                    if (SUCCEEDED(StringCchCat(szMessage, 
                                               ARRAYSIZE(szMessage), 
                                               szScratch)))
                    {
                        if (IDOK == MessageBox(NULL, 
                                               szMessage, 
                                               c_pszApplicationName, 
                                               MB_OKCANCEL))
                        {
                            ShellExecute(NULL, 
                                         NULL, 
                                         L"appwiz.cpl", 
                                         NULL, 
                                         NULL, 
                                         SW_SHOWNORMAL);
                        }
                    }
                }
            }
        }
    }
    return 0;
}
```



## <a name="registering-for-application-entry-points"></a>Registrieren für Anwendungseinstiegspunkte

Eine Anwendung kann viele Einstiegspunkte innerhalb des Betriebssystems haben. Folgende Speicherorte werden für Einstiegspunkte empfohlen:

-   Power BI Desktop
-   Startmenü
-   Schnellstart leiste (nur Windows Vista und früher)
-   Benachrichtigungsbereich
-   Kontextmenüs
-   Ordner-Taskband

Dieser Abschnitt konzentriert sich auf diese spezifischen Bereiche:

-   [Öffnen mit](#open-with)
-   [Startmenü und Schnellstart Leiste](#start-menu-and-quick-launch-bar)

### <a name="open-with"></a>Öffnen mit

Über **das Kontextmenü** Öffnen mit kann der Benutzer eine Anwendung auswählen, die einen bestimmten Dateityp verarbeiten kann. Während **Open With** verwendet werden kann, um eine Datei mit einer Anwendung einmal zu öffnen, kann sie auch verwendet werden, um die Standardeinstellung für diese Dateierweiterung zu setzen. Daher sollte sich eine Anwendung immer für **Open With registrieren,** damit Benutzern diese Anwendung als Auswahl zur Verfügung steht. Anwendungen können sowohl Dateitypen als auch Protokolle für **Open With registrieren.** Anwendungen, die Protokolle im Standardprogrammframework registrieren, werden automatisch den **Optionen Öffnen** mit für Protokolle hinzugefügt.

Informationen zum Registrieren für **Open With finden Sie** unter Einführung in [Dateizuordnungen.](fa-intro.md)

### <a name="start-menu-and-quick-launch-bar"></a>Startmenü und Schnellstart Leiste

Um für den Benutzer leichter auffindbar zu werden, können Anwendungen Verknüpfungen zu verschiedenen Speicherorten in Windows hinzufügen. Die gängigste Stelle zum Hinzufügen einer Verknüpfung ist das **Startmenü.** In Windows Vista und höher erstellt eine Anwendung eine Verknüpfung im ausgeblendeten Ordner %ProgramData% \\ Microsoft \\ \\ Windows-Startmenüprogramme, \\ die in der Programmliste des **Startmenüs** für alle Benutzer angezeigt wird. In der Regel fügt eine Anwendung einen Unterordner hinzu, der die Verknüpfung enthält.

Für Browser- und E-Mail-Programme zeigt das Windows **Vista-Startmenü** auch zwei dedizierte Links außerhalb der Programmliste an, die kanonisch **internet-** und **E-Mail-Titel** haben. Nachdem sich eine Anwendung für diese Kategorien registriert hat, kann das Standardprogrammframework verwalten, was über diese Links gestartet wird.

> [!Note]  
> Die  **dedizierten** Internet- und **E-Mail-Startmenülinks** sind ab Windows 7 nicht mehr vorhanden.

 

Um die Auffindbarkeit weiter zu erhöhen, können Anwendungen auch Verknüpfungen zum Desktop und zur Schnellstart leiste hinzufügen. Anwendungen sollten den Benutzer um die Berechtigung bitten (in der Regel während der Installation oder bei der ersten Ausführung), bevor sie dem **Startmenü,** Desktop oder Schnellstart Leiste ein Symbol hinzufügen.

> [!Note]  
> Die Schnellstart-Leiste ist ab Windows 7 nicht mehr verfügbar. Die Alternative zu Windows 7 besteht darin, die Anwendung an die Taskleiste anzuheften, aber das Anheften kann nicht programmgesteuert erfolgen, da es sich ausschließlich um eine Benutzerauswahl handelt.

 

Weitere Informationen finden Sie in den folgenden Themen:

-   [Registrieren eines Internetbrowsers oder E-Mail-Clients mit dem Windows-Startmenü](start-menu-reg.md)
-   [Registrieren von Programmen mit Clienttypen](reg-middleware-apps.md)

## <a name="application-installation-and-defaults"></a>Anwendungsinstallation und Standardwerte

Die Prozeduren für die Anwendungsinstallation haben sich seit Windows XP nicht grundlegend geändert, mit Ausnahme einer neuen Richtlinie für Systeme, auf denen Versionen von Windows ausgeführt werden, die älter als Windows 8: Übernehmen Sie zur Installationszeit computerspezifische Standardwerte, legen Sie jedoch keine Standardwerte pro Benutzer fest, bis dieser Benutzer die Anwendung zum ersten Mal ausführt. (Siehe [Application First Run and Defaults](#application-first-run-and-defaults).) Anwendungen sollten während der Installation keine Standardwerte pro Benutzer festlegen, da es Situationen gibt, in denen die Person, die die Anwendung installiert, nicht der beabsichtigte Benutzer ist. Ab Windows 8 werden Standardeinstellungen pro Computer nicht unterstützt, und Anwendungen können die Standardeinstellungen pro Benutzer nicht ändern.

Während der Installation sollte eine Anwendung ihre Binärdateien auf die Festplatte kopieren und ihre ProgIDs in die Registrierung schreiben. Die Anwendung sollte sich zu  diesem Zeitpunkt auch für Standardprogramme registrieren und mit für jede Dateiassoz, die sie verarbeiten soll, öffnen. Die Anwendung kann den **Unterschlüssel OpenWithProgIds** verwenden, um sich bei **Open With zu registrieren.**

Weitere Informationen finden Sie in den folgenden Themen:

-   [Standardprogramme](default-programs.md)
-   [Einführung in Dateizuordnungen](fa-intro.md)

## <a name="application-upgrades-and-defaults"></a>Anwendungsupgrades und -standardwerte

Viele Anwendungen haben die Möglichkeit, sich im Laufe der Zeit selbst zu aktualisieren. Diese Upgradeprozedur sollte den Status der Standardwerte pro Benutzer nicht ändern, da diese Änderung für den Benutzer unerwartet wäre. Es ist jedoch akzeptabel, dass eine Anwendung Dateizuordnungen auf Computerebene überprüft und repariert, wenn sie beschädigt wurden.

## <a name="application-first-run-and-defaults"></a>Erste Ausführung der Anwendung und Standardwerte

> [!Note]  
> Ab Windows 8 verarbeitet das System dieses Verfahren im Namen aller Anwendungen. Anwendungen selbst können Standardwerte nicht mehr abfragen und ändern. Nur der Benutzer kann dies tun. Daher sollten Anwendungen nicht versuchen, die aktuelle Standardeinstellung abfragt oder diese Standardeinstellung über einen Mechanismus zu ändern. Anwendungen können jedoch einen Einstiegspunkt für Standardprogramme in der Systemsteuerung bereitstellen, indem sie die [**LaunchAdvancedAssociationUI-Methode**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) der [**IApplicationAssociationRegistrationUI-Schnittstelle**](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui) aufrufen.

 

Mit der Einführung von benutzerspezifischen Standardeinstellungen in Windows Vista ist es wichtig, dass Anwendungen, die für beliebte Dateierweiterungen an wettbewerben, eine gemeinsame Benutzererfahrung bieten, um diese Erweiterungen zu beanspruchen. Da diese Standardwerte jetzt im Kontext des Benutzers festgelegt sind, sollten sie sich nur dann als Standardmöglichkeit darstellen, wenn der Benutzer das Programm nach der Installation ausführt.

Die Richtlinie für die Festlegung von Benutzerstandardeinstellungen lautet: Wenn eine Anwendung zum ersten Mal für einen bestimmten Benutzer ausgeführt wird, sollte diese Anwendung Benutzereinstellungen für Standardwerte und Dateizuordnungen für sich selbst anfordern.

Die empfohlene Benutzeroberfläche sollte dem Benutzer zwei klare Optionen bieten:

1.  Übernehmen Sie alle Standardwerte, die die Anwendung beanspruchen möchte. Diese Option kann auch andere Standardeigenschaften der Anwendung festlegen, z. B. Datenschutz oder Einstellungen für automatische Updates. Mit dieser Option kann die Anwendung alle registrierten Standardwerte beanspruchen.
2.  Passen Sie an, indem Sie Standardauswahlen und Programmeinstellungen einzeln akzeptieren oder nicht akzeptieren. Diese Option stellt eine weitere Benutzeroberfläche dar, die es dem Benutzer ermöglicht, präzise Optionen für seine Standardoptionen zu treffen.

Weitere Informationen finden Sie unter [Standardprogramme.](default-programs.md)

## <a name="verifying-defaults-and-asking-for-user-consent"></a>Überprüfen von Standardwerten und Erfragen der Zustimmung des Benutzers

> [!Note]  
> Dies wird ab Windows 8 nicht unterstützt.

 

Nachdem sich eine Anwendung bei Standardprogrammen in Windows Vista und höher registriert hat, sind bestimmte APIs für die Anwendung verfügbar. Beispielsweise muss eine Anwendung möglicherweise überprüfen, ob es sich um das Standardprogramm handelt. Die [**IApplicationAssociationRegistration-Schnittstelle**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) stellt hierfür Methoden bereit.

Jede Anwendung, die Standardwerte beanspruchen möchte, muss zuerst den Benutzer fragen und niemals Standardwerte ohne Berechtigung beanspruchen. Der Benutzer sollte gefragt werden, ob er die Anwendung als Standard festlegen oder den aktuellen Standardwert belassen möchte. Es sollte auch eine Option geben, diese Frage nicht erneut zu stellen, nachdem der Benutzer seine Entscheidung getroffen hat.

Weitere Informationen finden Sie unter [Standardprogramme.](default-programs.md)

## <a name="application-compatibility-tips"></a>Tipps zur Anwendungskompatibilität

Dieser Abschnitt enthält einige Tipps zur Anwendungskompatibilität im Zusammenhang mit der Benutzeroberfläche "Standardprogramme" in Windows.

### <a name="avoid-triggering-per-user-virtualization"></a>Vermeiden des Auslösens Per-User Virtualisierung

Mit der Umgebung für die Benutzerkontensteuerung (User Account Control, UAC) sollten Anwendungen immer nur mit Standardbenutzerrechten ausgeführt werden, um eine optimale Benutzerfreundlichkeit zu gewährleisten. Aus Sicherheitsgründen werden Anwendungen mit einer Standardbenutzerberechtigungsstufe am Schreiben in bestimmte Teile der Registrierung und in bestimmte Systemdateien blockiert. Windows Vista und spätere Versionen von Windows bieten eine temporäre Anwendungskompatibilitätsebene (AppCompat), um Anwendungen beim Übergang zu unterstützen. Blockierte Schreibversuche in die Registrierung oder in Systemdateien werden "virtualisiert", sodass die Anwendung weiterhin ausgeführt wird, aber die sensiblen Bereiche des Systems nicht geändert werden. Anwendungen sollten sich jedoch nicht auf die AppCompat-Technologie als langfristige Lösung verlassen. Stattdessen sollten Anwendungen die vielen verfügbaren Tools verwenden, um zu überprüfen, ob sie unter Standardbenutzerrechten erfolgreich ausgeführt werden können. Möglicherweise ist eine Neuprogrammierung der Anwendung erforderlich, um dies zu erreichen, aber dies sollte im Interesse der langfristigen Kompatibilität erfolgen.

### <a name="avoid-appcompat-warnings-or-blocks-from-the-program-compatibility-assistant"></a>Vermeiden von AppCompat-Warnungen oder -Blöcken im Programmkompatibilitäts-Assistenten

Der Programmkompatibilitäts-Assistent (Program Compatibility Assistant, PCA) wird in Windows Vista und höher bereitgestellt. Der Zweck besteht in der Bereitstellung einer automatisierten Methode, damit ältere Programme mit Kompatibilitätsproblemen besser funktionieren. Die PCA überwacht Programme auf bekannte Probleme. Wenn ein Problem erkannt wird, wird der Benutzer über das Problem benachrichtigt, und es wird angeboten, effektive Lösungen anzuwenden, bevor der Benutzer das Programm erneut ausgeführt. Um diese Warnungen oder Blöcke zu vermeiden, sollten ISVs die vielen verfügbaren Tools verwenden, um sicherzustellen, dass ihre Anwendungen mit Windows Vista, Windows 7 und höher kompatibel sind.

### <a name="support-for-previous-windows-operating-system-versions"></a>Unterstützung für frühere Windows-Betriebssystemversionen

Die Standardprogramminfrastruktur ist unter windows-Betriebssystemen vor Windows Vista nicht verfügbar. Wenn Anwendungen auf die neue Infrastruktur der Standardprogramme umgestellt werden, sollten sie daher ihren älteren Standardcode für Anwendungen beibehalten, um die Kompatibilität mit älteren Versionen von Windows zu gewährleisten. Eine Anwendung sollte im Rahmen der Installation eine Überprüfung der Betriebssystemversion ausführen, um zu bestimmen, welcher Anwendungsstandardcode ausgeführt werden soll.

Um ein Upgrade von Windows XP auf Windows Vista oder höher zu unterstützen, sollten Anwendungen alle Registrierungseinträge hinzufügen, die für Standardprogramme erforderlich sind, auch wenn sie auf einem Computer mit Windows XP installiert werden. Die Registrierung hat keine Auswirkungen auf einen Computer unter Windows XP, aber wenn der Computer später aktualisiert wird, ist die Anwendung bereits registriert und kann das Framework nutzen.

Weitere Informationen finden Sie unter [**OSVERSIONINFO.**](/windows/win32/api/winnt/ns-winnt-osversioninfoa)

## <a name="additional-resources"></a>Weitere Ressourcen

-   [Einführung in Dateizuordnungen](fa-intro.md)
-   [Registrieren eines Internetbrowsers oder E-Mail-Clients mit dem Windows-Startmenü](start-menu-reg.md)
-   [Registrieren einer Anwendung bei einem URI-Schema](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bewährte Methoden für Dateizuordnungen](fa-best-practices.md)
</dt> <dt>

[Dateizuordnungsbeispielszenario](fa-sample-scenarios.md)
</dt> <dt>

[Standardprogramme](default-programs.md)
</dt> <dt>

[Arbeiten mit Set Program Access and Computer Defaults (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
