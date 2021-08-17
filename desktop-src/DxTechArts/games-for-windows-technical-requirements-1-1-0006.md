---
title: Technische Anforderungen für Spiele für Windows; bewährte Methoden für Spiele für Windows XP, Windows Vista, Windows 7 und Windows 8
description: Dieser Artikel enthält technische Anforderungen und bewährte Methoden für Spiele, die auf Windows ausgeführt werden.
ms.assetid: 8b816e9f-de68-cf84-1501-a9c36c6b75d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ce541a1bd8b416bdd22431b59a2ca9490f331b693fe54d45397865d9c23e3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649368"
---
# <a name="games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a>Games for Windows Technical Requirements: Best Practices for Games on Windows XP, Windows Vista, Windows 7 und Windows 8

Dieser Artikel enthält technische Anforderungen und bewährte Methoden für Spiele, die auf Windows ausgeführt werden. Wir haben diese technischen Anforderungen und bewährten Methoden in erster Linie geschrieben, um Windows Vista und Windows 7 sowie das Legacybetriebssystem Windows XP abzudecken. Diese bewährten Methoden gelten im Allgemeinen auch für Win32-Desktop-Spiele auf Windows 8.

Dieser Artikel enthält die folgenden Abschnitte:

-   [Unterschiede bei Windows 8](#differences-for-windows-8)
    -   [Weitere Informationen](#additional-information)
-   [Spiele für Windows](#games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8)
    -   [1.1 Spiele-Explorer-Integration](#11-games-explorer-integration)
    -   [1.2 Unterstützung Family Safety/Jugendschutz](/windows)
    -   [1.3 Unterstützung von rich Saved Games](#13-support-rich-saved-games)
    -   [1.4 Unterstützung des Xbox 360 Common Controller für Windows \[ bedingte Anforderungen\]](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement)
    -   [1.5 Unterstützung mehrerer Seitenverhältnisse und -auflösungen](#15-support-multiple-aspect-ratios-and-resolutions)
    -   [1.6 Supportstart über Windows Media Center](#16-support-launch-from-windows-media-center)
    -   [1.7 Direct3D-Unterstützung](#17-direct3d-support)
    -   [1.8 Aktivieren von Hoch-DPI-fähigen Daten](#18-enable-high-dpi-aware)
-   [Sicherheit und Kompatibilität](#security-and-compatibility)
    -   [2.1 Befolgen der Richtlinien für die Benutzerkontensteuerung](#21-follow-user-account-control-guidelines)
    -   [2.2 Unterstützung Windows x64-Versionen](#22-support-windows-x64-versions)
    -   [2.3 Signieren von Dateien](#23-sign-files)
    -   [2.4 Signieren von Treibern](#24-sign-drivers)
    -   [2.5 Durchführen einer ordnungsgemäßen Versionsprüfung](#25-perform-proper-version-checking)
    -   [2.6 Unterstützung gleichzeitiger Benutzersitzungen](#26-support-concurrent-user-sessions)
    -   [2.7 Unterstützung langer Namen](#27-support-long-names)
-   [Installation](#32-support-user-account-control-for-installation)
    -   [3.1 Unterstützung der einfachen Installation](#31-support-easy-installation)
    -   [3.2 Unterstützung der Benutzerkontensteuerung für die Installation](#32-support-user-account-control-for-installation)
    -   [3.3 Installation in richtigen Ordnern](#33-install-to-correct-folders)
    -   [3.4 Installieren sie Windows Ressourcen ordnungsgemäß.](#34-install-windows-resources-properly)
    -   [3.5 Vermeiden von Neustarts während der Installation](#35-avoid-reboots-during-installation)
    -   [3.6 Richtiges Verwenden der Dateiversionsierung](#36-use-file-versioning-correctly)
    -   [3.7 Unterstützung von bedingten \[ Autorun-Anforderungen\]](#37-support-autorun-conditional-requirement)
-   [Zuverlässigkeit](#reliability)
    -   [4.1 Vermeiden unnötiger Neustarts](#41-eliminate-unnecessary-reboots)
    -   [4.2 Beseitigen von Application Verifier Fehlern](#42-eliminate-application-verifier-failures)
    -   [4.3 Unterstützung Windows-Fehlerberichterstattung und Dateiversionsinformationen](#43-support-windows-error-reporting-and-file-version-information)
-   [Xbox 360 Common Controller für Windows Terminologie](#xbox-360-common-controller-for-windows-terminology)
-   [Richtlinien für Middlewareprodukte für Spiele](#guidelines-for-game-middleware-products)
    -   [Introduction (Einführung)](#introduction)
    -   [Zusätzliche Empfehlungen](#additional-recommendations)
    -   [Spiele für Windows Showcases](#games-for-windows-showcases)
-   [Ressourcen](#resources)

## <a name="differences-for-windows-8"></a>Unterschiede bei Windows 8

Hier finden Sie eine Zusammenfassung der wichtigsten Unterschiede bei der Anwendung dieser technischen Anforderungen und bewährten Methoden auf Windows 8.

<dl> <dt>

<span id="The_Games_Explorer_UI_is_not_visible"></span><span id="the_games_explorer_ui_is_not_visible"></span><span id="THE_GAMES_EXPLORER_UI_IS_NOT_VISIBLE"></span>**Die Benutzeroberfläche des Games-Explorers ist nicht sichtbar.**
</dt> <dd>

Alle Spiele, die Sie beim [Spiele-Explorer](/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)) registrieren, werden als Kacheln in der neuen Windows Benutzeroberfläche angezeigt, aber ein Großteil der Metadaten, die dem Titel zugeordnet sind, ist nicht mehr sichtbar. Sie verwenden weiterhin das Game Definition File Maker-Tool (GDFMAKER.EXE), das jetzt im Windows Software Development Kit (SDK) verfügbar ist, um die Metadaten zu erstellen. Sie verwenden auch die vorhandenen Mechanismen zum Bereitstellen der Metadaten. Testen Sie ihre Games Explorer-Registrierung weiterhin mit Windows 7, und überprüfen Sie, ob die neue Kachel "Windows UI" angezeigt wird, wenn Sie sie auf Windows 8 installieren (siehe Integration von [1.1 Games Explorer](#11-games-explorer-integration)).

Informationen zum Herunterladen des Windows 8 SDK finden Sie unter Downloads für die [Entwicklung von Desktop-Apps.](https://msdn.microsoft.com/windows/desktop/aa904949)

</dd> <dt>

<span id="Registration_with_the_Game_Explorer_APIs_continues_to_be_the_mechanism_for_registering_your_game_with_Windows_Parental_Controls"></span><span id="registration_with_the_game_explorer_apis_continues_to_be_the_mechanism_for_registering_your_game_with_windows_parental_controls"></span><span id="REGISTRATION_WITH_THE_GAME_EXPLORER_APIS_CONTINUES_TO_BE_THE_MECHANISM_FOR_REGISTERING_YOUR_GAME_WITH_WINDOWS_PARENTAL_CONTROLS"></span>**Die Registrierung bei den Game Explorer-APIs ist weiterhin der Mechanismus zum Registrieren Ihres Spiels bei Windows Jugendschutz.**
</dt> <dd>

Es wird empfohlen, die Windows SDK-Version von GDFMAKER auf der veröffentlichten Version von Windows 8 auszuführen, um sicherzustellen, dass alle derzeit unterstützten Bewertungssysteme aufgefüllt werden können.

> [!Note]  
> Diese Version von GDFMAKER erfordert .NET 4.0.

 

Siehe [1.2 Unterstützung Family Safety/Jugendschutz.](/windows)

</dd> <dt>

<span id="There_are_now_three_choices_for_using_the_XINPUT_API_depending_on_your_requirements"></span><span id="there_are_now_three_choices_for_using_the_xinput_api_depending_on_your_requirements"></span><span id="THERE_ARE_NOW_THREE_CHOICES_FOR_USING_THE_XINPUT_API_DEPENDING_ON_YOUR_REQUIREMENTS"></span>**Es gibt jetzt drei Optionen für die Verwendung der XINPUT-API, je nach Ihren Anforderungen.**
</dt> <dd>

XINPUT 1.4 ist in Windows 8 integriert. Sowohl Windows Store- als auch Desktop-Win32-Apps können XINPUT 1.4 verwenden. Alle Versionen von Windows können XINPUT 9.1.0 für vereinfachte allgemeine Controller verwenden, aber es gibt kein Weiterverteilungspaket mit XINPUT 9.1.0. Alle Versionen von Windows können auch die vorhandene DirectX SDK-Version XINPUT 1.3 verwenden, für die DirectSetup bereitgestellt werden muss.

Weitere Informationen finden Sie unter [Unterstützung des Xbox 360 Common Controller für Windows](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement).

</dd> <dt>

<span id="Only_a_limited_set_of_desktop_Win32_apps_are_supported_on_"></span><span id="only_a_limited_set_of_desktop_win32_apps_are_supported_on_"></span><span id="ONLY_A_LIMITED_SET_OF_DESKTOP_WIN32_APPS_ARE_SUPPORTED_ON_"></span>**Nur eine begrenzte Gruppe von Win32-Desktop-Apps wird auf Windows RT**
</dt> <dd>

Spiele, die auf Windows 7 ausgeführt werden, können und sollten auf Windows 8 x86- und x64-Plattformen ordnungsgemäß ausgeführt werden.

Weitere Informationen finden Sie [unter Unterstützung Windows x64-Versionen.](#22-support-windows-x64-versions)

</dd> <dt>

<span id="Ensure_any_OS_checks_are_done_correctly"></span><span id="ensure_any_os_checks_are_done_correctly"></span><span id="ENSURE_ANY_OS_CHECKS_ARE_DONE_CORRECTLY"></span>**Sicherstellen, dass alle Betriebssystemüberprüfungen ordnungsgemäß durchgeführt werden**
</dt> <dd>

Die Windows 8 Betriebssystemversion ist 6.2. Windows 8 bestehen die aktuellen Mindestleistentests, die wir für die Spielebereitstellung empfehlen.

</dd> <dt>

<span id="The__DirectX_End-User_Redistribution__package_runs_successfully_on_Windows_8__as_it_does_on_Windows_7__to_deploy_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTEngine__and_so_on"></span><span id="the__directx_end-user_redistribution__package_runs_successfully_on_windows_8__as_it_does_on_windows_7__to_deploy_d3dx9__d3dx10__d3dx11__xinput_1.3__xaudio_2.7__xactengine__and_so_on"></span><span id="THE__DIRECTX_END-USER_REDISTRIBUTION__PACKAGE_RUNS_SUCCESSFULLY_ON_WINDOWS_8__AS_IT_DOES_ON_WINDOWS_7__TO_DEPLOY_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTENGINE__AND_SO_ON"></span>**Das DirectX End-User Redistribution-Paket wird wie auf Windows 7 erfolgreich auf Windows 8 ausgeführt, um D3DX9, D3DX10, D3DX11, XINPUT 1.3, XAUDIO 2.7, XACTEngine usw. bereitzustellen.**
</dt> <dd>

Aufgrund der Bereitstellungsbehandlung der älteren Verwalteten DirectX 1.1-Assemblys tritt jedoch ein bekanntes Problem mit DirectSetup auf Systemen auf, auf dem nur .NET 4.0 installiert ist. Dieses Problem gilt sowohl für Windows 8,die standardmäßig in .NET 4.5 enthalten sind, als auch für neue Windows XP-Computer, auf denen die .NET 4.0-Runtime installiert ist. Dieses Problem gilt jedoch nicht für .NET-Versionen vor .NET 4.0. Obwohl Windows 8 über ein Anwendungskompatibilitätsverhalten verfügt, um dieses Problem automatisch zu beheben (was Netzwerkzugriff erfordert), empfehlen wir, dass Spiele, die directSetup update weiterhin für die aktualisierte Version der REDIST-Dateien des DirectX SDK (Juni 2010) bereitstellen. Wenn Sie DirectSetup als Titel verwenden, kürzen Sie Ihren Titel wie immer auf die mindestens erforderliche Gruppe von CABs.

Weitere Informationen finden Sie unter [3.4 Installieren sie Windows Ressourcen ordnungsgemäß.](#34-install-windows-resources-properly)

</dd> <dt>

<span id="Games_that_require_the_.NET__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="games_that_require_the_.net__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="GAMES_THAT_REQUIRE_THE_.NET__2.0__COMPATIBLE_RUNTIME__2.0__3.0__3.5__CONTINUE_TO_USE_EXISTING_DEPLOYMENT_MECHANISMS"></span>**Spiele, für die die .NET 2.0-kompatible Runtime (2.0, 3.0, 3.5) erforderlich ist, verwenden weiterhin vorhandene Bereitstellungsmechanismen.**
</dt> <dd>

Diese Spiele lösen ein Anwendungskompatibilitätsverhalten auf Windows 8 aus, um die .NET 3.5-Runtime automatisch zu aktivieren (was Netzwerkzugriff erfordert). Es wird jedoch empfohlen, dass .NET-Entwickler zur .NET 4.0-Runtime wechseln.

> [!Note]  
> Die Legacyassemblys von Managed DirectX 1.1 sind nicht mit der .NET 4.x-Runtime kompatibel.

 

Weitere Informationen finden Sie unter [3.4 Installieren sie Windows Ressourcen ordnungsgemäß.](#34-install-windows-resources-properly)

</dd> <dt>

<span id="Use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.NET_is_not_recommended"></span><span id="use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.net_is_not_recommended"></span><span id="USE_OF_AN__AUTORUNNER__OR_OTHER_PRE-INSTALL_TECHNOLOGY_THAT_RELIES_ON_.NET_IS_NOT_RECOMMENDED"></span>**Die Verwendung eines Autorunners oder einer anderen vorinstallierten Technologie, die auf .NET basiert, wird nicht empfohlen.**
</dt> <dd>

Sie können davon ausgehen, dass nur .NET 2.0-kompatible Runtimes (2.0, 3.0, 3.5) auf Windows Vista und Windows 7 vorhanden sind. Standardmäßig ist nur die .NET 4.0-kompatible Runtime auf Windows 8 vorhanden.

Siehe [3.7 Support Autorun](#37-support-autorun-conditional-requirement).

</dd> <dt>

<span id="There_is_an_updated_Application_Verifier_for_Windows_8"></span><span id="there_is_an_updated_application_verifier_for_windows_8"></span><span id="THERE_IS_AN_UPDATED_APPLICATION_VERIFIER_FOR_WINDOWS_8"></span>**Es gibt eine aktualisierte Application Verifier für Windows 8**
</dt> <dd>

Das Windows 8 SDK enthält diese aktualisierte Application Verifier.

Weitere Informationen finden Sie unter [4.2 Beseitigen Application Verifier Fehler.](#42-eliminate-application-verifier-failures)

</dd> </dl>

### <a name="additional-information"></a>Zusätzliche Informationen

<dl>

[Windows 8- und Windows Server 2012-Kompatibilitäts-Cookbook](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal)  
[Wo finde ich das DirectX SDK?](/windows/desktop/directx-sdk--august-2009-)  
</dl>

## <a name="games-for-windows"></a>Spiele für Windows

**Zusammenfassung der Spieleanforderungen**

**Kundenvorteile**

Computerspiele sind eine wichtige Unterhaltungserfahrung auf Windows, aber Bedenken hinsichtlich der Benutzerfreundlichkeit haben im Laufe der Jahre zu Kundenverärkung geführt. Traditionell werden Spiele wie Anwendungen installiert, aber sie werden eher wie Unterhaltungsmedien (Filme oder Titel, z.B. ) verwendet. Innovationen, z. B. Games Explorer, machen Spiele auf konsistente Weise verfügbar, die sich von Standardanwendungen unterscheidet. Diese Innovationen geben spielen auch in Windows einen erstklassigen Bürgerstatus, zusammen mit Musik und Bildern. Die folgenden Anforderungen stellen sicher, dass Windows Vista und Windows 7 eine verbesserte, zugänglichere und einheitliche Spielerfahrung bieten. Gleichzeitig stellen sie die Kompatibilität mit Windows XP sicher.

### <a name="11-games-explorer-integration"></a>1.1 Spiele-Explorer-Integration

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Das Spiel muss im Spiele-Explorer (ordner **Games)** auf Windows Vista und Windows 7 angezeigt werden. Wenn diese Option ausgewählt ist, muss das Spiel auch die richtigen Metadaten anzeigen, einschließlich Herausgeber, Entwickler, Veröffentlichungsdatum, Version, Windows Experience Index-Bewertungen, Bewertung (falls zutreffend) und zugeordneter Links.

Wenn das Spiel digital über einen Onlinespieldienst verteilt wird, sollte der Dienstanbieter auch im Spiele-Explorer angezeigt werden. Um eine ordnungsgemäße Behandlung des Anbieters sicherzustellen und die Verwendung von RSS-Feeds zu ermöglichen, sollte Version 2 des Schemas für Spieldefinitionsdateien (GDFs) verwendet werden. (Weitere Informationen zu GDFs finden Sie unter Zusätzliche Informationen.)

Darüber hinaus müssen Spieleinstaller die folgenden Regeln beachten, wenn sie auf Windows Vista und Windows 7 ausgeführt werden:

-   Die Installation darf keine Verknüpfung erstellen, um das Spiel auf dem Desktop, im Startmenü oder an einem anderen Ort zu starten.
-   Tasks und Verknüpfungen zum Entfernen dürfen nicht erstellt werden.
-   Benutzer müssen in der Lage sein, das Spiel mithilfe von Programmen und Features in Systemsteuerung unter Windows Vista und Windows 7 oder mit dem Hinzufügen oder Entfernen von Programmen in Systemsteuerung auf Windows XP zu entfernen.

Auf Windows XP und in früheren Versionen von Windows kann der Spieleinstaller programmgruppen, Desktopsymbole oder Tastenkombinationen nach Bedarf erstellen.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Windows Der Spiele-Explorer ähnelt dem Konzept Windows **XP-Ordnern Eigene Dokumente** **oder Meine Bilder.** Die Idee ist, ähnliche Inhalte an einem Ort zu zentralisieren und eine einfachere Organisation und kontextorientierte Aktivitäten zu ermöglichen. Der Spiele-Explorer erweitert **das** Eigene Dokumente- oder **My Pictures-Konzept,** indem er eine vielfältigere Organisation und Kontrolle über Spiele ermöglicht. Der Spiele-Explorer ermöglicht Es Gamern, alle auf ihren Systemen installierten Spiele zu sehen, zu organisieren und mit ihnen zu interagieren. Außerdem können Spieleherausgeber wichtige Spielinformationen effektiver kommunizieren. Das System ist datengesteuert und macht es für einen Spieleherausgeber einfach, Spielinformationen über die Lebensdauer des Produkts zu aktualisieren.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Die Integration in den Spiele-Explorer erfordert, dass Sie eine Spieldefinitionsdatei (GDF) erstellen, bei der es sich um eine XML-Textdatei handelt, die in eine Binärdatei (eine ausführbare Datei oder eine DLL) als Ressource eingebettet ist, zusammen mit einem Windows-Symbol. Das Spiel muss dann beim Spiele-Explorer registriert werden. Mit der GDF können auch bereitgestellte Informationen wie Spieltitel, Herausgeber, Entwickler, Links zu Websites und optionale Aufgaben zur Verfügung gestellt werden. Beachten Sie, dass Supportaufgaben nur Links zu Websites sein können, wiedergabeaufgaben jedoch auch für optionale Supportaufgaben verwendet werden können.

Der Spiele-Explorer kann ein Miniaturbild einer Bitmap verwenden, es wird jedoch empfohlen, stattdessen eine Ressource Windows Symbol mit großen Symbolen (256 256) zur Verfügung zu stellen. Die Symbolressource sollte Bildgrößen von 256 256 48 48, 32 32 und 16 16 in 24-Bit-Farbtiefe (True Color) und 8-Bit-Farbtiefe (256) enthalten. Der symbol-Editor, der in Visual Studio 2008 und 2010 bereitgestellt wurde, unterstützt diese großen Symbolformate ebenso wie IconWorkshop Lite.

Details zur Integration in Windows **Games Explorer** finden Sie im DirectX SDK. Das DirectX SDK enthält einen GDF-Editor (Game Definition File) sowie ein GDF-Beispiel, das in GDFExampleBinary enthalten ist, ein Beispiel. Ein weiteres Beispiel, GameUxInstallHelper, enthält Routinen zum Integrieren der erforderlichen Funktionalität in vorhandene Installationssysteme. Das Game Definition File Validator (gdftrace.exe) bietet Debugunterstützung für die Auswertung einer GDF. Weitere Informationen finden Sie Windows Integration des Games Explorers in der DirectX SDK-Dokumentation für C++.

Windows 7 bietet Unterstützung für die zweite Version eines Schemas für GDF-Dateien. Die neue Version enthält eine vereinfachte Methode zum Erstellen von Spielaufgaben und Unterstützung für Updatebenachrichtigungen, Spieldienstanbieter, Spielstatistiken und RSS-Feeds für Spieldienstanbieter. Die neueste Version von GameUxInstallHelper übernimmt alle Registrierungs- und Legacyunterstützungen, die für die Verwendung einer GDF-Datei der Version 2 mit Windows Vista erforderlich sind. Verwenden Sie die Tools und den Beispielcode aus dem DirectX SDK vom August 2009 oder höher. Die Verwendung einer GDF-Datei der Version 2 wird empfohlen, um die Unterstützung für RSS-Feeds, Spielstatistiken und Updatebenachrichtigungen zu aktivieren. Sehen Sie sich auch die Beispiele ProviderGDFExampleBinary und GameStatisticsExample an.

In Windows Vista Business Edition, Windows 7 Professional Edition und Enterprise Edition von Windows Vista und Windows 7 ist der Link Spiele auf dem Startmenü ausgeblendet. Der Spiele-Explorer ist weiterhin im Startmenü, indem Sie auf **Alle Programme** und dann auf **Spiele klicken.**

Für zugehörige Anwendungen, die mit Ihrem Spiel installiert werden, aber nicht selbst Spiele, können Sie Startmenü-Programmgruppen, Verknüpfungen und Desktopsymbole in allen Versionen von Windows erstellen, einschließlich Windows Vista und Windows 7. Solche zugeordneten Anwendungen sollten entsprechende Spiele für Windows erfüllen. Weitere Informationen finden Sie unter [Richtlinien für Spiele-Middlewareprodukte.](#guidelines-for-game-middleware-products) Spieldienste sollten sich beim Spiele-Explorer als Game Provider für Windows 7 registrieren. 1

</dd> </dl>

### <a name="12-support-family-safety--parental-controls"></a>1.2 Unterstützung Family Safety/Jugendschutz

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Spiele müssen die Windows Family Safety vollständig unterstützen, indem sie die folgenden Regeln einhalten:

-   Spiele dürfen nicht erfordern, dass der Benutzer über Administratoranmeldeinformationen zum Spielen verfügen muss. Für installation, patching und removal können Administratoranmeldeinformationen erforderlich sein, die den Anforderungen in Abschnitt 3 entsprechen. (Im Zusammenhang mit dieser Ist-Anforderung 2.1: Befolgen Sie die Richtlinien für die Benutzerkontensteuerung.)
-   Spiele, die Windows von Bewertungsboards wie ESRB und PEGI bewertet werden, müssen ihre zugewiesenen Bewertungsinformationen in ihrer Spieldefinitionsdatei (GDF) enthalten. Alle verfügbaren Bewertungsdaten müssen in jeder lokalisierten Version der GDF sowie in der sprachneutralen Version enthalten sein.
-   Spiele müssen ihre ausführbaren Dateien in der GDF auflisten, um eine gute Benutzererfahrung für allgemeine Anwendungseinschränkungen zu bieten, es sei denn, das Spiel verwendet eine Anti-Technology, die zufällig benannte ausführbare Dateien zur Laufzeit erstellt.
-   Spiele müssen die **VerifyAccess-Methode** der Games Explorer-Schnittstelle beim Start aufrufen (falls verfügbar) und beenden, wenn \* pfHasAccess als FALSE zurückgegeben wird.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Alle Spiele müssen im Kontext eines Standardbenutzerkontos ausgeführt werden, damit Konten, die von der Windows Jugendschutz gesteuert werden, das Spiel spielen können. Eltern möchten die Möglichkeit haben, den Zugriff ihrer Kinder auf Spiele zu überwachen und zu steuern. Darüber hinaus wünschen sich zahlreiche Branchen-, Behörden- und Interessensgruppen bessere Möglichkeiten, Eltern die Überwachung und Kontrolle der Spiele zu ermöglichen, denen ihre Kinder ausgesetzt sind. In Verbindung mit der Architektur, die von Games Explorer angeboten wird, bietet Microsoft Eltern diese Möglichkeit über Windows Jugendschutz.

Selbst für Spiele, die nicht an einem Ratings Board-Programm teilnehmen, führt das Erfordern von erhöhten Rechten für die meisten Benutzerkonten zu einer schlechten Spielerfahrung. Dies ist insbesondere der Fall, wenn die Jugendschutz-Steuerung aktiviert ist. Dies würde erfordern, dass das übergeordnete Element das Administratorkennwort jedes Mal einzugeben, wenn das Spiel gestartet wird.

Das Windows Jugendschutzsystem ermöglicht es Eltern, die Bewertungen auszuwählen, die ihrer Meinung nach für ihre Kinder geeignet sind. Die Jugendschutzkontrollen unterstützen viele der weltweiten Bewertungssysteme. Außerdem können Eltern den Zugriff auf Spiele basierend auf Inhaltsdeskriptoren einschränken (sofern sie vom entsprechenden Bewertungssystem unterstützt werden) und den Zugriff auf einzelne Spiele zulassen oder verhindern.

Die Standardauswahl des Bewertungssystems für Windows-Jugendschutz basiert auf der Einstellung des System-Locale, kann jedoch vom Benutzer **unter** Regionale optionen und Sprachoptionen **in** Systemsteuerung. Aus diesem Grund sollte jede unterstützte Sprache alle verfügbaren Bewertungsdaten bereitstellen, damit der Benutzer das gewünschte Bewertungsboard auswählen kann.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Spiele ohne Bewertung müssen weiterhin die Anforderungen erfüllen, um die Wiedergabe als Standardbenutzer zu unterstützen und **VerifyAccess aufzurufen.** Solche Spiele verwenden standardmäßig die Kategorie Nicht bewertet, zeigen im Spiele-Explorer den  Text "No Rating Provided" (Keine Bewertung bereitgestellt) an und unterliegen der Einstellung Spieleinschränkungen in **Der** Jugendschutz für nicht bewertete Spiele. Die **Standardeinstellung Einschränkungen** ist Zulassen.

Bewertungsinformationen in der GDF werden ignoriert, wenn die enthaltende Binärdatei nicht ordnungsgemäß mit Authenticode signiert ist. Siehe Anforderung 2.3.

Der Datei-Editor für Spieldefinitionen im DirectX SDK enthält alle unterstützten Bewertungssysteme und repliziert diese Informationen ordnungsgemäß in alle lokalisierten Versionen der GDF sowie in eine sprachneutrale Version. Das GDFTrace-Tool decodiert und überprüft alle vorliegenden Bewertungsinformationen. Verwenden Sie die Version vom August 2009 oder höher dieser Tools.

Die GDF für einen Spieleanbieter enthält in der Regel keine Bewertungsinformationen und unterliegt den Einstellungen für nicht bewertete Inhalte.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Betriebssystem</th>
<th>Unterstützte Bewertungssysteme</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows Vista</td>
<td><ul>
<li>CERO (Japan)</li>
<li>ESRB (USA)</li>
<li>OFLC (Australien)</li>
<li>PEGI (Europa)</li>
<li>PEGI-Demo (veraltet)</li>
<li>PEGI Portugal</li>
<li>PEGI/BBFC (Vereinigtes Königreich)</li>
<li>USK (Deutschland)</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows Vista mit einem Service Pack</td>
<td>Service Packs für Windows Vista bieten Unterstützung für Folgendes:<br/>
<ul>
<li>GRB (Südkorea)</li>
<li>&quot; &quot; Esrb-Variant-Inhaltsdeskriptoren</li>
</ul></td>
</tr>
<tr class="odd">
<td>Windows 7</td>
<td>Windows 7 unterstützt die von Windows Vista unterstützten Bewertungssysteme und fügt Unterstützung für Folgendes hinzu: <br/>
<ul>
<li>CSRR (Taiwan)</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows 8</td>
<td>Windows 8 unterstützt die vorherigen Bewertungssysteme und fügt Unterstützung für Folgendes hinzu:<br/>
<ul>
<li>COB-AU (Australien)</li>
<li>DJCTQ (Brasilien)</li>
<li>PFB (Südafrika)</li>
<li>OFLC-NZ (Neuseeland)</li>
</ul>
Windows 8 die Unterstützung für die folgenden veralteten Systeme wird nicht mehr unterstützt:<br/>
<ul>
<li>PEGI-FI (Schweiz)</li>
<li>OFLC (Australien)</li>
</ul></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Alle Titel, die neue ESRB Windows Vista Service Pack 1 (SP1)-Inhaltsdeskriptoren enthalten, werden auf Windows Vista ohne Service Pack als Nicht berücksichtigt angezeigt.

 

Neuere Bewertungsdaten werden in Betriebssystemversionen ignoriert, ohne dass sie unterstützt werden. Die PEGI-Variante (Schweiz) ist jetzt zugunsten des PEGI-Standardbewertungssystems (Europa) veraltet. Das OFLC-System ist jetzt zugunsten von COB-AU für Australien veraltet.

Weitere Informationen zur Kompatibilität eines Spiels mit Standardbenutzerberechtigungen finden Sie im DirectX-Artikel [Benutzerkontensteuerung für Spieleentwickler.](/windows/desktop/DxTechArts/user-account-control-for-game-developers)

Weitere Informationen zur Spieldefinitionsdatei (GDF) finden Sie unter Anforderung 1.1.

</dd> </dl>

### <a name="13-support-rich-saved-games"></a>1.3 Unterstützung von rich Saved Games

\[Diese Anforderung wurde eingestellt.\]

### <a name="14-support-the-xbox-360-common-controller-for-windows-conditional-requirement"></a>1.4 Unterstützung des Xbox 360 Common Controller für Windows \[ bedingte Anforderungen\]

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Spiele, die Gamepadcontroller unterstützen, müssen die Xbox 360 Controller für Windows mithilfe der [XInput-API](/windows/desktop/xinput/xinput-game-controller-apis-portal) unterstützen. Wenn DirectInput-Peripheriegeräte ebenfalls unterstützt werden, kann auch DirectInput verwendet werden. XInput muss jedoch die Standard-API sein, wenn ein Xbox 360 kompatibles Gerät verwendet wird.

Alle Verweise auf allgemeine Controllertrigger und Schaltflächen müssen die Xbox 360 Namen verwenden. Weitere Informationen finden Sie in der Liste [Xbox 360 Common Controller for Windows Terminologie.](#xbox-360-common-controller-for-windows-terminology)

Controllervibration muss ausgeschaltet werden, wenn sich das Spiel in einem angehaltenen oder angehaltenen Zustand befindet.

Maus-/Tastatursteuerelement kann jederzeit nicht vollständig deaktiviert werden. Mindestens eine Option zum Kehren zu Spielmenüs muss verfügbar sein.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Diese Anforderung gibt Gamern die Möglichkeit, entweder den Xbox 360 Controller oder die Tastatur und Maus zu verwenden, je nachdem, welche Eingabemethode natürlicher und intuitiver ist.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Diese Anforderung gilt nicht für Spiele, die nur die Maus und/oder die Tastatur verwenden.

Es wird empfohlen, die Menünavigation zu implementieren, um die allgemein akzeptierten Standard-Controllerschaltflächen zu verwenden:

-   A – Akzeptieren
-   B – Abbrechen
-   Start : Akzeptieren oder anhalten
-   Zurück : Abbrechen, einen Bildschirm oder eine Menüebene wieder öffnen

Weitere Informationen finden Sie unter [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal).

Im Thema [XInput und DirectInput](/windows/desktop/xinput/xinput-and-directinput) werden Probleme mit der gleichzeitigen Verwendung beider APIs erläutert.

Es wird empfohlen, DirectInput nicht zum Implementieren von Tastatur- oder Maussteuerelementen zu verwenden. Tastatur- und Maussteuerelemente sollten nur mit Windows Nachrichten und Win32-APIs implementiert werden. Ausführliche Informationen zum Abrufen von Informationen zu hoch aufgelösten Mausbewegungen ohne Verwendung von DirectInput finden Sie unter [Nutzen High-Definition Mausbewegung.](/windows/desktop/DxTechArts/taking-advantage-of-high-dpi-mouse-movement)

</dd> </dl>

### <a name="15-support-multiple-aspect-ratios-and-resolutions"></a>1.5 Unterstützung mehrerer Seitenverhältnisse und -auflösungen

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Das Spiel muss mindestens die folgenden Seitenverhältnisse und die zugehörigen Bildschirmauflösungen unterstützen:

-   Normal 4:3 (800 600 oder 1024 768)
-   16:9 Widescreen (1280 720)
-   16:10 Widescreen (1152 720 oder 1680 1050 oder 800 480)

Für die Konfiguration und Erkennung der Bildschirmauflösung muss das Spiel die folgenden Regeln einhalten:

-   Das Spiel verwendet standardmäßig die Desktopauflösung des Anzeigegeräts, wenn es sich um eine unterstützte Auflösung handelt. Das Desktopaspektverhältnis muss als Suchkriterium verwendet werden, wenn das Spiel eine andere Standardauflösung wählt.
-   Das Spiel muss den Benutzer auffordern, neue Anzeigeeinstellungen zu bestätigen, wenn eine Änderung vorgenommen wird. Wenn der Benutzer nicht innerhalb von 15 Sekunden akzeptiert, muss die Anzeige auf die vorherige Einstellung zurückgesetzt werden.
-   Das Spiel darf keine Pixel gestreckt oder ein 4:3-Renderfenster zentriert werden, um Breitbild-Seitenverhältnisse zu unterstützen. Letterboxing ist jedoch akzeptabel.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Beim Windows 3D-Desktop kann aufgrund der folgenden Faktoren nicht von einem bestimmten Seitenverhältnis oder einer bestimmten Auflösung ausgegangen werden:

-   Unterstützung für Detailanzeigen.
-   Erhöhter Marktanteil von Widescreenmonitoren.
-   CAB-Bereitstellungen für Windows Media Center.
-   Barrierefreiheitsanforderungen.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Im Idealfall verwendet das Spiel standardmäßig das native Seitenverhältnis der Anzeige. Das zuverlässige Abrufen dieser Informationen kann jedoch eine Herausforderung sein, sodass das Spiel als allgemeinere Lösung davon ausgehen kann, dass der Desktop mit dem nativen Seitenverhältnis ausgeführt wird. Die Desktopauflösung kann durch Aufrufen von [**EnumDisplaySettings**](/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa) mit ENUM REGISTRY SETTINGS abgerufen \_ \_ werden.

Weitere Informationen finden Sie in den Abschnitten Seitenverhältnis und Widescreen des [DirectX-Artikels Introduction to the 10-Foot Experience for Windows Game Developers](/windows/desktop/DxTechArts/introduction-to-the-10-foot-experience-for-windows-game-developers).

</dd> </dl>

### <a name="16-support-launch-from-windows-media-center"></a>1.6 Supportstart über Windows Media Center

\[Diese Anforderung wurde eingestellt.\]

### <a name="17-direct3d-support"></a>1.7 Direct3D-Unterstützung

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Wenn das Spiel Direct3D verwendet, muss die unterstützte Mindestversion Direct3D 9 und Direct3D der ausgewählte Standardrenderer sein.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Die Grafikarchitektur Windows Vista und Windows 7 Kerne ist auf Direct3D ausgelegt. Direct3D 8 und frühere Versionen werden durch die Neuzuordnung von Legacyschnittstellen unterstützt.

Die Verwendung neuerer Direct3D-Versionen als Direct3D 9 wird dringend empfohlen. Weitere Informationen finden Sie unter Spiele für Windows Showcase S.1. Direct3D 10 oder Direct3D 11 ist vollständig konform mit Anforderung 1.7.

</dd> </dl>

### <a name="18-enable-high-dpi-aware"></a>1.8 Aktivieren von Hoch-DPI-fähigen Daten

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Spiele und deren Installationsprogramme müssen ohne visuelle Probleme ordnungsgemäß ausgeführt werden, wenn die Skalierung mit Punkten pro Zoll (DPI) auf Windows Vista und Windows 7 aktiviert ist (getestet mit 144 DPI für eine Skalierung von 150 % bei einer Anzeigeauflösung von 1600 1200).

Dies erfordert in der Regel, dass die ausführbare Spieldatei als DPI-fähig deklariert wird. Dies wird erreicht, indem ein Manifestelement eingebettet wird: <dpiAware> true <dpiAware> .

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Hochwertige LCM-Monitore werden häufig als Computeranzeigen verwendet und sehen am besten aus, wenn sie mit ihren nativen Auflösungen gesteuert werden (in der Regel 1280 1024, 1600 1200 usw.). Kunden, die Probleme beim Lesen von Text und beim Anzeigen von Bildern mit dieser Auflösung haben, legen ihre Computerdesktops häufig auf eine niedrigere Auflösung fest und erleiden visuelle Artefakte durch DIE SKALIERUNG. Stattdessen können Kunden die Auflösung in der nativen Größe belassen und den DPI der Windows Anzeigen ändern, wodurch die Darstellung von Element und Text ohne Einbußen bei der Imagequalität vergrößert wird.

Obwohl dieses Feature seit Windows XP in irgendeiner Form verfügbar ist, wird es selten von Kunden oder OEMs aktiviert. Mehr als die Hälfte aller Computeranzeigen ist heute basierend auf Kundenfeedback auf eine niedrigere Auflösung als die native Auflösung des Monitors festgelegt. Windows 7 macht dieses Feature für Kunden während der ersten Einrichtung und beim Ändern der Anzeigeeinstellungen deutlich sichtbarer, wodurch sie dazu aufgefordert werden, die DPI-Skalierung zu verwenden, anstatt die Desktopauflösung zu ändern.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Die [**SetProcessDPIAware-Funktion**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) kann stattdessen verwendet werden, wenn sie früh im Prozessstartcode aufgerufen wird. Das Hinzufügen zum Manifest wird bevorzugt, um sicherzustellen, dass keine Racebedingungen mit Softwareelementen (z. B. DLLs) vorhanden sind, die vor dem Aufruf des Haupteinstiegspunkts initialisiert werden können. Beachten Sie, dass **SetProcessDPIAware** nur auf Windows Vista und Windows 7 vorhanden ist.

Das Hinzufügen des Manifestelements ist mit Visual Studio 2005 und 2008 einfach. Erstellen Sie eine Datei namens dpiaware.manifest, die den folgenden Text enthält:

``` syntax
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
            <asmv3:application>
            <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
            <dpiAware>true</dpiAware>
            </asmv3:windowsSettings>
            </asmv3:application>
            </assembly>
```

Fügen Sie dann in Visual Studio dem Projekt dpiware.manifest hinzu. Stellen Sie sicher, dass **das Einbettungsmanifest** in den Projekteigenschaften auf **Ja** festgelegt ist. Beachten Sie, dass ältere Versionen des Manifesttools (Mt.exe) eine falsche Warnung mit den DPI-fähigen Manifestelementen generieren. Um dies zu beheben, aktualisieren Sie Mt.exe auf die neueste Version aus dem Windows SDK.

Visual Studio 2010 enthält eine Einstellung in den Projekteigenschaften mit dem Namen **Enable DPI Awareness (DPI-Awareness aktivieren),** die die Notwendigkeit einer Datei wie dpiaware.manifest entfällt. Suchen **Sie Enable DPI Awareness** ,indem Sie **Konfigurationseigenschaften** und **Manifesttool** erweitern, und wählen Sie dann **Eingabe & Ausgabe** aus.

Auf Windows ist der herkömmliche Anzeigemodus standardmäßig auf 96 DPI eingestellt, was bei CRT-Monitoren üblich war.

Während Vollbildanwendungen die Anzeigeauflösung ändern, verwenden sie beim Einrichten von Puffern und Anzeigerechtecke häufig Fenstermeldungen und Metriken. Die DPI-Virtualisierung bewirkt, dass diese Vollbildanzeigemodi zugeschnitten erscheinen, und das Deklarieren von DPI-fähigen Daten verhindert diese Probleme. Weitere Informationen finden Sie unter [Schreiben DPI-Aware Win32-Anwendungen.](../hidpi/high-dpi-desktop-application-development-on-windows.md)

</dd> </dl>

## <a name="security-and-compatibility"></a>Sicherheit und Kompatibilität

**Zusammenfassung der Sicherheits- und Kompatibilitätsanforderungen**

**Kundenvorteile**

Die folgenden Anforderungen verbessern die allgemeine Sicherheit von Spielen und stellen sicher, dass sie mit Windows in verschiedenen Architekturen, unter verschiedenen Konfigurationen und in verschiedenen Modi arbeiten.

### <a name="21-follow-user-account-control-guidelines"></a>2.1 Befolgen der Richtlinien für die Benutzerkontensteuerung

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Jede ausführbare Datei (also jede Datei mit der Erweiterung .exe) muss ein eingebettetes Manifest enthalten, das die Ausführungsebene definiert, indem das folgende Tag eingeschlossen wird:

``` syntax
            <requestedExecutionLevel>
```

Gemäß Anforderung 1.2 müssen das Hauptspiel und die ausführbare Datei Autorun über die Ausführungsebene asInvoker verfügen, um Standardbenutzerkontexte zu unterstützen.

Benutzerdatendateien, für die Dateizuordnungen im **Datei-Explorer** registriert sind, müssen in einem Unterordner des Ordners platziert werden, der von CSIDL PERSONAL angegeben wird \_ (auch als **Dokumente** oder **Eigene Dokumente** bezeichnet). Alle anderen Benutzerdatendateien müssen in einem Unterordner der Ordner gespeichert werden, die von CSIDL \_ LOCAL \_ APPDATA oder CSIDL COMMON APPDATA angegeben \_ \_ werden. (Diese Verzeichnisse sind standardmäßig für einzelne Benutzer und für alle Benutzer ausgeblendet.)

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Die Windows eines Benutzers ist sicherer, wenn Anwendungen nur mit den erforderlichen Berechtigungen ausgeführt werden.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Wenn nur wenige Funktionen in einer Anwendung Administratorrechte erfordern (z. B. eine Anwendung, die eine Firewall konfigurieren muss), muss der Hauptprozess der Anwendung weiterhin mithilfe von Standardbenutzerberechtigungen ausgeführt werden. Features, die Administratorrechte erfordern, müssen in einen separaten Prozess verschoben werden, z. B. ein Installationsprogramm oder ein Konfigurationshilfsprogramm.

Wenn keine Administratorrechte erforderlich sind, sollte die eingebettete Manifest-XML Folgendes enthalten:

``` syntax
            <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
            <ms_asmv2:trustInfo xmlns:ms_asmv2="urn:schemas-microsoft-com:asm.v2">
            <ms_asmv2:security>
            <ms_asmv2:requestedPrivileges>
            <ms_asmv2:requestedExecutionLevel level="asInvoker" uiAccess="false" />
            </ms_asmv2:requestedPrivileges>
            </ms_asmv2:security>
            </ms_asmv2:trustInfo>
            </assembly>
```

Wenn Administratorrechte erforderlich sind, sollte die eingebettete Manifest-XML Folgendes enthalten:

``` syntax
            <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
            <ms_asmv2:trustInfo xmlns:ms_asmv2="urn:schemas-microsoft-com:asm.v2">
            <ms_asmv2:security>
            <ms_asmv2:requestedPrivileges>
            <ms_asmv2:requestedExecutionLevel level="requireAdministrator" uiAccess="false" />
            </ms_asmv2:requestedPrivileges>
            </ms_asmv2:security>
            </ms_asmv2:trustInfo>
            </assembly>
```

Mit Visual Studio 2005 lässt sich dies leicht einbetten, indem Sie einfach eine Manifestdatei (.manifest) hinzufügen, die einen der vorangehenden Blöcke zum Projekt enthält, und sicherstellen, dass Manifest **einbetten** in den Projekteigenschaften für Manifesttool auf **Ja** festgelegt ist. Für Visual Studio 2008 und 2010 können UAC-Eigenschaften direkt in den Projekteigenschaften für den Linker auf der Seite **Manifestdatei** festgelegt werden. Beachten Sie, dass ältere Versionen des Manifesttools (Mt.exe) eine falsche Warnung mit den UAC-Manifestelementen generieren. Um dies zu beheben, aktualisieren Sie Mt.exe auf die neueste Version aus dem Windows SDK.

Ausführliche Informationen zu den Speziellen Fällen der Installation, des Patchens und des Entfernens finden Sie unter Anforderung 3.1.

Dynamic Link Libraries (DLLs) erfordern solche Manifeste nicht.

Weitere Informationen zur Benutzerkontensteuerung finden Sie unter [Benutzerkontensteuerung für Spieleentwickler.](/windows/desktop/DxTechArts/user-account-control-for-game-developers)

</dd> </dl>

### <a name="22-support-windows-x64-versions"></a>2.2 Unterstützung Windows x64-Versionen

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Um die Kompatibilität mit 64-Bit-Editionen von Windows zu gewährleisten, sollten Spiele die folgenden Anforderungen erfüllen.

-   Titel und Titelinstallationsprogramme dürfen keinen 16-Bit-Code enthalten und dürfen keine 16-Bit-Komponente verwenden.
-   Wenn das Spiel für den Betrieb von Kernelmodustreibern abhängig ist, müssen x64-Versionen dieser Treiber verfügbar sein. Das Spielsetup muss die richtigen Treiber und Komponenten für die 64-Bit-Editionen von Windows erkennen und installieren.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Viele Windows Vista- und Windows 7-Benutzer werden während der Lebensdauer des Produkts 64-Bit-Editionen des Betriebssystems ausführen. Daher ist es entscheidend, dass Anwendungen mit diesem Betriebssystem kompatibel sind.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Windows auf Windows 64 (WOW64) ermöglicht die Ausführung von 32-Bit-Code in 64-Bit-Editionen von Windows. Daher ist es nicht erforderlich, dass die Anwendung nativer 64-Bit-Code in 64-Bit-Editionen von Windows ist. 16-Bit-Code wird nicht in 64-Bit-Editionen von Windows ausgeführt.

Die Aufrechterhaltung der Kompatibilität mit Windows XP Professional x64 Edition ist nicht erforderlich, wird jedoch dringend empfohlen.

Weitere Informationen finden Sie unter [64-Bit-Programmierung für Spieleentwickler.](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers)

</dd> </dl>

### <a name="23-sign-files"></a>2.3 Signieren von Dateien

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Alle ausführbaren Codedateien (in der Regel Dateien mit der Erweiterung .exe oder .dll) müssen mit einem öffentlich gültigen Authenticode-Zertifikat signiert werden und über eine gültige Zeitstempelserver-URL für die Produktionssignatur verfügen.

Wenn Ihr Spiel Windows Installer verwendet, müssen die Installationspaketdateien (.msi Dateien) signiert werden.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Das Signieren einer Datei hilft Benutzern bei der Entscheidung, ob sie einer Anwendung vertrauen möchten, und stellt sicher, dass Dateien nicht manipuliert wurden. Außerdem können Anwendungen ordnungsgemäß in gesperrten Umgebungen ausgeführt werden.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Weitere Informationen finden Sie unter [Authenticode Signing for Game Developers](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

Wenn Ihr Spiel Windows Installer verwendet, empfiehlt es sich, UAC-/LUA-Patchen zu aktivieren, indem Sie eine MsiPatchCertificate-Tabelle einschließen. Weitere Informationen finden Sie unter [Benutzerkontensteuerung (User Account Control, UAC) Patching](/windows/desktop/Msi/user-account-control--uac--patching).

Es wird nicht empfohlen, Cab-Dateien (.cab) zu signieren, es sei denn, sie sind relativ klein (weniger als 100 MB).

</dd> </dl>

### <a name="24-sign-drivers"></a>2.4 Signieren von Treibern

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Alle Kernelmodustreiber, die vom Spiel installiert werden, müssen mit einem öffentlich gültigen Authenticode-Zertifikat signiert werden.

Jeder Hardwaregerätetreiber im Kernelmodus, der vom Spiel installiert wird, muss über eine Microsoft-Signatur verfügen, die über die Windows Hardware Quality Labs (WHQL) oder das Programm Driver Reliability Signature (DRS) abgerufen werden kann.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Schlecht geschriebene Treiber oder Schadsoftwaretreiber können die Stabilität und Sicherheit eines Systems erheblich beeinträchtigen. Bei 64-Bit-Editionen von Windows Vista und Windows 7 werden nicht signierte Treiber nicht geladen. Diese Richtlinie kann auch für 32-Bit-Editionen von Windows Vista und Windows 7 aktiviert werden.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Sowohl native 32-Bit- als auch 64-Bit-Versionen aller Kernelmodustreiber werden gemäß Anforderung 2.2 benötigt.

Weitere Informationen zu Microsoft-Treibersignaturprogrammen finden Sie im [Windows Hardwareentwicklerportal.](https://www.microsoft.com/whdc/winlogo/hwrequirements.mspx)

</dd> </dl>

### <a name="25-perform-proper-version-checking"></a>2.5 Durchführen einer ordnungsgemäßen Versionsprüfung

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Spiele dürfen nicht unter zukünftigen Betriebssystemen ausgeführt werden, wie durch Änderungen in der Windows Versionsnummer angegeben, es sei denn, der Endbenutzer-Lizenzvertrag untersagt die Verwendung auf zukünftigen Betriebssystemen. Wenn das Spiel fehlschlagen soll, muss es ordnungsgemäß erfolgen, indem dem Benutzer eine entsprechende Meldung angezeigt wird.

Wenn Windows Versionsprüfungen durchgeführt werden, müssen die VERSIONSÜBERPRÜFUNG-APIs ([**GetVersionEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa) oder [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa)) verwendet werden, um die Betriebssystemversion zu überprüfen. Registrierungsschlüssel dürfen nicht gelesen werden, um die Version zu bestimmen.

Explizite Versionsüberprüfungen für die DirectX-Runtime dürfen im Spiel nicht vorhanden sein. Diese Versionsüberprüfungen dürfen nicht in der Installation vorhanden sein, die das DirectX-Runtime-Setup (DirectSetup) startet.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Wenn Windows Benutzer ihr Betriebssystem aktualisieren, sollten sie nicht daran gehindert werden, aktuelle Spiele zu spielen, weil die Windows Versionsnummer erhöht wurde. Schlecht geschriebene Versionsüberprüfungen verursachen weiterhin Probleme bei Software, die andernfalls bei neueren Versionen von Windows oder einfach mit dem Hinzufügen eines Windows Service Packs funktioniert.

Die Vergleichslogik für die Überprüfung der fehlerhaften Version für die DirectX-Runtime hat zahlreiche fehlerhafte Installationen erstellt, wenn sie auf verschiedenen Versionen von Windows ausgeführt wird. Die DirectX-Versionsnummer gilt nur für die Kernkomponenten des Betriebssystems. Sie gilt nicht für die direkten DirectX SDK-Komponenten, die von vielen Spielen verwendet werden.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Es ist üblich, dass Installationsprogramme nach einer Mindestversion des Betriebssystems suchen. Diese Überprüfung muss jedoch mit Vorsicht durchgeführt werden, um sicherzustellen, dass sie auf mehr als oder gleich und nicht auf einfache Gleichheit überprüft, wodurch eine bestimmte Version des Betriebssystems gesperrt wird. Der **HighVersionLie-Test** von Application Verifier ist eine schnelle und einfache Möglichkeit, um zu bestimmen, wie Ihr Installationsprogramm auf eine erhebliche Änderung der Betriebssystemversionsnummer reagiert.

Die ordnungsgemäße Verwendung des DirectX-Laufzeitverteilungspakets (DirectX-Setup) umfasst immer den Start während der Installation, vorzugsweise im unbeaufsichtigten Modus. Dadurch kann der von Microsoft bereitgestellte Code alle erforderlichen Versionsupdates ausführen. Sie ermöglicht auch die Installation beliebiger optionaler direkter DirectX SDK-Komponenten wie D3DX, XACT, MDX oder XInput.

Bewährte Methoden für die Bereitstellung der DirectX-Runtime finden Sie unter [DirectX-Installation für Spieleentwickler.](/windows/desktop/DxTechArts/directx-setup-for-game-developers)

Es wird empfohlen, spiele, die Windows XP-Überprüfung für ein Service Pack-Level von 2 oder höher unterstützen, da Service Pack 2 (SP2) und Service Pack 3 (SP3) erhebliche Sicherheitsverbesserungen, eine vereinfachte DirectX Runtime Redistribution-Anforderung und eine äußerst umfassende Bereitstellung bieten. Die meisten modernen Microsoft-Technologien, die Windows XP unterstützen, erfordern SP2 oder SP3 (XAudio2, Games for Windows – LIVE usw.).

</dd> </dl>

### <a name="26-support-concurrent-user-sessions"></a>2.6 Unterstützung gleichzeitiger Benutzersitzungen

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Spiele, die auf 3D-Grafiken basieren, müssen nicht über eine Remotedesktopverbindung funktionieren, aber der Benutzer muss benachrichtigt werden, wenn das Spiel fehlschlägt.

Spiele müssen standardmäßige Windows Multitaskingszenarien unterstützen, indem sie die folgenden Regeln einhalten:

-   Spiele dürfen die Verwendung gleichzeitiger Benutzersitzungen nicht blockieren.
-   Ein Spiel muss in einer neuen Benutzersitzung ausgeführt werden, wenn es bereits in einer anderen Sitzung ausgeführt wird.
-   Spielsound in einer Benutzersitzung darf nicht gehört werden, wenn ein anderer Benutzer in einer anderen Sitzung aktiv ist.
-   Spiele müssen schnelle Benutzerwechsel unterstützen.
-   Spiele dürfen nicht versuchen, den Standardtaskwechsel zu deaktivieren. Spiele dürfen die Tastenkombination ALT+TAB nicht deaktivieren. Spiele dürfen Tastenkombinationen für die Barrierefreiheit deaktivieren, wie unter [Deaktivieren von Tastenkombinationen in Spielen](/windows/desktop/DxTechArts/disabling-shortcut-keys-in-games)beschrieben.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Windows Benutzer sollten in der Lage sein, gleichzeitige Sitzungen ohne Konflikte oder Unterbrechungen auszuführen. Dies ist ein häufiges Szenario für einen Windows Computer, der von einer Familie, Mitmenschen oder anderen gemeinsam genutzt wird.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Um zu testen, ob das Spiel in einer Remotesitzung gestartet wird, rufen [**Sie GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)(SM \_ REMOTESESSION) auf. Ein Wert ungleich 0 (null) gibt an, dass es sich bei der Sitzung um eine Remotesitzung handelt.

Weitere Informationen finden Sie unter [Schneller Benutzerwechsel.](/windows-hardware/drivers/display/fast-user-switching) Beachten Sie, dass ein schneller Benutzerwechsel erfolgt, wenn die Zeiteinschränkungen für die Jugendschutz-Steuerung aktiviert sind, wenn die Zeit des Benutzers aktiv ist. Weitere Informationen finden Sie unter Anforderung 1.2.

</dd> </dl>

### <a name="27-support-long-names"></a>2.7 Unterstützung langer Namen

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Wenn ein Spiel das Speichern von Dateien unterstützt, muss es Dateien mit langen Namen und Pfaden speichern können. Das Spiel muss spezielle Dateisystemzeichen wie \\ / : ? ordnungsgemäß verarbeiten. \* " < > in allen Benutzereingabefeldern, die zum Erstellen von Dateinamen oder Pfaden verwendet werden.

Spiele müssen ordnungsgemäß funktionieren, wenn ein Benutzer über einen langen Benutzernamen verfügt.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Player sind es gewohnt, lange Namen auf tiefen Pfaden zu verwenden, die vom zugrunde liegenden Betriebssystem unterstützt werden.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Lange Namen werden als namendefiniert, die die im Windows SDK definierten Höchstwerte enthalten.

</dd> </dl>

## <a name="installation"></a>Installation

**Zusammenfassung der Sicherheits- und Kompatibilitätsanforderungen**

**Kundenvorteile**

Kunden können sicher sein, dass Anwendungen auf Windows installiert werden, ohne das Betriebssystem oder andere Anwendungen zu beeinträchtigen, wenn Anwendungen offizielle Verteilungsmethoden für Systemkomponenten verwenden. Eine optimierte Installationserfahrung bietet eine einfachere und problemlosere Out-of-Box-Erfahrung für Spiele.

### <a name="31-support-easy-installation"></a>3.1 Unterstützung der einfachen Installation

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Spiele müssen einen vereinfachten Pfad in der Setup-Benutzeroberfläche bereitstellen, indem Folgendes implementiert wird:

-   Zeigt maximal eine EULA-Eingabeaufforderung an.
-   Der Standardinstallationspfad muss alle Auswahlmöglichkeiten für die Installation umgehen (z. B. Die Auswahl des Installationsordners oder der Komponente), die Standardauswahl übernehmen und das Spiel oder das Startelement nach erfolgreicher Installation ohne zusätzliche Eingabeaufforderungen ausführen. Bei Bedarf kann eine benutzerdefinierte Installationsoption für erweiterte Konfigurationsoptionen bereitgestellt werden.
-   Installieren Sie alle erforderlichen Betriebssystemkomponenten (z. B. directX- und Visual C-Runtimes) mit den richtigen Microsoft-Weiterverteilungspaketen. Die Installation sollte im Hintergrund, ohne Aufforderung und ohne Schutz durch Komponentenversionsprüfungen ausgeführt werden.
-   Stellen Sie das Entfernen über **Programme und Features** in **Systemsteuerung** sowohl für die Spielanwendung als auch für generierte Arbeitsdateien bereit. Eine Option zum Löschen von Datendateien, die vom Benutzer erstellt werden, wird empfohlen. Der Entfernungsprozess muss sicherstellen, dass alle installierten Dateien entfernt und alle Einstellungen (z. B. Einträge in der Firewallausnahmeliste und Registrierungsschlüssel) gelöscht werden. Neu verteilte Betriebssystemkomponenten dürfen nicht entfernt werden.
-   Wenn für das Spiel Ausnahmen zur Windows Firewall hinzugefügt werden müssen, kann der Setupprozess Benutzer darüber informieren, dass diese Änderung erforderlich ist. Diese Aufforderung sollte angezeigt werden, bevor die Installation beginnt.

Installation und Entfernung können Administratorrechte erfordern. Für das Patchen kann abhängig von der Aktualisierungshäufigkeit eine Aufforderung zur Eingabe von Administratoranmeldeinformationen erforderlich sein. Das normale Spiel darf keine Administratorrechte erfordern, gemäß Anforderung 2.1. Befolgen Sie die Richtlinien für die Benutzerkontensteuerung.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Die einfache Installation ist eine Windows-zentrierte Spielentwicklungs-Philosophie, die den manchmal mühsamen und verwirrenden Prozess der Installation von Spielen auf Computern vereinfacht und optimiert, auf denen Windows Betriebssystemen ausgeführt wird. Die einfache Installation wird durch die Verwendung einer Reihe von Technologien und bewährten Methoden ermöglicht, die die unnötige Komplexität und das wahrgenommene Risiko der Installation von Spielen auf Windows Computern reduzieren.

Die wichtigsten Ziele sind:

-   Verkürzen Sie die Zeit, um in das Spiel zu gelangen und mit dem Spielen zu beginnen.
-   Reduzieren Sie die Anzahl von Dialogfeldern und Auswahlmöglichkeiten auf sehr wenige oder gar keine, um die Spielinstallation zu vereinfachen.

Einige herkömmliche Installationen verfügen über Eingabeaufforderungen, die nicht funktionale Installationen zulassen, obwohl die Anwendung scheinbar erfolgreich installiert wurde. Beispielsweise kann ein Spiel erfordern, dass ein Benutzer eine Lizenzvereinbarung akzeptiert. Das Spiel wird dann installiert, und dann wird die Lizenzbedingungen für DirectX angezeigt. Durch diese Lizenzbedingungen können Benutzer die Installation der DirectX-Runtime ablehnen und überspringen. Dieses Szenario kann zu einem Spiel führen, das aufgrund fehlender Komponenten nicht ausgeführt werden kann.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Weitere Informationen zur Spieleinstallation, zu nicht herkömmlichen Spielinstallationstechniken, zu UAC-kompatiblen Patchlösungen und zur Behandlung häufiger Patches finden Sie in den folgenden DirectX-Artikeln:

-   [Vereinfachen der Spieleinstallation](/windows/desktop/DxTechArts/simplifying-game-installation)
-   [Install-on-Demand für Spiele](/windows/desktop/DxTechArts/install-on-demand-for-games)
-   [Patchen von Spielesoftware in Windows XP, Windows Vista und Windows 7](/windows/desktop/DxTechArts/patching-methods-in-windows-xp-and-vista)
-   [Bewährte Methoden für die Installation von Massively Multiplayer Online Games](/windows/desktop/DxTechArts/mmo-installation-best-practices)

> [!Note]  
> Das Entfernen benutzerspezifischer generierter Datendateien sollte nur für den aktuellen Benutzer und für gemeinsame freigegebene Benutzerspeicherorte ausgeführt werden. Es gibt keine stabile Möglichkeit, das System zu überprüfen, um benutzerspezifische Dateien für andere Benutzer zu entfernen, auch wenn die Entfernung Administratoranmeldeinformationen erfordert.

 

</dd> </dl>

### <a name="32-support-user-account-control-for-installation"></a>3.2 Unterstützung der Benutzerkontensteuerung für die Installation

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Das Spielinstallationsprogramm darf nicht davon ausgehen, dass es im selben Kontext wie der Benutzer ausgeführt wird. Benutzerspezifische Speicherorte unterscheiden sich aufgrund der Erhöhung der Administratoranmeldeinformationen auch bei Einzelbenutzersystemen vom Installationsprogramm und Player. Wenn ein Spiel zum ersten Mal ausgeführt wird, muss es daher benutzerspezifische Aufgaben separat vom Installationsvorgang ausführen.

Das Dialogfeld Windows Firewallausnahme darf nicht angezeigt werden, wenn ein Benutzer ein Multiplayer-Spiel hostet oder beitritt. Alle erforderlichen Konfigurationen müssen zur Installationszeit erfolgen. Die Setupanweisungen sollten den Benutzer darüber informieren, dass dieser Vorgang im Rahmen des Setups ausgeführt wird.

Der Spieleinstaller muss ein eingebettetes Manifest bereitstellen, das die erforderliche Ausführungsebene gemäß Anforderung 2.1 gemäß den Richtlinien für die Benutzerkontensteuerung angibt.

Wenn das Spiel nach Abschluss der Installation vom Installationsprogramm gestartet wird, muss es im Kontext des ursprünglichen Benutzers gestartet werden.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Eine der größten Änderungen am Windows Betriebssystem in Windows Vista ist die Hinzufügung der Benutzerkontensteuerung (User Account Control, UAC), die Anwendungen mit reduzierten Berechtigungen standardmäßig ausführt. Daher müssen Installationsprogramme Die Berechtigungsebenen entsprechend verwalten. Windows 7 nutzt auch die UAC in großem Umfang. Während Windows 7 die Benutzerfreundlichkeit der Benutzerkontenführung verbessert, müssen Installationsprogramme dennoch die gleichen Anforderungen wie für Windows Vista erfüllen, um ordnungsgemäß zu funktionieren, ohne sich auf potenziell verwirrendes Virtualisierungsverhalten verlassen zu müssen.

UAC ist standardmäßig auf Windows Vista und Windows 7 aktiv, und die große Mehrheit der Kunden (88 % oder mehr, basierend auf Feedback) lässt dieses Feature aktiviert.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Weitere Informationen zum Konfigurieren der Windows Firewall finden Sie im DirectX-Artikel [Windows Firewall für Spieleentwickler](/windows/desktop/DxTechArts/games-and-firewalls) und im FirewallInstallHelper-Beispiel.

Der Standardstart des Spiels am Ende des Installationsprozesses erfüllt nicht den letzten Aspekt dieser Anforderung, wenn die Installation von einem Standardbenutzer gestartet wird und der Setupprozess Administratorrechte erfordert (d. amp;n. b. zur Eingabe von Administratoranmeldeinformationen auffordert). Außerdem erbt er Administratorrechte, was ein potenzielles Sicherheitsrisiko darstellt. Stattdessen sollte ein Setup-Bootstrapladeprogramm das Spiel starten, nachdem es von einem erfolgreichen Aufruf des Installationsprogramms zurückgegeben wurde. Weitere Informationen finden Sie im MSDN Magazine-Artikel [Teach Your Apps to Play Nicely with Windows Vista User Account Control](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control).

</dd> </dl>

### <a name="33-install-to-correct-folders"></a>3.3 Installation in richtigen Ordnern

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Spiele, die für alle Benutzer installiert sind, müssen standardmäßig im Ordner Programme installiert werden. Benutzerdaten müssen geschrieben werden, wenn das Spiel zum ersten Mal und nicht während der Installation ausgeführt wird.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Benutzer sollten die Flexibilität haben, Anwendungen dort zu installieren, wo sie sie benötigen. Außerdem sollten sie über eine konsistente und sichere Umgebung mit dem Standardspeicherort von Dateien verfügen.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Spiele können die verschiedenen bekannten Ordnerspeicherorte (z. B. die von CSIDL \_ LOCAL \_ APPDATA und CSIDL \_ COMMON APPDATA angegebenen) \_ verwenden, um erhebliche Mengen von Spieldaten und unterstützende ausführbare Dateien zu speichern, um erweiterte Szenarien für die bedarfsbasierte Installation und das Patchen zu implementieren.

Da für die Installation während der Installation aller Benutzer eine Erhöhung auf ein anderes Benutzerkonto erforderlich sein kann, gibt es keinen richtigen Benutzerspeicherort, an dem Daten zur Installationszeit gespeichert werden sollen. Wenn die Dateiverschlüsselung aktiviert ist, kann auf verschlüsselte Dateien nur über das Benutzerkonto zugegriffen werden, das sie erstellt hat.

</dd> </dl>

### <a name="34-install-windows-resources-properly"></a>3.4 Installieren sie Windows Ressourcen ordnungsgemäß.

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Anwendungen dürfen nicht versuchen, Dateien oder Registrierungsschlüssel zu installieren, die durch Windows Resource Protection (WRP) geschützt sind. Wenn die Anwendung neuere Versionen von Systemkomponenten erfordert, muss sie diese Komponenten mithilfe eines Microsoft Service Packs oder eines von Microsoft genehmigten Installationspakets aktualisieren, das die Systemkomponente enthält. Systemkomponenten dürfen nie neu gepackt werden.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Windows Resource Protection (WRP) wurde entwickelt, um sicherzustellen, dass geschützte Systemressourcen nur mit von Microsoft genehmigten Installations- oder Updatemechanismen aktualisiert werden. WRP verbessert die Zuverlässigkeit des Systems, indem sichergestellt wird, dass die Ergebnisse einer Installation vorhersagbar sind.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

WRP ist der Nachfolger von Windows File Protection, der den Großteil der Systemkomponenten schützt, die im Ordner Windows installiert sind. WRP schützt die meisten Registrierungsschlüssel, die Einstellungen für die COM-Objekterstellung speichern. Außerdem reserviert er bestimmte Ordner für die ausschließliche Verwendung durch das Betriebssystem. Versuche, auf geschützte Ressourcen zuzugreifen, führen in der Regel zu einem Zugriffsverweigerungsfehler.

Ausführliche Informationen zu bewährten Methoden, wenn die DirectX-Runtime mit einem Spiel bereitgestellt wird, finden Sie im DirectX-Artikel [DirectX-Installation für Spieleentwickler.](/windows/desktop/DxTechArts/directx-setup-for-game-developers)

</dd> </dl>

### <a name="35-avoid-reboots-during-installation"></a>3.5 Vermeiden von Neustarts während der Installation

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Das Spieleinstallationsprogramm sollte nicht davon ausgehen, dass die Installation von Windows-Komponenten aus Weiterverteilungspaketen einen Neustart erfordert, es sei denn, der Neustart wird durch ein Rückgabeergebnis oder in der Microsoft-Dokumentation angegeben.

Wenn das Spieleinstallationsprogramm immer einen Neustart erzwingt, muss dies von Microsoft genehmigt werden.

Dialogfelder für in Verwendung enthaltene Dateien, die in Windows Installer-Paketen enthalten sind, müssen eine Option zum automatischen Schließen von Anwendungen und zum Versuch enthalten, sie nach Abschluss des Setups neu zu starten.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Ein Neustart des Systems nach einer Installation ist für Benutzer eine unbequeme Unterbrechung und in der Regel nicht erforderlich.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Weitere Informationen finden Sie unter [Using Windows Installer with Restart Manager](/windows/desktop/Msi/using-windows-installer-with-restart-manager).

</dd> </dl>

### <a name="36-use-file-versioning-correctly"></a>3.6 Verwenden sie die Dateiversionsierung ordnungsgemäß.

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Das Spielinstallationsprogramm muss ordnungsgemäß überprüfen, um sicherzustellen, dass die neuesten Dateiversionen installiert sind. Die Installation eines Spiels darf niemals Dateien zurückdrennen, die Sie nicht erzeugen oder die von Anwendungen freigegeben werden, die Sie nicht erstellen.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Freigegebene Komponenten und Systemkomponenten werden häufig aktualisiert, um Sicherheitskorrekturen und erweiterte Funktionen zu gewährleisten. Eine Installation, die eine ältere Version der aktualisierten Komponenten enthält, darf nicht zum Verlust von Updates und Fehlerbehebungen führen, die bereits angewendet wurden.

</dd> </dl>

### <a name="37-support-autorun-conditional-requirement"></a>3.7 Unterstützung der bedingungsbedingten Anforderung für die automatische \[ Genehmigung\]

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Bei Spielen, die auf CD, DVD oder anderen Wechselmedien verteilt werden, die Autorun unterstützen, muss die Anwendung bei erstmaliger Einfügung des Datenträgers automatisch ausgeführt werden oder den Benutzer auffordern, das Spiel zu installieren, es sei denn, der Benutzer hat das Autoun-Feature deaktiviert.

Nachdem die Anwendung erfolgreich installiert wurde, darf das erneute Einfügen des Datenträgers auf dem Laufwerk nicht dazu führen, dass die Installation automatisch erneut beginnt. Es ist akzeptabel, Benutzer zu fragen, ob sie ihre Installationsoptionen aktualisieren oder ändern möchten.

Die autoun-Anwendung darf nicht zur Erhöhung der Rechte auffordern (d. h., sie muss im Manifest über asInvoker verfügen( siehe Anforderung 2.1), obwohl sie das Setupprogramm oder ein anderes Hilfsprogramm starten kann, das Administratorrechte erfordert. Eine Erhöhung sollte nur erfolgen, wenn das Spiel nicht installiert ist oder der Benutzer es ausdrücklich auswählt.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Autorun vereinfacht die Verwendung von medienverteilten Anwendungen, z. B. Spielen, bei denen die Festplatte in der Regel auf dem Laufwerk vorhanden sein muss, um das Spiel spielen zu können.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Es ist nicht akzeptabel, dass der Benutzer im Datei-Explorer navigiert, um die Installation von der CD oder DVD aus zu starten.

Bei Spielen, die auf mehreren Datenträgern verteilt werden, sollten nachfolgende Datenträger idealerweise entweder das Autoun-Feature verwenden oder die Installation fortsetzen, ohne den Benutzer auf eine Taste zu drücken oder andere Maßnahmen zu ergreifen.

Stellen Sie beim Erstellen eines Autorun-Programms sicher, dass alle erforderlichen Komponenten bei neu installierten Windows. Typische Anwendungen basieren auf Technologien, die vom Setup installiert werden, aber Autorun selbst wird ausgeführt, bevor eine solche Einrichtung erfolgt. Ein häufiges Beispiel ist der Ausfall von Autorun-Programmen, da die Visual C-Laufzeit-DLLs nicht als Teil des Setups Windows wurden. Das Autorun-Programm muss daher die lokale CRT-Bereitstellung der Anwendung verwenden oder die CRT statisch verknüpfen.

Automatische Programme, die für Versionen von Windows vor Windows Vista geschrieben wurden, sollten die .NET-Runtime nicht verwenden, da diese Technologie nicht in Windows XP oder älteren Versionen von Windows. Windows Server 2003 und Windows Vista sind die ersten Versionen von Windows, die .NET Runtime als Teil ihres Betriebssystems enthalten.

Aus ähnlichen Gründen kann für Autorun-Programme nicht das Vorhandensein optionaler, nebeneinander verfügbarer DirectX SDK-Komponenten wie D3DX9, D3DX10, D3DX11, XAudio2, X3DAudio, XACT, XINPUT und MDX 1.1 erforderlich sein.

Ein Beispiel für die Verwendung von Autorun finden Sie unter AutoRun-Beispiel.

</dd> </dl>

## <a name="reliability"></a>Zuverlässigkeit

**Zusammenfassung der Sicherheits- und Kompatibilitätsanforderungen**

**Kundenvorteile**

Diese Anforderungen machen eine Anwendung zuverlässiger, da sie die Anzahl von Abstürzen, Hängen und Neustarts minimiert. Die Zuverlässigkeitsanforderungen können dazu beitragen, dass Software besser vorhersagbar, verfeinerbar, resilient und wiederherstellbar ist.

### <a name="41-eliminate-unnecessary-reboots"></a>4.1 Vermeiden unnötiger Neustarts

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Alle Anwendungsinstallationsprogramme müssen die Neustart-Manager-APIs nutzen, um Systemneustarts zu vermeiden (siehe Anforderung 3.5).

Spiele dürfen das Herunterfahren nicht blockieren.

Alle Anwendungen müssen auf den Neustart-Manager reagieren, indem sie die folgenden Meldungen zum Herunterfahren überwachen und darauf reagieren:

<dl> <dt>

<span id="WM_QUERYENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_queryendsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_QUERYENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM \_ QUERYENDSESSION with LPARAM = ENDSESSION \_ CLOSEAPP (0x1) 
</dt> <dd>

GUI-Anwendungen müssen sofort reagieren (TRUE) als Vorbereitung auf einen Neustart.

</dd> <dt>

<span id="WM_ENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_endsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_ENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM \_ ENDSESSION with LPARAM = ENDSESSION \_ CLOSEAPP (0x1) 
</dt> <dd>

Anwendungen müssen innerhalb von 5 Sekunden einen Wert von 0 zurückgeben und dann schließen.

</dd> <dt>

<span id="CTRL_C__"></span><span id="ctrl_c__"></span>STRG+C 
</dt> <dd>

Konsolenanwendungen, die diese Meldung empfangen, müssen sofort geschlossen werden.

</dd> </dl> </dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Systemneustarts sind eine erhebliche Unterbrechung. Sie führen zu einer schlechten Benutzererfahrung und sollten minimiert werden. Einige Vorgänge, z. B. kritische Systemupdates, können Neustarts erfordern. Durch das Lauschen auf Meldungen zum Herunterfahren können das Spiel und andere Anwendungen sofort auf Anforderungen vom Neustart-Manager reagieren. Auf diese Weise können sie unnötige Verzögerungen bei gültigen Neustartanforderungen vermeiden.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Wenn ein Spieleinstaller die Windows Installer-Technologie (MSI) ohne benutzerdefinierte Aktionen verwendet, wird diese Funktion automatisch bereitgestellt. Microsoft-Neuverteilungspakete unterstützen auch den Neustart-Manager.

Weitere Informationen zum Neustart-Manager finden Sie im MSDN-Artikel [Informationen zum Neustart-Manager.](/windows/desktop/RstMgr/about-restart-manager)

</dd> </dl>

### <a name="42-eliminate-application-verifier-failures"></a>4.2 Beseitigen Application Verifier Fehlern

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Das Spiel darf in den folgenden Tests keine Fehler generieren, die unter Microsoft Application Verifier (AppVerifier), Version 4.0 oder höher, ausgeführt werden:

-   Grundlagen: Handles, Heaps, Sperren, Arbeitsspeicher, TLS
-   Sonstiges: DangerousAPIs, DirtyStacks

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

AppVerifier testet auf viele bekannte Probleme, die zu Abstürzen und Hängen in Windows Anwendungen sowie bekannten Sicherheitsrisiken führen.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Weitere Informationen zu Application Verifier finden Sie [unter Application Verifier](/previous-versions/ms220948(v=vs.80)) und Verwenden von Application Verifier innerhalb [ihres Softwareentwicklungslebenszyklus](/previous-versions/aa480483(v=msdn.10)) auf MSDN. Sie können die Application Verifier [download details: Application Verifier](https://www.microsoft.com/downloads/details.aspx?familyid=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18) im Microsoft Download Center herunterladen.

Diese Anforderung gilt nicht für reine verwaltete Anwendungen ohne native Interop.

Diese Tests sollten in einem Release-Build ausgeführt werden. Beim Debuggen von Builds können falsche Fehler generiert werden. Einige Anti-Anti-Anti-Cheat-Technologien können die Ausführung von AppVerifier beeinträchtigen. Daher sollten diese Tests ohne aktivierte Anti-Cheat-Technologien durchgeführt werden.

Möglicherweise muss die Full-Eigenschaft des Tests "Basics:Heaps" auf FALSE festgelegt werden, da der vollständige PageHeap den Arbeitsspeicherdruck der ausgeführten Anwendung deutlich erhöht. Fehler werden weiterhin erkannt, können aber schwieriger zu finden sein, wenn Sie nur einen partiellen PageHeap verwenden.

Wenn Sie die UAC-/LUA-bezogenen Tests in Application Verifier verwenden, um die Anforderungen 2.1 und 3.2 der Benutzerkontensteuerung zu erfüllen, sollten Sie die Ergebnisse mit dem [Standard-Benutzeranalyse-Tool](/windows/desktop/Win7AppQual/standard-user-analyzer--sua--tool-and-standard-user-analyzer-wizard--sua-wizard-) überprüfen. Es gibt auch zahlreiche weitere nützliche Tests von Application Verifier denen dringend empfohlen wird, sie bei der Entwicklung und beim Testen zu verwenden, um ein hohes Maß an Kompatibilität mit aktuellen und zukünftigen Versionen von Windows. Der **HighVersionLie-Test** wird verwendet, um die Konformität mit Anforderung 2.5 zu überprüfen.

Visual Studio Team System umfasst eine Teilmenge der AppVerifier-Funktionalität, die in die Debugumgebung integriert ist. Dies kann sich als nützlich erweisen, um Probleme mit Den Grundlagen: Heaps, Handles und Sperrentests zu verfolgen und zu beheben.

</dd> </dl>

### <a name="43-support-windows-error-reporting-and-file-version-information"></a>4.3 Unterstützung Windows-Fehlerberichterstattung und Dateiversionsinformationen

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Um die Unterstützung von Windows-Fehlerberichterstattung zu aktivieren, müssen Spiele die folgenden Anforderungen erfüllen:

-   Spiele dürfen nur Ausnahmen behandeln, die bekannt und erwartet sind. Windows-Fehlerberichterstattung darf nicht deaktiviert werden. Wenn ein Fehler wie eine Zugriffsverletzung in einem Spiel auftritt, muss er es Windows-Fehlerberichterstattung, den Absturz zu melden.
-   Alle ausführbaren Dateien (z. B. .exe oder DLLs) müssen einen genauen Produktnamen, Unternehmensnamen und eine genaue Dateiversion enthalten.
-   Das normale Beenden des Spiels darf nicht zu einem unbekannten Ausnahmefehler führen.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Die Windows-Fehlerberichterstattung-APIs bieten Microsoft wichtiges Feedback zur Erkennung von weit verbreiteten Abstürzen und Hängen in Anwendungen. Dadurch können Microsoft und seine Partner System- und Treiberprobleme, die schnell zu Anwendungsfehlern führen, schnell erkennen und beheben.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Spiele können benutzerdefinierte Ausnahmehandler ohne Behandlung enthalten, um benutzerdefinierte Unterstützungs- und Berichterstellungsfunktionen auszuführen. Sie müssen jedoch jeden Fehler an die **ReportFault-** oder **WerReportSubmit-Funktionen** übergeben.

Die richtigen Dateiversionsinformationen können überprüft werden, indem Sie die Dateieigenschaften auf der Windows Desktopbenutzeroberfläche anzeigen und die Eigenschaftenseite Version überprüfen.

Weitere Informationen zu den Windows-Fehlerberichterstattung-APIs und zur Analyse der Absturzabbilddaten, die bei Verwendung dieses Diensts generiert werden, finden Sie im DirectX-Artikel [Absturzabbildanalyse](/windows/desktop/DxTechArts/crash-dump-analysis).

</dd> </dl>

## <a name="xbox-360-common-controller-for-windows-terminology"></a>Xbox 360 Common Controller for Windows Terminology



| Name                                          | BESCHREIBUNG                                                                                                 |
|------------------------------------------|--------------------------------------------------------------------------------------------------|
| Ein                                        | Die Schaltfläche A.                                                                                     |
| B                                        | Die B-Schaltfläche.                                                                                     |
| Zurück                                     | Die Schaltfläche Zurück.                                                                                  |
| (rechts/links) Bumper                      | Die Schaltfläche am oberen rechten und linken Rand des Controllers. Entspricht einer Schaltfläche für die Schaltfläche "Shoulder".    |
| Direktionales Pad                          | Das direktionale Pad des Controllers.                                                                   |
| D-Pad                                    | Akzeptierte Abkürzung des direktionalen Pads.                                                         |
| Dp                                       | Direktionale Padabkürzung und Controllerbezeichnung.                                                |
| RB, LB                                   | Abkürzungen und Controllerbezeichnungen von rechts und links.                                        |
| RS, LS                                   | Abkürzungen für rechte und linke Striche und Controllerbezeichnungen.                                         |
| RT, LT                                   | Rechte und linke Triggerabkürzungen und Controllerbezeichnungen.                                       |
| RSB, LSB                                 | Abkürzungen für rechte und linke Striche und Controllerbezeichnungen.                                         |
| START                                    | Die Schaltfläche "Start".                                                                                 |
| (rechts/links) stick                       | Der Controller-Stick. Ehemals Thumbstick.                                                       |
| Stick-Schaltfläche (rechts/links)                | Die Controller-Stick-Schaltfläche. Ehemals Thumbstick-Schaltfläche.                                         |
| Trigger (rechts/links)                     | Der Controllertrigger.                                                                          |
| Vibration                                | Vom Controller-Motor erzeugtes Feedback. Verwenden Sie nicht Rumble.                           |
| X                                        | Die X-Schaltfläche.                                                                                     |
| J                                        | Die Y-Schaltfläche.                                                                                     |
| Xbox 360 Controller für Windows          | Das Xbox 360 Gamepad, das als PC-Hardware-SKU verkauft wurde, einschließlich einer Windows Gerätetreiber-Datenträger.          |
| Xbox 360 Wireless Controller für Windows | Das Xbox 360 als PC-Hardware-SKU verkaufte drahtlose Gamepad, einschließlich eines Windows Gerätetreiber-Datenträgers. |



 

## <a name="guidelines-for-game-middleware-products"></a>Richtlinien für Middlewareprodukte für Spiele

### <a name="introduction"></a>Einführung

Damit Spiele für das Games for Windows-Programm qualifiziert werden können, müssen sie eine Liste der technischen Anforderungen erfüllen. Alle Drittanbieterkomponenten, die mit einem Titel ausgeliefert werden (ausführbare Dateien, DLLs, Treiber usw.), müssen auch diese Anforderungen erfüllen, damit das Spiel qualifiziert werden kann. In diesem Dokument werden die gängigsten Anforderungen hervorgehoben, die auch von den Komponenten von Drittanbietern erfüllt werden müssen, damit das Spiel die Konformitätstests bestehen kann. Installer und vollständige Spiele-Engine-/Produktionspakete sollten das vollständige Dokument games for Windows technical requirements (Spiele für Windows technische Anforderungen) lesen, da viele dieser Anforderungen von diesen Tools betroffen sind.

### <a name="additional-recommendations"></a>Zusätzliche Empfehlungen

Neben der Sicherstellung, dass Ihre Komponente die Erstellung von Titeln unterstützt, die den Anforderungen für Games for Windows entsprechen, müssen Sie beim Entwerfen und Bereitstellen einer Bibliothek oder des Unterstützungshilfsprogramms für ein Windows Spiel eine Reihe weiterer Überlegungen berücksichtigen.

-   Um Entwickler zu unterstützen, die an nativen 64-Bit-x64-Anwendungen arbeiten, stellen Sie sowohl native 32-Bit- als auch 64-Bit-Versionen Ihrer Bibliotheken bereit. Die 32-Bit-Version muss pro 2.2 64-Bit kompatibel sein. Bibliotheken für 32-Bit-Anwendungen sollten nicht davon ausgehen, dass das hohe Bit einer 32-Bit-Adresse nicht verwendet wird, um die Verwendung in LARGEADDRESSAWARE x86-Anwendungen zu unterstützen.
-   Wenn Sie native Codeheader (C/C++) bereitstellen, verwenden Sie die SAL-Attributsyntax (Standard Annotation Language), um Ihre öffentlichen API-Routinen zu versehen. Dadurch können Benutzer Ihrer Bibliothek den maximalen Vorteil der Verwendung von Static Code Analysis (/analyze) nutzen, das Teil Visual Studio Team System 2005, Visual Studio Team System 2008, Visual Studio 2010 Premium und Visual Studio 2010 Ultimate ist, sowie die öffentlich verfügbaren Windows SDK-Compilertools.
-   Wenn Ihr Produkt Threads innerhalb des Prozesses des Benutzers erstellt, müssen Sie jeden Thread benennen, damit debuggende Tools ausgeführte Threads ordnungsgemäß kommentieren können.
-   Wenn Sie Routinen schreiben, die innerhalb der Hauptschleife eines Spiels aufgerufen werden sollen, verwenden Sie die D3DX-Routinen D3DPERF \_ BeginEvent/EndEvent und D3DPERF \_ SetMarker, um vorgänge auf hoher Ebene mit Anmerkungen zu versehen, um Engpässe mit pix für Windows leichter zu erkennen.
    > [!Note]  
    > Für die Grafikdiagnosefunktionen Visual Studio 2012 werden diese D3DX- und PIX-Routinen durch die [**ID3DUserDefinedAnnotation-Schnittstelle**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation) ersetzt.

     

-   Stellen Sie für Netzwerkbibliotheken IP-neutrale Implementierungen bereit, und vermeiden Sie veraltete IPv4-Routinen, um die IPv6- und Teredo-Technologien in Windows XP mit Service Pack 2, Windows Vista und Windows 7 zu unterstützen.
-   Spieledienstanbieter sollten sich mit Version 2 des GDF-Schemas bei Games Explorer registrieren und das RSS-Feature nutzen, um dienstbezogene Nachrichten bereitzustellen.

### <a name="games-for-windows-showcases"></a>Spiele für Windows Showcases

### <a name="introduction"></a>Einführung

Spiele für Windows Zeigen gehen über die Bereitstellung einer soliden Spielerfahrung auf Windows PCs hinaus. Durch die Implementierung dieser Features können Spiele die Benutzerfreundlichkeit auf den neuesten Windows Plattformen verbessern.

Spiele für Windows Titel müssen alle in diesem Artikel aufgeführten technischen Anforderungen erfüllen, aber Showfeatures sind optional. Diese Titel können einige, keine oder alle dieser Showcases implementieren.

### <a name="s1-exploit-direct3d-11"></a>S.1 Exploit Direct3D 11

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Direct3D 11 ist die Rendering-API der nächsten Generation für Windows Vista und Windows 7. Spiele, die Direct3D 11 nutzen, verwenden optimierte Inhalte, erweiterte Renderingtechniken und neue Hardwarefeatures, um eine überzeugende Erfahrung auf Hardware zu schaffen, die 10, 10.1 und 11 unterstützt.

Wenn das Spiel auch Direct3D 9 implementiert, sollte ein paralleler Vergleich eine erkennbare Verbesserung der Inhaltsqualität, visueller Genauigkeit, Leistung, Szenenkomplexität und anderer Grafikgenauigkeitsbereiche für Direct3D 11 veranschaulichen. Diese Unterstützung unterliegt den technischen Anforderungen von Games for Windows 1.7.

Die Direct3D 10level9-Technologie kann verwendet werden, um die Videohardware des Shadermodells 2.0/3.0 Direct3D 9 auf Windows Vista und Windows 7 zu unterstützen, anstatt eine direkte Direct3D 9-Implementierung für umfassende Hardwareunterstützung zu verwenden. Dies reicht jedoch nicht aus, um dieses Showcase zu veranschaulichen.

Auf Computern, auf denen Windows Vista oder Windows 7 mit installiertem Direct3D 11 ausgeführt wird, sollte das Spiel standardmäßig Direct3D 11 verwenden.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Die Direct3D 11-API baut auf dem Windows Display Driver Model (WDDM) und der Direct3D 10.1-Infrastruktur auf, um neue Funktionen zu unterstützen: Hardware-Mosaik, Compute-Shader, Multithreadring und Ressourcenerstellung, neue Texturkomprimierungsformate und eine flexiblere Shadersprache. Direct3D 11 bietet einheitliche Hardwareunterstützung für moderne Grafikkarten, einschließlich der Direct3D 11-Teile der neuesten Generation, aller Direct3D 10- und 10.1-Grafikkarten sowie vieler Shader Model 2.0/3.0 Direct3D 9-Grafikkarten. Dies ist die minimale Videohardware, die für den 3D-Desktop vonEinheit 3D erforderlich ist.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Die Migration einer Direct3D 9-Rendering-Engine zur Verwendung der neuen Direct3D 11-Schnittstelle ist eine klar definierte Aufgabe:

-   Entfernen Sie alle Vorgänge mit fester Funktion zugunsten von programmierbaren Shadern.
-   Aktualisieren Sie alle vorhandenen Shader auf die neue Syntax des Shadermodells 4.x/5.
-   Aktualisieren Sie die Ressourcenverwaltung, um das neue Ansichtsmodell zu unterstützen.
-   Konvertieren Sie alle Ressourcen, um eine neue Liste der verfügbaren Formate zu verwenden.
-   Aktualisieren Sie die Renderzustandsbehandlung, um unveränderliche Zustandsblöcke zu verwenden, und überarbeiten Sie Shaderkonstanten in Konstantenpuffer.

Diese Konvertierung ist wichtig, um das Direct3D 11-Showcase zu aktivieren, obwohl das Ergebnis nicht der Anforderung entspricht, die neue API zu nutzen.

Die neue API und das zugehörige HLSL-Programmiermodell bieten viele Möglichkeiten für verbesserte Inhalte:

-   Nutzen vorhandener Direct3D 10-Hardwarefeatures wie Geometry Shader, Stream Out, Texturarrays und die komprimierten BC4/BC5-Texturformate.
-   Nutzen vorhandener Direct3D 10.1-Hardwarefeatures, z.B. unabhängige Blendmodi pro Renderziel, MSAA-Tiefenlesemodus, MSAA-Zugriff pro Beispiel-Shader, Cubezuordnungsarrays und Rendering in blockkomprimierten Formaten (BLOCK-Compressed, BC).
-   Implementieren erweiterter GPU-Algorithmen mithilfe von Compute-Shader mit CS4.x auf vorhandenen Direct3D 10/10.1-Grafikkarten (aktiviert durch aktualisierte Videotreiber) oder CS 5.0 auf Direct3D 11-Grafikkarten der nächsten Generation.
-   Rendern in mehreren Threads mithilfe der Erstellung von Freethreadressourcen und mehreren Gerätekontexten zur Verbesserung der Leistung auf Multi-Core-Systemen (mit aktualisierten Videotreibern). Weitere Informationen finden Sie unter Games for Windows Showcase S.3.
-   Unter Verwendung neuer Features der Videohardware der Direct3D 11-Klasse, z. B. Hardware-Mosaik mit Hüllen- und Domänen-Shadern, Bietet shader Model 5.0 HLSL shader hardware features BC6HBC7 compressed texture formats und Dynamic Shader Linkage( Dynamische Shaderverknüpfung).

Techniken, die mit Direct3D 9 (größtenteils durch hohe CPU-Kosten) implementiert werden können, können effizient auf die GPU geladen werden, wodurch CPU-Ressourcen zur Unterstützung anderer Spielanforderungen freigegeben werden.

Direct3D 11-APIs, unterstützende Tools und Beispiele sind im DirectX SDK verfügbar. Weitere Informationen finden Sie unter Grafik-APIs in Windows.

</dd> </dl>

### <a name="s2-exploit-x64-native"></a>S.2 Exploit x64 Native

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Das Spiel enthält eine native 64-Bit-Ausführbare Datei, die eine überzeugende neue Erfahrung bietet, die von x64-Editionen von Windows, die auf x64-fähiger Hardware ausgeführt werden. Ein vergleichsseitiger Vergleich mit der 32-Bit-Version des Spiels sollte eine wahrnehmbare Verbesserung der Komplexität des Inhalts, eine reduzierung der Gesamtauslastungszeiten und die Leistung zeigen.

Bei 64-Bit-Editionen von Windows sollte die Installation immer die native 64-Bit-Version des Spiels als Standard für Verknüpfungen im Games Explorer und Windows XP Professional x64 Edition einrichten. Wenn eine duale Installation gewünscht ist, kann eine zusätzliche Play-Aufgabe für den Spiele-Explorer unter Windows Vista und Windows 7 angegeben werden, die auf die 32-Bit-Version verweist, aber der Standardwert sollte die native 64-Bit-Version bleiben.

Beachten Sie, dass das Spiel die 64-Bit-Editionen von Windows Vista und Windows 7 unterstützen sollte, um diese Vorzeigeempfehlung zu erfüllen. Unterstützung für Windows XP Professional x64 Edition wird empfohlen, ist aber nicht erforderlich.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Die x64-Technologie bietet 64-Bit-Adressierungsfunktionen sowohl für den Consumer- als auch für den Servermarkt, die 32-Bit-Abwärtskompatibilität mit Vollständiger Geschwindigkeit für vorhandene Anwendungen umfassen. x64 ist ein wichtiger Bestandteil der Roadmap für AMD (AMD64) und Intel (EMT64) und unterstützt mit Ausnahme von ultra-mobilen CPUs die Technologie für alle Prozessoren der aktuellen und zukünftigen Generation.

Windows XP Professional x64 Edition war das erste consumerorientierte Windows-Betriebssystem, das x64-Technologie unterstützt, und Windows Vista und Windows 7 erweitern die Verfügbarkeit der Betriebssystem-Aktivierung für 64-Bit-Consumercomputing. Da auf vielen neuen Computern standardmäßig 2 GB RAM verfügbar sind, profitieren weitere Verbesserungen bei der Speicherskalierung nicht von 32-Bit-Einzelanwendungen, die nicht mehr als 2 GB physischen RAM verarbeiten können. Viele Spiele stehen heute vor Herausforderungen, die alle verfügbaren Inhalte in die Einschränkungen von 2 GB virtuellem Adressraum einpassen, insbesondere in Kombination mit den großen Videospeichern, die auf High-End-GPUs verfügbar sind, und der Wechsel zur x64-Technologie erhöht die unterstützungsfähige Detailebene deutlich.

Die x64-Kompatibilität für 32-Bit-Spiele ist eine technische Anforderung von Games for Windows (2.2), aber die nutzungsbasierte Nutzung der neuen Technologien erfordert eine native 64-Bit-Implementierung.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Der Hauptvorteil der 64-Bit-Adressierung ist die Möglichkeit, direkt auf mehr als 2 GB physischen und virtuellen Arbeitsspeicher zu zugreifen. Der große Adressraum des virtuellen Arbeitsspeichers ermöglicht eine umfangreiche Verwendung von speicherabgezuordnungsbasierten E/A-Daten, ohne dass Probleme mit der VM-Adressraumerschöpfung bei der 32-Bit-Programmierung auftreten. Spiele können den neuen Speicherplatz nutzen, um ladezeiten stark zu verbessern oder in einigen Fällen Pausen für das Laden von Inhalten zu vermeiden.

Vorhandene 32-Bit-Anwendungen können von x64-Editionen profitieren, da sie Adressen mit vollständigen 32-Bit-Daten verarbeiten können, wenn sie mit der Linkeroption Große Adressen aktivieren (**/LARGEADDRESSAWARE**) erstellt wurden. In 32-Bit-Versionen von Windows XP ermöglichten spezielle Startmodi, dass solche Anwendungen bis zu 3 GB RAM unterstützen, und x64-Editionen bieten Zugriff auf bis zu 4 GB RAM für LAA-Apps (Large Address Aware). Obwohl die Verwendung von LAA in einer 32-Bit-Anwendung diese Vorzeigeanforderung nicht erfüllt, ist diese Bridgetechnologie eine äußerst nützliche Möglichkeit, zusätzliche Skalierungsvorteile für x64-Versionen von Windows für diejenigen zu bieten, die diese Vorzeigeanforderung nicht vollständig implementieren.

Weitere Informationen finden Sie unter [64-Bit-Programmierung](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers) für Game Developers und [RAM, VRAM und More RAM: 64-Bit Gaming Is Here](https://www.gamasutra.com/view/feature/3602/sponsored_feature_ram_vram_and_.php) in Gamasutra.

> [!Note]  
> Eine wichtige Herausforderung für diese Präsentation besteht darin, sicherzustellen, dass alle Bibliotheken oder Komponenten von Drittanbietern, auf die Ihr Spiel basiert, für die native 64-Bit-Entwicklung verfügbar sind. Viele ältere Microsoft-APIs wurden auch aus der nativen 64-Bit-Umgebung entfernt, was sich als Herausforderung für Engine-Codebasen erweisen kann, die ältere Implementierungen von Schlüsselsystemen enthalten.

 

</dd> </dl>

### <a name="s3-exploit-many-core-processors"></a>S.3 Exploit Many-Core-Prozessoren

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Das Spiel implementiert Features, die Mehrkernprozessoren nutzen, die auf 3, 4 oder mehr Kerne skaliert werden, wenn verfügbar.

Wenn das Spiel Einzelprozessor- oder Dual-Core-Systeme unterstützt, sollte ein paralleler Vergleich mit einem Quad-Core-System erkennbare neue Features, zusätzliche überzeugende Effekte, eine Verbesserung der Inhaltsqualität und/oder eine verbesserte Leistung zeigen.

Da die Dual-Core-Skalierung bereits umfassend von Spielen unterstützt wird und von verschiedenen Erweiterungen des Direct3D-Treibers automatisch genutzt wird, reicht die Dual-Core-Skalierung nicht aus, um dieses Beispiel zu veranschaulichen.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Das kontinuierliche Wachstum der Leistung für CPUs hat sich von Verbesserungen der Taktfrequenz auf die Ergänzung von Berechnungskernen umgeschaltet. Sowohl AMD- als auch Intel-Roadmaps basieren auf skalierbaren Designs mit mehreren Kernen. Aufgrund dieser grundlegenden Verschiebung in der Entwicklung von Prozessoren verfügen alle Spielplattformen der nächsten Generation über CPUs mit mehreren Kernen. Singlethreadanwendungen erzielen keine signifikanten Vorteile mehr durch CPUs der nächsten Generation. Einfaches Multithreading kann auch nicht skaliert werden, wenn die Anzahl der häufig verwendeten CPU-Kerne auf drei oder mehr steigt.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Beachten Sie, dass die Kernanzahl keine Zweierleistung sein muss, sodass Spiele linear skaliert werden und die Kernanzahl von 3, 4, 5, 6, 7, 8 und so weiter verarbeiten sollten.

Das Skalieren durch Erhöhen der Anzahl von Threads in einer Anwendung bietet nur dann eine Rendite, wenn die Kosten für Kommunikation und Threadsynchronisierung überprüft werden. Die featurebasierte Skalierung kann sich kurzfristig als einfachere Lösung erweisen, sodass das Spiel ohne die zusätzlichen Threads auf Einzelkernsystemen normal ausgeführt werden kann, und diese aktivieren, wenn die zusätzliche CPU-Leistung verfügbar ist.

Weitere Informationen finden Sie unter [Coding For Multiple Cores on Xbox 360](/windows/desktop/DxTechArts/coding-for-multiple-cores) and Microsoft Windows and Lockless Programming Considerations for Xbox 360 and Microsoft Windows (Programmierüberlegungen für Xbox 360 und Microsoft [Windows)](/windows/desktop/DxTechArts/lockless-programming) in den DirectX-Artikeln sowie im DxUTLockFreePipe-Hilfsprogramm und im CoreDetection-Beispiel.

Die Verwendung der Direct3D 11-Freethread-Ressourcenerstellung und der Gerätekontexte ist nützlich, um beim Rendern und Laden von Grafikressourcen Eine-Kern-Skalierbarkeit zu erzielen. Siehe Games for Windows Showcase S.1.

Beachten Sie, dass die direkte Verwendung der CPU-Anweisung rdtsc anstelle von Windows-APIs zum Berechnen der Zeitsteuerung auf Systemen mit mehreren Kernen zu Problemen bei einigen Hardware- und Betriebssystemkonfigurationen führen kann. weitere [Informationen finden Sie unter Game Timing and Multicore Processors](/windows/desktop/DxTechArts/game-timing-and-multicore-processors) in den DirectX-Artikeln.

</dd> </dl>

### <a name="s4-support-games-for-windows---live"></a>S.4 Support Games for Windows – LIVE

Games for Windows – LIVE wird von Microsoft nicht mehr unterstützt.

### <a name="s5-support-windows-touch"></a>S.5 Support Windows Touch

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Windows Touch-fähige Spiele können mithilfe von Touch- und/oder Gesten auf Computern, auf denen Windows 7 ausgeführt wird, mit touchbasiertem Display abspielbar sein. Tastatureingaben können auch verwendet werden, aber die primäre Wiedergabeschnittstelle muss touch-basiert sein.

Das Aktivieren der Fingerbewegung sollte die Verwendung der Maus oder des gemeinsamen Controllers nicht verhindern, was der technischen Anforderung 1.4 unterliegt.

Es wird nicht erwartet, dass das Installationsprogramm des Spiels Windows Touch-Funktionalität unterstützt.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Multi-Touch-fähige Displays für Computer sind für Laptops und Desktops verfügbar und stellen ein wichtiges Hardwarefeature dar, das mit der Veröffentlichung von Windows 7 Windows wird. Windows 7 unterstützt Windows Touch auf den Desktop- und allgemeinen Steuerelementschnittstellen.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Native Codeanwendungen können über die WM TOUCH-Nachrichten in Kombination mit der \_ [**RegisterTouchWindow-Funktion auf Multitouch zugreifen.**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) Siehe auch die API für Manipulationen und Trägheit.

Windows Presentation Foundation (WPF) 4.0 bietet eine verwaltete Lösung für Multi-Touch-Schnittstellen.

Weitere Informationen finden Sie im Windows Touch SDK.

</dd> </dl>

### <a name="s6-support-high-color"></a>S.6 Unterstützung für hohe Farbe

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Spiele, die High Color unterstützen, verwenden ein 10:10:10:2 (DXGI \_ FORMAT \_ R10G10B10A2, D3DFMT \_ A2B10G10R10) oder ein 16:16:16:16:16-Format \_ (DXGI-FORMAT \_ R16G16B16A16, D3DFMT \_ A16B16G16R16) für den Rendering-Hintergrundpuffer- und Vollbildanzeigemodus.

Mithilfe eines High Color-Renderziels können HDR-Inhalte (High-Dynamic Range) mit einem erweiterten oder breiten Gamut gerendert werden, wenn eine Tonzuordnung zu einem 10-Bit- oder 16-Bit-Bereich erstellt wird.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Monitore können seit vielen Jahren mehr als 256 Farbebenen pro Kanal anzeigen, auch wenn CRT-Anzeigen weit verbreitet waren. Die Überprüfung der Hardware auf Grafikkarten war der begrenzende Faktor. Moderne GPUs, einschließlich der meisten Direct3D 9-Klassenhardware und aller Direct3D 10-Klassen und besserer Hardware, verfügen über Scan out-Hardware, die mindestens 10 Bits pro Kanal unterstützt, und die Hardwarefunktion wird in Zukunft auf 16 Bits pro Farbkanal anwachsen. HD TV-Verbindungssysteme (HK, DisplayPort) wurden auch für die Handhabung von mehr als 8 Bits pro Kanal entwickelt, und analoge VGA-Geräte werden solche Signale bereits empfangen.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Beachten Sie, dass High Color oder Hi Color sich in der Vergangenheit auf das Verschieben von 256 (8-Bit)-Farbanzeigen in 15- oder 16-Bit-Farbanzeigen bezieht. Die meisten Anzeigesysteme sind schon lange auf True Color (24-Bit-Farbe) oder 8 Bits pro Farbkanal für Rot, Grün und Blau umgezogen. Unter High Color (Hohe Farbe) wird hier eine neue Generation von Anzeigesystemen bezeichnet, die mit mehr als 8 Bits pro einzelnem Farbkanal arbeiten können. Wird auch als Tiefe Farbe bezeichnet.

</dd> </dl>

### <a name="recommended-best-practices"></a>Empfohlene bewährte Methoden

### <a name="introduction"></a>Einführung

Zusätzlich zur Erfüllung der technischen Anforderungen und der Einführung eines oder mehrere Showcases in Ihrem Titel gibt es eine Reihe von bewährten Methoden, die für alle spiele Windows werden sollten. Obwohl diese Empfehlungen nicht in den Rahmen der grundlegenden technischen Anforderungen fallen, wird dringend empfohlen, sie für alle Spiele für Windows zu verwenden.

### <a name="additional-recommendations"></a>Zusätzliche Empfehlungen

-   Verwenden Sie den neuesten Visual Studio compiler und runtime. Neuere Versionen des Compilers implementieren erhebliche Verbesserungen für die Qualität des generierten Codes und für Sicherheitsprobleme und nutzen moderne Strategien zur Prozessoroptimierung. Die Aktualisierung des Compilers und die Verwendung der neuesten C-Runtime ist eine einfache Möglichkeit, zu modernen Codierungsmethoden zu migrieren.
-   Verwenden Sie anstelle der statischen Verknüpfung die DLL-Version (Dynamic Link Library) der C-Runtime, und verwenden Sie Secure CRT. (Ausnahmen können in speziellen Vorinstallationsfällen vorgenommen werden, z. B. für ein Autorun-Programm oder für das Installationsprogramm selbst).)
-   Verwenden Sie für Spielaudiodaten XAudio2, X3DAudio und/oder XACT anstelle von DirectSound. Verwenden Sie DirectSound unter Windows XP (nur) und WASAPI unter Windows Vista und Windows 7 für Audio-Engines, die alle Mischungs- und Quellratenkonvertierungen verwenden und nur eine Lösung mit geringer Latenz für die Audioausgabe benötigen.
-   Vermeiden Sie die Verwendung veralteter und veralteter APIs: DirectDraw, DirectSound, DirectPlay, Die Leistungsebene von Direct Soll, DirectPlay Voice und der beibehaltene Direct3D-Modus. Beachten Sie, dass DirectPlay Voice und der beibehaltene Direct3D-Modus unter Windows Vista oder Windows 7 überhaupt nicht verfügbar sind. Die Leistungsebene von DirectPlay und DirectPerformance ist für x64-native Anwendungen nicht verfügbar.
-   Optimieren sie mithilfe von SSE/SSE2 SIMD-Anweisungssätzen. Sehen Sie [sich die DirectXMath-API](/windows/desktop/dxmath/directxmath-portal) im Windows SDK als plattformübergreifende Lösung für SIMD-optimierte mathematische Operationen an.
-   Verwenden Sie moderne bewährte Methoden für Windows-Sicherheit (einschließlich Compiler- und Linkeroptionen wie **/NXCOMPAT,** **/GS,** **/SAFESEH,** **/DYNAMICBASE,** **/SDL** und so weiter). Weitere Informationen finden Sie unter [Best Security Practices in Game Development](/windows/desktop/DxTechArts/best-security-practices-in-game-development).
-   Verwenden Sie die Windows SDK-Komponenten und -Bibliotheken. Entfernen Sie Abhängigkeiten von den älteren, von DirectSetup bereitgestellten Out-of-Band-Komponenten wie D3DX9, D3DX10 und D3DX11. Erwägen Sie [die Verwendung von DirectXTex](https://github.com/Microsoft/DirectXTex) oder [DirectXTK](https://github.com/Microsoft/DirectXTK) oder beidem.
-   Vermeiden Sie die Verwendung des älteren HLSL-Compilers, und verwenden Sie stattdessen den modernen HLSL-Compiler. Wenn die Anwendung Unterstützung für Pixels shader 1.x benötigt, verwenden Sie anstelle von HLSL die Shader-Assembly, oder beschränken Sie die Verwendung des älteren Compilers auf diese Szenarien.

## <a name="resources"></a>Ressourcen



| Begriff                                                                                                                                                                                                                         | Beschreibung                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Games_for_Windows__Test_Cases__"></span><span id="games_for_windows__test_cases__"></span><span id="GAMES_FOR_WINDOWS__TEST_CASES__"></span>Spiele für Windows: Testfälle <br/>                              | Bewährte Methoden für Spiele auf Windows XP, Windows Vista und Windows 7<br/>                                                                               |
| <span id="Windows_SDK__"></span><span id="windows_sdk__"></span><span id="WINDOWS_SDK__"></span>Windows Sdk <br/>                                                                                                      | [Windows Sdks](https://msdn.microsoft.com/bb980924.aspx)<br/>                                                                                      |
| <span id="User_Account_Control_Guidelines__"></span><span id="user_account_control_guidelines__"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES__"></span>Richtlinien für die Benutzerkontensteuerung <br/>                      | [Windows Anforderungen an die Vista-Anwendungsentwicklung für die Kompatibilität der Benutzerkontensteuerung](/previous-versions/dotnet/articles/bb530410(v=msdn.10))<br/> |
| <span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual-Entwicklerportal <br/>                                                  | [Windows Quality Online Services (Winqual)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)<br/>                                                                         |
| <span id="DirectX_Developer_Portal__"></span><span id="directx_developer_portal__"></span><span id="DIRECTX_DEVELOPER_PORTAL__"></span>DirectX-Entwicklerportal <br/>                                                  | [Directx Developer Center](/previous-versions/windows/apps/hh452744(v=win.10))<br/>                                                                               |
| <span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog zu Spielen für Windows und DirectX SDK<br/> | [Spiele für Windows und das DirectX SDK](https://walbourn.github.io/)<br/>                                                                           |
| <span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Zusätzliche DirectX-Artikel<br/>                                             | [Technische Artikel zu DirectX](/windows/desktop/DxTechArts/dx9-technical-articles)<br/>                                                                                    |



 

 

