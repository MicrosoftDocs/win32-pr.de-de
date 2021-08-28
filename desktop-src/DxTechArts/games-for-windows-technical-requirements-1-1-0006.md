---
title: Technische Anforderungen für Spiele für Windows; bewährte Methoden für Spiele für Windows XP, Windows Vista, Windows 7 und Windows 8
description: Dieser Artikel enthält technische Anforderungen und bewährte Methoden für Spiele, die auf Windows ausgeführt werden.
ms.assetid: 8b816e9f-de68-cf84-1501-a9c36c6b75d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a5c1480f8ef5ef67a2bd2b998e0dcbe28ed397
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482116"
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
    -   [1.8 Aktivieren von hohen DPI-fähigen Daten](#18-enable-high-dpi-aware)
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
    -   [3.4 Ordnungsgemäßes Installieren von Windows-Ressourcen](#34-install-windows-resources-properly)
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

Alle Spiele, die Sie beim [Spiele-Explorer](/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)) registrieren, werden als Kacheln in der neuen Windows Benutzeroberfläche angezeigt, aber ein Großteil der Metadaten, die dem Titel zugeordnet sind, ist nicht mehr sichtbar. Sie verwenden weiterhin das Game Definition File Maker-Tool (GDFMAKER.EXE), das jetzt im Windows Software Development Kit (SDK) verfügbar ist, um die Metadaten zu erstellen. Sie verwenden auch die vorhandenen Mechanismen zum Bereitstellen der Metadaten. Testen Sie ihre Games Explorer-Registrierung mit Windows 7, und überprüfen Sie, ob die neue Kachel für die Windows Benutzeroberfläche angezeigt wird, wenn Sie sie auf Windows 8 installieren (siehe [1.1 Games Explorer Integration](#11-games-explorer-integration)).

Informationen zum Herunterladen des Windows 8 SDK finden Sie unter [Downloads für die Entwicklung von Desktop-Apps.](https://msdn.microsoft.com/windows/desktop/aa904949)

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

XINPUT 1.4 ist in Windows 8 integriert. Sowohl Windows Store-Apps als auch Desktop-Win32-Apps können XINPUT 1.4 verwenden. Alle Versionen von Windows können XINPUT 9.1.0 für vereinfachte allgemeine Controller verwenden, aber es gibt kein Weiterverteilungspaket mit XINPUT 9.1.0. Alle Versionen von Windows können auch die vorhandene DirectX SDK-Version XINPUT 1.3 verwenden, für die DirectSetup bereitgestellt werden muss.

Informationen zum Windows finden Sie unter [Unterstützung des allgemeinen Xbox 360-Controllers in 1.4.](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement)

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

<span id="The__DirectX_End-User_Redistribution__package_runs_successfully_on_Windows_8__as_it_does_on_Windows_7__to_deploy_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTEngine__and_so_on"></span><span id="the__directx_end-user_redistribution__package_runs_successfully_on_windows_8__as_it_does_on_windows_7__to_deploy_d3dx9__d3dx10__d3dx11__xinput_1.3__xaudio_2.7__xactengine__and_so_on"></span><span id="THE__DIRECTX_END-USER_REDISTRIBUTION__PACKAGE_RUNS_SUCCESSFULLY_ON_WINDOWS_8__AS_IT_DOES_ON_WINDOWS_7__TO_DEPLOY_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTENGINE__AND_SO_ON"></span>**Das DirectX End-User Redistribution-Paket wird wie bei Windows 7 erfolgreich auf Windows 8 ausgeführt, um D3DX9, D3DX10, D3DX11, XINPUT 1.3, XAUDIO 2.7, XACTEngine usw. bereitzustellen.**
</dt> <dd>

Aufgrund der Bereitstellungsbehandlung der älteren Verwalteten DirectX 1.1-Assemblys tritt jedoch ein bekanntes Problem mit DirectSetup auf Systemen auf, auf dem nur .NET 4.0 installiert ist. Dieses Problem gilt sowohl für Windows 8,die standardmäßig in .NET 4.5 enthalten sind, als auch für neue Windows XP-Computer, auf denen die .NET 4.0-Runtime installiert ist. Dieses Problem gilt jedoch nicht für .NET-Versionen vor .NET 4.0. Während Windows 8 über ein Anwendungskompatibilitätsverhalten verfügt, um dieses Problem automatisch zu beheben (was Netzwerkzugriff erfordert), empfehlen wir, dass Spiele, die directSetup update weiterhin für die aktualisierte Version der REDIST-Dateien des DirectX SDK (Juni 2010) bereitstellen. Wenn Sie DirectSetup als Titel verwenden, kürzen Sie Ihren Titel wie immer auf die mindestens erforderliche Gruppe von CABs.

Weitere Informationen finden Sie unter [3.4 Installieren sie Windows Ressourcen ordnungsgemäß.](#34-install-windows-resources-properly)

</dd> <dt>

<span id="Games_that_require_the_.NET__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="games_that_require_the_.net__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="GAMES_THAT_REQUIRE_THE_.NET__2.0__COMPATIBLE_RUNTIME__2.0__3.0__3.5__CONTINUE_TO_USE_EXISTING_DEPLOYMENT_MECHANISMS"></span>**Spiele, für die die .NET 2.0-kompatible Runtime (2.0, 3.0, 3.5) erforderlich ist, verwenden weiterhin vorhandene Bereitstellungsmechanismen.**
</dt> <dd>

Diese Spiele lösen ein Anwendungskompatibilitätsverhalten auf Windows 8 aus, um die .NET 3.5-Runtime automatisch zu aktivieren (was Netzwerkzugriff erfordert). Es wird jedoch empfohlen, dass .NET-Entwickler zur .NET 4.0-Runtime wechseln.

> [!Note]  
> Die Legacyassemblys von Managed DirectX 1.1 sind nicht mit der .NET 4.x-Runtime kompatibel.

 

Weitere Informationen finden Sie unter [3.4 Installieren sie Windows Ressourcen ordnungsgemäß.](#34-install-windows-resources-properly)

</dd> <dt>

<span id="Use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.NET_is_not_recommended"></span><span id="use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.net_is_not_recommended"></span><span id="USE_OF_AN__AUTORUNNER__OR_OTHER_PRE-INSTALL_TECHNOLOGY_THAT_RELIES_ON_.NET_IS_NOT_RECOMMENDED"></span>**Die Verwendung eines AutoRunners oder einer anderen Vorinstallationstechnologie, die auf .NET basiert, wird nicht empfohlen.**
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

Das Spiel muss in Games Explorer (im Ordner **Games)** auf Windows Vista und Windows 7 sichtbar sein. Wenn diese Option ausgewählt ist, muss das Spiel auch die richtigen Metadaten anzeigen, einschließlich Herausgeber, Entwickler, Veröffentlichungsdatum, Version, Windows Experience Index-Bewertungen, Bewertung (falls zutreffend) und zugehöriger Links.

Wenn das Spiel digital über einen Onlinespieldienst verteilt wird, sollte der Dienstanbieter auch im Spiele-Explorer angezeigt werden. Um eine ordnungsgemäße Verarbeitung des Anbieters sicherzustellen und die Verwendung von RSS-Feeds zu ermöglichen, sollte Version 2 des Schemas für Spieldefinitionsdateien (GDFs) verwendet werden. (Weitere Informationen zu GDFs finden Sie unter Zusätzliche Informationen.)

Darüber hinaus müssen Spielinstallationsprogramme die folgenden Regeln beachten, wenn sie auf Windows Vista und Windows 7 ausgeführt werden:

-   Die Installation darf keine Verknüpfung erstellen, um das Spiel auf dem Desktop, im Startmenü oder an einem anderen Ort zu starten.
-   Aufgaben und Verknüpfungen zum Entfernen dürfen nicht erstellt werden.
-   Benutzer müssen das Spiel entfernen können, indem sie Programme und Features in Systemsteuerung auf Windows Vista und Windows 7 oder Programme in Systemsteuerung auf Windows XP hinzufügen oder entfernen.

Auf Windows XP und in früheren Versionen von Windows kann das Spielinstallationsprogramm programmgruppen, Desktopsymbole oder Verknüpfungen nach Bedarf erstellen.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Windows Games Explorer ähnelt dem Konzept der Windows XP-Ordner **Eigene Dokumente** oder **Meine Bilder.** Die Idee besteht darin, ähnliche Inhalte an einem Ort zu zentralisieren und eine einfachere Organisation und kontextbezogene Aktivitäten zu ermöglichen. Games Explorer erweitert das **Eigene Dokumente-** oder **My Pictures-Konzept,** indem eine umfassendere Organisation und Kontrolle über Spiele ermöglicht wird. Der Spiele-Explorer ermöglicht es Gamern, alle auf ihren Systemen installierten Spiele anzuzeigen, zu organisieren und mit ihnen zu interagieren. Außerdem können Spieleverleger wichtige Spielinformationen effektiver kommunizieren. Das System ist datengesteuert und erleichtert es einem Spielherausgeber, Spielinformationen über die Lebensdauer des Produkts zu aktualisieren.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Die Integration in Games Explorer erfordert, dass Sie eine Spieledefinitionsdatei (GDF) erstellen, bei der es sich um eine XML-Textdatei handelt, die zusammen mit einem Windows-Symbol in eine Binärdatei (eine ausführbare Datei oder eine DLL) als Ressource eingebettet ist. Das Spiel muss dann beim Spiele-Explorer registriert werden. Die GDF ermöglicht auch die Weitergabe von bereitgestellten Informationen, z. B. den Titel des Spiels, den Herausgeber, den Entwickler, Links zu Websites und optionale Aufgaben. Beachten Sie, dass Supporttasks nur Links zu Websites sein können, aber wiedergabetasks können auch für optionale Supportaufgaben verwendet werden.

Games-Explorer kann ein Miniaturbild einer Bitmap verwenden, es wird jedoch empfohlen, stattdessen eine Windows Symbolressource mit großen Symbolen (256 256) bereitzustellen. Die Symbolressource sollte Bildgrößen von 256 256 48 48, 32 32 und 16 16 in 24-Bit-Farbtiefe (True Color) und 8-Bit-Farbtiefe (256) enthalten. Der in Visual Studio 2008 und 2010 bereitgestellte Symbol-Editor unterstützt diese großen Symbolformate, ebenso wie IconWorkshop Lite.

Details zur Integration in **Windows Games Explorer** finden Sie im DirectX SDK. Das DirectX SDK enthält einen GdF-Editor (Game Definition File) sowie ein GDF-Beispiel, das in GDFExampleBinary, einem Beispiel, enthalten ist. Ein weiteres Beispiel, GameUxInstallHelper, stellt Routinen für die Integration der erforderlichen Funktionalität in vorhandene Installationssysteme bereit. Das Game Definition File Validator (gdftrace.exe) bietet Debugunterstützung für die Auswertung einer GDF. Siehe auch "Windows Games Explorer Integration" in der DirectX SDK-Dokumentation für C++.

Windows 7 bietet Unterstützung für die zweite Version eines Schemas für GDF-Dateien. Die neue Version enthält eine vereinfachte Methode zum Erstellen von Spielaufgaben und Unterstützung für Updatebenachrichtigungen, Spieledienstanbieter, Spielstatistiken und RSS-Feeds für Spieledienstanbieter. Die neueste Version von GameUxInstallHelper übernimmt die gesamte Registrierung und legacy-Unterstützung, die für die Verwendung einer GDF-Datei der Version 2 mit Windows Vista erforderlich ist. Verwenden Sie die Tools und den Beispielcode aus dem DirectX SDK von August 2009 oder höher. Es wird empfohlen, eine GDF-Datei der Version 2 zu verwenden, um die Unterstützung für RSS-Feeds, Spielstatistiken und Updatebenachrichtigungen zu aktivieren. Siehe auch die Beispiele ProviderGDFExampleBinary und GameStatisticsExample.

Auf Windows Vista Business Edition, Windows 7 Professional Edition und Enterprise Edition von Windows Vista und Windows 7 ist der Games-Link auf der Startmenü ausgeblendet. Games Explorer ist weiterhin auf dem Startmenü verfügbar, indem Sie auf **Alle Programme** und dann auf **Spiele** klicken.

Für zugehörige Anwendungen, die mit Ihrem Spiel installiert werden, aber nicht selbst, können Sie Startmenü Programmgruppen, Verknüpfungen und Desktopsymbole für alle Versionen von Windows erstellen, einschließlich Windows Vista und Windows 7. Solche zugehörigen Anwendungen sollten die anwendbaren Spiele für Windows Anforderungen erfüllen. Weitere Informationen finden Sie unter [Richtlinien für Spiele-Middlewareprodukte.](#guidelines-for-game-middleware-products) Spieldienste sollten sich bei Games Explorer als Spieleanbieter für Windows 7 registrieren. 1

</dd> </dl>

### <a name="12-support-family-safety--parental-controls"></a>1.2 Unterstützung Family Safety/Jugendschutz

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Spiele müssen Windows Family Safety durch Einhaltung der folgenden Regeln vollständig unterstützen:

-   Spiele dürfen nicht erfordern, dass der Benutzer über Administratoranmeldeinformationen zum Spielen verfügen muss. Installation, Patchen und Entfernen können Administratoranmeldeinformationen erfordern, je nach den Anforderungen in Abschnitt 3. (Im Zusammenhang mit dieser Anforderung 2.1 befolgen Sie die Richtlinien für die Benutzerkontensteuerung.)
-   Spiele, die von Windows unterstützten Bewertungsboards wie ESRB und PEGI bewertet werden, müssen ihre zugewiesenen Bewertungsinformationen in ihre Spieledefinitionsdatei (GDF) einschließen. Alle verfügbaren Bewertungsdaten müssen in jeder lokalisierten Version der GDF sowie in der sprachneutralen Version enthalten sein.
-   Spiele müssen ihre ausführbaren Dateien in der GDF auflisten, um eine gute Benutzererfahrung für allgemeine Anwendungseinschränkungen zu bieten, es sei denn, das Spiel verwendet eine Anti-Anti- anti- anti- antivirus-Technologie, die zufällig benannte ausführbare Dateien zur Laufzeit erstellt.
-   Spiele müssen die **VerifyAccess-Methode** der Games Explorer-Schnittstelle während des Starts aufrufen, falls verfügbar, und beenden, wenn \* pfHasAccess als FALSE zurückgegeben wird.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Alle Spiele müssen innerhalb des Kontexts eines Standardbenutzerkontos ausgeführt werden, damit Konten, die von Windows Jugendschutz gesteuert werden, das Spiel spielen können. Eltern möchten den Zugriff ihrer Kinder auf Spiele überwachen und steuern können. Darüber hinaus wünschen sich zahlreiche Branchen-, Behörden- und Gruppierungsgruppen bessere Möglichkeiten, um es Eltern zu ermöglichen, die Spiele zu überwachen und zu steuern, denen ihre Kinder ausgesetzt sind. In Verbindung mit der von Games Explorer angebotenen Architektur bietet Microsoft Eltern diese Möglichkeit über Windows Jugendschutz.

Selbst bei Spielen, die nicht an einem Ratings Board-Programm teilnehmen, führt das Erfordern erhöhter Berechtigungen zu einer schlechten Spielerfahrung für die meisten Benutzerkonten. Dies ist insbesondere der Fall, wenn die Jugendschutzfunktionen aktiviert sind, die erfordern, dass das übergeordnete Element bei jedem Start des Spiels das Administratorkennwort eingibt.

Mit dem Windows System für die Jugendschutzfunktionen können Eltern die Bewertungen auswählen, die ihrer Meinung nach für ihre Kinder geeignet sind. Die Jugendschutzmaßnahmen unterstützen viele der weltweiten Bewertungssysteme. Die Jugendschutzmaßnahmen ermöglichen es Eltern auch, den Zugriff auf Spiele basierend auf Inhaltsdeskriptoren einzuschränken (sofern das entsprechende Bewertungssystem sie unterstützt) und den Zugriff auf einzelne Spiele zuzulassen oder zu unterbinden.

Die Standardauswahl des Bewertungssystems für Windows Jugendschutz basiert auf der Gebietsschemaeinstellung des Systems, kann jedoch vom Benutzer unter **Regionale Optionen und Sprachoptionen** in **Systemsteuerung** geändert werden. Daher sollte jede unterstützte Sprache alle verfügbaren Bewertungsdaten bereitstellen, damit der Benutzer die Möglichkeit hat, das gewünschte Bewertungsboard auszuwählen.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Spiele ohne Bewertung müssen weiterhin die Anforderungen erfüllen, um Das Spielen als Standardbenutzer zu unterstützen und **VerifyAccess** aufzurufen. Solche Spiele werden standardmäßig in der Kategorie Unrated verwendet, zeigen den Text "No Rating Provided" (Keine Bewertung bereitgestellt) im Spiele-Explorer an und unterliegen der Einstellung **Game Restrictions (Spieleinschränkungen)** unter **Jugendschutz** für nicht bewertete Spiele. Die Standardeinstellung **Einschränkungen** ist Zulassen.

Bewertungsinformationen in der GDF werden ignoriert, wenn die enthaltende Binärdatei nicht ordnungsgemäß authenticode signiert ist. Siehe Anforderung 2.3.

Der Game Definition File Editor im DirectX SDK enthält alle unterstützten Bewertungssysteme und repliziert diese Informationen ordnungsgemäß in alle lokalisierten Versionen der GDF sowie in eine sprachneutrale Version. Das GDFTrace-Tool decodiert und überprüft alle vorhandenen Bewertungsinformationen. Verwenden Sie die Version august 2009 oder höher dieser Tools.

Die GDF für einen Spieleanbieter enthält in der Regel keine Bewertungsinformationen und unterliegt den Einstellungen für nicht bewertete Inhalte.




| Betriebssystem | Unterstützte Bewertungssysteme | 
|------------------|--------------------------|
| Windows Vista | <ul><li>CERO (Japan)</li><li>ESRB (USA)</li><li>OFLC (Australien)</li><li>PEGI (Europa)</li><li>PEGI-Schweiz (veraltet)</li><li>PEGI Portugal</li><li>PEGI/BBFC (Vereinigtes Königreich)</li><li>USK (Deutschland)</li></ul> | 
| Windows Vista mit einem Service Pack | Service Packs für Windows Vista bieten Unterstützung für Folgendes:<br /><ul><li>GRB (Südkorea)</li><li>ESRB-Variantinhaltsdeskriptoren "Soll"</li></ul> | 
| Windows 7 | Windows 7 unterstützt die von Windows Vista unterstützten Bewertungssysteme und fügt Unterstützung für Folgendes hinzu: <br /><ul><li>CSRR (Taiwan)</li></ul> | 
| Windows 8 | Windows 8 unterstützt die vorherigen Bewertungssysteme und fügt Unterstützung für Folgendes hinzu:<br /><ul><li>COB-AU (Australien)</li><li>DJCTQ (Brasilien)</li><li>PFB (Südafrika)</li><li>OFLC-NZ (Neuseeland)</li></ul>Windows 8 wird die Unterstützung für die folgenden jetzt veralteten Systeme eingestellt:<br /><ul><li>PEGI-FI (Spanien)</li><li>OFLC (Australien)</li></ul> | 




 

> [!Note]  
> Jeder Titel, der neue ESRB Windows Vista Service Pack 1 (SP1)-Inhaltsdeskriptoren enthält, wird in Windows Vista ohne Service Pack als Nicht mitRating angezeigt.

 

Neuere Bewertungsdaten werden in Versionen von Betriebssystemen ignoriert, ohne sie zu unterstützen. Die PEGI-Variante (Europe) ist jetzt zugunsten des standardmäßigen PEGI-Bewertungssystems (Europe) veraltet. Das OFLC-System ist jetzt zugunsten von COB-AU für Australien veraltet.

Weitere Informationen dazu, wie Sie ein Spiel mit Standardbenutzerberechtigungen kompatibel machen, finden Sie im DirectX-Artikel [Benutzerkontensteuerung für Spieleentwickler.](/windows/desktop/DxTechArts/user-account-control-for-game-developers)

Weitere Informationen zur Spieldefinitionsdatei (GDF) finden Sie unter Anforderung 1.1.

</dd> </dl>

### <a name="13-support-rich-saved-games"></a>1.3 Unterstützung von Rich Saved Games

\[Diese Anforderung wurde nicht mehr erfüllt.\]

### <a name="14-support-the-xbox-360-common-controller-for-windows-conditional-requirement"></a>1.4 Unterstützung des Xbox 360 Common Controller für Windows \[ Bedingung\]

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Spiele, die Gamepad-Controller unterstützen, müssen die Xbox 360 Controller für Windows [XInput-API](/windows/desktop/xinput/xinput-game-controller-apis-portal) unterstützen. Wenn auch DirectInput-Peripheriegeräte unterstützt werden, kann DirectInput auch verwendet werden. XInput muss jedoch die Standard-API sein, wenn ein Xbox 360 kompatibles Gerät verwendet wird.

Alle Verweise auf allgemeine Controllertrigger und Schaltflächen müssen die Xbox 360 verwenden. Weitere Informationen [finden Xbox 360 common controller for Windows Terminologieliste.](#xbox-360-common-controller-for-windows-terminology)

Controller-Vibration muss deaktiviert werden, wenn sich das Spiel in einem angehaltenen oder angehaltenen Zustand befindet.

Die Maus-/Tastatursteuerung kann zu einem beliebigen Zeitpunkt nicht vollständig deaktiviert werden. Es muss mindestens eine Option zur Rückkehr zu Spielmenüs verfügbar sein.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Diese Anforderung gibt Gamern die Wahl, entweder den Xbox 360-Controller oder die Tastatur und Maus zu verwenden, je nachdem, welche Eingabemethode natürlicher und intuitiver ist.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Diese Anforderung gilt nicht für Spiele, die nur die Maus und/oder die Tastatur verwenden.

Es wird empfohlen, die Menünavigation so zu verwenden, dass die allgemein akzeptierten Standardcontrollerschaltflächen verwendet werden:

-   A – Akzeptieren
-   B – Abbrechen
-   Start: Akzeptieren oder Anhalten
-   Zurück– Abbrechen, Sichern eines Bildschirms oder einer Menüebene

Weitere Informationen finden Sie unter [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal).

Im Thema [XInput und DirectInput](/windows/desktop/xinput/xinput-and-directinput) werden Probleme bei der gleichzeitigen Verwendung beider APIs erläutert.

Es wird empfohlen, DirectInput nicht zum Implementieren von Tastatur- oder Maussteuerelementen zu verwenden. Tastatur- und Maussteuerelemente sollten nur mithilfe von Windows und Win32-APIs implementiert werden. Weitere Informationen zum Abrufen von informationen zur Mausbewegung mit hoher Auflösung ohne DirectInput finden Sie unter Nutzen High-Definition [Mausbewegung.](/windows/desktop/DxTechArts/taking-advantage-of-high-dpi-mouse-movement)

</dd> </dl>

### <a name="15-support-multiple-aspect-ratios-and-resolutions"></a>1.5 Unterstützung mehrerer Seitenverhältnisse und Auflösungen

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Das Spiel muss mindestens die folgenden Seitenverhältnisse und die zugehörigen Bildschirmauflösungen unterstützen:

-   4:3 normal (800 600 oder 1024 768)
-   16:9 Widescreen (1280 720)
-   16:10 Widescreen (1152 720 oder 1680 1050 oder 800 480)

Für die Konfiguration und Erkennung der Bildschirmauflösung muss das Spiel die folgenden Regeln einhalten:

-   Das Spiel verwendet standardmäßig die Desktopauflösung des Anzeigegeräts, wenn es sich um eine unterstützte Auflösung handelt. Das Desktop-Seitenverhältnis muss als Suchkriterium verwendet werden, wenn das Spiel eine andere Standardauflösung auswählt.
-   Das Spiel muss den Benutzer auffordern, neue Anzeigeeinstellungen zu bestätigen, wenn eine Änderung vorgenommen wird. Wenn der Benutzer nicht innerhalb von 15 Sekunden akzeptiert, muss die Anzeige auf die vorherige Einstellung zurückverwenden.
-   Das Spiel darf keine Pixel strecken oder ein 4:3-Renderfenster zentriert werden, um Breitbildschirm-Seitenverhältnisse zu unterstützen. Letterboxing ist jedoch akzeptabel.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Beim Windows 3D-Desktop kann aufgrund der folgenden Faktoren nicht von einem bestimmten Seitenverhältnis oder einer bestimmten Auflösung ausgegangen werden:

-   Unterstützung für Anzeige mit hohen Details.
-   Größerer Marktanteil von Widescreen-Monitoren.
-   MEDIEN-Bereitstellungen für Windows Media Center.
-   Anforderungen an die Barrierefreiheit.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Im Idealfall verwendet das Spiel standardmäßig das native Seitenverhältnis der Anzeige. Das zuverlässige Abrufen dieser Informationen kann jedoch eine Herausforderung darstellen, sodass das Spiel als allgemeinere Lösung davon ausgehen kann, dass der Desktop mit dem nativen Seitenverhältnis ausgeführt wird. Die Desktopauflösung kann durch Aufrufen von [**EnumDisplaySettings mit**](/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa) ENUM \_ REGISTRY SETTINGS ermittelt \_ werden.

Weitere Informationen finden Sie in den Abschnitten Seitenverhältnis und Widescreen des [DirectX-Artikels Introduction to the 10-Foot Experience for Windows Game Developers](/windows/desktop/DxTechArts/introduction-to-the-10-foot-experience-for-windows-game-developers).

</dd> </dl>

### <a name="16-support-launch-from-windows-media-center"></a>1.6 Supportstart über Windows Media Center

\[Diese Anforderung wurde nicht mehr erfüllt.\]

### <a name="17-direct3d-support"></a>1.7 Direct3D-Unterstützung

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Wenn das Spiel Direct3D verwendet, muss die unterstützte Mindestversion Direct3D 9 und Direct3D der ausgewählte Standardrenderer sein.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Die Windows Vista und Windows 7-Kern-Grafikarchitektur sind auf Direct3D ausgelegt. Direct3D 8 und frühere Versionen werden unterstützt, indem legacy-Schnittstellen neu gelten.

Die Verwendung von Direct3D-Versionen, die neuer als Direct3D 9 sind, wird dringend empfohlen. Weitere Informationen finden Sie unter Games for Windows Showcase S.1. Das Erfordern von Direct3D 10 oder Direct3D 11 ist vollständig konform mit Anforderung 1.7.

</dd> </dl>

### <a name="18-enable-high-dpi-aware"></a>1.8 Aktivieren von "High-DPI-Aware" (Hohe DPI-Leistung)

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Spiele und ihre Installationsprogramme müssen ohne visuelle Probleme ordnungsgemäß ausgeführt werden, wenn die DPI-Skalierung (Dots-per-Inch) aktiviert ist (getestet mit 144 DPI für eine Skalierung von 150 % bei einer Anzeigeauflösung von 1600 1200) auf Windows Vista und Windows 7).

Dies erfordert in der Regel, dass die ausführbare Datei des Spiels deklarieren muss, dass sie DPI-bewusst ist. Dies wird durch ein Einbetten eines Manifestelements <dpiAware> erreicht: true <dpiAware> .

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

HOCHWERTIGE MONITORE sind üblich, wenn Computer angezeigt werden, und sie sehen am besten aus, wenn sie mit ihren nativen Auflösungen gesteuert werden (in der Regel 1280 1024, 1600 1200 und so weiter). Kunden, die Schwierigkeiten beim Lesen von Text und beim Anzeigen von Bildern mit dieser Auflösung haben, legen ihre Computerdesktops häufig auf eine niedrigere Auflösung fest und erhalten visuelle Artefakte durch die SKALIERUNG von DISPLAYS. Stattdessen können Kunden die Auflösung bei der nativen Größe be lassen und den DPI-Anteil der Windows ändern, wodurch die Darstellung von Element und Text größer wird, ohne die Bildqualität zu einbußen.

Dieses Feature ist zwar seit der Windows XP in irgendeiner Form verfügbar, wird jedoch nur selten von Kunden oder OEMs aktiviert. Mehr als die Hälfte aller Computeranzeigen ist heute basierend auf Kundenfeedback auf eine niedrigere Auflösung als die native Auflösung des Monitors festgelegt. Windows 7 macht dieses Feature für Kunden bei der anfänglichen Einrichtung und beim Ändern der Anzeigeeinstellungen deutlich sichtbarer, und sie werden dazu ermutigen, die DPI-Skalierung zu verwenden, anstatt die Desktopauflösung zu ändern.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Die [**SetProcessDPIAware-Funktion**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) kann stattdessen verwendet werden, wenn sie früh im Prozessstartcode aufgerufen wird. Das Hinzufügen zum Manifest wird bevorzugt, um sicherzustellen, dass keine Racebedingungen mit Softwareelementen (z. B. DLLs) vor dem Aufruf des Haupteinstiegspunkts initialisiert werden. Beachten **Sie, dass SetProcessDPIAware** nur auf Windows Vista und Windows 7 vorhanden ist.

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

Fügen Sie dann in Visual Studio "dpiware.manifest" zum Projekt hinzu. Stellen Sie **sicher, dass Manifest einbetten** in **den** Eigenschaften des Projekts auf Ja festgelegt ist. Beachten Sie, dass ältere Versionen des Manifesttools (Mt.exe) eine falsche Warnung mit den DPI-orientierte Manifestelementen generieren. Um dies zu beheben, aktualisieren Mt.exe aus dem Windows SDK auf die neueste Version.

Visual Studio 2010 enthält eine Einstellung in den Projekteigenschaften mit dem Namen **Enable DPI Awareness (DPI-Bewusstsein** aktivieren), die eine Datei wie dpiaware.manifest nicht mehr benötigt. Suchen **Sie enable DPI Awareness (DPI-Bewusstsein** aktivieren), indem Sie **Konfigurationseigenschaften** und **Manifesttool erweitern** und dann Eingabe und & **auswählen.**

Bei Windows ist der herkömmliche Anzeigemodus standardmäßig auf 96 DPI festgelegt, was bei CRT-Monitoren üblich war.

Während Vollbildanwendungen die Anzeigeauflösung ändern, verwenden sie beim Einrichten von Puffern und Anzeigerechtecken häufig Fenstermeldungen und Metriken. Die DPI-Virtualisierung bewirkt, dass diese Vollbildanzeigemodi zugeschnitten angezeigt werden, und das Deklarieren von DPI-orientiertem Modus verhindert diese Probleme. Weitere Informationen finden Sie unter [Schreiben DPI-Aware Win32-Anwendungen](../hidpi/high-dpi-desktop-application-development-on-windows.md).

</dd> </dl>

## <a name="security-and-compatibility"></a>Sicherheit und Kompatibilität

**Zusammenfassung der Sicherheits- und Kompatibilitätsanforderungen**

**Kundenvorteile**

Die folgenden Anforderungen verbessern die allgemeine Sicherheit von Spielen und tragen dazu bei, dass sie mit Windows in verschiedenen Architekturen, unter verschiedenen Konfigurationen und in unterschiedlichen Modi funktionieren.

### <a name="21-follow-user-account-control-guidelines"></a>2.1 Befolgen Sie die Richtlinien für die Benutzerkontensteuerung.

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Jede ausführbare Datei (d. h. jede Datei mit der Erweiterung .exe) muss ein eingebettetes Manifest enthalten, das die Ausführungsebene durch Das folgende Tag definiert:

``` syntax
            <requestedExecutionLevel>
```

Nach Anforderung 1.2 müssen das Hauptspiel und die ausführbare Autoun-Datei die Ausführungsebene asInvoker haben, um Standardbenutzerkontexte zu unterstützen.

Benutzerdatendateien mit Dateizuordnungen, die im **Datei-Explorer** registriert sind, müssen in einem Unterordner des Ordners platziert werden, der von CSIDL PERSONAL angegeben wird (auch als Dokumente oder \_ Eigene Dokumente).   Alle anderen Benutzerdatendateien müssen in einem Unterordner der Ordner gespeichert werden, die von CSIDL LOCAL APPDATA oder \_ \_ CSIDL \_ COMMON \_ APPDATA angegeben werden. (Diese Verzeichnisse werden standardmäßig für einzelne Benutzer und für alle Benutzer ausgeblendet.)

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Die Benutzerfreundlichkeit Windows benutzerfreundlicher, wenn Anwendungen nur mit den erforderlichen Berechtigungen ausgeführt werden.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Wenn nur einige Features in einer Anwendung Administratorrechte erfordern (z. B. eine Anwendung, die eine Firewall konfigurieren muss), muss der Hauptprozess der Anwendung weiterhin mithilfe von Standardbenutzerberechtigungen ausgeführt werden. Features, die Administratorrechte erfordern, müssen in einen separaten Prozess verschoben werden, z. B. ein Installationsprogramm oder ein Konfigurations-Hilfsprogramm.

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

Mit Visual Studio 2005 kann dies problemlos eingebettet werden, indem einfach eine Manifestdatei (.manifest) hinzugefügt  wird, die einen der vorherigen Blöcke zum Projekt enthält, und um sicherzustellen, dass Manifest einbetten **in** den Projekteigenschaften für Manifesttool auf Ja festgelegt ist. Für Visual Studio 2008 und 2010 können UAC-Eigenschaften direkt in den Projekteigenschaften für den Linker auf der Seite **Manifestdatei festgelegt** werden. Beachten Sie, dass ältere Versionen des Manifesttools (manifest tool, Mt.exe) eine falsche Warnung mit den UAC-Manifestelementen generieren. Um dies zu beheben, aktualisieren Mt.exe aus dem Windows SDK auf die neueste Version.

Unter Anforderung 3.1 finden Sie Details zu den speziellen Fällen von Installation, Patchen und Entfernen.

Dynamic Link Libraries (DLLs) erfordern keine solchen Manifeste.

Weitere Informationen zur Benutzerkontensteuerung finden Sie unter [Benutzerkontensteuerung für Spieleentwickler.](/windows/desktop/DxTechArts/user-account-control-for-game-developers)

</dd> </dl>

### <a name="22-support-windows-x64-versions"></a>2.2 Unterstützung Windows x64-Versionen

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Um die Kompatibilität mit 64-Bit-Editionen von Windows, sollten Spiele die folgenden Anforderungen erfüllen.

-   Titel- und Titelinstallationsprogramme dürfen keinen 16-Bit-Code enthalten oder 16-Bit-Komponenten verwenden.
-   Wenn das Spiel für den Betrieb von Kernelmodustreibern abhängig ist, müssen x64-Versionen dieser Treiber verfügbar sein. Das Spielsetup muss die richtigen Treiber und Komponenten für die 64-Bit-Editionen von Windows.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Viele Windows Vista- und Windows 7-Benutzer führen während der Lebensdauer des Produkts 64-Bit-Editionen des Betriebssystems aus. Daher ist es entscheidend, dass Anwendungen mit diesem Betriebssystem kompatibel sind.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Windows unter Windows 64 (WOW64) ermöglicht die Ausführung von 32-Bit-Code auf 64-Bit-Editionen von Windows, sodass es nicht erforderlich ist, dass die Anwendung nativen 64-Bit-Code auf 64-Bit-Editionen von Windows. 64-Bit-Code wird nicht auf 64-Bit-Editionen von Windows.

Die Aufrechterhaltung der Windows XP Professional x64 Edition ist nicht erforderlich, wird jedoch dringend empfohlen.

Weitere Informationen finden Sie unter [64-Bit-Programmierung für Spieleentwickler.](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers)

</dd> </dl>

### <a name="23-sign-files"></a>2.3 Signieren von Dateien

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Alle ausführbaren Codedateien (in der Regel Dateien mit der Erweiterung .exe oder .dll) müssen mit einem öffentlich gültigen Authenticode-Zertifikat signiert sein und über eine gültige Zeitstempelserver-URL für die Produktionssignatur verfügen.

Wenn Ihr Spiel Windows Installer verwendet, müssen die Installationspaketdateien (.msi-Dateien) signiert sein.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Das Signieren einer Datei hilft Benutzern bei der Entscheidung, ob sie einer Anwendung vertrauen, und stellt sicher, dass Dateien nicht manipuliert wurden. Außerdem können Anwendungen in gesperrten Umgebungen ordnungsgemäß ausgeführt werden.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Weitere Informationen finden Sie unter [Authenticode Signing for Game Developers (Authenticode-Signierung für Spieleentwickler).](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)

Wenn Ihr Spiel Windows Installer verwendet, empfiehlt es sich, das Patchen von UAC/LUA zu aktivieren, indem Sie eine MsiPatchCertificate-Tabelle verwenden. Weitere Informationen finden Sie unter [Patchen von Benutzerkontensteuerung (User Account Control, UAC).](/windows/desktop/Msi/user-account-control--uac--patching)

Es wird nicht empfohlen, .cab-Dateien zu signieren, es sei denn, sie sind relativ klein (weniger als 100 MB).

</dd> </dl>

### <a name="24-sign-drivers"></a>2.4 Signieren von Treibern

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Jeder Kernelmodustreiber, der vom Spiel installiert wird, muss mit einem öffentlich gültigen Authenticode-Zertifikat signiert werden.

Jeder Hardwaregerätetreiber im Kernelmodus, der vom Spiel installiert wird, muss über eine Microsoft-Signatur verfügen, die aus den Windows Hardware Quality Labs (WHQL) oder dem DrS-Programm (Driver Reliability Signature) erhalten werden kann.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Schlecht geschriebene Treiber oder Schadsoftwaretreiber können die Stabilität und Sicherheit eines Systems erheblich beeinträchtigen. In 64-Bit-Editionen von Windows Vista und Windows 7 werden nicht signierte Treiber nicht geladen. Diese Richtlinie kann auch für 32-Bit-Editionen von Windows Vista und Windows 7 aktiviert werden.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Sowohl native 32-Bit- als auch 64-Bit-Versionen aller Kernelmodustreiber werden pro Anforderung 2.2 benötigt.

Weitere Informationen zu Microsoft-Treibersignaturprogrammen finden Sie im [Windows-Entwicklerportal.](https://www.microsoft.com/whdc/winlogo/hwrequirements.mspx)

</dd> </dl>

### <a name="25-perform-proper-version-checking"></a>2.5 Durchführen der richtigen Versionsprüfung

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Spiele dürfen nicht auf zukünftigen Betriebssystemen ausgeführt werden, wie durch Änderungen an der Windows-Versionsnummer angegeben, es sei denn, der Endbenutzer-Lizenzvertrag untersagt die Verwendung auf zukünftigen Betriebssystemen. Wenn das Spiel fehlschlagen soll, muss es dies ordnungsgemäß tun, indem dem Benutzer eine entsprechende Meldung angezeigt wird.

Wenn Windows Versionsprüfung durchgeführt wird, müssen die APIs zur Versionsüberprüfung ([**GetVersionEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa) oder [**VerifyVersionInfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa)) verwendet werden, um die Betriebssystemversion zu überprüfen. Registrierungsschlüssel dürfen nicht gelesen werden, um die Version zu bestimmen.

Explizite Versionsprüfungen für die DirectX-Runtime dürfen nicht im Spiel vorhanden sein. Diese Versionsüberprüfungen dürfen nicht in der Installation vorhanden sein, die das DirectX-Laufzeitsetup (DirectSetup) startet.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Wenn Windows Betriebssystem aktualisieren, sollten sie nicht daran blockiert werden, aktuelle Spiele zu spielen, einfach weil Windows Versionsnummer erhöht wurde. Schlecht geschriebene Versionsüberprüfungen verursachen weiterhin Probleme mit Software, die andernfalls in neueren Versionen von Windows oder einfach mit dem Zusatz eines service packs Windows funktioniert.

Die Vergleichslogik für die Vergleichslogik der Schwachversionsprüfung für die DirectX-Runtime hat zahlreiche fehlerhafte Installationen erstellt, wenn sie in verschiedenen Versionen von Windows. Die DirectX-Versionsnummer gilt nur für die Kernkomponenten des Betriebssystems. Sie gilt nicht für die komponentenseitigen DirectX SDK-Komponenten, die von vielen Spielen verwendet werden.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Es ist üblich, zu sehen, dass Installationsprogramme eine Mindestversion des Betriebssystems überprüfen. Diese Überprüfung muss jedoch mit Vorsicht durchgeführt werden, um sicherzustellen, dass sie auf mehr als oder gleich testet und nicht auf einfache Gleichheit, wodurch eine bestimmte Version des Betriebssystems gesperrt wird. Die Application Verifier **HighVersionLie** von Application Verifier ist eine schnelle und einfache Möglichkeit, um zu bestimmen, wie Ihr Installationsprogramm auf eine erhebliche Änderung der Betriebssystemversionsnummer reagiert.

Bei der ordnungsgemäßen Verwendung des DirectX-Laufzeitverteilungspakets (DirectX-Setup) wird es immer während der Installation gestartet, vorzugsweise im automatischen Modus. Dadurch kann der von Microsoft bereitgestellte Code alle erforderlichen Versionsupdates ausführen. Sie ermöglicht auch die Installation optionaler, nebeneinander verfügbarer DirectX SDK-Komponenten wie D3DX, XACT, MDX oder XInput.

Bewährte Methoden für die Bereitstellung der DirectX-Runtime finden Sie unter [DirectX-Installation für Spieleentwickler.](/windows/desktop/DxTechArts/directx-setup-for-game-developers)

Es wird empfohlen, dass Spiele, die Windows XP unterstützen, nach einer Service Pack-Ebene von 2 oder höher prüfen, da Service Pack 2 (SP2) und Service Pack 3 (SP3) erhebliche Sicherheitsverbesserungen, eine vereinfachte DirectX Runtime Redistribution-Anforderung und eine äußerst umfassende Bereitstellung bieten. Die meisten modernen Microsoft-Technologien, die Windows XP unterstützen, erfordern SP2 oder SP3 (XAudio2, Games for Windows – LIVE und so weiter).

</dd> </dl>

### <a name="26-support-concurrent-user-sessions"></a>2.6 Unterstützung gleichzeitiger Benutzersitzungen

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Spiele, die auf 3D-Grafiken basieren, sind nicht erforderlich, um über eine Remotedesktopverbindung zu arbeiten, aber der Benutzer muss benachrichtigt werden, wenn das Spiel ausfällt.

Spiele müssen standardmäßige Windows multitasking-Szenarien unterstützen, indem sie die folgenden Regeln einhalten:

-   Spiele dürfen die Verwendung von gleichzeitigen Benutzersitzungen nicht blockieren.
-   Ein Spiel muss in einer neuen Benutzersitzung ausgeführt werden, wenn es bereits in einer anderen Sitzung ausgeführt wird.
-   Spielsound in einer Benutzersitzung darf nicht gehört werden, wenn ein anderer Benutzer in einer anderen Sitzung aktiv ist.
-   Spiele müssen schnelle Benutzerwechsel unterstützen.
-   Spiele dürfen nicht versuchen, den Standard-Aufgabenwechsel zu deaktivieren. Spiele dürfen die Tastenkombination ALT+TAB nicht deaktivieren. Spiele dürfen Tastenkombinationen für die Barrierefreiheit deaktivieren, wie unter [Deaktivieren von Tastenkombinationen in Games beschrieben.](/windows/desktop/DxTechArts/disabling-shortcut-keys-in-games)

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Windows Benutzer sollten gleichzeitige Sitzungen ohne Konflikte oder Unterbrechungen ausführen können. Dies ist ein häufiges Szenario für einen Windows, der von einer Familie, Mitinsassen oder anderen gemeinsam genutzt wird.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Um zu testen, ob das Spiel in einer Remotesitzung gestartet wird, rufen [**Sie GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)(SM \_ REMOTESESSION) auf. Ein Wert ungleich 0 (null) gibt an, dass die Sitzung remote ist.

Weitere Informationen finden Sie unter [Schneller Benutzerwechsel.](/windows-hardware/drivers/display/fast-user-switching) Beachten Sie, dass ein schneller Benutzerwechsel erfolgt, wenn Die Zeiteinschränkungen der Elternsteuerung aktiviert sind, wenn die Zeit des Benutzers aktiv ist. Weitere Informationen finden Sie unter Anforderung 1.2.

</dd> </dl>

### <a name="27-support-long-names"></a>2.7 Unterstützung für lange Namen

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Wenn ein Spiel das Speichern von Dateien unterstützt, muss es in der Lage sein, Dateien mit langen Namen und Pfaden zu speichern. Das Spiel muss spezielle Dateisystemzeichen ordnungsgemäß verarbeiten, z. B. \\ / : \* ? " < > in allen Benutzereingabefeldern, die zum Erstellen von Dateinamen oder Pfaden verwendet werden.

Spiele müssen ordnungsgemäß funktionieren, wenn ein Benutzer über einen langen Benutzernamen verfügt.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Player sind daran gewohnt, lange Namen auf tiefen Pfaden zu verwenden, die vom zugrunde liegenden Betriebssystem unterstützt werden.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Lange Namen werden als namen definiert, die die maximalen Werte enthalten, die im Windows WERDEN.

</dd> </dl>

## <a name="installation"></a>Installation

**Zusammenfassung der Sicherheits- und Kompatibilitätsanforderungen**

**Kundenvorteile**

Kunden können sicher sein, dass Anwendungen auf Windows installiert werden, ohne das Betriebssystem oder andere Anwendungen zu herabsetzen, wenn Anwendungen offizielle Verteilungsmethoden für Systemkomponenten verwenden. Eine optimierte Installationserfahrung bietet eine zugänglichere und problemlosere Vor-/Aus-Erfahrung für Spiele.

### <a name="31-support-easy-installation"></a>3.1 Unterstützung der einfachen Installation

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Spiele müssen einen vereinfachten Pfad in der Setup-Benutzeroberfläche bereitstellen, indem Folgendes implementiert wird:

-   Maximal eine EuLA-Eingabeaufforderung anzeigen.
-   Der Standardinstallationspfad muss alle Auswahlen für die Installation (z. B. Installationsordner oder Komponentenauswahl) umgehen, die Standardauswahl annehmen und das Spiel oder Startfeld nach erfolgreicher Installation ohne zusätzliche Eingabeaufforderungen ausführen. Bei Wunsch kann eine benutzerdefinierte Installationsoption für erweiterte Konfigurationsoptionen bereitgestellt werden.
-   Installieren Sie alle erforderlichen Betriebssystemkomponenten (z. B. DirectX- und Visual C-Runtimes) mithilfe der richtigen Microsoft-Neuverteilungspakete. Die Installation sollte ohne Aufforderung und ohne Schutz durch Komponentenversionsüberprüfungen im Hintergrund ausgeführt werden.
-   Stellen Sie das **Entfernen über Programme und Features** in **Systemsteuerung** sowohl für die Spieleanwendung als auch für generierte Arbeitsdateien zur Verfügung. Eine Option zum Löschen von Datendateien, die vom Benutzer erstellt werden, wird empfohlen. Der Entfernungsprozess muss sicherstellen, dass alle installierten Dateien entfernt und alle Einstellungen (z. B. Einträge in der Firewallausnahmeliste und Registrierungsschlüssel) gelöscht werden. Neu verteilte Betriebssystemkomponenten dürfen nicht entfernt werden.
-   Wenn für das Spiel Ausnahmen zur Windows Firewall hinzugefügt werden müssen, kann der Setupprozess benutzeraufforderungsaufforderungen, dass diese Änderung erforderlich ist. Diese Aufforderung sollte angezeigt werden, bevor die Installation beginnt.

Installation und Entfernung können Administratorrechte erfordern. Für das Patchen kann je nach Aktualisierungshäufigkeit eine Aufforderung zur Eingabe von Administratoranmeldeinformationen erforderlich sein. Die normale Wiedergabe des Spiels darf keine Administratorrechte erfordern, wie in Anforderung 2.1 unter Befolgen der Richtlinien zur Benutzerkontensteuerung festgelegt.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Die einfache Installation ist eine Windows-zentrierte Spielentwicklungsgedanke, die entwickelt wurde, um den manchmal mühsamen und verwirrenden Prozess der Installation von Spielen auf Computern zu vereinfachen und zu optimieren, auf denen Windows ausgeführt werden. Die einfache Installation wird durch die Verwendung einer Reihe von Technologien und bewährten Methoden ermöglicht, die die unnötige Komplexität und das wahrgenommene Risiko der Installation von Spielen auf Windows reduzieren.

Die wichtigsten Ziele sind:

-   Reduzieren Sie die Zeit, um in das Spiel zu kommen und mit dem Spielen zu beginnen.
-   Reduzieren Sie die Anzahl der Dialogfelder und Optionen auf sehr wenige oder keine, um die Spielinstallation zu vereinfachen.

Einige herkömmliche Installationen verfügen über Eingabeaufforderungen, die nicht funktionsfähige Installationen zulassen, obwohl die Anwendung scheinbar erfolgreich installiert wurde. Beispielsweise kann ein Spiel erfordern, dass ein Benutzer einen EuLA akzeptiert. Das Spiel wird dann installiert, und dann wird der DirectX-EULA angezeigt. Mit diesem EuLA können Benutzer die Installation der DirectX-Runtime ablehnen und somit überspringen. Dieses Szenario kann zu einem Spiel führen, das aufgrund fehlender Komponenten nicht ausgeführt werden kann.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Weitere Informationen zur Spieleinstallation, zu nicht herkömmlichen Spielinstallationstechniken, zu UAC-kompatiblen Patchlösungen und zur Behandlung häufiger Patches finden Sie in den folgenden DirectX-Artikeln:

-   [Vereinfachen der Spieleinstallation](/windows/desktop/DxTechArts/simplifying-game-installation)
-   [Install-on-Demand für Spiele](/windows/desktop/DxTechArts/install-on-demand-for-games)
-   [Patchen von Spielsoftware in Windows XP, Windows Vista und Windows 7](/windows/desktop/DxTechArts/patching-methods-in-windows-xp-and-vista)
-   [Bewährte Methoden für die Installation von Massively Multiplayer Online Games](/windows/desktop/DxTechArts/mmo-installation-best-practices)

> [!Note]  
> Das Entfernen von benutzerspezifischen generierten Datendateien sollte nur für den aktuellen Benutzer und für gemeinsame freigegebene Benutzerstandorte ausgeführt werden. Es gibt keine stabile Möglichkeit, das System zu überprüfen, um benutzerspezifische Dateien für andere Benutzer zu entfernen, auch wenn das Entfernen Administratoranmeldeinformationen erfordert.

 

</dd> </dl>

### <a name="32-support-user-account-control-for-installation"></a>3.2 Unterstützung der Benutzerkontensteuerung für die Installation

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Der Spieleinstaller darf nicht davon ausgehen, dass er im gleichen Kontext wie der Benutzer ausgeführt wird. Benutzerspezifische Speicherorte unterscheiden sich aufgrund der Erhöhung der Administratoranmeldeinformationen vom Installationsprogramm und Player auch für Einzelbenutzersysteme. Wenn ein Spiel zum ersten Mal ausgeführt wird, muss es daher benutzerspezifische Aufgaben unabhängig vom Installationsprozess ausführen.

Das Windows Firewallausnahmedialogfeld darf nicht angezeigt werden, wenn ein Benutzer ein Multiplayerspiel hostet oder beitritt. Alle erforderlichen Konfigurationen müssen zum Zeitpunkt der Installation erfolgen. Die Setupanweisungen sollten den Benutzer darüber informieren, dass dieser Vorgang im Rahmen des Setups erfolgt.

Das Spieleinstallationsprogramm muss ein eingebettetes Manifest bereitstellen, das die erforderliche Ausführungsebene gemäß Anforderung 2.1 gemäß den Richtlinien zur Benutzerkontensteuerung bestimmt.

Wenn das Spiel nach Abschluss der Installation vom Installationsprogramm gestartet wird, muss es im Kontext des ursprünglichen Benutzers gestartet werden.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Eine der größten Änderungen am Windows-Betriebssystem in Windows Vista ist die Ergänzung der Benutzerkontensteuerung (User Account Control, UAC), mit der Anwendungen standardmäßig mit reduzierten Berechtigungen ausgeführt werden. Daher müssen Installationsprogramme Berechtigungsebenen entsprechend verwalten. Windows 7 wird auch die UAC umfassend verwendet. Während Windows 7 die Benutzerfreundlichkeit von UAC verbessert, müssen Installationsprogramme weiterhin die gleichen Anforderungen wie unter Windows Vista erfüllen, um ordnungsgemäß zu funktionieren, ohne sich auf potenziell verwirrendes Virtualisierungsverhalten verlassen zu müssen.

Die UAC ist in Windows Vista und Windows 7 standardmäßig aktiv, und die große Mehrheit der Kunden (88 % oder mehr, basierend auf Feedback) lässt dieses Feature aktiviert.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Weitere Informationen zum Konfigurieren der Windows Firewall finden Sie im DirectX-Artikel [Windows Firewall für](/windows/desktop/DxTechArts/games-and-firewalls) Spieleentwickler und im Beispiel FirewallInstallHelper.

Der Standardstart des Spiels am Ende des Installationsprozesses erfüllt nicht den letzten Aspekt dieser Anforderung, wenn die Installation von einem Standardbenutzer gestartet wird und der Setupprozess Administratorrechte erfordert (d. h. zur Eingabe von Administratoranmeldeinformationen aufgefordert wird). Außerdem werden Administratorrechte geerbt, was ein potenzielles Sicherheitsrisiko darstellen kann. Stattdessen sollte ein Setup-Bootstrapladeprogramm das Spiel starten, nachdem es nach einem erfolgreichen Aufruf des Installationsprogramms zurückgekehrt wurde. Weitere Informationen finden Sie im MSDN Magazine-Artikel [Teach Your Apps to Play Nicely with Windows Vista User Account Control](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control).

</dd> </dl>

### <a name="33-install-to-correct-folders"></a>3.3 Installieren in korrekten Ordnern

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Spiele, die für alle Benutzer installiert werden, müssen standardmäßig im Ordner Programme installiert werden. Benutzerdaten müssen geschrieben werden, wenn das Spiel zum ersten Mal ausgeführt wird, nicht während der Installation.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Benutzer sollten die Flexibilität haben, Anwendungen dort zu installieren, wo sie sie benötigen. Außerdem sollten sie über eine konsistente und sichere Umgebung mit dem Standardspeicherort von Dateien verfügen.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Spiele können die verschiedenen bekannten Ordnerspeicherorte (z. B. die von CSIDL LOCAL APPDATA und \_ \_ CSIDL \_ COMMON APPDATA angegebenen) verwenden, um erhebliche Mengen von Spieldaten und unterstützende ausführbare Dateien zu speichern, um erweiterte Installations- und Patchszenarien zu \_ implementieren.

Da für die Installation während des Installationsvorgangs für alle Benutzer eine Rechteerweiterung auf ein anderes Benutzerkonto erforderlich sein kann, gibt es keinen richtigen Benutzerspeicherort, an dem Daten zur Installationszeit gespeichert werden. Wenn die Dateiverschlüsselung aktiviert ist, kann nur über das Benutzerkonto, das sie erstellt hat, auf verschlüsselte Dateien zugegriffen werden.

</dd> </dl>

### <a name="34-install-windows-resources-properly"></a>3.4 Ordnungsgemäßes Installieren Windows Ressourcen

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Anwendungen dürfen nicht versuchen, Dateien oder Registrierungsschlüssel zu installieren, die durch Windows Resource Protection (WRP) geschützt sind. Wenn die Anwendung neuere Versionen von Systemkomponenten erfordert, muss sie diese Komponenten mithilfe eines Microsoft Service Packs oder eines von Microsoft genehmigten Installationspakets aktualisieren, das die Systemkomponente enthält. Systemkomponenten dürfen nie neu gepackt werden.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Windows Resource Protection (WRP) wurde entwickelt, um sicherzustellen, dass geschützte Systemressourcen nur mithilfe von von Microsoft genehmigter Installations- oder Updatemechanismen aktualisiert werden. WRP verbessert die Systemzuverlässigkeit, indem sichergestellt wird, dass die Ergebnisse einer Installation vorhersagbar sind.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

WRP ist der Nachfolger von Windows File Protection, der den Großteil der Systemkomponenten schützt, die im Ordner Windows sind. WRP schützt die meisten Registrierungsschlüssel, die Einstellungen für die Erstellung von COM-Objekten speichern. Außerdem werden bestimmte Ordner für die ausschließliche Verwendung durch das Betriebssystem reserviert. Versuche, auf geschützte Ressourcen zu zugreifen, führen in der Regel zu einem Zugriffsverweigerungsfehler.

Weitere Informationen zu bewährten Methoden, wenn die DirectX-Runtime mit einem Spiel bereitgestellt wird, finden Sie im DirectX-Artikel [DirectX-Installation für Spieleentwickler.](/windows/desktop/DxTechArts/directx-setup-for-game-developers)

</dd> </dl>

### <a name="35-avoid-reboots-during-installation"></a>3.5 Vermeiden von Neustarts während der Installation

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Das Spielinstallationsprogramm sollte nicht davon ausgehen, dass die Installation von Windows Komponenten aus Weiterverteilungspaketen einen Neustart erfordert, es sei denn, der Neustart wird durch ein Rückgabeergebnis oder die Microsoft-Dokumentation angegeben.

Wenn das Spielinstallationsprogramm immer einen Neustart erzwingt, muss dies von Microsoft genehmigt werden.

Dialogfelder mit verwendeten Dateien, die in Windows Installer-Paketen enthalten sind, müssen eine Option zum automatischen Schließen von Anwendungen und zum Versuch enthalten, sie nach Abschluss des Setups neu zu starten.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Der Neustart des Systems nach einer Installation ist für Benutzer eine unpraktisch und in der Regel unnötig.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Weitere Informationen finden Sie unter [Using Windows Installer with Restart Manager](/windows/desktop/Msi/using-windows-installer-with-restart-manager).

</dd> </dl>

### <a name="36-use-file-versioning-correctly"></a>3.6 Richtiges Verwenden der Dateiversionsierung

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Das Spielinstallationsprogramm muss ordnungsgemäß überprüfen, um sicherzustellen, dass die neuesten Dateiversionen installiert sind. Die Installation eines Spiels darf niemals Dateien zurückstellen, die Sie nicht erstellen oder die von Anwendungen gemeinsam genutzt werden, die Sie nicht erstellen.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Freigegebene Komponenten und Systemkomponenten werden häufig aktualisiert, um Sicherheitsfixes und erweiterte Funktionen zu erhalten. Eine Installation, die eine ältere Version der aktualisierten Komponenten enthält, sollte nicht zu einem Verlust von Updates und Fehlerbehebungen führen, die bereits angewendet wurden.

</dd> </dl>

### <a name="37-support-autorun-conditional-requirement"></a>3.7 Unterstützung von bedingten \[ Autorun-Anforderungen\]

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Bei Spielen, die auf CD, DVD oder anderen Wechselmedien verteilt werden, die Autorun unterstützen, muss die Anwendung beim erstmaligen Einfügen des Datenträgers automatisch ausgeführt werden oder den Benutzer auffordern, das Spiel zu installieren, es sei denn, der Benutzer hat das Autorun-Feature deaktiviert.

Nachdem die Anwendung erfolgreich installiert wurde, darf das erneute Einfügen des Datenträgers auf dem Laufwerk nicht dazu führen, dass die Installation automatisch erneut gestartet wird. Es ist akzeptabel, Benutzer zu fragen, ob sie ihre Installationsoptionen aktualisieren oder ändern möchten.

Die Autorunanwendung darf nicht zur Erhöhung der Rechte auffordern (d. h. sie muss gemäß Anforderung 2.1 über asInvoker im Manifest verfügen, obwohl sie das Setupprogramm oder ein anderes Hilfsprogramm starten kann, das Administratorrechte erfordert. Erhöhte Rechte sollten nur auftreten, wenn das Spiel nicht installiert ist oder der Benutzer es ausdrücklich auswählt.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Autorun vereinfacht die Verwendung von medienverteilten Anwendungen, wie z. B. Spielen, bei denen die Platte in der Regel im Laufwerk vorhanden sein muss, um das Spiel zu spielen.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Es ist nicht akzeptabel, dass der Benutzer im Datei-Explorer navigiert, um die Installation über die CD oder DVD zu starten.

Bei Spielen, die auf mehreren Datenträgern verteilt sind, sollten nachfolgende Datenträger idealerweise entweder das Autorun-Feature verwenden oder die Installation fortsetzen, ohne den Benutzer aufzufordern, eine Taste zu drücken oder andere Maßnahmen zu ergreifen.

Stellen Sie beim Erstellen eines Autorun-Programms sicher, dass alle erforderlichen Komponenten auf neu installierten Windows vorhanden sind. Typische Anwendungen basieren auf Technologien, die vom Setup installiert werden. Autorun selbst wird jedoch ausgeführt, bevor ein solches Setup durchgeführt wird. Ein häufiges Beispiel ist der Fehler von Autorun-Programmen, da die Visual C-Runtime-DLLs nicht im Rahmen des Windows-Setups enthalten waren. Das Autorun-Programm muss daher die lokale CRT-Bereitstellung der Anwendung verwenden oder die CRT statisch verknüpfen.

Autorun-Programme, die zur Verwendung in Versionen von Windows vor Windows Vista geschrieben wurden, sollten die .NET-Runtime nicht verwenden, da diese Technologie nicht in Windows XP oder älteren Versionen von Windows enthalten ist. Windows Server 2003 und Windows Vista sind die ersten Versionen von Windows, die .NET-Runtime als Teil ihres Betriebssystems enthalten.

Aus ähnlichen Gründen können Autorun-Programme das Vorhandensein von optionalen parallelen DirectX SDK-Komponenten wie D3DX9, D3DX10, D3DX11, XAudio2, X3DAudio, XACT, XINPUT und MDX 1.1 nicht erfordern.

Ein Beispiel für die Verwendung von Autorun finden Sie unter AutoRun Sample.

</dd> </dl>

## <a name="reliability"></a>Zuverlässigkeit

**Zusammenfassung der Sicherheits- und Kompatibilitätsanforderungen**

**Kundenvorteile**

Diese Anforderungen machen eine Anwendung zuverlässiger, indem sie die Anzahl von Abstürzen, Hängen und Neustarts minimiert. Mithilfe der Zuverlässigkeitsanforderungen kann sichergestellt werden, dass Software besser vorhersagbar, wartbar, resilient und wiederherstellbar ist.

### <a name="41-eliminate-unnecessary-reboots"></a>4.1 Vermeiden unnötiger Neustarts

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Alle Anwendungsinstallationsprogramme müssen die Neustart-Manager-APIs nutzen, um Systemneustarts zu vermeiden (siehe Anforderung 3.5).

Spiele dürfen das Herunterfahren nicht blockieren.

Alle Anwendungen müssen auf den Neustart-Manager reagieren, indem sie die folgenden Meldungen zum Herunterfahren überwachen und darauf reagieren:

<dl> <dt>

<span id="WM_QUERYENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_queryendsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_QUERYENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM \_ QUERYENDSESSION mit LPARAM = ENDSESSION \_ CLOSEAPP (0x1) 
</dt> <dd>

GUI-Anwendungen müssen sofort (TRUE) reagieren, um einen Neustart vorzubereiten.

</dd> <dt>

<span id="WM_ENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_endsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_ENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM \_ ENDSESSION mit LPARAM = ENDSESSION \_ CLOSEAPP (0x1) 
</dt> <dd>

Anwendungen müssen innerhalb von 5 Sekunden einen Wert von 0 zurückgeben und dann schließen.

</dd> <dt>

<span id="CTRL_C__"></span><span id="ctrl_c__"></span>STRG+C 
</dt> <dd>

Konsolenanwendungen, die diese Meldung empfangen, müssen sofort geschlossen werden.

</dd> </dl> </dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Systemneustarts stellen eine große Unterbrechung dar. Sie führen zu einer schlechten Benutzererfahrung und sollten minimiert werden. Einige Vorgänge, z. B. kritische Systemupdates, können Neustarts erfordern. Durch lauschen auf Meldungen zum Herunterfahren können das Spiel und andere Anwendungen sofort auf Anforderungen des Neustart-Managers reagieren. Auf diese Weise können sie unnötige Verzögerungen bei gültigen Neustartanforderungen vermeiden.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Wenn ein Spielinstallationsprogramm die Windows Installer-Technologie (MSI) ohne benutzerdefinierte Aktionen verwendet, wird diese Funktionalität automatisch bereitgestellt. Microsoft-Weiterverteilungspakete unterstützen auch den Neustart-Manager.

Weitere Informationen zum Neustart-Manager finden Sie im MSDN-Artikel Informationen zum [Neustart-Manager.](/windows/desktop/RstMgr/about-restart-manager)

</dd> </dl>

### <a name="42-eliminate-application-verifier-failures"></a>4.2 Beseitigen von Application Verifier Fehlern

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Das Spiel darf in den folgenden Tests keine Fehler generieren, die unter Microsoft Application Verifier (AppVerifier), Version 4.0 oder höher, ausgeführt werden:

-   Grundlagen: Handles, Heaps, Sperren, Arbeitsspeicher, TLS
-   Sonstiges: DangerousAPIs, DirtyStacks

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

AppVerifier testet auf viele bekannte Probleme, die abstürzen und in Windows Anwendungen hängen bleiben, sowie auf bekannte Sicherheitsrisiken.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Weitere Informationen zu Application Verifier finden Sie unter [Application Verifier](/previous-versions/ms220948(v=vs.80)) und [Using Application Verifier Within Your Software Development Lifecycle (Verwenden von Application Verifier in Ihrem Softwareentwicklungslebenszyklus)](/previous-versions/aa480483(v=msdn.10)) auf MSDN. Sie können Application Verifier unter [Downloaddetails herunterladen: Application Verifier](https://www.microsoft.com/downloads/details.aspx?familyid=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18) im Microsoft Download Center herunterladen.

Diese Anforderung gilt nicht für reine verwaltete Anwendungen ohne native Interop.

Diese Tests sollten in einem Releasebuild ausgeführt werden. Beim Debuggen von Builds können falsche Fehler generiert werden. Einige Anti-Anti-Cheat-Technologien können die Ausführung von AppVerifier beeinträchtigen. Daher sollten diese Tests ohne aktivierte Anti-Anti-Cheat-Technologien durchgeführt werden.

Es kann erforderlich sein, die Full-Eigenschaft des Basics:Heaps-Tests auf FALSE festzulegen, da die vollständige PageHeap die Arbeitsspeicherauslastung der ausgeführten Anwendung erheblich erhöht. Fehler werden weiterhin erkannt, aber sie können schwieriger nachverfolgt werden, wenn Sie nur teilweise PageHeap verwenden.

Wenn Sie die UAC-/LUA-bezogenen Tests in Application Verifier verwenden, um die Anforderungen an die Benutzerkontensteuerung 2.1 und 3.2 zu erfüllen, sollten Sie die Ergebnisse mithilfe der [Standardbenutzeranalyse](/windows/desktop/Win7AppQual/standard-user-analyzer--sua--tool-and-standard-user-analyzer-wizard--sua-wizard-) überprüfen. Es gibt auch zahlreiche weitere nützliche Tests, die von Application Verifier bereitgestellt werden, die Sie unbedingt in der Entwicklung und bei Tests verwenden sollten, um ein hohes Maß an Kompatibilität mit aktuellen und zukünftigen Versionen von Windows sicherzustellen. Der **HighVersionLie-Test** wird verwendet, um die Konformität mit Anforderung 2.5 zu überprüfen.

Visual Studio Team System enthält eine Teilmenge der AppVerifier-Funktionalität, die in die Debugumgebung integriert ist. Dies kann sich als nützlich erweisen, um Probleme mit Den Grundlagen nachzuverfolgen und zu beheben: Heaps, Handles und Sperrentests.

</dd> </dl>

### <a name="43-support-windows-error-reporting-and-file-version-information"></a>4.3 Unterstützung Windows-Fehlerberichterstattung und Dateiversionsinformationen

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Um die Unterstützung von Windows-Fehlerberichterstattung zu ermöglichen, müssen Spiele die folgenden Anforderungen erfüllen:

-   Spiele dürfen nur Ausnahmen behandeln, die bekannt und erwartet sind. Windows-Fehlerberichterstattung darf nicht deaktiviert werden. Wenn ein Fehler wie eine Zugriffsverletzung in einem Spiel auftritt, muss es Windows-Fehlerberichterstattung ermöglichen, den Absturz zu melden.
-   Alle ausführbaren Dateien (z. B. .exe Dateien oder DLLs) müssen einen genauen Produktnamen, Einen Firmennamen und eine Dateiversion enthalten.
-   Das normale Beenden des Spiels darf nicht zu einem unbekannten Ausnahmefehler führen.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Die Windows-Fehlerberichterstattung-APIs geben Microsoft wichtiges Feedback, um weit verbreitete Abstürze und Hängen in Anwendungen zu erkennen. Dadurch können Microsoft und seine Partner System- und Treiberprobleme, die zu Anwendungsfehlern führen, schnell erkennen und beheben.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Spiele können benutzerdefinierte Ausnahmehandler ohne Behandlung enthalten, um benutzerdefinierte Unterstützungs- und Berichtsfunktionen auszuführen. Sie müssen jedoch jeden Fehler an die **Funktionen ReportFault** oder **WerReportSubmit** übergeben.

Die richtigen Informationen zur Dateiversion können überprüft werden, indem Sie die Dateieigenschaften auf der Windows Desktopbenutzeroberfläche anzeigen und die Eigenschaftenseite Version überprüfen.

Weitere Informationen zu den Windows-Fehlerberichterstattung-APIs und zur Analyse der Absturzabbilder, die bei Verwendung dieses Diensts generiert werden, finden Sie im DirectX-Artikel [Absturzabbildanalyse.](/windows/desktop/DxTechArts/crash-dump-analysis)

</dd> </dl>

## <a name="xbox-360-common-controller-for-windows-terminology"></a>Xbox 360 Common Controller für Windows Terminologie



| Name                                          | BESCHREIBUNG                                                                                                 |
|------------------------------------------|--------------------------------------------------------------------------------------------------|
| Ein                                        | Die Schaltfläche A.                                                                                     |
| B                                        | Die B-Schaltfläche.                                                                                     |
| Zurück                                     | Die Schaltfläche Zurück.                                                                                  |
| (rechts/links) Bumper                      | Die Schaltfläche am oberen rechten und linken Rand des Controllers. Entspricht einer Schaltfläche für die Schaltfläche "Shoulder".    |
| Direktionales Pad                          | Das direktionale Pad des Controllers.                                                                   |
| D-Pad                                    | Akzeptierte Abkürzung des direktionalen Pads.                                                         |
| DP                                       | Direktionale Padabkürzung und Controllerbezeichnung.                                                |
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
| Xbox 360 Controller für Windows          | Das Xbox 360 Gamepad, das als PC-Hardware-SKU verkauft wurde, einschließlich einer Windows Gerätetreiber-DATENTRÄGER.          |
| Xbox 360 Wireless Controller für Windows | Das Xbox 360 als PC-Hardware-SKU verkaufte drahtlose Gamepad, einschließlich einer Windows Gerätetreiber- Disc. |



 

## <a name="guidelines-for-game-middleware-products"></a>Richtlinien für Spiele-Middlewareprodukte

### <a name="introduction"></a>Einführung

Damit Sich Spiele für das Games for Windows-Programm qualifizieren können, müssen sie eine Liste mit technischen Anforderungen erfüllen. Alle Drittanbieterkomponenten, die mit einem Titel ausgeliefert werden (ausführbare Dateien, DLLs, Treiber usw.), müssen auch diese Anforderungen erfüllen, damit das Spiel qualifiziert werden kann. In diesem Dokument werden die gängigsten Anforderungen hervorgehoben, die auch von den Komponenten von Drittanbietern erfüllt werden müssen, damit das Spiel die Konformitätstests bestehen kann. Installer und vollständige Spiele-Engine-/Produktionspakete sollten das vollständige Dokument games for Windows technical requirements (Spiele für Windows technische Anforderungen) lesen, da viele dieser Anforderungen von diesen Tools betroffen sind.

### <a name="additional-recommendations"></a>Zusätzliche Empfehlungen

Neben der Sicherstellung, dass Ihre Komponente die Erstellung von Titeln unterstützt, die den Anforderungen für Games for Windows entsprechen, müssen Sie beim Entwerfen und Bereitstellen einer Bibliothek oder eines Unterstützungshilfsprogramms für ein Windows Spiel eine Reihe weiterer Aspekte berücksichtigen.

-   Um Entwickler zu unterstützen, die an nativen 64-Bit-x64-Anwendungen arbeiten, stellen Sie sowohl native 32-Bit- als auch 64-Bit-Versionen Ihrer Bibliotheken bereit. Die 32-Bit-Version muss pro 2.2 64-Bit-kompatibel sein. Bibliotheken für 32-Bit-Anwendungen sollten nicht davon ausgehen, dass das hohe Bit einer 32-Bit-Adresse nicht verwendet wird, um die Verwendung in LARGEADDRESSAWARE x86-Anwendungen zu unterstützen.
-   Wenn Sie native Codeheader (C/C++) bereitstellen, verwenden Sie die SAL-Attributsyntax (Standard Annotation Language), um Ihre öffentlichen API-Routinen zu versehen. Dadurch können Benutzer Ihrer Bibliothek den maximalen Vorteil der Verwendung von Static Code Analysis (/analyze) nutzen, das Teil Visual Studio Team System 2005, Visual Studio Team System 2008, Visual Studio 2010 Premium und Visual Studio 2010 Ultimate ist, sowie die öffentlich verfügbaren Windows SDK-Compilertools.
-   Wenn Ihr Produkt Threads innerhalb des Prozesses des Benutzers erstellt, müssen Sie jeden Thread benennen, damit debuggende Tools ausgeführte Threads ordnungsgemäß kommentieren können.
-   Wenn Sie Routinen schreiben, die innerhalb der Hauptschleife eines Spiels aufgerufen werden sollen, verwenden Sie die D3DX-Routinen D3DPERF \_ BeginEvent/EndEvent und D3DPERF \_ SetMarker, um vorgänge auf hoher Ebene mit Anmerkungen zu versehen, um Engpässe mit pix für Windows leichter zu erkennen.
    > [!Note]  
    > Für die Grafikdiagnosefunktionen Visual Studio 2012 werden diese D3DX- und PIX-Routinen durch die [**ID3DUserDefinedAnnotation-Schnittstelle**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation) ersetzt.

     

-   Stellen Sie für Netzwerkbibliotheken IP-neutrale Implementierungen bereit, und vermeiden Sie veraltete IPv4-Routinen, um die IPv6- und Teredo-Technologien in Windows XP mit Service Pack 2, Windows Vista und Windows 7 zu unterstützen.
-   Spieledienstanbieter sollten sich mit Version 2 des GDF-Schemas bei Games Explorer registrieren und das RSS-Feature nutzen, um dienstbezogene Nachrichten bereitzustellen.

### <a name="games-for-windows-showcases"></a>Spiele für Windows Showcases

### <a name="introduction"></a>Einführung

Spiele für Windows Zeigen gehen über die Bereitstellung einer soliden Spielerfahrung auf Windows PCs hinaus. Durch die Implementierung dieser Features können Spiele die Benutzerfreundlichkeit auf den neuesten Windows Plattformen weiter verbessern.

Spiele für Windows Titel müssen alle in diesem Artikel aufgeführten technischen Anforderungen erfüllen, aber Showcasefeatures sind optional. Diese Titel können einige, keine oder alle dieser Showcases implementieren.

### <a name="s1-exploit-direct3d-11"></a>S.1 Exploit Direct3D 11

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Direct3D 11 ist die Rendering-API der nächsten Generation für Windows Vista und Windows 7. Spiele, die Direct3D 11 nutzen, verwenden optimierte Inhalte, erweiterte Renderingtechniken und neue Hardwarefeatures, um eine überzeugende Erfahrung auf Hardware zu schaffen, die 10, 10.1 und 11 unterstützt.

Wenn das Spiel auch Direct3D 9 implementiert, sollte ein paralleler Vergleich eine erkennbare Verbesserung der Inhaltsqualität, visueller Genauigkeit, Leistung, Szenenkomplexität und anderer Grafikgenauigkeitsbereiche für Direct3D 11 veranschaulichen. Diese Unterstützung unterliegt den technischen Anforderungen von Games for Windows 1.7.

Direct3D 10level9-Technologie kann verwendet werden, um Shadermodell 2.0/3.0 Direct3D 9-Videohardware auf Windows Vista und Windows 7 zu unterstützen, anstatt eine direkte Direct3D 9-Implementierung für umfassende Hardwareunterstützung zu verwenden. Dies reicht jedoch nicht aus, um dieses Showcase zu veranschaulichen.

Auf Computern, auf denen Windows Vista oder Windows 7 mit installiertem Direct3D 11 ausgeführt wird, sollte das Spiel standardmäßig Direct3D 11 verwenden.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Die Direct3D 11-API baut auf dem Windows Display Driver Model (WDDM) und der Direct3D 10.1-Infrastruktur auf, um neue Funktionen zu unterstützen: Hardware-Mosaik, Compute-Shader, Multithreadring und Ressourcenerstellung, neue Texturkomprimierungsformate und eine flexiblere Shadersprache. Direct3D 11 bietet einheitliche Hardwareunterstützung für moderne Grafikkarten, einschließlich der Direct3D 11-Teile der neuesten Generation, aller Direct3D 10- und 10.1-Grafikkarten sowie vieler Shader Model 2.0/3.0 Direct3D 9-Grafikkarten, die die minimale Videohardware darstellt, die für den 3D-Desktop von "Einheit 3D" erforderlich ist.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Die Migration einer Direct3D 9-Rendering-Engine zur Verwendung der neuen Direct3D 11-Schnittstelle ist eine klar definierte Aufgabe:

-   Entfernen Sie alle Vorgänge mit fester Funktion zugunsten von programmierbaren Shadern.
-   Aktualisieren Sie alle vorhandenen Shader auf die neue Syntax des Shadermodells 4.x/5.
-   Aktualisieren Sie die Ressourcenverwaltung, um das neue Ansichtsmodell zu unterstützen.
-   Konvertieren Sie alle Ressourcen, um eine neue Liste der verfügbaren Formate zu verwenden.
-   Aktualisieren Sie die Renderzustandsbehandlung, um unveränderliche Zustandsblöcke zu verwenden, und überarbeiten Sie Shaderkonstanten in Konstantenpuffer.

Diese Konvertierung ist wichtig, um das Direct3D 11-Showcase zu aktivieren, obwohl das Ergebnis nicht die Showcase-Anforderung der Nutzung der neuen API erfüllt.

Die neue API und das zugehörige HLSL-Programmiermodell bieten viele Möglichkeiten für verbesserte Inhalte:

-   Nutzen vorhandener Direct3D 10-Hardwarefeatures wie Geometry Shader, Stream Out, Texturarrays und die komprimierten BC4/BC5-Texturformate.
-   Nutzen vorhandener Direct3D 10.1-Hardwarefeatures, z.B. unabhängige Blendmodi pro Renderziel, MSAA-Tiefenlesemodus, MSAA-Zugriff pro Beispiel-Shader, Cubezuordnungsarrays und Rendering in blockkomprimierten Formaten (BLOCK-Compressed, BC).
-   Implementieren erweiterter GPU-Algorithmen mithilfe von Compute-Shader mit CS4.x auf vorhandenen Direct3D 10/10.1-Grafikkarten (aktiviert durch aktualisierte Videotreiber) oder CS 5.0 auf Direct3D 11-Grafikkarten der nächsten Generation.
-   Rendern in mehreren Threads mithilfe der Erstellung von Freethreadressourcen und mehreren Gerätekontexten zur Verbesserung der Leistung auf Multi-Core-Systemen (mit aktualisierten Videotreibern). Weitere Informationen finden Sie unter Games for Windows Showcase S.3.
-   Unter Verwendung neuer Features der Videohardware der Direct3D 11-Klasse, z. B. Hardware-Mosaik mit Hüllen- und Domänen-Shadern, Shadermodell 5.0 HLSL-Shaderhardware mit komprimierten Texturformaten BC6HBC7 und dynamischer Shaderverknüpfung.

Techniken, die mit Direct3D 9 (größtenteils durch hohe CPU-Kosten) implementiert werden können, können effizient auf die GPU geladen werden, wodurch CPU-Ressourcen zur Unterstützung anderer Spielanforderungen freigegeben werden.

Direct3D 11-APIs, unterstützende Tools und Beispiele sind im DirectX SDK verfügbar. Siehe auch Grafik-APIs in Windows.

</dd> </dl>

### <a name="s2-exploit-x64-native"></a>S.2 Exploit x64 Native

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Das Spiel enthält eine native 64-Bit-Ausführbare Datei, die eine überzeugende neue Benutzeroberfläche bietet, die von x64-Editionen von Windows auf x64-fähiger Hardware ausgeführt wird. Ein paralleler Vergleich mit der 32-Bit-Version des Spiels sollte eine erkennbare Verbesserung der Komplexität der Inhalte, kürzere Ladezeiten und leistung zeigen.

Bei 64-Bit-Editionen von Windows sollte bei der Installation immer die native 64-Bit-Version des Spiels als Standard für Tastenkombinationen in Games Explorer und Windows XP Professional x64 Edition eingerichtet werden. Wenn eine duale Installation gewünscht wird, kann eine zusätzliche Wiedergabeaufgabe für Games Explorer auf Windows Vista und Windows 7 angegeben werden, die auf die 32-Bit-Version verweist. Der Standardwert sollte jedoch die native 64-Bit-Version bleiben.

Beachten Sie, dass das Spiel die 64-Bit-Editionen von Windows Vista und Windows 7 unterstützen sollte, um diese Präsentationsempfehlung zu erfüllen. Die Unterstützung für Windows XP Professional x64 Edition wird empfohlen, ist jedoch nicht erforderlich.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Die x64-Technologie bietet 64-Bit-Adressierungsfunktionen sowohl für den Consumer- als auch für den Servermarkt, die eine 32-Bit-Vollgeschwindigkeits-Abwärtsadressierung für vorhandene Anwendungen umfassen. x64 ist ein wichtiger Bestandteil der Roadmap für AMD (AMD64) und Intel (EMT64) und unterstützt mit Ausnahme von ultra-mobilen CPUs die Technologie für alle aktuellen und zukünftigen Prozessoren.

Windows XP Professional x64 Edition war das erste consumerorientierte Windows Betriebssystem(OS), das x64-Technologie unterstützt, und Windows Vista und Windows 7 erweitern die Verfügbarkeit der Betriebssystem-Aktivierung für 64-Bit-Consumercomputing erheblich. Bei standardmäßig 2 GB RAM auf vielen neuen Computern profitieren weitere Verbesserungen der Speicherskalierung nicht von einzelnen 32-Bit-Anwendungen, die nicht mehr als 2 GB physischen RAM adressieren können. Viele Spiele stehen heute vor Herausforderungen, alle verfügbaren Inhalte in die Einschränkungen von 2 GB des virtuellen Adressraums zu integrieren, insbesondere in Kombination mit den großen Videospeichern, die auf High-End-GPUs verfügbar sind, und der Wechsel zur x64-Technologie erhöht die unterstützungsfähigen Detailebenen erheblich.

Die x64-Kompatibilität für 32-Bit-Spiele ist eine Games for Windows technische Anforderung (2.2), aber die Nutzung der neuen Technologien erfordert eine native 64-Bit-Implementierung.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Der Hauptvorteil der 64-Bit-Adressierung ist die Möglichkeit, direkt auf mehr als 2 GB physischen und virtuellen Arbeitsspeicher zuzugreifen. Der große Adressraum des virtuellen Arbeitsspeichers ermöglicht eine umfangreiche Verwendung von speicherabbildten E/A-Auslastungen, ohne dass Probleme mit der Auslastung des VM-Adressraums in der 32-Bit-Programmierung auftreten. Spiele können den neuen Speicherplatz nutzen, um die Ladezeiten erheblich zu verbessern oder in einigen Fällen Pausen beim Laden von Inhalten zu vermeiden.

Vorhandene 32-Bit-Anwendungen können von x64-Editionen profitieren, indem sie adressen mit vollständigen 32-Bit-Daten verarbeiten können, wenn sie mit der Linkeroption Große Adressen aktivieren (**/LARGEADDRESSAWARE**) erstellt werden. Bei 32-Bit-Versionen von Windows XP ermöglichten spezielle Startmodi, dass solche Anwendungen bis zu 3 GB RAM adressieren konnten, und x64-Editionen bieten Zugriff auf bis zu 4 GB RAM für LAA-Apps (Large Address Aware). Obwohl die Verwendung von LAA in einer 32-Bit-Anwendung diese Vorzeigeanforderung nicht erfüllt, ist diese Bridge-Technologie eine äußerst nützliche Möglichkeit, zusätzliche Skalierungsvorteile für x64-Versionen von Windows für diejenigen bereitzustellen, die diese Showanforderung nicht vollständig implementieren.

Weitere Informationen finden Sie unter [64-Bit-Programmierung für Spieleentwickler](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers) und [RAM, VRAM und mehr RAM: 64-Bit-Gaming ist hier](https://www.gamasutra.com/view/feature/3602/sponsored_feature_ram_vram_and_.php) in Gamasutra.

> [!Note]  
> Eine wichtige Herausforderung für diese Präsentation besteht darin, sicherzustellen, dass alle Bibliotheken oder Komponenten von Drittanbietern, auf denen Ihr Spiel basiert, für die native 64-Bit-Entwicklung verfügbar sind. Viele ältere Microsoft-APIs wurden auch aus der nativen 64-Bit-Umgebung entfernt, was eine Herausforderung für Engine-Codebasen mit älteren Implementierungen von Schlüsselsystemen darstellen kann.

 

</dd> </dl>

### <a name="s3-exploit-many-core-processors"></a>S.3 Exploit Many-Core Prozessoren

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Das Spiel implementiert Features, die multicore-Prozessoren nutzen, die auf 3, 4 oder mehr Kerne skaliert werden, sofern verfügbar.

Wenn das Spiel Einzelprozessor- oder Dual-Core-Systeme unterstützt, sollte ein paralleler Vergleich mit einem Quad-Core-System wahrnehmbare neue Features, zusätzliche überzeugende Effekte, eine Verbesserung der Inhaltsqualität und/oder eine verbesserte Leistung veranschaulichen.

Da die Dual-Core-Skalierung bereits umfassend von Spielen unterstützt und automatisch von verschiedenen Direct3D-Treibererweiterungen genutzt wird, reicht die Dual-Core-Skalierung nicht aus, um dieses Showbeispiel zu veranschaulichen.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Das kontinuierliche Leistungswachstum für CPUs hat sich von der Verbesserung der Taktfrequenz auf die Hinzufügung von Computekernen umgestellt. Amd- und Intel-Roadmaps basieren auf skalierbaren Designs mit mehreren Kernen. Aufgrund dieser grundlegenden Änderung bei der Entwicklung von Prozessoren verfügen alle Spieleplattformen der nächsten Generation über CPUs mit mehreren Kernen. Singlethreadanwendungen erzielen keine signifikanten Vorteile mehr von CPUs der nächsten Generation. Einfaches Multithreading kann ebenfalls nicht skaliert werden, da die Anzahl der häufig verwendeten CPU-Kerne auf drei oder mehr steigt.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Beachten Sie, dass die Kernanzahl keine Potenz von zwei sein muss. Daher sollten Spiele linear skaliert werden und die Kernanzahl von 3, 4, 5, 6, 7, 8 usw. verarbeiten.

Die Skalierung durch Erhöhen der Anzahl von Threads in einer Anwendung liefert nur dann eine Rendite, wenn die Kosten für Kommunikation und Threadsynchronisierung in Check gehalten werden. Die featurebasierte Skalierung kann sich auf kurze Sicht als einfachere Lösung erweisen, sodass das Spiel normal ohne die zusätzlichen Threads auf Einzelkernsystemen betrieben werden kann und sie aktiviert wird, wenn die zusätzliche CPU-Leistung verfügbar ist.

Weitere Informationen finden Sie unter [Coding For Multiple Cores on Xbox 360 and Microsoft Windows](/windows/desktop/DxTechArts/coding-for-multiple-cores) and [Lockless Programming Considerations for Xbox 360 and Microsoft Windows](/windows/desktop/DxTechArts/lockless-programming) in den DirectX-Artikeln sowie im DXUTLockFreePipe-Hilfsprogramm und im CoreDetection-Beispiel.

Die Verwendung der Direct3D 11-Freithread-Ressourcenerstellung und der Gerätekontexte ist nützlich, um die Skalierbarkeit von Grafikressourcen mit vielen Kernen zu erreichen. Weitere Informationen finden Sie unter Spiele für Windows Showcase S.1.

Beachten Sie, dass die direkte Verwendung der CPU-Anweisung rdtsc anstelle von Windows-APIs zum Berechnen der Zeitsteuerung auf Multi-Core-Systemen zu Problemen bei einigen Hardware- und Betriebssystemkonfigurationen führen kann. Weitere Informationen finden Sie in den DirectX-Artikeln unter [Game Timing and Multicore Processors (Spielzeitsteuerung und Multicore-Prozessoren).](/windows/desktop/DxTechArts/game-timing-and-multicore-processors)

</dd> </dl>

### <a name="s4-support-games-for-windows---live"></a>S.4 Support Games for Windows – LIVE (S.4 Support Games für Windows – LIVE)

Spiele für Windows: LIVE wird von Microsoft nicht mehr unterstützt.

### <a name="s5-support-windows-touch"></a>S.5 Support Windows Touch

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Windows Touch-fähige Spiele können mit Toucheingaben und/oder Gesten auf Computern, auf denen Windows 7 ausgeführt wird, mit einer Touchanzeige wiedergegeben werden. Tastatureingaben können ebenfalls verwendet werden, aber die primäre Wiedergabeschnittstelle muss touchbasiert sein.

Die Aktivierung der Toucheingabe sollte die Verwendung der Maus oder des allgemeinen Controllers gemäß der technischen Anforderung 1.4 nicht verhindern.

Es wird nicht erwartet, dass das Installationsprogramm des Spiels Windows Touchfunktionen unterstützt.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Multitouch-fähige Displays für Computer sind für Laptops und Desktops verfügbar und stellen ein wichtiges Hardwarefeature dar, das mit der Veröffentlichung von Windows 7 heraufgestuft wird. Windows 7 unterstützt Windows Touch in den Desktop- und allgemeinen Steuerelementschnittstellen.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Native Codeanwendungen können über die WM \_ TOUCH-Nachrichten in Kombination mit der [**RegisterTouchWindow-Funktion**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) auf Multitouch zugreifen. Siehe auch die Manipulations- und Trägheits-API.

Windows Presentation Foundation (WPF) 4.0 bietet eine verwaltete Lösung für Multitouchschnittstellen.

Weitere Informationen finden Sie im Windows Touch SDK.

</dd> </dl>

### <a name="s6-support-high-color"></a>S.6-Unterstützung für hohe Farbe

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Anforderung**
</dt> <dd>

Spiele, die Hohe Farbe unterstützen, verwenden 10:10:10:2 (DXGI \_ FORMAT \_ R10G10B10A2, D3DFMT \_ A2B10G10R10) oder ein 16:16:16:16-Format (DXGI \_ FORMAT \_ R16G16B16A16, D3DFMT \_ A16B16G16R16) für den Rendering-Hintergrundpuffer und den Vollbildanzeigemodus.

Mithilfe eines Renderziels mit hoher Farbe können High-Dynamic-Inhalt (HDR) mit einem erweiterten oder breiten Gamut gerendert werden, wenn eine Tonzuordnung zu einem 10-Bit- oder 16-Bit-Bereich durchgeführt wird.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gründe**
</dt> <dd>

Monitore können seit vielen Jahren mehr als 256 Farbebenen pro Kanal anzeigen, auch wenn CRT-Anzeigen weit verbreitet waren. Die Überprüfung der Hardware auf Grafikkarten war der einschränkende Faktor. Moderne GPUs, einschließlich der meisten Direct3D 9-Klassen-Hardware und aller Direct3D-Hardware der 10- und höher-Klasse, verfügen über Scan-Out-Hardware, die mindestens 10 Bits pro Kanal kann, und die Hardwarefunktion wird in Zukunft auf 16 Bits pro Farbkanal anwachsen. HD TV-Verbindungssysteme (CSV, DisplayPort) wurden auch für die Verarbeitung von mehr als 8 Bits pro Kanal entwickelt, und analoge VGA wird solche Signale bereits übertragen.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Zusätzliche Informationen**
</dt> <dd>

Beachten Sie, dass "Hohe Farbe" oder "Hohe Farbe" sich in der Vergangenheit auf das Verschieben von 256 (8-Bit)-Farbanzeigen in 15- oder 16-Bit-Farbanzeigen bezieht. Die meisten Anzeigesysteme haben sich seit langem auf True Color (Echte Farbe) verschoben, die 24-Bit-Farbe ist, oder 8 Bits pro Farbkanal für Rot, Grün und Blau. Unter Hohe Farbe bedeutet dies eine neue Generation von Anzeigesystemen, die mit mehr als 8 Bit pro einzelnem Farbkanal arbeiten können. Wird auch als Tiefe Farbe bezeichnet.

</dd> </dl>

### <a name="recommended-best-practices"></a>Empfohlene bewährte Methoden

### <a name="introduction"></a>Einführung

Zusätzlich zur Erfüllung der technischen Anforderungen und zur Einführung eines oder mehrerer Showcases in Ihrem Titel gibt es eine Reihe von bewährten Methoden, die für alle Windows Spiele befolgt werden sollten. Diese Empfehlungen fallen zwar nicht in den Bereich der grundlegenden technischen Anforderungen, aber Es wird dringend empfohlen, sie für alle Spiele für Windows Titel zu verwenden.

### <a name="additional-recommendations"></a>Zusätzliche Empfehlungen

-   Verwenden Sie die neueste Visual Studio Compiler und Runtime. Neuere Versionen des Compilers implementieren erhebliche Verbesserungen für die Qualität des generierten Codes und für Sicherheitsprobleme und verwenden moderne Strategien zur Prozessoroptimierung. Das Aktualisieren des Compilers und die Verwendung der neuesten C-Runtime ist eine einfache Möglichkeit, zu modernen Codierungsmethoden zu migrieren.
-   Verwenden Sie anstelle der statischen Verknüpfung die DLL-Version (Dynamic Link Library) der C-Runtime, und verwenden Sie Secure CRT. (Ausnahmen können in speziellen Fällen vor der Installation vorgenommen werden, z. B. für ein Autorun-Programm oder für das Installationsprogramm selbst.)
-   Verwenden Sie für Spielaudio XAudio2, X3DAudio und/oder XACT anstelle von DirectSound. Verwenden Sie directSound für Windows XP (nur) und WASAPI für Windows Vista und Windows 7 für Audio-Engines, die alle Kombinations- und Quellratenkonvertierungen durchführen und nur eine Lösung mit geringer Latenz für die Audioausgabe benötigen.
-   Vermeiden Sie die Verwendung veralteter und veralteter APIs: DirectDraw, DirectSound, DirectPlay, Die Leistungsschicht von Direct Voice, DirectPlay Voice und Der Direct3D-Modus wird beibehalten. Beachten Sie, dass DirectPlay Voice und der beibehaltene Direct3D-Modus auf Windows Vista oder Windows 7 überhaupt nicht verfügbar sind. Die Leistungsebene von DirectPlay und DirectPlay ist für native x64-Anwendungen nicht verfügbar.
-   Optimieren sie mithilfe von SSE/SSE2 SIMD-Anweisungssätzen. Sehen Sie sich die [DirectXMath-API](/windows/desktop/dxmath/directxmath-portal) im Windows SDK als plattformübergreifende Lösung für SIMD-optimierte mathematische Operationen an.
-   Verwenden Sie moderne bewährte Methoden für Windows Sicherheit (einschließlich Compiler- und Linkeroptionen wie **"/NXCOMPAT",** **"/GS",** **"/SAFESEH",** **"/DYNAMICBASE",** **"/SDL"** usw.). Weitere Informationen finden Sie unter [Bewährte Sicherheitsmethoden in der Spieleentwicklung.](/windows/desktop/DxTechArts/best-security-practices-in-game-development)
-   Verwenden Sie die neuesten Windows SDK-Komponenten und -Bibliotheken. Entfernen Sie Abhängigkeiten von den legacy bereitgestellten DirectSetup-Out-of-Band-Komponenten wie D3DX9, D3DX10 und D3DX11. Erwägen Sie die Verwendung von [DirectXTex](https://github.com/Microsoft/DirectXTex) oder [DirectXTK](https://github.com/Microsoft/DirectXTK) oder beidem.
-   Vermeiden Sie die Verwendung des älteren HLSL-Compilers, und verwenden Sie stattdessen den modernen HLSL-Compiler. Wenn ihre Anwendung Unterstützung für Pixel Shader 1.x benötigt, verwenden Sie anstelle von HLSL die Shaderassembly, oder beschränken Sie die Verwendung des älteren Compilers auf diese Szenarien.

## <a name="resources"></a>Ressourcen



| Begriff                                                                                                                                                                                                                         | BESCHREIBUNG                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Games_for_Windows__Test_Cases__"></span><span id="games_for_windows__test_cases__"></span><span id="GAMES_FOR_WINDOWS__TEST_CASES__"></span>Spiele für Windows: Testfälle <br/>                              | Bewährte Methoden für Spiele auf Windows XP, Windows Vista und Windows 7<br/>                                                                               |
| <span id="Windows_SDK__"></span><span id="windows_sdk__"></span><span id="WINDOWS_SDK__"></span>Windows SDK <br/>                                                                                                      | [Windows Sdks](https://msdn.microsoft.com/bb980924.aspx)<br/>                                                                                      |
| <span id="User_Account_Control_Guidelines__"></span><span id="user_account_control_guidelines__"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES__"></span>Richtlinien für die Benutzerkontensteuerung <br/>                      | [Windows Anforderungen an die Vista-Anwendungsentwicklung für die Kompatibilität der Benutzerkontensteuerung](/previous-versions/dotnet/articles/bb530410(v=msdn.10))<br/> |
| <span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>WinQual-Entwicklerportal <br/>                                                  | [Windows Quality Online Services (Winqual)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)<br/>                                                                         |
| <span id="DirectX_Developer_Portal__"></span><span id="directx_developer_portal__"></span><span id="DIRECTX_DEVELOPER_PORTAL__"></span>DirectX-Entwicklerportal <br/>                                                  | [Directx Developer Center](/previous-versions/windows/apps/hh452744(v=win.10))<br/>                                                                               |
| <span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog zu Games for Windows und DirectX SDK<br/> | [Spiele für Windows und das DirectX SDK](https://walbourn.github.io/)<br/>                                                                           |
| <span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Zusätzliche DirectX-Artikel<br/>                                             | [Technische Artikel zu DirectX](/windows/desktop/DxTechArts/dx9-technical-articles)<br/>                                                                                    |



 

 

