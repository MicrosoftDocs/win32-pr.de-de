---
title: Technische Anforderungen für Spiele für Windows; bewährte Methoden für Spiele für Windows XP, Windows Vista, Windows 7 und Windows 8
description: Dieser Artikel enthält technische Anforderungen und bewährte Methoden für Spiele, die unter Windows ausgeführt werden.
ms.assetid: 8b816e9f-de68-cf84-1501-a9c36c6b75d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e38b9476a4ab2aad5edc6210f55bc4d2b85845f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730048"
---
# <a name="games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8"></a>Spiele für technische Windows-Anforderungen: bewährte Methoden für Spiele unter Windows XP, Windows Vista, Windows 7 und Windows 8

Dieser Artikel enthält technische Anforderungen und bewährte Methoden für Spiele, die unter Windows ausgeführt werden. Wir haben diese technischen Anforderungen und bewährten Methoden in erster Linie für Windows Vista und Windows 7 sowie das ältere Betriebssystem Windows XP beschrieben. Diese bewährten Methoden gelten in der Regel auch für Win32-Desktop Spiele unter Windows 8.

Diese Artikel enthalten die folgenden Abschnitte:

-   [Unterschiede für Windows 8](#differences-for-windows-8)
    -   [Weitere Informationen](#additional-information)
-   [Spiele für Windows](#games-for-windows-technical-requirements-best-practices-for-games-on-windows-xp-windows-vista-windows-7-and-windows-8)
    -   [1,1 Spiele-Explorer-Integration](#11-games-explorer-integration)
    -   [1,2 Unterstützung der Familien Sicherheit/Jugendschutz Kontrolle](/windows)
    -   [1,3 Unterstützung von umfangreichen gespeicherten spielen](#13-support-rich-saved-games)
    -   [1,4 Unterstützung von "Xbox 360 Common Controller for Windows \[ Conditional Requirements"\]](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement)
    -   [1,5 Unterstützung mehrerer Seitenverhältnisse und Auflösungen](#15-support-multiple-aspect-ratios-and-resolutions)
    -   [1,6 Support von Windows Media Center starten](#16-support-launch-from-windows-media-center)
    -   [1,7 Direct3D-Unterstützung](#17-direct3d-support)
    -   [1,8 Aktivieren von High-dpi-Werten](#18-enable-high-dpi-aware)
-   [Sicherheit und Kompatibilität](#security-and-compatibility)
    -   [2,1 befolgen Sie die Richtlinien zur Benutzerkontensteuerung](#21-follow-user-account-control-guidelines)
    -   [2,2 Unterstützung für Windows x64-Versionen](#22-support-windows-x64-versions)
    -   [2,3 Signier Dateien](#23-sign-files)
    -   [2,4-Signatur Treiber](#24-sign-drivers)
    -   [2,5 Ausführen einer ordnungsgemäßen Versions Überprüfung](#25-perform-proper-version-checking)
    -   [2,6 Unterstützung von gleichzeitigen Benutzersitzungen](#26-support-concurrent-user-sessions)
    -   [2,7 Unterstützung von langen Namen](#27-support-long-names)
-   [Installation](#32-support-user-account-control-for-installation)
    -   [3,1 Unterstützung der einfachen Installation](#31-support-easy-installation)
    -   [3,2 Unterstützung der Benutzerkontensteuerung für die Installation](#32-support-user-account-control-for-installation)
    -   [3,3 in richtigen Ordnern installieren](#33-install-to-correct-folders)
    -   [3,4 Windows-Ressourcen ordnungsgemäß installieren](#34-install-windows-resources-properly)
    -   [3,5 vermeiden Neustarts während der Installation](#35-avoid-reboots-during-installation)
    -   [3,6 verwenden Sie die Datei Versionsverwaltung ordnungsgemäß.](#36-use-file-versioning-correctly)
    -   [3,7 Unterstützung für die bedingte Anforderung von Autorun \[\]](#37-support-autorun-conditional-requirement)
-   [Zuverlässigkeit](#reliability)
    -   [4,1 Entfernen unnötiger Neustarts](#41-eliminate-unnecessary-reboots)
    -   [4,2 Vermeiden von Application Verifier Fehlern](#42-eliminate-application-verifier-failures)
    -   [4,3 Support Windows-Fehlerberichterstattung und Datei Versionsinformationen](#43-support-windows-error-reporting-and-file-version-information)
-   [Xbox 360 Common Controller für Windows-Terminologie](#xbox-360-common-controller-for-windows-terminology)
-   [Richtlinien für Spiele Middleware-Produkte](#guidelines-for-game-middleware-products)
    -   [Introduction (Einführung)](#introduction)
    -   [Weitere Empfehlungen](#additional-recommendations)
    -   [Spiele für Windows-Präsentationen](#games-for-windows-showcases)
-   [Ressourcen](#resources)

## <a name="differences-for-windows-8"></a>Unterschiede für Windows 8

Im folgenden finden Sie eine Zusammenfassung der wichtigsten Unterschiede bei der Anwendung dieser technischen Anforderungen und bewährten Methoden auf Windows 8.

<dl> <dt>

<span id="The_Games_Explorer_UI_is_not_visible"></span><span id="the_games_explorer_ui_is_not_visible"></span><span id="THE_GAMES_EXPLORER_UI_IS_NOT_VISIBLE"></span>**Die Spiele-Explorer-Benutzeroberfläche ist nicht sichtbar.**
</dt> <dd>

Alle Spiele, die Sie mit dem [Games Explorer](/previous-versions/windows/desktop/legacy/hh437965(v=vs.85)) registrieren, werden in der neuen Windows-Benutzeroberfläche als Kacheln angezeigt, aber ein Großteil der Metadaten, die dem Titel zugeordnet sind, ist nicht mehr sichtbar. Sie verwenden weiterhin das Tool "Games Definition File Maker" (GDFMAKER.EXE), das jetzt im Windows Software Development Kit (SDK) verfügbar ist, um die Metadaten zu erstellen. Außerdem verwenden Sie die vorhandenen Mechanismen für die Bereitstellung der Metadaten. Testen Sie Ihre Spiele-Explorer-Registrierung weiterhin mithilfe von Windows 7, und überprüfen Sie, ob die neue Windows-Benutzeroberflächen Kachel bei der Installation unter Windows 8 angezeigt wird (siehe [1,1 Games Explorer-Integration](#11-games-explorer-integration)).

Informationen zum Herunterladen des Windows 8 SDK finden Sie unter [Downloads für die Entwicklung von Desktop-Apps](https://msdn.microsoft.com/windows/desktop/aa904949).

</dd> <dt>

<span id="Registration_with_the_Game_Explorer_APIs_continues_to_be_the_mechanism_for_registering_your_game_with_Windows_Parental_Controls"></span><span id="registration_with_the_game_explorer_apis_continues_to_be_the_mechanism_for_registering_your_game_with_windows_parental_controls"></span><span id="REGISTRATION_WITH_THE_GAME_EXPLORER_APIS_CONTINUES_TO_BE_THE_MECHANISM_FOR_REGISTERING_YOUR_GAME_WITH_WINDOWS_PARENTAL_CONTROLS"></span>**Die Registrierung bei den Game Explorer-APIs ist weiterhin der Mechanismus für die Registrierung Ihres Spiels bei Windows-Jugendschutz-Steuerelementen.**
</dt> <dd>

Es wird empfohlen, dass Sie die Windows SDK Version von gdfmaker in der veröffentlichten Version von Windows 8 ausführen, um sicherzustellen, dass alle derzeit unterstützten Bewertungssysteme aufgefüllt werden können.

> [!Note]  
> Diese Version von gdfmaker erfordert .NET 4,0.

 

Weitere Informationen finden Sie [unter 1,2 Unterstützung der Familien Sicherheit/Eltern](/windows)

</dd> <dt>

<span id="There_are_now_three_choices_for_using_the_XINPUT_API_depending_on_your_requirements"></span><span id="there_are_now_three_choices_for_using_the_xinput_api_depending_on_your_requirements"></span><span id="THERE_ARE_NOW_THREE_CHOICES_FOR_USING_THE_XINPUT_API_DEPENDING_ON_YOUR_REQUIREMENTS"></span>**Es gibt jetzt drei Möglichkeiten für die Verwendung der xinput-API, abhängig von Ihren Anforderungen.**
</dt> <dd>

Xinput 1,4 ist in Windows 8 integriert. Sowohl Windows Store-Apps als auch Win32-Desktop-Apps können xinput 1,4 verwenden. Alle Versionen von Windows können xinput 9.1.0 für vereinfachte allgemeine Controller verwenden, aber es ist kein Weitergabepaket mit xinput 9.1.0 vorhanden. Alle Versionen von Windows können auch die vorhandene DirectX SDK-Version xinput 1,3 verwenden, die für die Bereitstellung von DirectSetup erforderlich ist.

Weitere Informationen finden Sie [unter 1,4 Support the Xbox 360 Common Controller for Windows](#14-support-the-xbox-360-common-controller-for-windows-conditional-requirement).

</dd> <dt>

<span id="Only_a_limited_set_of_desktop_Win32_apps_are_supported_on_"></span><span id="only_a_limited_set_of_desktop_win32_apps_are_supported_on_"></span><span id="ONLY_A_LIMITED_SET_OF_DESKTOP_WIN32_APPS_ARE_SUPPORTED_ON_"></span>**Auf Windows rt werden nur eine begrenzte Anzahl von Win32-Desktop-Apps unterstützt.**
</dt> <dd>

Spiele, die unter Windows 7 ausgeführt werden, können und ordnungsgemäß auf Windows 8 x86-und x64-Plattformen ausgeführt werden.

Weitere Informationen finden Sie [unter 2,2 Support Windows x64-Versionen](#22-support-windows-x64-versions).

</dd> <dt>

<span id="Ensure_any_OS_checks_are_done_correctly"></span><span id="ensure_any_os_checks_are_done_correctly"></span><span id="ENSURE_ANY_OS_CHECKS_ARE_DONE_CORRECTLY"></span>**Stellen Sie sicher, dass alle Betriebssystem Überprüfungen ordnungsgemäß**
</dt> <dd>

Die Windows 8-Betriebssystemversion ist 6,2. Windows 8 übergibt die aktuellen minimalen Balken Tests, die für die Spiele Bereitstellung empfohlen werden.

</dd> <dt>

<span id="The__DirectX_End-User_Redistribution__package_runs_successfully_on_Windows_8__as_it_does_on_Windows_7__to_deploy_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTEngine__and_so_on"></span><span id="the__directx_end-user_redistribution__package_runs_successfully_on_windows_8__as_it_does_on_windows_7__to_deploy_d3dx9__d3dx10__d3dx11__xinput_1.3__xaudio_2.7__xactengine__and_so_on"></span><span id="THE__DIRECTX_END-USER_REDISTRIBUTION__PACKAGE_RUNS_SUCCESSFULLY_ON_WINDOWS_8__AS_IT_DOES_ON_WINDOWS_7__TO_DEPLOY_D3DX9__D3DX10__D3DX11__XINPUT_1.3__XAUDIO_2.7__XACTENGINE__AND_SO_ON"></span>**Das DirectX End-User-Weitergabepaket wird auf Windows 8 wie unter Windows 7 erfolgreich ausgeführt, um D3DX9, d3dx10, Bibliothek d3dx11, xinput 1,3, xaudio2,7, xactengine usw. bereitzustellen.**
</dt> <dd>

Es gibt jedoch ein bekanntes Problem mit DirectSetup auf Systemen, auf denen nur .NET 4,0 aufgrund der Bereitstellungs Verarbeitung der verwalteten DirectX 1,1-Assemblys installiert ist. Dieses Problem gilt für Windows 8, das standardmäßig .NET 4,5 und neue Windows XP-Computer mit installierter .NET 4,0-Laufzeit enthält. Dieses Problem gilt jedoch nicht für .NET-Versionen vor .NET 4,0. Obwohl Windows 8 ein Anwendungs Kompatibilitäts Verhalten aufweist, um dieses Problem automatisch zu beheben (was den Netzwerk Zugriff erfordert), empfiehlt es sich, dass Spiele, die weiterhin das DirectSetup-Update für das DirectX SDK (Juni 2010), aktualisierte Version der Redist-Dateien bereitstellen. Wenn Sie DirectSetup für Ihren Titel verwenden, kürzen Sie den Titel wie immer auf den mindestens erforderlichen Satz von Cabs.

Weitere Informationen finden Sie unter [3,4 Installieren von Windows-Ressourcen](#34-install-windows-resources-properly).

</dd> <dt>

<span id="Games_that_require_the_.NET__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="games_that_require_the_.net__2.0__compatible_runtime__2.0__3.0__3.5__continue_to_use_existing_deployment_mechanisms"></span><span id="GAMES_THAT_REQUIRE_THE_.NET__2.0__COMPATIBLE_RUNTIME__2.0__3.0__3.5__CONTINUE_TO_USE_EXISTING_DEPLOYMENT_MECHANISMS"></span>**Spiele, die die .NET 2,0-kompatible Laufzeit (2,0, 3,0, 3,5) erfordern, verwenden weiterhin vorhandene Bereitstellungs Mechanismen**
</dt> <dd>

Diese Spiele veranlassen ein Anwendungs Kompatibilitäts Verhalten unter Windows 8, um die .NET 3,5-Runtime automatisch zu aktivieren (für die ein Netzwerk Zugriff erforderlich ist). Es wird jedoch empfohlen, dass .NET-Entwickler auf die .NET 4,0-Laufzeit umsteigen.

> [!Note]  
> Die verwalteten, verwalteten DirectX 1,1-Assemblys sind nicht kompatibel mit der .NET 4. x-Laufzeit.

 

Weitere Informationen finden Sie unter [3,4 Installieren von Windows-Ressourcen](#34-install-windows-resources-properly).

</dd> <dt>

<span id="Use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.NET_is_not_recommended"></span><span id="use_of_an__autorunner__or_other_pre-install_technology_that_relies_on_.net_is_not_recommended"></span><span id="USE_OF_AN__AUTORUNNER__OR_OTHER_PRE-INSTALL_TECHNOLOGY_THAT_RELIES_ON_.NET_IS_NOT_RECOMMENDED"></span>**Die Verwendung eines AutoRunner-oder einer anderen Vorinstallations Technologie, die auf .NET basiert, wird nicht empfohlen.**
</dt> <dd>

Sie können davon ausgehen, dass nur .NET 2,0 kompatible Laufzeiten (2,0, 3,0, 3,5) unter Windows Vista und Windows 7 vorhanden sind. In Windows 8 ist standardmäßig nur die .NET 4,0-kompatible Laufzeit vorhanden.

Weitere Informationen finden Sie [unter 3,7 Support Autorun](#37-support-autorun-conditional-requirement).

</dd> <dt>

<span id="There_is_an_updated_Application_Verifier_for_Windows_8"></span><span id="there_is_an_updated_application_verifier_for_windows_8"></span><span id="THERE_IS_AN_UPDATED_APPLICATION_VERIFIER_FOR_WINDOWS_8"></span>**Es gibt eine aktualisierte Application Verifier für Windows 8.**
</dt> <dd>

Das Windows 8 SDK enthält diese aktualisierte Application Verifier.

Siehe [4,2 eliminieren von Application Verifier Fehlern](#42-eliminate-application-verifier-failures).

</dd> </dl>

### <a name="additional-information"></a>Zusätzliche Informationen

<dl>

[Cookbook zur Kompatibilität von Windows 8 und Windows Server 2012](/windows/desktop/w8cookbook/windows-8-and-windows-server-8-compatibility-cookbook-portal)  
[Wo finde ich das DirectX SDK?](/windows/desktop/directx-sdk--august-2009-)  
</dl>

## <a name="games-for-windows"></a>Spiele für Windows

**Zusammenfassung der Spiele Anforderungen**

**Kunden Vorteile**

Bei Computer spielen handelt es sich um eine wichtige Unterhaltung bei Windows, aber Benutzerfreundlichkeit hat im Laufe der Jahre die Frustration der Kunden verursacht. Üblicherweise werden Spiele wie Anwendungen installiert, aber Sie werden eher wie Unterhaltungsmedien (z. b. Filme oder Lieder) eingesetzt. Innovationen, wie z. b. Games Explorer, machen Spiele auf konsistente Weise verfügbar, die sich von Standardanwendungen unterscheidet. Mit diesen Neuerungen können auch Spiele in Windows, auch Musik und Bilder, in Windows angezeigt werden. Mithilfe der folgenden Anforderungen wird sichergestellt, dass Windows Vista und Windows 7 ein verbessertes, zugänglicheres und einheitlicheres Spielverhalten bereitstellen. Gleichzeitig wird die Kompatibilität mit Windows XP sichergestellt.

### <a name="11-games-explorer-integration"></a>1,1 Spiele-Explorer-Integration

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Das Spiel muss in Games Explorer (dem Ordner **Games** ) unter Windows Vista und Windows 7 sichtbar sein. Wenn diese Option ausgewählt ist, muss das Spiel auch korrekte Metadaten anzeigen. dazu zählen Verleger, Entwickler, Veröffentlichungsdatum, Version, Index Ergebnisse von Windows-Funktionen, Bewertung (falls zutreffend) und zugehörige Hyperlinks.

Wenn das Spiel Digital über einen Onlinespiel Dienst verteilt wird, sollte der Dienstanbieter auch im Spiele-Explorer angezeigt werden. Um sicherzustellen, dass der Anbieter ordnungsgemäß verarbeitet und die Verwendung von RSS-Feeds ermöglicht wird, sollte Version 2 des Schemas für die Spiel Definitions Dateien (DSFs) verwendet werden. (Weitere Informationen zu dsfs finden Sie unter zusätzliche Informationen.)

Außerdem müssen Game Installer die folgenden Regeln beachten, wenn Sie unter Windows Vista und Windows 7 ausgeführt werden:

-   Bei der Installation darf keine Verknüpfung erstellt werden, um das Spiel auf dem Desktop, im Startmenü oder an einem anderen Speicherort zu starten.
-   Aufgaben und Verknüpfungen zum Entfernen dürfen nicht erstellt werden.
-   Benutzer müssen das Spiel mithilfe der Option "Programme und Funktionen" in der Systemsteuerung unter Windows Vista und Windows 7 oder unter "Software" in der Systemsteuerung unter Windows XP entfernen können.

Unter Windows XP und früheren Versionen von Windows kann das Game Installer Programm Gruppen, Desktop Symbole oder Verknüpfungen nach Bedarf erstellen.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Windows Games Explorer ähnelt dem Konzept der Windows XP-Ordner " **meine Dokumente** " oder " **meine Bilder**". Die Idee besteht darin, ähnliche Inhalte an einem Ort zu zentralisieren und eine einfachere Organisation und kontextabhängige Aktivitäten zu ermöglichen. Spiele-Explorer erweitert das Konzept " **meine Dokumente** " oder " **meine Bilder** ", indem es eine umfassendere Organisation und Kontrolle über Spiele ermöglicht. Mit Games Explorer können Spieler alle Spiele anzeigen, organisieren und mit ihnen interagieren, die auf Ihren Systemen installiert sind. Außerdem können Spiele Verleger wichtige Spielinformationen effektiver übermitteln. Das System ist Daten gesteuert, sodass ein Spiel Verleger das Aktualisieren von Spielinformationen über die Lebensdauer des Produkts erleichtert.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Die Integration in Games Explorer erfordert, dass Sie eine Spiel Definitionsdatei (GDF) erstellen, bei der es sich um eine XML-Textdatei handelt, die in eine Binärdatei (eine ausführbare Datei oder eine DLL) als Ressource eingebettet ist, sowie ein Windows-Symbol. Das Spiel muss dann bei Games Explorer registriert werden. Die GDF ermöglicht außerdem das verfügbar machen von bereitgestellten Informationen, wie z. b. Spieltitel, Verleger, Entwickler, Links zu Websites und optionalen Aufgaben. Beachten Sie, dass Support Aufgaben nur Links zu Websites sein können, aber Wiedergabe Aufgaben können auch für optionale Support Aufgaben verwendet werden.

Games Explorer kann ein Miniatur Ansichts Bitmap-Bild verwenden. es wird jedoch empfohlen, stattdessen eine Windows-Symbol Ressource mit großen Symbolen (256 256) bereitzustellen. Die Symbol Ressource sollte die Bildgrößen 256 256 48 48, 32 32 und 16 16 sowohl in 24-Bit-Farben (echte Farbe) als auch in 8-Bit-Farben (256) enthalten. Der in Visual Studio 2008 und 2010 bereitgestellte Symbol-Editor unterstützt diese großen Symbol Formate, wie iconworkshop Lite.

Details zur Integration in **Windows Games Explorer** werden im DirectX SDK bereitgestellt. Das DirectX SDK umfasst einen GDF-Editor (Game Definition File) sowie ein Beispiel für GDF, das in gdfexamplebinary enthalten ist, ein Beispiel. Ein weiteres Beispiel, gameuxinstallhelper, stellt Routinen bereit, mit denen die erforderlichen Funktionen in vorhandene Installationssysteme integriert werden können. Das Datei Validierungs Steuerelement für Spiel Definitionen (gdftrace.exe) bietet Debugunterstützung zum Auswerten einer GDF. Siehe auch "Windows Games Explorer-Integration" in der DirectX SDK-Dokumentation für C++.

Windows 7 bietet Unterstützung für die zweite Version eines Schemas für GDF-Dateien. Die neue Version enthält eine vereinfachte Methode zum Erstellen von Wiedergabe Aufgaben und zur Unterstützung von Aktualisierungs Benachrichtigungen, Spiele Dienstanbietern, Spielstatistiken und RSS-Feeds für Spiele Dienstanbieter. Die neueste Version von gameuxinstallhelper behandelt alle Registrierungs-und Legacy Unterstützung, die für die Verwendung einer GDF-Datei der Version 2 mit Windows Vista erforderlich sind. Verwenden Sie die Tools und den Beispielcode aus dem DirectX SDK ab August 2009 oder höher. Die Verwendung einer GDF-Datei der Version 2 wird empfohlen, um die Unterstützung für RSS-Feeds, Spielstatistiken und Update Benachrichtigungen zu aktivieren. Weitere Informationen finden Sie auch in den Beispielen "providergdfexamplebinary" und "gamestatisticsexample".

Unter Windows Vista Business Edition, Windows 7 Professional Edition und Enterprise Edition von Windows Vista und Windows 7 wird der Link Games im Startmenü ausgeblendet. Spiele-Explorer ist weiterhin im Startmenü verfügbar, indem Sie auf **Alle Programme** und dann auf **Games** klicken.

Für zugeordnete Anwendungen, die mit Ihrem Spiel installiert werden, aber nicht selbst, können Sie in allen Versionen von Windows, einschließlich Windows Vista und Windows 7, Startmenü-Programm Gruppen, Verknüpfungen und Desktop Symbole erstellen. Solche zugeordneten Anwendungen sollten anwendbare Spiele für Windows-Anforderungen passieren. Weitere Informationen finden Sie unter [Richtlinien für Spiele Middleware-Produkte](#guidelines-for-game-middleware-products). Spiele Dienste werden empfohlen, sich mit Games Explorer als Spielanbieter für Windows 7 zu registrieren. 1

</dd> </dl>

### <a name="12-support-family-safety--parental-controls"></a>1,2 Unterstützung der Familien Sicherheit/Jugendschutz Kontrolle

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Spiele müssen die Sicherheit der Windows-Familie vollständig unterstützen, indem Sie die folgenden Regeln einhalten:

-   Spiele dürfen nicht verlangen, dass der Benutzer über Administrator Anmelde Informationen verfügt. Das installieren, Patchen und Entfernen von kann administrative Anmelde Informationen erfordern, je nach den Anforderungen in Abschnitt 3. (Im Zusammenhang mit der Anforderung 2,1 befolgen Sie die Richtlinien für die Benutzerkontensteuerung.)
-   Spiele, die von von Windows unterstützten bewertungsboards (z. b. ESRB und Peer) bewertet werden, müssen ihre zugewiesenen Bewertungsinformationen in Ihre Spiel Definitionsdatei (GDF) einschließen. Alle verfügbaren Bewertungsdaten müssen in jeder lokalisierten Version der GDF sowie in der sprach neutralen Version enthalten sein.
-   Spiele müssen Ihre ausführbaren Dateien im GDF auflisten, um eine gute Benutzerumgebung für allgemeine Anwendungs Einschränkungen bereitzustellen, es sei denn, das Spiel verwendet eine Antipiraterie-Technologie, die zur Laufzeit zufällig benannte ausführbare Dateien erstellt.
-   Spiele müssen während des Starts die **VerifyAccess** -Methode der Games Explorer-Schnittstelle aufrufen, sofern verfügbar, und beenden, wenn \* pfhasaccess als false zurückgegeben wird.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Alle Spiele müssen im Kontext eines Standard Benutzerkontos ausgeführt werden, damit Konten, die von Windows-Jugendschutz Steuerelementen gesteuert werden, das Spiel spielen können. Übergeordnete Elemente haben die Möglichkeit, den Zugriff auf Spiele durch Ihren Kinder zu überwachen und zu steuern. Außerdem wünschen zahlreiche Branchen-, Regierungs-und Interessengruppen bessere Möglichkeiten, um den übergeordneten Elementen zu ermöglichen, die Spiele zu überwachen und zu steuern, auf die die untergeordneten Elemente In Verbindung mit der Architektur von Games Explorer stellt Microsoft übergeordnete Steuerelemente von Windows übergeordnete Steuerelemente bereit.

Selbst bei spielen, die nicht an einem bewertungsboard-Programm teilnehmen, wird für die Mehrzahl der Benutzerkonten eine schlechte Wiedergabe Freundlichkeit geschaffen, wenn erhöhte Rechte erforderlich sind. Dies ist insbesondere dann der Fall, wenn die Jugend Kontrollen aktiviert sind, bei denen das übergeordnete Element bei jedem Start des Spiels das Administrator Kennwort eingeben muss.

Mit dem Windows-Steuerelement "Jugendschutz" können übergeordnete Steuerelemente auswählen, die für ihre untergeordneten Elemente geeignet sind. Elterliche Kontrollen unterstützen viele der weltweiten Bewertungssysteme. Mithilfe von Eltern Kontrollen können übergeordnete Steuerelemente den Zugriff auf Spiele auf der Grundlage von Inhalts Deskriptoren (sofern das anwendbare Bewertungssystem unterstützt) und das zulassen oder Verweigern des Zugriffs auf einzelne Spiele einschränken.

Die Standardauswahl für das Bewertungssystem für Windows-Jugend **Schutz-Steuer** Elemente basiert auf der Gebiets Schema Einstellung des Systems, kann jedoch vom Benutzer in den Regions **-und Sprachoptionen** in der Systemsteuerung geändert werden. Daher sollte jede unterstützte Sprache alle verfügbaren Bewertungsdaten bereitstellen, sodass der Benutzer die Möglichkeit hat, das gewünschte bewertungsboard auszuwählen.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Spiele ohne Bewertung müssen weiterhin die Anforderungen erfüllen, um die Wiedergabe als Standard Benutzer zu unterstützen und " **VerifyAccess**" aufzurufen. Diese Spiele werden standardmäßig auf die Kategorie "nicht bewertet" festgelegt, zeigen den Text "keine Bewertung bereitgestellt" in Games Explorer an und unterliegen der Einstellung " **Spiel Einschränkungen** " in Jugendschutz **Kontrollen** für nicht bewertete Spiele. Die Standardeinstellung für **Einschränkungen** ist zulassen.

Bewertungsinformationen im GDF werden ignoriert, wenn die enthaltende Binärdatei nicht ordnungsgemäß mit Authenticode signiert ist. Siehe Anforderung 2,3.

Der spieldefinitions-Datei-Editor im DirectX SDK umfasst alle unterstützten Bewertungssysteme und repliziert diese Informationen ordnungsgemäß in alle lokalisierten Versionen der GDF sowie in einer sprach neutralen Version. Das gdftrace-Tool decodiert und überprüft alle Bewertungsinformationen, die vorhanden sind. Verwenden Sie die Version vom August 2009 oder später dieser Tools.

Die GDF für einen Spielanbieter enthält in der Regel keine Bewertungsinformationen und unterliegt den Einstellungen für nicht bewerteten Inhalt.



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
<li>Peer (Europa)</li>
<li>Peer-Finnland (veraltet)</li>
<li>Peer-Portugal</li>
<li>Peer-/BBFC (Vereinigtes Königreich)</li>
<li>USA (Deutschland)</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows Vista mit einer Service Pack</td>
<td>Service Packs für Windows Vista fügen Unterstützung für Folgendes hinzu:<br/>
<ul>
<li>GRB (Südkorea)</li>
<li>ESRB-, &quot; milde &quot; Variant-Inhalts Deskriptoren</li>
</ul></td>
</tr>
<tr class="odd">
<td>Windows 7</td>
<td>Windows 7 unterstützt die von Windows Vista unterstützten Bewertungssysteme und bietet Unterstützung für Folgendes: <br/>
<ul>
<li>CSRR (Taiwan)</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows 8</td>
<td>Windows 8 unterstützt die vorherigen Bewertungssysteme und bietet Unterstützung für Folgendes:<br/>
<ul>
<li>COB-au (Australien)</li>
<li>Djctq (Brasilien)</li>
<li>PFB (Südafrika)</li>
<li>OFLC-NZ (Neuseeland)</li>
</ul>
Windows 8 unterstützt die folgenden veralteten Systeme:<br/>
<ul>
<li>Peer-fi (Finnland)</li>
<li>OFLC (Australien)</li>
</ul></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Jeder Titel, der neue ESRB Windows Vista Service Pack 1 (SP1)-Inhalts Deskriptoren enthält, wird unter Windows Vista ohne Service Pack als nicht bewertet angezeigt.

 

Neuere Bewertungsdaten werden bei Versionen von Betriebssystemen ohne Unterstützung ignoriert. Die Variante von "Peer-(Finnland)" ist jetzt veraltet und wird zugunsten des standardmäßigen Peer-Bewertungssystems (Europa) eingestellt. Das OFLC-System ist nun als veraltet für "COB-au für Australien" eingestellt.

Weitere Informationen dazu, wie Sie ein Spiel mit Standardbenutzer Berechtigungen kompatibel machen, finden Sie im DirectX-Artikel [Benutzerkontensteuerung für Spieleentwickler](/windows/desktop/DxTechArts/user-account-control-for-game-developers).

Weitere Informationen zur Spiel Definitionsdatei (GDF) finden Sie unter Anforderung 1,1.

</dd> </dl>

### <a name="13-support-rich-saved-games"></a>1,3 Unterstützung von umfangreichen gespeicherten spielen

\[Diese Anforderung wurde zurückgezogen.\]

### <a name="14-support-the-xbox-360-common-controller-for-windows-conditional-requirement"></a>1,4 Unterstützung von "Xbox 360 Common Controller for Windows \[ Conditional Requirements"\]

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Spiele, die Gamepad-Controller unterstützen, müssen den Xbox 360-Controller für Windows mithilfe der [xinput](/windows/desktop/xinput/xinput-game-controller-apis-portal) -API unterstützen. Wenn DirectInput-Peripheriegeräte ebenfalls unterstützt werden, kann auch DirectInput verwendet werden. Xinput muss jedoch die Standard-API sein, wenn ein Xbox 360-kompatibles Gerät verwendet wird.

Alle Verweise auf allgemeine Controller Trigger und-Schaltflächen müssen die Xbox 360-Namen verwenden. Weitere Informationen finden Sie in der Liste der [Begriffe "Xbox 360 Common Controller for Windows](#xbox-360-common-controller-for-windows-terminology) ".

Die Controller Vibrationen müssen ausgeschaltet werden, wenn sich das Spiel im angehaltenen oder angehaltenen Zustand befindet.

Das Maus-/Tastatur-Steuerelement kann jederzeit nicht vollständig deaktiviert werden. Es muss mindestens eine Option zum zurückkehren zu den Spiel Menüs verfügbar sein.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Diese Anforderung gibt den Spieler die Möglichkeit, entweder den Xbox 360-Controller oder die Tastatur und die Maus zu verwenden, je nachdem, welche Eingabemethode eine natürlichere und intuitivere Benutzeroberfläche ist.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Diese Anforderung gilt nicht für Spiele, die nur die Maus und/oder die Tastatur verwenden.

Es wird empfohlen, die Menü Navigation zu implementieren, um die weit verbreiteten Standard Controller Schaltflächen zu verwenden:

-   A-Accept
-   B-Abbrechen
-   Start-Accept oder Pause
-   Zurück-abbrechen, einen Bildschirm oder eine Menü Ebene nach oben

Weitere Informationen finden Sie unter [xinput](/windows/desktop/xinput/xinput-game-controller-apis-portal).

Im Thema [XInput und DirectInput](/windows/desktop/xinput/xinput-and-directinput) werden Probleme bei der gleich zeigenden Verwendung beider APIs erörtert.

Es wird empfohlen, DirectInput nicht zum Implementieren von Tastatur-oder Maus Steuerelementen zu verwenden. Tastatur-und Maus Steuerelemente sollten nur mithilfe von Windows-Meldungen und Win32-APIs implementiert werden. Ausführliche Informationen zum erhalten von Informationen zur Mausbewegung mit hoher Auflösung ohne DirectInput finden Sie [unter Nutzen der High-Definition Mausbewegung](/windows/desktop/DxTechArts/taking-advantage-of-high-dpi-mouse-movement).

</dd> </dl>

### <a name="15-support-multiple-aspect-ratios-and-resolutions"></a>1,5 Unterstützung mehrerer Seitenverhältnisse und Auflösungen

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Das Spiel muss mindestens die folgenden Seitenverhältnisse und zugeordneten Bildschirmauflösungen unterstützen:

-   4:3 Normal (800 600 oder 1024 768)
-   16:9-Breitbild (1280 720)
-   16:10-Breitbild (1152 720 oder 1680 1050 oder 800 480)

Für die Konfiguration und Erkennung der Bildschirmauflösung muss das Spiel den folgenden Regeln entsprechen:

-   Das Spiel verwendet standardmäßig die Desktop Auflösung des Anzeige Geräts, wenn es sich um eine unterstützte Auflösung handelt. Das Seitenverhältnis des Desktops muss als Suchkriterium verwendet werden, wenn das Spiel eine andere Standardauflösung wählt.
-   Das Spiel muss den Benutzer auffordern, neue Anzeigeeinstellungen zu bestätigen, wenn eine Änderung vorgenommen wird. Wenn der Benutzer nicht innerhalb von 15 Sekunden akzeptiert, muss die Anzeige auf die vorherige Einstellung zurückgesetzt werden.
-   Das Spiel darf keine Pixel Strecken oder ein 4:3-Rendering-Fenster zentrieren, um die Unterstützung der Widescreen-Seitenverhältnisse Das Letterbox ist jedoch akzeptabel.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Beim Windows 3D-Desktop kann aufgrund der folgenden Faktoren nicht auf ein bestimmtes Seitenverhältnis oder eine bestimmte Auflösung eingegangen werden:

-   Unterstützung für detaillierte anzeigen.
-   Erhöhter Marktanteil von Breitbild Monitoren.
-   HDTV-bereit Stellungen für Windows Media Center.
-   Barrierefreiheits Anforderungen.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Im Idealfall verwendet das Spiel standardmäßig das systemeigene Seitenverhältnis der Anzeige. Das zuverlässige Abrufen dieser Informationen kann jedoch eine Herausforderung darstellen. als allgemeinere Lösung kann das Spiel beispielsweise davon ausgehen, dass der Desktop mit dem systemeigenen Seitenverhältnis ausgeführt wird. Die Desktop Auflösung kann durch Aufrufen von [**enumdisplaysettings**](/windows/desktop/api/winuser/nf-winuser-enumdisplaysettingsa) mit enumerationsregistrierungs Einstellungen abgerufen werden \_ \_ .

Weitere Informationen finden Sie in den Abschnitten "Seitenverhältnis" und "Widescreen" im DirectX-Artikel [Einführung in die 10-Fuß-Darstellung für Windows-Spieleentwickler](/windows/desktop/DxTechArts/introduction-to-the-10-foot-experience-for-windows-game-developers).

</dd> </dl>

### <a name="16-support-launch-from-windows-media-center"></a>1,6 Support von Windows Media Center starten

\[Diese Anforderung wurde zurückgezogen.\]

### <a name="17-direct3d-support"></a>1,7 Direct3D-Unterstützung

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Wenn das Spiel Direct3D verwendet, muss die mindestens unterstützte Version Direct3D 9 sein, und Direct3D muss der Standard-Renderer ausgewählt sein.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Die Windows Vista-und Windows 7-Kern Grafik Architektur ist um Direct3D ausgelegt. Direct3D 8 und frühere Versionen werden durch das Neuzuordnen von Legacy Schnittstellen unterstützt.

Die Verwendung von Versionen von Direct3D neuer als Direct3D 9 wird dringend empfohlen. Sehen Sie sich die Spiele für Windows-Showcase S. 1 an. Das verlangen von Direct3D 10 oder Direct3D 11 ist vollständig mit der Anforderung 1,7 kompatibel.

</dd> </dl>

### <a name="18-enable-high-dpi-aware"></a>1,8 Aktivieren von High-dpi-Werten

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Spiele und deren Installer müssen ohne visuelle Probleme ordnungsgemäß ausgeführt werden, wenn die DPI-Skalierung (dpi) aktiviert ist (mit 144 dpi für 150% Skalierung bei der Bildschirmauflösung von 1600 1200) unter Windows Vista und Windows 7.

Dies erfordert in der Regel, dass die ausführbare Datei des Spiels die dpi-Werten deklariert. Dies wird durch Einbetten eines manifeselement erreicht: <dpiAware> true <dpiAware> .

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Hochwertige LCD-Monitore sind bei der Anzeige des Computers üblich, und Sie sehen sich am besten an, wenn Sie auf ihre systemeigenen Auflösungen (in der Regel 1280 1024, 1600 1200 usw.) abzielen. Kunden, die Probleme mit dem Lesen von Text und der Anzeige von Bildern bei dieser Lösung haben, legen die Computer Desktops häufig auf eine geringere Auflösung fest und haben visuelle Artefakte von der LCD-Skalierung Stattdessen können Kunden die Auflösung in der systemeigenen Größe belassen und den dpi-Wert der Windows-Anzeige ändern, sodass die Element-und Textdarstellung größer wird, ohne die Bildqualität zu beeinträchtigen.

Obwohl dieses Feature seit Windows XP in irgendeiner Form verfügbar ist, wird es selten von Kunden oder OEMs aktiviert. Mehr als die Hälfte der Computer, die heute angezeigt werden, sind auf eine niedrigere Auflösung festgelegt als die systemeigene Auflösung des Monitors, basierend auf Kundenfeedback. Windows 7 macht diese Funktion für Kunden bei der anfänglichen Einrichtung und bei der Änderung der Anzeigeeinstellungen deutlich besser sichtbar, sodass Sie die DPI-Skalierung verwenden können, anstatt die Desktop Auflösung zu ändern.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Die [**SetProcessDPIAware**](/windows/desktop/api/winuser/nf-winuser-setprocessdpiaware) -Funktion kann stattdessen verwendet werden, wenn Sie früh im Prozessstart Code aufgerufen wird. Das Hinzufügen zum Manifest wird bevorzugt, um sicherzustellen, dass keine Racebedingungen mit Software Elementen (z. b. DLLs) vorliegen, die vor dem Aufrufen des Haupt Einstiegs Punkts initialisiert werden können. Beachten Sie, dass **SetProcessDPIAware** nur unter Windows Vista und Windows 7 vorhanden ist.

Das Hinzufügen des Manifest-Elements ist mit Visual Studio 2005 und 2008 einfach. Erstellen Sie eine Datei mit dem Namen "dpiaware. Manifest", die den folgenden Text enthält:

``` syntax
            <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0" xmlns:asmv3="urn:schemas-microsoft-com:asm.v3">
            <asmv3:application>
            <asmv3:windowsSettings xmlns="http://schemas.microsoft.com/SMI/2005/WindowsSettings">
            <dpiAware>true</dpiAware>
            </asmv3:windowsSettings>
            </asmv3:application>
            </assembly>
```

Fügen Sie dann in Visual Studio dem Projekt die Datei dpiware. Manifest hinzu. Stellen Sie sicher, dass das **Einbettungs Manifest** in den Eigenschaften des Projekts auf **Ja** festgelegt ist. Beachten Sie, dass ältere Versionen des Manifest-Tools (Mt.exe) eine falsche Warnung mit den dpi-fähigen manifestressementen generieren. Aktualisieren Sie Mt.exe auf die neueste Version des Windows SDK, um dieses Problem zu beheben.

Visual Studio 2010 enthält eine Einstellung in den Projekteigenschaften mit dem Namen " **dpi-Bewusstsein aktivieren**", die eine Datei wie "dpiaware. Manifest" nicht mehr benötigt. Suchen Sie die Option dpi-Erkennung **aktivieren** , indem Sie **Konfigurations Eigenschaften** und **Manifest-Tool** erweitern und dann **Eingabe & Ausgabe** auswählen.

Unter Windows wird der herkömmliche Anzeigemodus standardmäßig auf 96 dpi festgelegt, was für CRT-Monitore üblich war.

Während Vollbildanwendungen die Bildschirmauflösung ändern, verwenden Sie häufig Fenster Meldungen und Metriken, wenn Sie Puffer einrichten und Rechtecke anzeigen. Die dpi-Virtualisierung bewirkt, dass diese Vollbild-Anzeigemodi beschnitten angezeigt werden, und das Deklarieren von dpi-Werten verhindert diese Probleme. Weitere Informationen finden Sie unter [Schreiben von DPI-Aware Win32-Anwendungen](../hidpi/high-dpi-desktop-application-development-on-windows.md).

</dd> </dl>

## <a name="security-and-compatibility"></a>Sicherheit und Kompatibilität

**Zusammenfassung der Sicherheits-und Kompatibilitätsanforderungen**

**Kunden Vorteile**

Die folgenden Anforderungen verbessern die Gesamtsicherheit von spielen und sorgen dafür, dass Sie mit Windows auf verschiedenen Architekturen, unter verschiedenen Konfigurationen und in unterschiedlichen Modi funktionieren.

### <a name="21-follow-user-account-control-guidelines"></a>2,1 befolgen Sie die Richtlinien zur Benutzerkontensteuerung

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Jede ausführbare Datei (d. h. jede Datei mit der Erweiterung. exe) muss ein eingebettetes Manifest enthalten, das die Ausführungs Ebene durch Einschließen des folgenden Tags definiert:

``` syntax
            <requestedExecutionLevel>
```

Pro Anforderung 1,2 müssen das Hauptspiel und die ausführbare autorun-Datei die Ausführungs Ebene "asInvoker" aufweisen, um Standard Benutzer Kontexte zu unterstützen.

Benutzer Datendateien, die über Dateizuordnungen verfügen, die im **Datei-Explorer** registriert sind, müssen in einem Unterordner des Ordners abgelegt werden, der von CSIDL \_ Personal (auch als **Dokumente** oder **Eigene Dokumente** bezeichnet) angegeben wird. Alle anderen Benutzer Datendateien müssen in einem Unterordner der Ordner gespeichert werden, die von \_ lokalen \_ AppData-oder CSIDL- \_ AppData (CSIDL) angegeben werden \_ . (Diese Verzeichnisse werden standardmäßig für einzelne Benutzer und für alle Benutzer ausgeblendet.)

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Die Windows-Benutzer Darstellung eines Benutzers ist sicherer, wenn Anwendungen nur mit den erforderlichen Berechtigungen ausgeführt werden.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Wenn nur einige Features in einer Anwendung Administratorrechte erfordern (z. b. eine Anwendung, die eine Firewall konfigurieren muss), muss der Hauptprozess der Anwendung weiterhin mit Standardbenutzer Berechtigungen ausgeführt werden. Funktionen, für die Administratorrechte erforderlich sind, müssen in einen separaten Prozess verschoben werden, z. b. ein Installationsprogramm oder ein Konfigurations Hilfsprogramm

Wenn keine Administratorrechte erforderlich sind, sollte die eingebettete Manifest-XML Folgendes umfassen:

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

Wenn Administratorrechte erforderlich sind, sollte die eingebettete Manifest-XML Folgendes umfassen:

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

Mit Visual Studio 2005 kann dies problemlos eingebettet werden, indem Sie dem Projekt einfach eine Manifest-Datei (Manifest-Datei) hinzufügen, die einen der vorangehenden Blöcke enthält, und sicherstellen, dass das **Einbettungs Manifest** im Projekteigenschaften für das Manifest-Tool auf **Yes** festgelegt ist. Für Visual Studio 2008 und 2010 können UAC-Eigenschaften direkt in den Projekteigenschaften für den Linker auf der Seite **Manifest-Datei** festgelegt werden. Beachten Sie, dass ältere Versionen des Manifest-Tools (Mt.exe) eine falsche Warnung mit den UAC-Manifest-Elementen generieren. Aktualisieren Sie Mt.exe auf die neueste Version des Windows SDK, um dieses Problem zu beheben.

Ausführliche Informationen zu den besonderen Installations-, Patching-und Entfernungs Fällen finden Sie unter Anforderung 3,1.

Dynamic Link Libraries (DLLs) erfordern keine solchen Manifeste.

Weitere Informationen zur Benutzerkontensteuerung finden Sie unter [Benutzerkontensteuerung für Spieleentwickler](/windows/desktop/DxTechArts/user-account-control-for-game-developers).

</dd> </dl>

### <a name="22-support-windows-x64-versions"></a>2,2 Unterstützung für Windows x64-Versionen

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Um die Kompatibilität mit 64-Bit-Editionen von Windows aufrechtzuerhalten, sollten Spiele die folgenden Anforderungen erfüllen.

-   Titel und Titel-Installer dürfen keinen 16-Bit-Code enthalten oder auf eine 16-Bit-Komponente zurückgreifen.
-   Wenn das Spiel von Kernelmodustreibern für den Betrieb abhängt, müssen x64-Versionen dieser Treiber verfügbar sein. Die Spiel Einrichtung muss die richtigen Treiber und Komponenten für die 64-Bit-Editionen von Windows erkennen und installieren.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Viele Windows Vista-und Windows 7-Benutzer führen die 64-Bit-Editionen des Betriebssystems über die Lebensdauer des Produkts aus. Daher ist es wichtig, dass Anwendungen mit diesem Betriebssystem kompatibel sind.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Windows unter Windows 64 (WOW64) ermöglicht das Ausführen von 32-Bit-Code auf 64-Bit-Editionen von Windows. Daher ist es nicht erforderlich, dass die 64 Anwendung 64 auf der Windows-Version von Windows auf der Basis von Windows-Editionen in der Windows-Version ist. 16-Bit-Code kann nicht auf 64-Bit-Editionen von Windows ausgeführt werden.

Die Beibehaltung der Kompatibilität mit Windows XP Professional x64 Edition ist nicht erforderlich, wird jedoch dringend empfohlen.

Weitere Informationen finden Sie unter [64-Bit-Programmierung für Spieleentwickler](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers).

</dd> </dl>

### <a name="23-sign-files"></a>2,3 Signier Dateien

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Alle ausführbaren Code Dateien (in der Regel Dateien mit der Erweiterung ". exe" oder ". dll") müssen mit einem öffentlich gültigen Authenticode-Zertifikat signiert werden und müssen über eine gültige Zeitstempel Server-URL für die Produktions Signatur verfügen.

Wenn Ihr Spiel Windows Installer verwendet, müssen die Installer-Paketdateien (MSI-Dateien) signiert sein.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Das Signieren einer Datei hilft Benutzern bei der Entscheidung, ob eine Anwendung als vertrauenswürdig eingestuft wird, und stellt sicher, dass Benutzer nicht manipuliert wurden. Außerdem können Anwendungen in gesperrten Umgebungen ordnungsgemäß ausgeführt werden.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Weitere Informationen finden Sie [unter Authenticode-Signierung für Spieleentwickler](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).

Wenn Ihr Spiel Windows Installer verwendet, wird empfohlen, dass Sie UAC/Lua-Patching aktivieren, indem Sie eine MsiPatchCertificate-Tabelle einschließen. Weitere Informationen finden Sie unter [User Account Control (UAC) Patching](/windows/desktop/Msi/user-account-control--uac--patching).

Es wird nicht empfohlen, CAB-Dateien (CAB-Dateien) zu signieren, es sei denn, Sie sind relativ klein (weniger als 100 MB).

</dd> </dl>

### <a name="24-sign-drivers"></a>2,4-Signatur Treiber

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Jeder Kernelmodustreiber, der durch das Spiel installiert wird, muss mit einem öffentlich gültigen Authenticode-Zertifikat signiert werden.

Jeder vom Spiel installierte Kernel Modus-Hardware Gerätetreiber muss über eine Microsoft-Signatur verfügen, die vom Windows Hardware Quality Labs (WHQL) oder vom DRS (Driver Zuverlässigkeits Signature)-Programm abgerufen werden kann.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Schlecht geschriebene oder schadsoftwaretreiber können die Stabilität und Sicherheit eines Systems stark beeinträchtigen. Bei 64-Bit-Editionen von Windows Vista und Windows 7 werden nicht signierte Treiber nicht geladen. Diese Richtlinie kann auch für 32-Bit-Editionen von Windows Vista und Windows 7 aktiviert werden.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Pro Anforderung 2,2 werden sowohl die systemeigenen 32-Bit-als auch die 64-Bit-Version aller Kernelmodustreiber benötigt.

Weitere Informationen zu Microsoft-Treiber Signatur Programmen finden Sie im [Windows-Hardware Entwickler Portal](https://www.microsoft.com/whdc/winlogo/hwrequirements.mspx).

</dd> </dl>

### <a name="25-perform-proper-version-checking"></a>2,5 Ausführen einer ordnungsgemäßen Versions Überprüfung

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Spiele dürfen nicht für zukünftige Betriebssysteme ausgeführt werden, die durch Änderungen der Windows-Versionsnummer angegeben werden, es sei denn, der Endbenutzer-Lizenzvertrag untersagt die Verwendung bei zukünftigen Betriebssystemen. Wenn das Spiel fehlschlagen soll, muss es ordnungsgemäß ausgeführt werden, indem dem Benutzer eine entsprechende Meldung angezeigt wird.

Wenn Windows-Versions Überprüfungen vorgenommen werden, müssen die APIs für die Versions Überprüfung ([**GetVersionEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa) oder [**verifyversioninfo**](/windows/desktop/api/winbase/nf-winbase-verifyversioninfoa)) verwendet werden, um die Betriebssystemversion zu überprüfen. Die Registrierungsschlüssel dürfen nicht gelesen werden, um die Version zu bestimmen.

Explizite Versions Prüfungen für die DirectX-Laufzeit dürfen im Spiel nicht vorhanden sein. Diese Versions Prüfungen dürfen nicht in der Installation vorhanden sein, die das DirectX-Lauf Zeit Setup (DirectSetup) gestartet.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Wenn Windows-Benutzer ein Upgrade ihrer Betriebssysteme durchführen, sollten Sie die Spiele der aktuellen Spiele nicht blockieren, weil sich die Windows-Versionsnummer verbessert hat. Schlecht geschriebene Versions-Checker erstellen weiterhin Probleme für Software, die in neueren Versionen von Windows oder einfach mit dem Hinzufügen eines Windows-Service Pack einwandfrei funktioniert.

Die Vergleichs Logik der fragilen Versions Überprüfung für die DirectX-Laufzeit hat zahlreiche fehlgeschlagene Installationen erstellt, wenn Sie in verschiedenen Versionen von Windows ausgeführt wird. Die DirectX-Versionsnummer gilt nur für die wichtigsten Betriebssystemkomponenten. Es gilt nicht für die parallelen DirectX SDK-Komponenten, die von vielen Spielen verwendet werden.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Es kommt häufig vor, dass Installationsprogramme auf eine Mindestversion des Betriebssystems überprüft werden. Diese Überprüfung muss jedoch sorgfältig durchgeführt werden, um sicherzustellen, dass Sie auf eine größere oder gleichmäßige statt auf einfache Gleichheit prüft und somit eine Sperre für eine bestimmte Version des Betriebssystems durchzuführen. Die Verwendung von Application Verifier **highversionlag** -Test ist eine schnelle und einfache Möglichkeit, um zu bestimmen, wie Ihr Installer auf eine bedeutende Änderung der Betriebssystem-Versionsnummer reagieren wird.

Die ordnungsgemäße Verwendung des DirectX-Lauf Zeit Weitergabepakets (DirectX-Setup) umfasst das automatische Starten während der Installation, vorzugsweise im unbeaufsichtigten Modus. Dadurch kann der von Microsoft bereitgestellte Code alle erforderlichen Versions Updates ausführen. Sie ermöglicht auch die Installation optionaler paralleler DirectX-SDK-Komponenten, z. b. D3DX, XACT, MDX oder xinput.

Bewährte Methoden für die Bereitstellung der DirectX-Laufzeit finden Sie unter [DirectX-Installation für Spieleentwickler](/windows/desktop/DxTechArts/directx-setup-for-game-developers).

Es wird empfohlen, dass Spiele, die Windows XP unterstützen, eine Service Pack Stufe von 2 oder höher überprüfen, da Service Pack 2 (SP2) und Service Pack 3 (SP3) bedeutende Verbesserungen an der Sicherheit, eine vereinfachte Anforderung der DirectX-Lauf Zeitverteilung und eine extrem breite Bereitstellung bieten. Die meisten modernen Microsoft-Technologien, die Windows XP unterstützen, erfordern SP2 oder SP3 (XAudio2, Games for Windows-Live usw.).

</dd> </dl>

### <a name="26-support-concurrent-user-sessions"></a>2,6 Unterstützung von gleichzeitigen Benutzersitzungen

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Spiele, die auf 3D-Grafiken basieren, sind nicht erforderlich, um über eine Remote Desktop Verbindung zu arbeiten. der Benutzer muss jedoch benachrichtigt werden, wenn das Spiel fehlschlägt.

Spiele müssen standardmäßige Windows-Multitasking-Szenarien unterstützen, indem Sie die folgenden Regeln einhalten:

-   Spiele dürfen die Verwendung von gleichzeitigen Benutzersitzungen nicht blockieren.
-   Ein Spiel muss in einer neuen Benutzersitzung ausgeführt werden, wenn es bereits in einer anderen Sitzung ausgeführt wird.
-   Spiele Geräusche in einer Benutzersitzung dürfen nicht gehört werden, wenn ein anderer Benutzer in einer anderen Sitzung aktiv ist.
-   Spiele müssen die schnelle Benutzerumschaltung unterstützen.
-   Spiele dürfen nicht versuchen, den Standard Task Wechsel zu deaktivieren. Spiele dürfen die Tastenkombination Alt + Tab nicht deaktivieren. Spiele dürfen Zugriffstasten Kombinationen deaktivieren, wie unter [Deaktivieren von Tastenkombinationen in spielen](/windows/desktop/DxTechArts/disabling-shortcut-keys-in-games)beschrieben.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Windows-Benutzer sollten in der Lage sein, gleichzeitige Sitzungen ohne Konflikte oder Unterbrechungen auszuführen. Dies ist ein gängiges Szenario für einen Windows-Computer, der von einer Familie, einem RoomMates oder anderen Benutzern gemeinsam genutzt wird.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Um zu testen, ob das Spiel in einer Remote Sitzung gestartet wird, nennen Sie [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)(SM \_ remotesession). Ein Wert ungleich 0 (null) gibt an, dass die Sitzung Remote ist.

Weitere Informationen finden Sie unter [schnelle Benutzerumschaltung](/windows-hardware/drivers/display/fast-user-switching). Beachten Sie, dass die schnelle Benutzerumschaltung auftritt, wenn die Zeitbeschränkungen der Jugend Kontrollen aktiviert sind, wenn die Benutzer Zeit in der Zeit liegt Weitere Informationen finden Sie unter Anforderung 1,2.

</dd> </dl>

### <a name="27-support-long-names"></a>2,7 Unterstützung von langen Namen

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Wenn ein Spiel das Speichern von Dateien unterstützt, muss es in der Lage sein, Dateien mit langen Namen und Pfaden zu speichern. Das Spiel muss spezielle Dateisystem Zeichen ordnungsgemäß verarbeiten, z. b. \\ /: \* ? " < > in allen Benutzereingabe Feldern, die zum Erstellen von Dateinamen oder Pfaden verwendet werden.

Spiele müssen ordnungsgemäß funktionieren, wenn ein Benutzer über einen langen Benutzernamen verfügt.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Die Spieler sind daran gewöhnt, lange Namen in Deep-Pfaden zu verwenden, die vom zugrunde liegenden Betriebssystem unterstützt werden.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Lange Namen werden als jene definiert, die die maximalen Werte enthalten, die in der Windows SDK definiert sind.

</dd> </dl>

## <a name="installation"></a>Installation

**Zusammenfassung der Sicherheits-und Kompatibilitätsanforderungen**

**Kunden Vorteile**

Kunden können sich darauf verlassen, dass Anwendungen unter Windows installiert werden, ohne das Betriebssystem oder andere Anwendungen zu beeinträchtigen, wenn Anwendungen offizielle Verteilungsmethoden für Systemkomponenten verwenden. Eine optimierte Installation bietet eine besser verfügbare und problemlose out-of-Box-Funktion für Spiele.

### <a name="31-support-easy-installation"></a>3,1 Unterstützung der einfachen Installation

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Spiele müssen einen vereinfachten Pfad in der Setup-Benutzeroberfläche bereitstellen, indem Sie Folgendes implementieren:

-   Maximal eine EULA-Eingabeaufforderung anzeigen.
-   Der Standard Installationspfad muss alle Auswahlmöglichkeiten für die Installation umgehen (z. b. Installationsordner oder Komponentenauswahl), die Standardauswahl annehmen und dann das Spiel oder das Start Programm nach erfolgreicher Installation ausführen, ohne dass zusätzliche Eingabe Aufforderungen angezeigt werden. Falls gewünscht, kann eine benutzerdefinierte Installationsoption für Erweiterte Konfigurationsoptionen bereitgestellt werden.
-   Installieren Sie alle erforderlichen Betriebssystemkomponenten (z. b. DirectX-und Visual C-Laufzeiten) mithilfe der richtigen Microsoft-Verteilungs Pakete. Die Installation sollte unbeaufsichtigt ausgeführt werden, ohne dass eine Aufforderung angefordert und keine Überprüfung der Komponenten Version durchgeführt werden muss.
-   Stellen Sie die Entfernung über **Programme und Funktionen** in der **Systemsteuerung** sowohl für die Spiel Anwendung als auch für generierte Arbeitsdateien bereit. Eine Option zum Löschen von Datendateien, die vom Benutzer erstellt werden, wird empfohlen. Beim Entfernungs Vorgang muss sichergestellt werden, dass alle installierten Dateien entfernt werden und alle Einstellungen (z. b. Firewallausnahme-Listeneinträge und Registrierungsschlüssel) gelöscht werden. Neuverteilte Betriebssystemkomponenten dürfen nicht entfernt werden.
-   Wenn das Spiel Ausnahmen zur Windows-Firewall hinzugefügt werden muss, kann der Setup Vorgang auffordern, Benutzer darüber zu informieren, dass diese Änderung erforderlich ist. Diese Eingabeaufforderung sollte vor Beginn der Installation angezeigt werden.

Das Installieren und Entfernen von kann Administratorrechte erfordern. Das Patchen kann abhängig von der Aktualisierungshäufigkeit eine Aufforderung zur Eingabe administrativer Anmelde Informationen erfordern. Für das normale spielen des Spiels dürfen keine Administratorrechte erforderlich sein. 2,1 befolgen Sie die Richtlinien für die Benutzerkontensteuerung.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Die einfache Installation ist eine Windows-zentrierte Spiel Entwicklungsphilosophie, mit der der manchmal mühsame und unübersichtlich Prozess der Installation von Spielen auf Computern, auf denen Windows-Betriebssysteme ausgeführt werden, vereinfacht und optimiert werden soll. Die einfache Installation wird durch die Verwendung einer Reihe von Technologien und bewährten Methoden ermöglicht, die die unnötige Komplexität und das erkannte Risiko der Installation von Spielen auf Windows-Computern verringern.

Die wichtigsten Ziele sind:

-   Verkürzen Sie den Zeitaufwand für das Spiel, und beginnen Sie mit der Wiedergabe.
-   Reduzieren Sie die Anzahl der Dialogfelder und Optionen auf nur wenige oder keine, um die Spielinstallation zu vereinfachen.

Einige herkömmliche Installationen enthalten Eingabe Aufforderungen, die nicht funktionstüchtige Installationen zulassen, obwohl die Anwendung anscheinend erfolgreich installiert wurde. Beispielsweise kann ein Spiel verlangen, dass ein Benutzer einen EULA akzeptiert. Anschließend wird das Spiel installiert, und die DirectX-EULA wird angezeigt. Diese Lizenzbedingungen ermöglichen es Benutzern, die Installation der DirectX-Laufzeit abzulehnen und damit zu überspringen. Dieses Szenario kann zu einem Spiel führen, das aufgrund fehlender Komponenten nicht ausgeführt werden kann.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Weitere Informationen zur Spiele Installation, nicht herkömmlichen Techniken zur Spielinstallation, UAC-kompatiblen Patchlösungen und zum Verarbeiten von häufigen Patches finden Sie in den folgenden DirectX-Artikeln:

-   [Vereinfachen der Spiele Installation](/windows/desktop/DxTechArts/simplifying-game-installation)
-   [Installation bei Bedarf für Spiele](/windows/desktop/DxTechArts/install-on-demand-for-games)
-   [Patchen von Spiel Software in Windows XP, Windows Vista und Windows 7](/windows/desktop/DxTechArts/patching-methods-in-windows-xp-and-vista)
-   [Bewährte Methoden für die Installation von Massively Multiplayer Online Games](/windows/desktop/DxTechArts/mmo-installation-best-practices)

> [!Note]  
> Das Entfernen Benutzer spezifischer generierter Datendateien sollte nur für den aktuellen Benutzer und für gemeinsame freigegebene Benutzerspeicher Orte ausgeführt werden. Es gibt keinen robusten Weg, das System zu überprüfen, um benutzerspezifische Dateien für andere Benutzer zu entfernen, auch wenn für das Entfernen administrative Anmelde Informationen erforderlich sind.

 

</dd> </dl>

### <a name="32-support-user-account-control-for-installation"></a>3,2 Unterstützung der Benutzerkontensteuerung für die Installation

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Der Game Installer darf nicht davon ausgehen, dass er im gleichen Kontext wie der Benutzer ausgeführt wird. Benutzerspezifische Speicherorte unterscheiden sich vom Installer und vom Player selbst für Einzelbenutzer Systeme aufgrund der Erhöhung der Rechte für die Administratorrechte. Wenn ein Spiel zum ersten Mal ausgeführt wird, muss es daher unabhängig vom Installationsvorgang benutzerspezifische Tasks ausführen.

Das Dialogfeld "Ausnahme der Windows-Firewall" darf nicht angezeigt werden, wenn ein Benutzer ein Multiplayer-Spiel hostet Alle erforderlichen Konfigurationen müssen zum Installations Zeitpunkt ausgeführt werden. Die Setup Anweisungen sollten den Benutzer darüber informieren, dass dieser Vorgang im Rahmen des Setups stattfindet.

Das Game Installer muss ein eingebettetes Manifest bereitstellen, das die erforderliche Ausführungs Ebene festlegt, je nach Anforderung 2,1 gemäß den Richtlinien für die Benutzerkontensteuerung.

Wenn das Spiel nach Abschluss der Installation vom Installationsprogramm gestartet wird, muss es im Kontext des ursprünglichen Benutzers gestartet werden.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Eine der größten Änderungen am Windows-Betriebssystem in Windows Vista ist das Hinzufügen der Benutzerkontensteuerung (User Account Control, UAC), mit der standardmäßig Anwendungen mit eingeschränkten Berechtigungen ausgeführt werden. Daher müssen die Installationsprogramme Berechtigungsstufen entsprechend verwalten. Windows 7 nutzt auch die UAC umfassend. Obwohl Windows 7 die Benutzer Leistung von UAC verbessert, müssen Installationsprogramme immer noch dieselben Anforderungen wie bei Windows Vista erfüllen, damit Sie ordnungsgemäß funktionieren, ohne dass sich dies auf das potenziell verwirrende Virtualisierungsverhalten verlässt.

UAC ist unter Windows Vista und Windows 7 standardmäßig aktiv, und die große Mehrheit der Kunden (88% oder mehr, basierend auf dem Feedback) lassen diese Funktion aktiviert.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Weitere Informationen zum Konfigurieren der Windows-Firewall finden Sie im DirectX-Artikel [Windows-Firewall für Spieleentwickler](/windows/desktop/DxTechArts/games-and-firewalls) und im firewallinstallhelper-Beispiel.

Der Standard Start des Spiels am Ende des Installationsvorgangs kann den letzten Aspekt dieser Anforderung nicht erfüllen, wenn die Installation von einem Standardbenutzer gestartet wird und der Setup Vorgang Administratorrechte erfordert (d. h., Sie werden zur Eingabe von Administrator Anmelde Informationen aufgefordert). Er erbt außerdem Administratorrechte, die ein potenzielles Sicherheitsrisiko darstellen. Stattdessen sollte ein Setup Bootstrap-Lade Programm das Spiel starten, nachdem es von einem erfolgreichen Aufruf des Installers zurückgegeben wurde. Weitere Informationen finden Sie im MSDN Magazine-Artikel untersuchen [Ihrer Apps für die Windows Vista-Benutzerkontensteuerung](/archive/msdn-magazine/2007/january/teach-your-apps-to-work-with-windows-vista-user-account-control).

</dd> </dl>

### <a name="33-install-to-correct-folders"></a>3,3 in richtigen Ordnern installieren

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Spiele, die für alle Benutzer installiert werden, müssen standardmäßig im Ordner "Programme" installiert werden. Benutzerdaten müssen geschrieben werden, wenn das Spiel zum ersten Mal ausgeführt wird, nicht während der Installation.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Benutzer sollten die Flexibilität haben, Anwendungen zu installieren, wo Sie Sie benötigen. Sie sollten auch eine konsistente und sichere Benutzerfunktion mit dem Standard Speicherort von Dateien haben.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Spiele können die verschiedenen bekannten Ordner Speicherorte (z. b. die von CSIDL \_ local \_ AppData und CSIDL \_ Common \_ appdata) verwenden, um große Mengen an Spieldaten zu speichern und ausführbare Dateien zu unterstützen, um erweiterte Installations-on-Demand-und patchszenarios zu implementieren.

Da die Installation während der Installation aller Benutzer zu einem anderen Benutzerkonto herauf Stufung erfordern kann, gibt es keinen korrekten Benutzer Speicherort, an dem die Daten zum Installations Zeitpunkt gespeichert werden. Auch wenn die Dateiverschlüsselung aktiviert ist, kann auf verschlüsselte Dateien nur über das Benutzerkonto zugegriffen werden, von dem Sie erstellt wurden.

</dd> </dl>

### <a name="34-install-windows-resources-properly"></a>3,4 Windows-Ressourcen ordnungsgemäß installieren

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Anwendungen dürfen nicht versuchen, Dateien oder Registrierungsschlüssel zu installieren, die durch Windows-Ressourcenschutz (WRP) geschützt sind. Wenn für die Anwendung neuere Versionen von Systemkomponenten erforderlich sind, müssen diese Komponenten mithilfe eines Microsoft Service Packs oder eines von Microsoft genehmigten Installationspakets, das die Systemkomponente enthält, aktualisiert werden. System Komponenten dürfen nie neu verpackt werden.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Windows-Ressourcenschutz (WRP) soll sicherstellen, dass geschützte Systemressourcen nur mit von Microsoft genehmigten Installations-oder Aktualisierungs Mechanismen aktualisiert werden. WRP verbessert die Systemzuverlässigkeit, indem sichergestellt wird, dass die Ergebnisse einer Installation vorhersagbar sind.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

WRP ist der Nachfolger von Windows-Datei Schutz, der die Mehrzahl der im Windows-Ordner installierten Systemkomponenten schützt. WRP schützt die meisten Registrierungsschlüssel, die Einstellungen für die Erstellung von COM-Objekten speichern. Außerdem werden bestimmte Ordner für die ausschließliche Verwendung durch das Betriebssystem reserviert. Versuche, auf geschützte Ressourcen zuzugreifen, führen in der Regel zu einem Zugriffs Verweigerungs Fehler.

Ausführliche Informationen zu bewährten Methoden bei der Bereitstellung der DirectX-Laufzeit mit einem Spiel finden Sie im DirectX-Artikel [DirectX-Installation für Spieleentwickler](/windows/desktop/DxTechArts/directx-setup-for-game-developers).

</dd> </dl>

### <a name="35-avoid-reboots-during-installation"></a>3,5 vermeiden Neustarts während der Installation

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Der Game Installer sollte nicht davon ausgehen, dass die Installation von Windows-Komponenten aus weitergabepaketen einen Neustart erfordert, es sei denn, der Neustart wird durch ein Rückgabe Ergebnis oder von der Microsoft-Dokumentation angegeben.

Wenn das Game Installer immer einen Neustart erzwingt, muss dies von Microsoft genehmigt werden.

In Windows Installer Paketen enthaltene Dialogfelder in Dateien müssen eine Option zum automatischen Schließen von Anwendungen enthalten und versuchen, Sie nach Abschluss des Setups neu zu starten.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Das Neustarten des Systems nach einer Installation ist eine unnotwendige Unterbrechung für Benutzer und ist in der Regel unnötig.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Weitere Informationen finden Sie unter [Verwenden von Windows Installer mit dem Neustart-Manager](/windows/desktop/Msi/using-windows-installer-with-restart-manager).

</dd> </dl>

### <a name="36-use-file-versioning-correctly"></a>3,6 verwenden Sie die Datei Versionsverwaltung ordnungsgemäß.

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Das Spiel Installationsprogramm muss ordnungsgemäß überprüft werden, um sicherzustellen, dass die aktuellsten Dateiversionen installiert sind. Bei der Installation eines Spiels dürfen keine Dateien erneut verwendet werden, die Sie nicht erstellt haben oder die von nicht erzeugten Anwendungen gemeinsam genutzt werden.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Freigegebene Komponenten und Systemkomponenten werden häufig für Sicherheitskorrekturen und erweiterte Funktionen aktualisiert. Eine Installation, die eine ältere Version aktualisierter Komponenten umfasst, sollte nicht zum Verlust von Updates und Korrekturen führen, die bereits angewendet wurden.

</dd> </dl>

### <a name="37-support-autorun-conditional-requirement"></a>3,7 Unterstützung für die bedingte Anforderung von Autorun \[\]

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Bei spielen, die auf CD, DVD oder anderen Wechselmedien verteilt sind, die Autorun unterstützen, muss die Anwendung beim ersten Einfügen der Festplatte automatisch ausgeführt werden oder den Benutzer zur Installation des Spiels auffordern, es sei denn, der Benutzer hat die Autorun-Funktion deaktiviert.

Nachdem die Anwendung erfolgreich installiert wurde, muss das erneute Einfügen der Festplatte auf dem Laufwerk nicht bewirken, dass die Installation automatisch startet. Es ist akzeptabel, Benutzer zu Fragen, ob Sie die Installationsoptionen aktualisieren oder ändern möchten.

Die Auto ausführen-Anwendung darf nicht zur Erhöhung der Rechte auffordern (d. h., Sie muss im Manifest über asInvoker verfügen, je nach Anforderung 2,1, obwohl das Setup Programm oder ein anderes Hilfsprogramm gestartet werden kann, das Administratorrechte erfordert). Die Rechte Erweiterung sollte nur auftreten, wenn das Spiel nicht installiert ist, oder wenn der Benutzer Sie ausdrücklich auswählt.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Autorun vereinfacht die Verwendung von Medien verteilten Anwendungen, wie z. b. spielen, bei denen normalerweise die Festplatte auf dem Laufwerk vorhanden sein muss, um das Spiel zu spielen.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Es ist nicht zulässig, dass der Benutzer im Datei-Explorer navigieren muss, um die Installation von der CD oder DVD zu starten.

Bei spielen, die auf mehrere Festplatten verteilt werden, sollten nachfolgende CDs im Idealfall entweder die Autorun-Funktion verwenden oder die Installation fortsetzen, ohne den Benutzer aufzufordern, eine Taste zu drücken oder andere Aktionen auszuführen.

Wenn Sie ein Autorun-Programm erstellen, stellen Sie sicher, dass alle erforderlichen Komponenten bei Neuinstallationen von Windows vorhanden sind. Typische Anwendungen basieren auf Technologien, die vom-Setup installiert werden, aber Autorun selbst wird ausgeführt, bevor eine solche Einrichtung erfolgt. Ein häufiges Beispiel ist der Ausfall von Autorun-Programmen, weil die Visual C-Lauf Zeit-DLLs nicht als Teil des Windows-Setups enthalten waren. Das Autorun-Programm muss daher die lokale CRT-Bereitstellung von Anwendungen verwenden oder die CRT statisch verknüpfen.

Autorun-Programme, die zur Verwendung in Windows-Versionen vor Windows Vista geschrieben wurden, sollten die .NET-Runtime nicht verwenden, da diese Technologie nicht in Windows XP oder älteren Windows-Versionen enthalten ist. Windows Server 2003 und Windows Vista sind die ersten Versionen von Windows, die .NET-Laufzeit als Teil Ihres Betriebssystems einschließen.

Aus ähnlichen Gründen können für autorun-Programme keine optionalen DirectX SDK-Komponenten wie z. b. D3DX9, d3dx10, Bibliothek d3dx11, XAudio2, X3DAudio, XACT, XInput und MDX 1,1 erforderlich sein.

Ein Beispiel für die Verwendung von Autorun finden Sie unter Autorun Sample.

</dd> </dl>

## <a name="reliability"></a>Zuverlässigkeit

**Zusammenfassung der Sicherheits-und Kompatibilitätsanforderungen**

**Kunden Vorteile**

Durch diese Anforderungen wird eine Anwendung zuverlässiger, da die Anzahl der Abstürze, Abstürze und Neustarts minimiert wird. Mithilfe der Zuverlässigkeitsanforderungen können Sie sicherstellen, dass Software vorhersagbar, wart Bar, robust und wiederherstellbar ist.

### <a name="41-eliminate-unnecessary-reboots"></a>4,1 Entfernen unnötiger Neustarts

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Alle Anwendungsinstallations Programme müssen die APIs für den Neustart-Manager nutzen, um Systemneustarts zu vermeiden (siehe Anforderung 3,5).

Spiele dürfen das Herunterfahren nicht blockieren.

Alle Anwendungen müssen auf den Neustart-Manager reagieren, indem Sie die folgenden Nachrichten zum Herunterfahren lauschen und darauf antworten:

<dl> <dt>

<span id="WM_QUERYENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_queryendsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_QUERYENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM \_ queryendsession mit lParam = EndSession \_ CloseApp (0x1) 
</dt> <dd>

GUI-Anwendungen müssen bei der Vorbereitung auf einen Neustart sofort Antworten (true).

</dd> <dt>

<span id="WM_ENDSESSION_with_LPARAM___ENDSESSION_CLOSEAPP__0x1___"></span><span id="wm_endsession_with_lparam___endsession_closeapp__0x1___"></span><span id="WM_ENDSESSION_WITH_LPARAM___ENDSESSION_CLOSEAPP__0X1___"></span>WM \_ EndSession with lParam = EndSession \_ CloseApp (0x1) 
</dt> <dd>

Anwendungen müssen einen 0-Wert innerhalb von 5 Sekunden zurückgeben und dann schließen.

</dd> <dt>

<span id="CTRL_C__"></span><span id="ctrl_c__"></span>STRG + C 
</dt> <dd>

Konsolen Anwendungen, die diese Nachricht empfangen, müssen sofort geschlossen werden.

</dd> </dl> </dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

System Neustarts sind eine wesentliche Unterbrechung. Sie führen zu einer ungültigen Benutzer Leistung und sollten minimiert werden. Einige Vorgänge, z. b. kritische Systemupdates, können Neustarts erfordern. Durch lauschen auf das Herunterfahren von Nachrichten können das Spiel und andere Anwendungen umgehend auf Anforderungen vom Neustart-Manager reagieren. Auf diese Weise können Sie unnötige Verzögerungen bei gültigen Neustart Anforderungen vermeiden.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Wenn ein Spiel Installationsprogramm die Windows Installer-Technologie (MSI) ohne benutzerdefinierte Aktionen verwendet, wird diese Funktion automatisch bereitgestellt. Außerdem wird der Neustart-Manager von Microsoft-Verteilungs Paketen unterstützt.

Weitere Informationen zum Neustart-Manager finden Sie im MSDN-Artikel zum [Neustart-Manager](/windows/desktop/RstMgr/about-restart-manager).

</dd> </dl>

### <a name="42-eliminate-application-verifier-failures"></a>4,2 Vermeiden von Application Verifier Fehlern

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Das Spiel muss in den folgenden Tests keine Fehler erzeugen, die unter Microsoft Application Verifier (AppVerifier), Version 4,0 oder höher, ausgeführt werden:

-   Grundlagen: Handles, Heaps, sperren, Arbeitsspeicher, TLS
-   Sonstige: dangerousapis, dirtystacks

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

AppVerifier testet auf viele bekannte Probleme, die Abstürze und Abstürze in Windows-Anwendungen verursachen, sowie auf bekannte Sicherheitsrisiken.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Weitere Informationen zu Application Verifier finden Sie unter [Application Verifier](/previous-versions/ms220948(v=vs.80)) und [Verwenden von Application Verifier in Ihrem Lebenszyklus der Software Entwicklung](/previous-versions/aa480483(v=msdn.10)) auf MSDN. Sie können Application Verifier von den [Download Details herunterladen: Application Verifier](https://www.microsoft.com/downloads/details.aspx?familyid=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18) im Microsoft Download Center.

Diese Anforderung gilt nicht für reine verwaltete Anwendungen ohne systemeigene Interop.

Diese Tests sollten auf einem Releasebuild ausgeführt werden. Beim Debuggen von Builds können falsch Fehler generiert werden. Einige Antipiraterie-und antispick Technologien können die Ausführung von AppVerifier beeinträchtigen. Daher sollten diese Tests ohne Antipiraterie und Anticheat-Technologien durchgeführt werden.

Möglicherweise ist es erforderlich, die vollständige Eigenschaft der Grundlagen: Heaps-Test auf false festzulegen, da die vollständige Arbeitsspeicher Auslastung der laufenden Anwendung durch die vollständige Zusammenfassung erheblich erhöht wird. Es werden weiterhin Fehler erkannt, aber es ist möglicherweise schwieriger, Sie zu finden, wenn Sie nur partielle paarweise verwenden.

Wenn Sie die UAC/Lua-bezogenen Tests in Application Verifier verwenden, um die Anforderungen der Benutzerkontensteuerung 2,1 und 3,2 zu erfüllen, sollten Sie die Ergebnisse mit der [Standard Benutzer Analyse](/windows/desktop/Win7AppQual/standard-user-analyzer--sua--tool-and-standard-user-analyzer-wizard--sua-wizard-) überprüfen. Es gibt auch zahlreiche weitere nützliche Tests, die von Application Verifier bereitgestellt werden, die Sie bei der Entwicklung und beim Testen dringend unterstützt haben, um ein hohes Maß an Kompatibilität mit aktuellen und zukünftigen Versionen von Windows sicherzustellen. Der **highversionlie** -Test wird verwendet, um die Konformität mit Anforderung 2,5 zu überprüfen.

Visual Studio Team System enthält eine Teilmenge der AppVerifier-Funktionalität, die in die Debuggingumgebung integriert ist. Dies kann sich als nützlich erweisen, um Probleme mit Grundlagen zu verfolgen und zu beheben: Heaps, Handles und Sperr Tests.

</dd> </dl>

### <a name="43-support-windows-error-reporting-and-file-version-information"></a>4,3 Support Windows-Fehlerberichterstattung und Datei Versionsinformationen

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Zum Aktivieren der Unterstützung von Windows-Fehlerberichterstattung müssen Spiele die folgenden Anforderungen erfüllen:

-   Spiele müssen nur bekannte Ausnahmen verarbeiten. Windows-Fehlerberichterstattung dürfen nicht deaktiviert werden. Wenn ein Fehler wie eine Zugriffsverletzung in einem Spiel auftritt, muss Windows-Fehlerberichterstattung den Absturz melden können.
-   Alle ausführbaren Dateien (z. b. exe-Dateien oder DLLs) müssen einen exakten Produktnamen, den Firmennamen und die Dateiversion enthalten.
-   Der normale Beenden des Spiels darf keinen unbekannten Ausnahme Fehler verursachen.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Die Windows-Fehlerberichterstattung-APIs bieten Microsoft wichtige Informationen zum Erkennen von weit verbreiteten abstürzen und hängen von Anwendungen. Dadurch können Microsoft und seine Partner System-und Treiber Probleme, die zu Anwendungsfehlern führen, schnell erkennen und beheben.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Spiele können benutzerdefinierte nicht behandelte Ausnahmehandler enthalten, um benutzerdefinierte Support-und Berichterstattungs Funktionen auszuführen, aber Sie müssen jeden beliebigen Fehler an die Funktionen **Report Fault** oder **werreportsubmit** übergeben.

Die richtigen Datei Versionsinformationen können überprüft werden, indem Sie die Dateieigenschaften in der Windows-Desktop Benutzeroberfläche anzeigen und die Eigenschaften Seite Version überprüfen.

Weitere Informationen zu den Windows-Fehlerberichterstattung-APIs und zur Analyse der Absturz Abbilder, die generiert werden, wenn Sie diesen Dienst verwenden, finden Sie im Artikel zur Absturz Abbild [Analyse](/windows/desktop/DxTechArts/crash-dump-analysis)von DirectX.

</dd> </dl>

## <a name="xbox-360-common-controller-for-windows-terminology"></a>Xbox 360 Common Controller für Windows-Terminologie



|                                          |                                                                                                  |
|------------------------------------------|--------------------------------------------------------------------------------------------------|
| A                                        | Schaltfläche "A"                                                                                     |
| B                                        | Die B-Schaltfläche                                                                                     |
| Zurück                                     | Schaltfläche "zurück"                                                                                  |
| (rechts/links) Stoßstange                      | Die Schaltfläche am oberen rechten und linken Rand des Controllers. Äquivalent zu einer Schulter Schaltfläche.    |
| direktionaler Pad                          | Controller direktionaler Pad                                                                   |
| D-Pad                                    | Akzeptierte Abkürzung des direktionalen Pads                                                         |
| Gbar                                       | Direktionale Pad-Abkürzung und Controller Bezeichnung                                                |
| RB, lb                                   | Rechter und Linker Abkürzungen und Controller Bezeichnungen                                        |
| RS, ls                                   | Rechts-und Left-Stick-Abkürzungen und Controller Bezeichnungen                                         |
| RT, lt                                   | Rechts-und linke Auslöse Abkürzungen und Controller Bezeichnungen                                       |
| RSB, LSB                                 | Rechts-und Left-Stick-Abkürzungen und Controller Bezeichnungen                                         |
| START                                    | Die Schaltfläche „Start“                                                                                 |
| (rechts/links) Stift                       | Der Controller Stift. Vorheriger Thumbstick.                                                       |
| (rechts/links) Schaltfläche "Stift"                | Die Schaltfläche für den Controller Stick. Schaltfläche für den früheren Fingerabdruck.                                         |
| (rechter/linker)-Auslösung                     | Der Controller--auslöst.                                                                          |
| Vibration                                | Das vom Controller-Motor erzeugte Spiel Feedback. Verwenden Sie keine Gerüchte.                           |
| X                                        | Schaltfläche "X"                                                                                     |
| J                                        | Die Y-Schaltfläche                                                                                     |
| Xbox 360-Controller für Windows          | Das Xbox 360-Gamepad, das als PC-Hardware-SKU verkauft wird, einschließlich einer Windows-Gerätetreiber-CD.          |
| Xbox 360-drahtlos Controller für Windows | Das Xbox 360 Wireless-Gamepad, das als PC-Hardware-SKU verkauft wird, einschließlich einer Windows-Gerätetreiber-CD. |



 

## <a name="guidelines-for-game-middleware-products"></a>Richtlinien für Spiele Middleware-Produkte

### <a name="introduction"></a>Einführung

Damit Spiele für das Programmieren für Windows qualifiziert werden können, müssen Sie eine Liste der technischen Anforderungen erfüllen. Alle Komponenten von Drittanbietern, die mit einem Titel ausgeliefert werden (ausführbare Dateien, DLLs, Treiber usw.) müssen auch diese Anforderungen erfüllen, damit das Spiel qualifiziert werden kann. In diesem Dokument werden die gängigsten Anforderungen hervorgehoben, die auch von den Komponenten von Drittanbietern erfüllt werden müssen, damit die Konformitätstests bestanden werden. Installer und vollständige Spiele-Engine/Produktions Pakete sollten das Dokument vollständige Spiele für technische Anforderungen von Windows lesen, da viele dieser Anforderungen von diesen Tools betroffen sind.

### <a name="additional-recommendations"></a>Zusätzliche Empfehlungen

Wenn Sie sicherstellen, dass Ihre Komponente die Erstellung von Titeln unterstützt, die mit den Anforderungen für Spiele für Windows kompatibel sind, müssen Sie beim Entwerfen und Bereitstellen einer Bibliothek oder eines Support Hilfsprogramms für ein Windows-Spiel einige andere Aspekte berücksichtigen.

-   Zur Unterstützung von Entwicklern, die an systemeigenen x64-Anwendungen mit 64-Bit arbeiten, stellen Sie sowohl die systemeigenen Versionen 32-Bit als auch 64-Bit bereit. Die 32-Bit-Version muss pro 2,2 mit 64 Bit kompatibel sein. Bibliotheken für 32-Bit-Anwendungen sollten nicht davon ausgehen, dass das hohe Bit einer 32-Bit-Adresse nicht verwendet wird, um die Verwendung innerhalb von LARGEADDRESSAWARE x86-Anwendungen zu unterstützen.
-   Wenn Sie Native Code Header (C/C++) bereitstellen, verwenden Sie die SAL-Attribut Syntax (Standard Annotation Language), um ihre öffentlichen API-Routinen zu ergänzen. Auf diese Weise können Benutzer Ihrer Bibliothek den maximalen Vorteil der Verwendung der statischen Code Analyse (/analyze) erzielen, die Teil von Visual Studio Team System 2005, Visual Studio Team System 2008, Visual Studio 2010 Premium und Visual Studio 2010 Ultimate ist, sowie die öffentlich verfügbaren Windows SDK Compilertools.
-   Wenn Ihr Produkt Threads innerhalb des Benutzer Prozesses erstellt, achten Sie darauf, dass Sie jeden Thread benennen, damit die Debuggingtools das Ausführen von Threads korrekt kommentieren können.
-   Wenn Sie Routinen schreiben, die in der Hauptschleife eines Spiels aufgerufen werden sollen, verwenden Sie die D3DX-Routinen D3DPERF \_ beginevent/endevent und D3DPERF \_ setmarker, um Vorgänge auf hoher Ebene für eine einfachere Identifizierung von Engpässen mithilfe von Pix für Windows zu kommentieren.
    > [!Note]  
    > Für die Visual Studio 2012-Grafik Diagnosefunktionen werden diese D3DX-und pix-Routinen durch die [**ID3DUserDefinedAnnotation**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3duserdefinedannotation) -Schnittstelle ersetzt.

     

-   Stellen Sie für Netzwerk Bibliotheken IP-neutrale Implementierungen bereit, und vermeiden Sie als veraltet markierte reine IPv4-Routinen zur Unterstützung der IPv6-und Teredo-Technologien in Windows XP mit Service Pack 2, Windows Vista und Windows 7.
-   Game Service-Anbieter sollten sich mit Version 2 des GDF-Schemas bei Games Explorer registrieren und die RSS-Funktion verwenden, um Dienst bezogene Nachrichten bereitzustellen.

### <a name="games-for-windows-showcases"></a>Spiele für Windows-Präsentationen

### <a name="introduction"></a>Einführung

Spiele für Windows-Präsentationen gehen über die Bereitstellung einer soliden Spiele Darstellung auf Windows-PCs hinaus. Durch die Implementierung dieser Features können Spiele die Benutzer Leistung auf den neuesten Windows-Plattformen steigern.

Spiele für Windows-Titel müssen alle technischen Anforderungen erfüllen, die in diesem Artikel aufgeführt sind, aber die Showcase-Features sind optional. Mit diesen Titeln können einige, keine oder alle dieser Präsentationen implementiert werden.

### <a name="s1-exploit-direct3d-11"></a>S. 1 Exploit Direct3D 11

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Direct3D 11 ist die Renderingebene API der nächsten Generation für Windows Vista und Windows 7. Spiele, die Direct3D 11 ausnutzen, verwenden optimierten Inhalt, erweiterte Renderingverfahren und neue Hardware Features, um eine überzeugende Hardware Funktion zu erstellen, die 10, 10,1 und 11 unterstützt.

Wenn das Spiel auch Direct3D 9 implementiert, sollte ein paralleler Vergleich eine spürbare Verbesserung der Inhaltsqualität, der visuellen Genauigkeit, der Leistung, der Komplexität der Szene und anderer Bereiche der Grafik Treue für Direct3D 11 veranschaulichen. Diese Unterstützung unterliegt den Spielen für die technische Windows-Anforderung 1,7.

Die Direct3D 10level9-Technologie kann verwendet werden, um Shadermodell 2.0/3.0 Direct3D 9-Klassen-Video Hardware unter Windows Vista und Windows 7 zu unterstützen, anstatt eine parallele Direct3D 9-Implementierung für eine umfassende Hardwareunterstützung zu verwenden. Dies reicht jedoch nicht aus, um diese Präsentation zu veranschaulichen.

Auf Computern, auf denen Windows Vista oder Windows 7 mit installiertem Direct3D 11 ausgeführt wird, sollte das Spiel standardmäßig Direct3D 11 verwenden.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Die Direct3D 11-API baut auf der Windows-Anzeigetreiber Modell (WDDM) und der Direct3D 10,1-Infrastruktur auf, um neue Funktionen zu unterstützen: Hardware Mosaik, COMPUTE-Shader, Multithread-Rendering und Ressourcen Erstellung, neue Textur Komprimierungs Formate und eine flexiblere Shader-Sprache. Direct3D 11 bietet Unified Hardware-Unterstützung für moderne Grafikkarten, einschließlich der neuesten Generation Direct3D 11 Teile, alle Direct3D 10-und 10,1-Videokarten und viele Shader Model 2.0/3.0 Direct3D 9-Grafikkarten, die die mindestens erforderliche Video Hardware für den Aero 3D-Desktop ist.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Das Migrieren einer Direct3D 9-Rendering-Engine zur Verwendung der neuen Direct3D 11-Schnittstelle ist eine klar definierte Aufgabe:

-   Entfernen Sie alle Vorgänge mit fester Funktionsweise zugunsten von programmierbaren Shadern.
-   Aktualisieren Sie alle vorhandenen Shader auf die neue Syntax von Shadermodell 4. x/5.
-   Aktualisieren der Ressourcenverwaltung, um das neue Ansichts Modell zu unterstützen.
-   Konvertieren Sie alle Assets, um eine neue Liste der verfügbaren Formate zu verwenden.
-   Aktualisieren Sie die Verarbeitung des renderzustands, um unveränderliche Zustands Blöcke zu verwenden, und rearbeiten Sie shaderkonstanten in konstantenpuffern.

Diese Konvertierung ist erforderlich, um das Showcase Direct3D 11 zu aktivieren, obwohl das Ergebnis nicht der Showcase-Anforderung zur Nutzung der neuen API entspricht.

Die neue API und das zugehörige HLSL-Programmiermodell bieten viele Möglichkeiten für erweiterte Inhalte:

-   Nutzen vorhandener Direct3D 10-Hardware Features, wie z. b. Geometry-Shader, Stream-Out, Textur Arrays und die komprimierten BC4/BC5-Textur Formate.
-   Nutzen vorhandener Direct3D 10,1-Hardware Features, wie z. b. unabhängige Blend-Modi pro Renderziel, Lesevorgänge für die MSAA-Tiefe, MSAA pro Beispiel-Shader-Zugriff, cubemaparrays und Rendering in Block komprimierte Formate (BC).
-   Implementieren von erweiterten GPU-Algorithmen mithilfe von Compute-Shader mit "CS4. x" auf vorhandenen Direct3D 10/10.1-Grafikkarten (durch aktualisierte Videotreiber aktiviert) oder CS 5,0 auf Direct3D 11-Grafikkarten der nächsten Generation.
-   Rendering in mehreren Threads mithilfe der frei Hand Thread-Ressourcen Erstellung und mehrerer Geräte Kontexte, um die Leistung auf mehr Kernsystemen (mit aktualisierten Video Treibern) zu verbessern. Weitere Informationen finden Sie in den Spielen für Windows-Showcase S. 3.
-   Nutzen neuer Features von Video Hardware der Direct3D 11-Klasse, z. b. Hardware-Mosaik mit Hull und Domänen-Shadern, Shader-Modell 5,0 HLSL-Shader-Hardware Features BC6HBC7 komprimierte Textur Formate und dynamische shaderverknüpfung.

Techniken, die mit Direct3D 9 implementiert werden können (größtenteils durch hohe CPU-Kosten), können auf effiziente Weise auf die GPU geladen werden, wodurch CPU-Ressourcen freigegeben werden, um andere Spiel Anforderungen zu unterstützen.

Direct3D 11 APIs, unterstützende Tools und Beispiele sind im DirectX SDK verfügbar. Siehe auch Grafik-APIs in Windows.

</dd> </dl>

### <a name="s2-exploit-x64-native"></a>S. 2 Exploit x64 Native

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Das Spiel enthält eine systemeigene 64-Bit-ausführbare Datei, die eine überzeugende, neue, von x64-Editionen von Windows auf x64-fähiger Hardware aktivierte Funktion bereitstellt. Ein paralleler Vergleich mit der 32-Bit-Version des Spiels sollte eine spürbare Verbesserung der Inhalts Komplexität, geringere Gesamt Ladezeiten und Leistung zeigen.

Bei 64-Bit-Editionen von Windows sollte bei der Installation immer die native 64-Bit-Version des Spiels als Standardeinstellung für Verknüpfungen in Games Explorer und Windows XP Professional x64 Edition eingerichtet werden. Wenn eine Dual-Installation gewünscht ist, kann eine zusätzliche Wiedergabe Aufgabe für den Spiele-Explorer unter Windows Vista und Windows 7 angegeben werden, die auf die 32-Bit-Version verweist. der Standardwert sollte jedoch die systemeigene 64-Bit-Version beibehalten werden.

Beachten Sie, dass das Spiel die 64-Bit-Editionen von Windows Vista und Windows 7 unterstützen sollte, um diese Showcase-Empfehlung zu erfüllen. Unterstützung für Windows XP Professional x64 Edition wird empfohlen, ist jedoch nicht erforderlich.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

die x64-Technologie bietet 64-Bit-Adressierungs Funktionen sowohl für den Consumerserver als auch für die Server Märkte, die eine voll Geschwindigkeit 32-Bit-Abwärtskompatibilität für vorhandene Anwendungen beinhalten. x64 ist ein wichtiger Bestandteil der Roadmap für AMD (amd64) und Intel (EMT64), und mit Ausnahme von ultramobilen CPUs unterstützen Sie die Technologie für alle aktuellen und zukünftigen Generations Prozessoren.

Windows XP Professional x64 Edition war das erste consumerorientierte Windows-Betriebssystem zur Unterstützung von x64-Technologie, und Windows Vista und Windows 7 erweitern die Verfügbarkeit der OS-Aktivierung für 64-Bit-Consumer Computing erheblich. Wenn auf vielen neuen Computern 2 GB RAM als Standard verwendet werden, profitieren weitere Verbesserungen bei der Speicher Skalierung nicht von einzelnen Anwendungen mit 32-Bit-Anwendungen, die mehr als 2 GB physischen RAM nicht adressieren können. Heutzutage gibt es Herausforderungen, die alle verfügbaren Inhalte an die Einschränkungen von 2 GB virtuellem Adressraum anpassen, insbesondere in Kombination mit den großen Videos, die in High-End-GPUs verfügbar sind, und die Umstellung auf die x64-Technologie steigert die unter stützbaren Detailstufen erheblich.

die x64-Kompatibilität für 32-Bit-Spiele ist ein Spiel für die technische Windows-Anforderung (2,2), aber die Vorteile der neuen Technologien erfordern eine native 64-Bit-Implementierung.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Der Hauptvorteil der 64-Bit-Adressierung ist die Möglichkeit, direkt auf mehr als 2 GB physischen und virtuellen Arbeitsspeicher zuzugreifen. Der große Adressraum des virtuellen Speichers ermöglicht eine umfassende Verwendung von Speicher Abbild-e/a-Vorgängen, ohne dass Probleme bei der Auslastung des VM-Adressraums bei der 32-Bit-Programmierung auftreten. Spiele können den neuen Bereich nutzen, um die Ladezeiten erheblich zu verbessern oder in einigen Fällen Pausen zum Laden von Inhalten auszuschließen.

Vorhandene 32-Bit-Anwendungen können von x64-Editionen profitieren, da Sie bei der Erstellung mit der Linkeroption große Adressen aktivieren (**/LARGEADDRESSAWARE**) die Möglichkeit haben, Adressen mit vollständigen 32-Bit-Daten zu verarbeiten. Bei 32-Bit-Versionen von Windows XP konnten solche Anwendungen von einem bestimmten Start Modus bis zu 3 GB RAM adressiert werden, und x64-Editionen bieten Zugriff auf bis zu 4 GB RAM für Anwendungen mit großen Adressen Unterstützung (Laa). Obwohl die Verwendung von Laa in einer 32-Bit-Anwendung diese Showcase-Anforderung nicht erfüllt, ist diese Brückentechnologie eine äußerst nützliche Methode, um zusätzliche Skalierungs Vorteile für x64-Versionen von Windows bereitzustellen, um diese Showcase-Anforderungen nicht vollständig zu implementieren.

Weitere Informationen finden Sie unter [64-Bit-Programmierung für Spieleentwickler](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers) und [RAM, VRAM und mehr RAM: 64-Bit Gaming ist hier](https://www.gamasutra.com/view/feature/3602/sponsored_feature_ram_vram_and_.php) in Gamasutra.

> [!Note]  
> Eine wesentliche Herausforderung für dieses Showcase besteht darin sicherzustellen, dass alle Bibliotheken oder Komponenten von Drittanbietern, auf denen Ihr Spiel basiert, für die native 64-Bit-Entwicklung verfügbar sind. Viele ältere Microsoft-APIs wurden auch aus der systemeigenen 64-Bit-Umgebung entfernt, was eine Herausforderung für Engine-Codebasen mit älteren Implementierungen von Schlüssel Systemen darstellen kann.

 

</dd> </dl>

### <a name="s3-exploit-many-core-processors"></a>S. 3 Exploit Many-Core-Prozessoren

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Das Spiel implementiert Features, die mehr Kern Prozessoren nutzen und auf 3, 4 oder mehr Kerne skalieren, falls verfügbar.

Wenn das Spiel Einzel Prozessor-oder Dual-Core-Systeme unterstützt, sollte ein paralleler Vergleich mit einem Quad-Core-System wahrnehmbare neue Features, zusätzliche überzeugende Effekte, Verbesserung der Inhaltsqualität und/oder eine verbesserte Leistung veranschaulichen.

Da die Dual-Core-Skalierung bereits häufig von spielen unterstützt wird und automatisch von verschiedenen Erweiterungen des Direct3D-Treibers genutzt wird, reicht die Dual-Core-Skalierung nicht aus, um diese Präsentation zu veranschaulichen.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Das Verbesserungen bei der Leistung für CPUs hat sich von den Verbesserungen der Taktrate zum Hinzufügen von Rechen Kernen geändert. Sowohl AMD-als auch Intel-Roadmaps basieren auf skalierbaren, mehr Kern Designs. Alle Spielplattformen der nächsten Generation haben aufgrund dieser grundlegenden Verschiebung bei der Weiterentwicklung von Prozessoren mehr Kern CPUs. Anwendungen mit nur einem Thread werden keine signifikanten Vorteile der CPUs der nächsten Generation mehr erkennen. Einfaches Multithreading kann auch nicht skaliert werden, wenn die Anzahl der verwendeten CPU-Kerne auf drei oder mehr erhöht wird.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Beachten Sie, dass die Kern Anzahlen keine Potenz von zwei sein müssen. Daher sollten Spiele linear skaliert werden und die Kern Anzahl von 3, 4, 5, 6, 7, 8 usw. verarbeiten.

Das Skalieren durch Erhöhen der Anzahl von Threads in einer Anwendung stellt nur dann eine Rückgabe dar, wenn die Kosten für die Kommunikation und die Thread Synchronisierung überprüft werden. Die featurebasierte Skalierung kann kurzfristig eine einfachere Lösung darstellen, sodass das Spiel ohne die zusätzlichen Threads auf Einzel Kernsystemen normal betrieben werden kann, und wenn die zusätzliche CPU-Leistung verfügbar ist.

Weitere Informationen finden Sie unter [Codieren mehrerer Kerne auf Xbox 360 und Microsoft Windows](/windows/desktop/DxTechArts/coding-for-multiple-cores) und [Überlegungen zur lockless-Programmierung für Xbox 360 und Microsoft Windows](/windows/desktop/DxTechArts/lockless-programming) in den DirectX-Artikeln sowie unter dem Hilfsprogramm dxutlockfrepipe und dem coreerkennungs-Beispiel.

Die Verwendung der Direct3D 11-Ressourcen Erstellung und von Geräte Kontexten in der kostenlosen Thread Umgebung ist hilfreich, um die Skalierbarkeit von vielen Kernen beim Rendern und Laden von Grafik Ressourcen zu erreichen. Siehe Games for Windows Showcase S. 1.

Beachten Sie, dass bei der direkten Verwendung der CPU-Anweisung RDTSC anstelle der Verwendung von Windows-APIs zur Berechnung der zeitliche Steuerung auf mehr Kernsystemen bei manchen Hardware-und Betriebs Systemkonfigurationen zu Problemen führen kann. Weitere Informationen finden Sie unter [Game Timing und Multicore-Prozessoren](/windows/desktop/DxTechArts/game-timing-and-multicore-processors) in den DirectX-Artikeln.

</dd> </dl>

### <a name="s4-support-games-for-windows---live"></a>S. 4 Unterstützung von Spielen für Windows Live

Spiele für Windows: Live wird von Microsoft nicht mehr unterstützt.

### <a name="s5-support-windows-touch"></a>S. 5 Unterstützung von Windows-Fingereingabe

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Windows touchfähige Spiele können mithilfe von toucheingaben und/oder Gesten auf Computern, auf denen Windows 7 ausgeführt wird, mit einer touchanzeige abgespielt werden. Tastatureingaben können auch verwendet werden, aber die primäre Wiedergabe Schnittstelle muss Berührungs basiert sein.

Die Aktivierung der Fingereingabe sollte die Verwendung der Maus oder des allgemeinen Controllers nicht verhindern, da die technische Anforderung 1,4 erforderlich ist.

Es wird davon ausgegangen, dass das Installationsprogramm des Spiels keine Windows-Berührungs Funktionen unterstützt.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Multitouch-fähige anzeigen für Computer sind für Laptops und Desktops verfügbar und stellen ein wichtiges Hardware Feature dar, das mit der Veröffentlichung von Windows 7 höher gestuft wird. Windows 7 unterstützt Windows-Finger Eingaben in den Desktop-und allgemeinen Steuerungs Schnittstellen.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Anwendungen mit System eigenem Code können mithilfe der WM Touch- \_ Nachrichten in Verbindung mit der [**RegisterTouchWindow**](/windows/desktop/api/winuser/nf-winuser-registertouchwindow) -Funktion auf Multitouch zugreifen. Siehe auch die Manipulationen und Trägheits-API.

Windows Presentation Foundation (WPF) 4,0 stellt eine verwaltete Lösung für Multitouch-Schnittstellen bereit.

Weitere Informationen finden Sie unter Windows-Fingereingabe-SDK.

</dd> </dl>

### <a name="s6-support-high-color"></a>S. 6 Unterstützung für hohe Farbe

<dl> <dt>

<span id="Requirement"></span><span id="requirement"></span><span id="REQUIREMENT"></span>**Ung**
</dt> <dd>

Bei spielen, die eine hohe Farbe unterstützen, wird ein 10:10:10:2-Format (DXGI \_ \_ -Format R10G10B10A2, D3DFMT \_ A2B10G10R10) oder ein 16:16:16:16-Format (DXGI \_ \_ -Format R16G16B16A16, D3DFMT \_ A16B16G16R16) für den renderingbackpuffer und den voll Bild Anzeigemodus verwendet.

Mithilfe eines High Color-Renderziels kann der Inhalt des High-Dynamic Bereichs (HDR) mit einem erweiterten oder großen Bereich gerendert werden, wenn eine Ton Zuordnung zu einem 10-Bit-oder 16-Bit-Bereich durchgeführt wird.

</dd> <dt>

<span id="Rationale"></span><span id="rationale"></span><span id="RATIONALE"></span>**Gedanke**
</dt> <dd>

Monitore konnten viele Jahre lang mehr als 256 Farbebenen pro Kanal anzeigen, auch wenn die CRT-Anzeige weit verbreitet war. Die Überprüfung der Hardware auf Grafikkarten war der einschränkende Faktor. Moderne GPUs, einschließlich der meisten Direct3D 9-Klassen Hardware und alle Direct3D 10-Klassen und bessere Hardware, verfügen über eine ausgescanungs Hardware, die mindestens 10 Bits pro Kanal unterstützt, und die Hardware Funktion ist so festgelegt, dass Sie in Zukunft auf 16 Bits pro Farbkanal zuwächst. Die HD-TV-Interconnect-Systeme (HDMI, Display Port) wurden so konzipiert, dass Sie mehr als 8 Bits pro Kanal verarbeiten können, und eine analoge VGA-Verbindung führt diese Signale bereits durch.

</dd> <dt>

<span id="Additional_Information"></span><span id="additional_information"></span><span id="ADDITIONAL_INFORMATION"></span>**Weitere Informationen**
</dt> <dd>

Beachten Sie, dass High Color oder Hi Color in der Vergangenheit auf den Wechsel von 256 (8-Bit)-Farbanzeige zu 15-oder 16-Bit-Farbanzeige verweist. Die meisten Anzeigesysteme haben lange Zeit auf die Farbe "true" (24-Bit-Farbe) oder 8 Bits pro Farbkanal für Rot, grün und blau verschoben. In hoher Farbe bedeutet dies, dass eine neue Generation von Systemen anzeigt, die mit mehr als 8 Bits pro Farbkanal betrieben werden können. Wird auch als tiefe Farbe bezeichnet.

</dd> </dl>

### <a name="recommended-best-practices"></a>Empfohlene Vorgehensweisen

### <a name="introduction"></a>Einführung

Zusätzlich zu den technischen Anforderungen und der Übernahme eines oder mehrerer Präsentationen in Ihrem Titel gibt es eine Reihe bewährter Methoden, die für alle Windows-Spiele befolgt werden sollten. Diese Empfehlungen liegen zwar außerhalb des Umfangs der technischen Grundanforderungen, Sie werden jedoch dringend empfohlen, Sie für alle Spiele für Windows-Titel einzusetzen.

### <a name="additional-recommendations"></a>Zusätzliche Empfehlungen

-   Verwenden Sie den neuesten Visual Studio-Compiler und die Common Language Runtime. Neuere Versionen des Compilers implementieren bedeutende Verbesserungen für die Qualität des generierten Codes und für Sicherheitsprobleme und nutzen moderne Strategien für die Prozessor Optimierung. Das Aktualisieren des Compilers und die Verwendung der neuesten C-Laufzeit ist eine einfache Möglichkeit, zu modernen Codierungs Methoden zu migrieren.
-   Verwenden Sie die dll-Version (Dynamic-Link Library) der C-Laufzeit anstelle von statischem verknüpfen, und verwenden Sie Secure CRT. (Ausnahmen können in speziellen Vorinstallations Fällen (z. b. für ein Autorun-Programm oder das Installationsprogramm selbst) vorgenommen werden.
-   Verwenden Sie für Game Audio XAudio2, X3DAudio und/oder XACT anstelle von DirectSound. Für audioengines, die alle Mischungs-und Quell Raten Umwandlungen ausführen und nur eine Lösung mit geringer Latenz für die Audioausgabe benötigen, verwenden Sie DirectSound unter Windows XP (nur) und WASAPI unter Windows Vista und Windows 7.
-   Vermeiden Sie die Verwendung von Legacy-und veralteten APIs: DirectDraw, DirectSound, DirectPlay, die Leistungs Ebene von DirectMusic, die DirectPlay-Sprache und der Direct3D beibehaltene Modus. Beachten Sie, dass der Modus "DirectPlay Voice" und "Direct3D beibehaltene Modus" in Windows Vista oder Windows 7 nicht verfügbar ist. DirectPlay und die Leistungs Ebene von DirectMusic sind für x64-native Anwendungen nicht verfügbar.
-   Optimieren Sie mithilfe von SSE/SSE2 SIMD-Anweisungs Sätzen. Weitere Informationen finden Sie in der [directxmath](/windows/desktop/dxmath/directxmath-portal) -API in der Windows SDK als plattformübergreifende Lösung für SIMD-optimierte mathematische Vorgänge.
-   Verwenden Sie moderne bewährte Methoden für die Windows-Sicherheit (einschließlich Compileroptionen und Linkeroptionen wie **/NXCOMPAT**, **/GS**, **/SAFESEH**, **/DynamicBase**, **/SDL** usw.). Weitere Informationen finden Sie unter [Bewährte Sicherheitsmethoden bei der Spieleentwicklung](/windows/desktop/DxTechArts/best-security-practices-in-game-development).
-   Verwenden Sie die neuesten Windows SDK Komponenten und Bibliotheken. Entfernen Sie Abhängigkeiten von der Vorgängerversion von DirectSetup, die Out-of-Band-Komponenten wie D3DX9, d3dx10 und Bibliothek d3dx11 bereitgestellt werden. Verwenden Sie ggf. [directxtex](https://github.com/Microsoft/DirectXTex) oder [directxtk](https://github.com/Microsoft/DirectXTK) oder beides.
-   Vermeiden Sie die Verwendung des älteren HLSL-Compilers, und verwenden Sie stattdessen den modernen HLSL-Compiler. Wenn für Ihre Anwendung die Unterstützung für Pixel Shader 1. x erforderlich ist, verwenden Sie die Shader-Assembly anstelle von HLSL, oder beschränken Sie die Verwendung des älteren Compilers auf diese Szenarien.

## <a name="resources"></a>Ressourcen



| Begriff                                                                                                                                                                                                                         | BESCHREIBUNG                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Games_for_Windows__Test_Cases__"></span><span id="games_for_windows__test_cases__"></span><span id="GAMES_FOR_WINDOWS__TEST_CASES__"></span>Spiele für Windows: Testfälle <br/>                              | Bewährte Methoden für Spiele unter Windows XP, Windows Vista und Windows 7<br/>                                                                               |
| <span id="Windows_SDK__"></span><span id="windows_sdk__"></span><span id="WINDOWS_SDK__"></span>Windows SDK <br/>                                                                                                      | [Windows sdche](https://msdn.microsoft.com/bb980924.aspx)<br/>                                                                                      |
| <span id="User_Account_Control_Guidelines__"></span><span id="user_account_control_guidelines__"></span><span id="USER_ACCOUNT_CONTROL_GUIDELINES__"></span>Richtlinien für die Benutzerkontensteuerung <br/>                      | [Windows Vista-Anwendungs Entwicklungsanforderungen für die Kompatibilität mit der Benutzerkontensteuerung](/previous-versions/dotnet/articles/bb530410(v=msdn.10))<br/> |
| <span id="WinQual_Developer_Portal__"></span><span id="winqual_developer_portal__"></span><span id="WINQUAL_DEVELOPER_PORTAL__"></span>Winqual-Entwickler Portal <br/>                                                  | [Windows Quality Online Services (Winqual)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)<br/>                                                                         |
| <span id="DirectX_Developer_Portal__"></span><span id="directx_developer_portal__"></span><span id="DIRECTX_DEVELOPER_PORTAL__"></span>DirectX-Entwickler Portal <br/>                                                  | [DirectX-Entwickler Center](/previous-versions/windows/apps/hh452744(v=win.10))<br/>                                                                               |
| <span id="Games_for_Windows_and_DirectX_SDK_Blog"></span><span id="games_for_windows_and_directx_sdk_blog"></span><span id="GAMES_FOR_WINDOWS_AND_DIRECTX_SDK_BLOG"></span>Blog zu spielen für Windows und DirectX SDK<br/> | [Spiele für Windows und das DirectX SDK](https://walbourn.github.io/)<br/>                                                                           |
| <span id="Additional_DirectX_Articles"></span><span id="additional_directx_articles"></span><span id="ADDITIONAL_DIRECTX_ARTICLES"></span>Weitere DirectX-Artikel<br/>                                             | [Technische Artikel zu DirectX](/windows/desktop/DxTechArts/dx9-technical-articles)<br/>                                                                                    |



 

 

