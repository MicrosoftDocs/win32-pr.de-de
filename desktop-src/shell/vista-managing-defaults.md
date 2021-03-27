---
description: In diesem Thema werden unabhängige Softwarehersteller (Independent Softwareherstellers, ISVs) mit einer kurzen Anleitung zu den erforderlichen Schritten zum Registrieren und Verwalten von Anwendungs Standardwerten in Windows Vista und höher bereitstellt. Links werden für ausführlichere Artikel zum Thema der einzelnen Abschnitte bereitgestellt.
ms.assetid: 649eb20d-07d3-4209-abff-45fc50f05631
title: Verwalten von Standardanwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de40d6c80aae4005fc015c08ef7bf2907289e795
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864895"
---
# <a name="managing-default-applications"></a>Verwalten von Standardanwendungen

Das Feature " **Programm Zugriffs-und Computer Standards festlegen** (SPAD)" wurde Windows XP und neueren Windows-Versionen hinzugefügt, um Standardeinstellungen für Computer zu verwalten. Zusätzlich zu SPAD wurde in Windows Vista das Konzept der benutzerspezifischen Standardanwendungen und des Elements " **Standardprogramme** " in der Systemsteuerung eingeführt.

> [!IMPORTANT]
> Dieses Thema gilt nicht für Windows 10. Die Art und Weise, wie standardmäßige Dateizuordnungen in Windows 10 geändert werden. Weitere Informationen finden Sie im Abschnitt zu den **Änderungen in Windows 10** für die Behandlung von Standard-apps in [diesem Beitrag](https://blogs.windows.com/bloggingwindows/2015/05/20/announcing-windows-10-insider-preview-build-10122-for-pcs/).

 

Die Standardeinstellungen pro Benutzer sind für ein einzelnes Benutzerkonto im systemspezifisch. Wenn benutzerspezifische Standardeinstellungen vorhanden sind, haben Sie Vorrang vor den entsprechenden Standardeinstellungen für dieses Konto. Ab Windows 8 ist das Erweiterbarkeits System für Dateityp-und Protokoll Standardwerte ausschließlich pro Benutzer, und Computer spezifische Standardwerte werden ignoriert. SPAD hat sich auch in Windows 8 geändert, um benutzerspezifische Standardeinstellungen festzulegen.

-   Auf Systemen, auf denen ältere Windows-Versionen als Windows 8 ausgeführt werden, erhält ein neu erstelltes Benutzerkonto Standardeinstellungen pro Computer, bis die Standardeinstellungen festgelegt sind. In Windows Vista und höher können Benutzer das Element " **Standardprogramme** " in der Systemsteuerung verwenden, um die Standardeinstellungen für Benutzer festzulegen oder zu ändern. Wenn eine Anwendung zum ersten Mal ausgeführt wird, können benutzerspezifische Standardeinstellungen mithilfe der Richtlinien festgelegt werden, die im Abschnitt [Anwendung First Run und defaults](#application-first-run-and-defaults) befolgt werden.
-   Auf Systemen, auf denen Windows 8 ausgeführt wird, werden für ein neu erstelltes Benutzerkonto von Anfang an benutzerspezifische Standardeinstellungen verwendet, und die Einstellung dieser Standardeinstellungen wird bei der ersten Ausführung wie im Abschnitt [erste Ausführung und Werte der Anwendung](#application-first-run-and-defaults) erläutert nicht mehr unterstützt.

Eine Anwendung muss sich sowohl bei SPAD als auch bei der standardmäßigen Programme registrieren, die in Windows Vista und höher als Standardprogramm angeboten werden.

In diesem Thema werden unabhängige Softwarehersteller (Independent Softwareherstellers, ISVs) mit einer kurzen Anleitung zu den erforderlichen Schritten zum Registrieren und Verwalten von Anwendungs Standardwerten in Windows Vista und höher bereitstellt. Links werden für ausführlichere Artikel zum Thema der einzelnen Abschnitte bereitgestellt.

-   [Standardprogramm Element in der Systemsteuerung](#default-programs-item-in-control-panel)
-   [Festlegen des Programm Zugriffs und der Standardeinstellungen des Computers](#set-program-access-and-computer-defaults)
    -   [Festlegen von Standardwerten in SPAD](#setting-defaults-in-spad)
    -   [Zugriff in SPAD ausblenden](#hide-access-in-spad)
-   [Registrieren für Anwendungs Einstiegspunkte](#registering-for-application-entry-points)
    -   [Öffnen mit](#open-with)
    -   [Startmenü und Schnellstartleiste](#start-menu-and-quick-launch-bar)
-   [Anwendungs Installation und Standardeinstellungen](#application-installation-and-defaults)
-   [Anwendungs Upgrades und-Standardwerte](#application-upgrades-and-defaults)
-   [Erste Testlauf der Anwendung und Standardeinstellungen](#application-first-run-and-defaults)
-   [Überprüfen der Standardwerte und Anfordern der Zustimmung des Benutzers](#verifying-defaults-and-asking-for-user-consent)
-   [Tipps zur Anwendungs Kompatibilität](#application-compatibility-tips)
    -   [Vermeiden Sie das Auslösen Per-User Virtualisierung](#avoid-triggering-per-user-virtualization)
    -   [Vermeiden von AppCompat-Warnungen oder-Blöcken aus dem Programmkompatibilitäts-Assistenten](#avoid-appcompat-warnings-or-blocks-from-the-program-compatibility-assistant)
    -   [Unterstützung für frühere Versionen des Windows-Betriebssystems](#support-for-previous-windows-operating-system-versions)
-   [Weitere Ressourcen](#additional-resources)
-   [Zugehörige Themen](#related-topics)

## <a name="default-programs-item-in-control-panel"></a>Standardprogramm Element in der Systemsteuerung

**Standardprogramme** ist eine in Windows Vista eingeführte Funktion, auf die Sie direkt über das **Startmenü** und die Systemsteuerung zugreifen können. Sie bietet eine neue Infrastruktur, die mit Standardbenutzer Berechtigungen (nicht mit erhöhten Rechten) funktioniert und so konzipiert ist, dass Benutzer und Anwendungen benutzerspezifische Standardeinstellungen verwalten können. Standardprogramme bieten Benutzern eine einheitliche und leicht zugängliche Möglichkeit zum Verwalten von Standardwerten, Dateizuordnungen und Einstellungen für die automatische Wiedergabe in allen Anwendungen auf dem System. Für-Anwendungen bietet die Verwendung des Bereichs pro Benutzer, der von den APIs für Standardprogramme bereitgestellt wird, die folgenden Vorteile:

-   **Keine Erhöhung**

    Eine Anwendung muss die Berechtigungen nicht erhöhen, um Standardwerte zu beanspruchen.

-   **Gute Bürgerschaft**

    Auf einem Computer mit mehreren Benutzern können von jedem Benutzer verschiedene Standardanwendungen ausgewählt werden.

-   **Standard Verwaltung**

    Standardprogramme-APIs bieten einen zuverlässigen und konsistenten Mechanismus zum selbst überprüfen des Standardstatus und zum Freigeben verlorener Einstellungen, ohne direkt in die Registrierung schreiben zu müssen. Ab Windows 8 empfiehlt es sich jedoch nicht, dass Anwendungen den Standardstatus Abfragen, weil eine Anwendung die Standardeinstellungen nicht mehr ändern kann – diese Änderungen können nur vom Benutzer vorgenommen werden.

Damit Ihre Anwendung die Standardwerte effektiv verwalten kann, müssen Sie die Anwendung als potenzielles Standardprogramm registrieren. Ausführliche Informationen zum Registrieren und Verwenden der APIs für Standardprogramme finden Sie unter [Standardprogramme](default-programs.md).

Standardprogramme bieten außerdem die folgenden beiden Features:

-   **Wiederverwendbare Benutzeroberfläche**

    Die Benutzeroberfläche der Programm **Standardwerte (Standardprogramme festlegen**) und Dateizuordnungen (**einem Programm einen Dateityp oder ein Protokoll zuordnen**) kann wieder verwendet und innerhalb einer Anwendung aufgerufen werden. Dies ermöglicht es Anwendungen, eine Standardbenutzer Oberfläche für die Verwaltung von Standardeinstellungen bereitzustellen und ISVs daran zu arbeiten, eine benutzerdefinierte oder gleichwertige Benutzeroberfläche zu entwickeln.

-   **Einbindung von URL-und Marketing Informationen**

    Als Teil der Seite " **Festlegen der Standardprogramme** " des Elements " **Standardprogramme** " in der Systemsteuerung kann eine Anwendung Marketinginformationen und einen Link zur Website des Anbieters bereitstellen. Diese URL wird vom Authenticode-Zertifikat abgeleitet, mit dem die Anwendung signiert wurde. Dadurch wird ein Missbrauch und ein nicht autorisierter Austausch dieses Links verhindert. Wenn eine Anwendung über ein Authenticode-Zertifikat verfügt, das eine eingebettete URL enthält, zeigt die Windows-Benutzeroberfläche diese eingebettete URL an Diese Funktion sollte von ISVs genutzt werden, um Benutzer zu Updates und anderen Downloads an Ihre Website weiterzuleiten.

## <a name="set-program-access-and-computer-defaults"></a>Festlegen des Programm Zugriffs und der Standardeinstellungen des Computers

Mithilfe von **Programm Zugriff und Computer** Standards (SPAD) festlegen können Administratoren Computer weite Standardwerte verwalten, die von allen neuen Benutzern dieses Computers geerbt werden. Vor Windows 8 ermöglichte SPAD Administratoren auch das Reparieren von Dateizuordnungen, wenn Sie beschädigt werden, wenn Programme aus dem System entfernt wurden. Ab Windows 8 wirkt sich SPAD jedoch nur auf benutzerspezifische Standardwerte aus.

Weitere Informationen zum Registrieren einer Anwendung in SPAD finden Sie unter [Arbeiten mit Set Program Access und Computer defaults (SPAD)](cpl-setprogramaccess.md) und [Registrieren von Programmen mit Client Typen](reg-middleware-apps.md). Bestimmte Änderungen und neue Empfehlungen werden in den folgenden Abschnitten erläutert.

### <a name="setting-defaults-in-spad"></a>Festlegen von Standardwerten in SPAD

Benutzerspezifische Standardeinstellungen überschreiben Computer Standardwerte.

-   **Vor Windows 8**: die Standardwerte, die in SPAD (pro Computer) festgelegt werden, werden von Benutzern nicht angezeigt, wenn entsprechende benutzerspezifische Standardeinstellungen festgelegt sind. Wenn ein Benutzer keine Standardeinstellung für Benutzer festgelegt hat, verwendet das System den entsprechenden Standard Computer. Neue Benutzerkonten auf einem Computer erben zunächst die Standardeinstellungen des Computers. Wenn ein Benutzer zum ersten Mal eine Anwendung ausführt, sollte die Anwendung den Benutzer auffordern, seine Standardeinstellungen zuzuweisen. Siehe [erste Testlauf der Anwendung und Standardeinstellungen](#application-first-run-and-defaults).
-   **Ab Windows 8**: alle Standardwerte sind pro Benutzer und jede Standardeinstellung wird ignoriert. Anwendungen können nicht mehr Standardoptionen festlegen, sodass Sie den Benutzer nicht durch die Zuweisung dieser Standardwerte durchlaufen können.

Wenn eine Anwendung vor Windows 8 in SPAD **als Standard festgelegt** ist, sollten diese Richtlinien befolgt werden:

-   Anwendungen sollten nur Standardeinstellungen auf Computer Ebene über SPAD beanspruchen.
-   Anwendungen sollten *keine* benutzerspezifischen Standardeinstellungen über SPAD beanspruchen.

Wenn eine Windows 8-Anwendung in SPAD **als Standard festgelegt** wird, müssen Sie Ihre Dateitypen und Protokolle in [Standardprogrammen](default-programs.md)registrieren, wobei Sie den gleichen Anwendungsnamen verwenden, der in SPAD verwendet wird. Dadurch kann eine Änderung in SPAD als Änderung des entsprechenden Standardprogramm Eintrags für den aktuellen Benutzer angezeigt werden.

### <a name="hide-access-in-spad"></a>Zugriff in SPAD ausblenden

Der Zugriff auf die Option "Zugriff ausblenden" für jeden möglichen Standardwert in SPAD erfolgt auf zwei Arten:

-   Wählen Sie die Kategorie standardmäßig **nicht-Microsoft** aus, wodurch der Zugriff auf alle Standardwerte von Microsoft entfällt.
-   Wählen Sie die Kategorie **Benutzer** definiert aus, und deaktivieren Sie das Kontrollkästchen **Zugriff auf dieses Programm aktivieren** .

Zuvor wurden bei einer dieser Aktionen alle Einstiegspunkte in die entsprechenden Anwendungen auf dem System entfernt. Bestimmte Richtlinien für diese Situation sind das Entfernen von Verknüpfungen und Symbolen aus den folgenden Speicherorten:

-   Desktop
-   Startmenü
-   Schnellstartleiste (nur Windows Vista und frühere Versionen)
-   Benachrichtigungsbereich
-   Kontextmenüs
-   Ordnertaskband

Lieferanten wird empfohlen, diese Richtlinien in der Rückruffunktion zum Ausblenden des Zugriffs auf die Anwendung zu implementieren.

### <a name="alternate-hide-access-method-in-spad"></a>Alternative Ausblenden der Zugriffsmethode in SPAD

Bei einigen Legacy Anwendungen ist eine vollständige Implementierung des Ausblenden des Zugriffs möglicherweise nicht praktikabel. Eine alternative Methode, die denselben Effekt erzielt, aber vom Benutzer nicht leicht umkehrbar ist, besteht darin, die Anwendung zu deinstallieren. Im folgenden finden Sie Beispiel Verhalten und Beispielcode zum Implementieren dieses.

Für diese Alternative werden folgende Benutzeroberflächen empfohlen:

-   Wenn der Benutzer das **Kontrollkästchen Zugriff auf dieses Programm aktivieren** in SPAD löscht, wird die folgende Benutzeroberfläche angezeigt.

    ![Vista (Dialogfeld) zum Ausblenden des Programm Zugriffs](images/hideaccessvista.png)

-   Wenn der Benutzer auf " **OK**" klickt, wird das Element " **Programme und Funktionen** " in der Systemsteuerung angezeigt, sodass der Benutzer die Anwendung deinstallieren kann.
-   Windows XP-Benutzern sollte das folgende Dialogfeld angezeigt werden.

    ![Dialogfeld "Windows XP" zum Ausblenden des Programm Zugriffs](images/hideaccessxp.png)

-   Wenn der Windows XP-Benutzer auf " **OK**" klickt, wird das Element "Software" **in der System** Steuerung angezeigt, sodass der Benutzer die Anwendung deinstallieren kann.

Der folgende Code stellt eine wiederverwendbare Implementierung für die Funktion "Zugriff ausblenden" bereit, wie zuvor beschrieben. Sie kann unter Windows XP, Windows Vista und Windows 7 verwendet werden.


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



## <a name="registering-for-application-entry-points"></a>Registrieren für Anwendungs Einstiegspunkte

Eine Anwendung kann über viele Einstiegspunkte innerhalb des Betriebssystems verfügen. Die folgenden Speicherorte für Einstiegspunkte werden empfohlen:

-   Desktop
-   Startmenü
-   Schnellstartleiste (nur Windows Vista und frühere Versionen)
-   Benachrichtigungsbereich
-   Kontextmenüs
-   Ordnertaskband

Dieser Abschnitt konzentriert sich auf diese speziellen Bereiche:

-   [Öffnen mit](#open-with)
-   [Startmenü und Schnellstartleiste](#start-menu-and-quick-launch-bar)

### <a name="open-with"></a>Öffnen mit

Das Kontextmenü **Öffnen mit** ermöglicht dem Benutzer das Auswählen einer Anwendung, die einen bestimmten Dateityp verarbeiten kann. Obwohl mit **Öffnen mit** eine Datei mit einer Anwendung einmalig geöffnet werden kann, kann Sie auch verwendet werden, um den Standardwert für die Dateinamenerweiterung festzulegen. Aus diesem Grund sollte sich eine Anwendung immer für **Öffnen mit** registrieren, damit Benutzer mit der Anwendung als Wahl angezeigt werden. Anwendungen können sowohl Dateitypen als auch Protokolle für **Öffnen mit** registrieren. Anwendungen, die Protokolle im Standardprogramm Framework registrieren, werden automatisch den Optionen **Öffnen mit** Optionen für Protokolle hinzugefügt.

Informationen zum Registrieren von für **Open mit** finden [Sie unter Einführung in Dateizuordnungen](fa-intro.md).

### <a name="start-menu-and-quick-launch-bar"></a>Startmenü und Schnellstartleiste

Um dem Benutzer leichter auffindbar zu sein, können Anwendungen Verknüpfungen zu verschiedenen Positionen in Windows hinzufügen. Am häufigsten wird das **Startmenü** hinzugefügt. In Windows Vista und höher erstellt eine Anwendung eine Verknüpfung im ausgeblendeten Ordner% Program Data% \\ Microsoft \\ Windows \\ -Startmenü \\ Programme, die im **Startmenü** der Liste der Programme für alle Benutzer angezeigt werden. Häufig fügt eine Anwendung einen Unterordner hinzu, der die Verknüpfung enthält.

Für Browser-und e-Mail-Programme zeigt das Windows Vista- **Startmenü** auch zwei dedizierte Links außerhalb der Programmliste mit dem kanonisch bezeichneten **Internet** und **e-Mail** an. Nachdem eine Anwendung für diese Kategorien registriert wurde, kann das Standardprogramm Framework das von diesen Links gestartete Programm verwalten.

> [!Note]  
> Die Verknüpfungen **Internet** und **E-Mail** dedizierter **Startmenü** sind ab Windows 7 nicht mehr vorhanden.

 

Um die Auffindbarkeit weiter zu erhöhen, können Anwendungen dem Desktop und der Schnellstartleiste auch Verknüpfungen hinzufügen. Anwendungen sollten den Benutzer zur Berechtigung auffordern (normalerweise während der Installation oder bei der ersten Ausführung), bevor Sie dem **Startmenü** , dem Desktop oder der Schnellstartleiste ein Symbol hinzufügen.

> [!Note]  
> Die Schnellstartleiste ist ab Windows 7 nicht mehr verfügbar. Die Alternative zu Windows 7 besteht darin, dass die Anwendung an die Taskleiste angeheftet ist, aber das Anheften kann nicht Programm gesteuert ausgeführt werden, da es sich um eine Benutzer Auswahl handelt.

 

Weitere Informationen finden Sie in den folgenden Themen:

-   [Registrieren eines Internet Browsers oder e-Mail-Clients über das Windows-Startmenü](start-menu-reg.md)
-   [Registrieren von Programmen mit Client Typen](reg-middleware-apps.md)

## <a name="application-installation-and-defaults"></a>Anwendungs Installation und Standardeinstellungen

Die Installationsverfahren für die Anwendung wurden seit Windows XP nicht grundlegend geändert. eine neue Richtlinie für Systeme, auf denen ältere Windows-Versionen als Windows 8 ausgeführt werden, ist jedoch nicht erforderlich: nehmen Sie zum Installations Zeitpunkt Computer spezifische Standardeinstellungen vor, legen Sie keine benutzerspezifischen Standardeinstellungen fest, bis der Benutzer die Anwendung zum ersten Mal ausführt. (Siehe [erste ausführen und Standardeinstellungen der Anwendung](#application-first-run-and-defaults).) Anwendungen sollten während der Installation keine benutzerspezifischen Standardeinstellungen festlegen, da es Situationen gibt, in denen die Person, die die Anwendung installiert, nicht der beabsichtigte Benutzer ist. Ab Windows 8 werden standardmäßige Standardeinstellungen nicht unterstützt, und Anwendungen können die Standardeinstellungen für Benutzer nicht ändern.

Während der Installation sollte eine Anwendung Ihre Binärdateien auf die Festplatte kopieren und ihre ProgIDs in die Registrierung schreiben. Die Anwendung sollte sich auch für Standardprogramme registrieren und mit zu diesem Zeitpunkt für jede Datei Zuordnung **geöffnet** werden, um Sie zu verarbeiten. Die Anwendung kann den Unterschlüssel **OpenWithProgIds** verwenden, um sich bei **Open with** zu registrieren.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Standardprogramme](default-programs.md)
-   [Einführung in Dateizuordnungen](fa-intro.md)

## <a name="application-upgrades-and-defaults"></a>Anwendungs Upgrades und-Standardwerte

Viele Anwendungen können sich im Laufe der Zeit selbst aktualisieren. Bei diesem Upgradeverfahren sollte der Status der benutzerspezifischen Standardeinstellungen nicht geändert werden, da diese Änderung für den Benutzer unerwartet wäre. Allerdings ist es für eine Anwendung akzeptabel, Dateizuordnungen auf Computer Ebene zu überprüfen und zu reparieren, wenn Sie beschädigt wurden.

## <a name="application-first-run-and-defaults"></a>Erste Testlauf der Anwendung und Standardeinstellungen

> [!Note]  
> Ab Windows 8 verarbeitet das System dieses Verfahren im Namen aller Anwendungen. Anwendungen selbst können keine Standardwerte mehr Abfragen und ändern. Dies ist nur für den Benutzer möglich. Daher sollten Anwendungen nicht versuchen, die aktuelle Standardeinstellung abzufragen oder diese Standardeinstellung über einen beliebigen Mechanismus zu ändern. Allerdings können Anwendungen einen Einstiegspunkt für Standardprogramme in der Systemsteuerung bereitstellen, indem Sie die [**launchadvancedassociationui**](/windows/desktop/api/Shobjidl/nf-shobjidl-iapplicationassociationregistrationui-launchadvancedassociationui) -Methode der [**iapplicationassociationregistrationui**](/windows/desktop/api/Shobjidl/nn-shobjidl-iapplicationassociationregistrationui) -Schnittstelle aufrufen.

 

Mit der Einführung von benutzerspezifischen Standardeinstellungen in Windows Vista ist es wichtig, dass Anwendungen, die für beliebte Dateinamen Erweiterungen Wettbewerben, eine gängige Benutzerfunktion zum Anfordern dieser Erweiterungen bereitstellen. Da diese Standardwerte jetzt im Kontext des Benutzers festgelegt sind, sollten Sie sich nur dann als Standard Möglichkeit vorstellen, wenn der Benutzer das Programm nach der Installation ausführt.

Die Richtlinie für die Einrichtung von benutzerspezifischen Standardeinstellungen lautet: Wenn eine Anwendung zum ersten Mal für einen bestimmten Benutzer ausgeführt wird, sollte diese Anwendung Benutzereinstellungen für Standardwerte und Dateizuordnungen für sich selbst anfordern.

Die empfohlene Benutzeroberfläche sollte zwei klare Optionen für den Benutzer bereitstellen:

1.  Akzeptieren Sie alle Standardwerte, die die Anwendung beanspruchen soll. Mit dieser Option können auch andere Standardeigenschaften der Anwendung festgelegt werden, z. b. Datenschutzeinstellungen oder Einstellungen für automatische Updates. Mit dieser Option kann die Anwendung alle registrierten Standardwerte beanspruchen.
2.  Passen Sie an, indem Sie die Standardauswahl und die Programmeinstellungen einzeln akzeptieren oder nicht akzeptieren. Diese Option stellt eine weitere Benutzeroberfläche zur Verfügung, die es dem Benutzer ermöglicht, genaue Auswahlmöglichkeiten für die Standardoptionen zu treffen.

Weitere Informationen finden Sie unter [Standardprogramme](default-programs.md).

## <a name="verifying-defaults-and-asking-for-user-consent"></a>Überprüfen der Standardwerte und Anfordern der Zustimmung des Benutzers

> [!Note]  
> Dies wird ab Windows 8 nicht unterstützt.

 

Nachdem eine Anwendung mit Standardprogrammen in Windows Vista und höher registriert wurde, stehen bestimmte APIs für die Anwendung zur Verfügung. Beispielsweise muss eine Anwendung möglicherweise überprüfen, ob es sich um das Standardprogramm handelt. Die [**iapplicationassociationregistration**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationassociationregistration) -Schnittstelle stellt hierfür Methoden bereit.

Jede Anwendung, die Standardwerte beanspruchen möchte, muss zunächst den Benutzer Abfragen und nie Standardwerte ohne Berechtigungen beanspruchen. Der Benutzer sollte gefragt werden, ob er die Anwendung als Standardwert festlegen oder die aktuelle Standardeinstellung belassen soll. Es sollte auch eine Option vorhanden sein, nach der diese Frage nicht mehr beantwortet werden muss, nachdem der Benutzer seine Wahl getroffen hat.

Weitere Informationen finden Sie unter [Standardprogramme](default-programs.md).

## <a name="application-compatibility-tips"></a>Tipps zur Anwendungs Kompatibilität

In diesem Abschnitt finden Sie einige Tipps zur Anwendungs Kompatibilität im Zusammenhang mit der Standardprogramm Darstellung in Windows.

### <a name="avoid-triggering-per-user-virtualization"></a>Vermeiden Sie das Auslösen Per-User Virtualisierung

Mit der Benutzerkontensteuerung (User Account Control, UAC) sollten Anwendungen immer nur mit Standardbenutzer Rechten ausgeführt werden, um die bestmögliche Benutzerfreundlichkeit zu erzielen. Aus Sicherheitsgründen werden Anwendungen mit einer standardmäßigen Benutzer Berechtigungsstufe blockiert, um in bestimmte Teile der Registrierung und bestimmte Systemdateien zu schreiben. Windows Vista und spätere Versionen von Windows stellen eine temporäre Anwendungskompatibilitäts-Schicht (appcompat) bereit, um Anwendungen den Übergang zu erleichtern. Blockierte Versuche zum Schreiben in die Registrierung oder Systemdateien werden "virtualisiert", sodass die Anwendung weiterhin ausgeführt wird, aber die sensiblen Bereiche des Systems nicht geändert werden. Anwendungen sollten sich jedoch nicht auf die AppCompat-Technologie als langfristige Lösung verlassen. Stattdessen sollten Anwendungen die zahlreichen verfügbaren Tools verwenden, um sicherzustellen, dass Sie erfolgreich unter den Standardbenutzer Rechten ausgeführt werden können. Hierfür ist möglicherweise eine Neuprogrammierung der Anwendung erforderlich. Dies sollte jedoch im Interesse der langfristigen Kompatibilität erfolgen.

### <a name="avoid-appcompat-warnings-or-blocks-from-the-program-compatibility-assistant"></a>Vermeiden von AppCompat-Warnungen oder-Blöcken aus dem Programmkompatibilitäts-Assistenten

Der Programmkompatibilitäts-Assistent (PCA) wird in Windows Vista und höher bereitgestellt. Der Zweck besteht darin, eine automatisierte Methode bereitzustellen, damit ältere Programme mit Kompatibilitätsproblemen besser funktionieren. Der PCA überwacht Programme auf bekannte Probleme. Wenn ein Problem erkannt wird, wird der Benutzer über das Problem benachrichtigt, und es wird angeboten, wirksame Lösungen anzuwenden, bevor der Benutzer das Programm erneut ausführt. Um zu vermeiden, dass diese Warnungen oder Blöcke angezeigt werden, sollten ISVs die zahlreichen verfügbaren Tools verwenden, um sicherzustellen, dass Ihre Anwendungen mit Windows Vista, Windows 7 und höher kompatibel sind.

### <a name="support-for-previous-windows-operating-system-versions"></a>Unterstützung für frühere Versionen des Windows-Betriebssystems

Die standardmäßige Programme-Infrastruktur ist auf Windows-Betriebssystemen vor Windows Vista nicht verfügbar. Wenn Anwendungen in die neue Standardprogramm Infrastruktur verschoben werden, sollten Sie daher Ihren älteren Standard Code für die Anwendung beibehalten, um die Kompatibilität mit älteren Versionen von Windows aufrechtzuerhalten. Eine Anwendung sollte im Rahmen der Installation eine Betriebssystem-Versions Überprüfung ausführen, um zu bestimmen, welche Anwendung-Standard Code ausgeführt werden soll.

Zur Unterstützung eines Upgrades von Windows XP auf Windows Vista oder höher sollten Anwendungen alle Registrierungseinträge hinzufügen, die für Standardprogramme erforderlich sind, auch wenn Sie auf einem Computer mit Windows XP installiert werden. Die Registrierung hat keine Auswirkung auf einen Computer, auf dem Windows XP ausgeführt wird, aber wenn der Computer später aktualisiert wird, ist die Anwendung bereits registriert und kann das Framework nutzen.

Weitere Informationen finden Sie unter [**OSVersionInfo**](/windows/win32/api/winnt/ns-winnt-osversioninfoa).

## <a name="additional-resources"></a>Weitere Ressourcen

-   [Einführung in Dateizuordnungen](fa-intro.md)
-   [Registrieren eines Internet Browsers oder e-Mail-Clients über das Windows-Startmenü](start-menu-reg.md)
-   [Registrieren einer Anwendung in einem URI-Schema](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bewährte Methoden für Dateizuordnungen](fa-best-practices.md)
</dt> <dt>

[Beispielszenario für Datei Zuordnung](fa-sample-scenarios.md)
</dt> <dt>

[Standardprogramme](default-programs.md)
</dt> <dt>

[Arbeiten mit Festlegen des Programm Zugriffs und der Computer Standardwerte (SPAD)](cpl-setprogramaccess.md)
</dt> </dl>

 

 
