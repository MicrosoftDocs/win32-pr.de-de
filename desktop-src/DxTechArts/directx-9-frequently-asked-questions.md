---
title: Häufig gestellte Fragen zu DirectX
description: Dieser Artikel enthält eine Sammlung häufig gestellter Fragen (FAQ) zu Microsoft DirectX.
ms.assetid: 58d9fe45-a2c7-8280-2826-e2e14ecea983
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cd5fd70f1a651121b8d977dbb9479cef6edd024
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039271"
---
# <a name="directx-frequently-asked-questions"></a>Häufig gestellte Fragen zu DirectX

Dieser Artikel enthält eine Sammlung häufig gestellter Fragen (FAQ) zu Microsoft DirectX.

-   [Allgemeine DirectX-Entwicklungsprobleme](#general-directx-development-issues)
-   [Direct3D Fragen](#direct3d-questions)
    -   [Allgemeine Direct3D Fragen](#general-direct3d-questions)
    -   [Geometrie Verarbeitung (Scheitelpunkt)](#geometry-vertex-processing)
    -   [Leistungsoptimierung](#performance-tuning)
    -   [D3DX-Hilfsprogrammbibliothek](#d3dx-utility-library)
-   [Fragen zu DirectSound](#directsound-questions)
-   [DirectX-Erweiterungen für Alias Maya](#directx-extensions-for-alias-maya)
-   [Fragen zu xinput](#xinput-questions)

## <a name="general-directx-development-issues"></a>Allgemeine DirectX-Entwicklungsprobleme

<dl> <dt>

<span id="Should_game_developers_really_care_about_supporting_x64_editions_"></span><span id="should_game_developers_really_care_about_supporting_x64_editions_"></span><span id="SHOULD_GAME_DEVELOPERS_REALLY_CARE_ABOUT_SUPPORTING_X64_EDITIONS_"></span>**Sollten Spieleentwickler die Unterstützung von x64-Editionen wirklich interessieren?**
</dt> <dd>

Natürlich. x64-Technologie ist auf dem Markt allgemein verfügbar. Die Mehrzahl der neuen CPUs, die in den letzten Jahren verkauft wurden, und fast alle Prozessor Linien bei der Entwicklung von AMD und Intel sind x64-fähig. In Windows XP Professional x64 Edition wurde die Betriebssystem-Aktivierungs Technologie für x64 eingeführt, die im April von 2005 veröffentlicht wurde. Da x64-Editionen eine neue Generation von systemeigenen 64-Bit-Treibern erfordern, war dieses erste Release auf die OEM-Verteilung beschränkt.

Mit Windows Vista können Kunden beim Erwerb von Windows-basierten Computern entweder 32-Bit-oder 64-Bit-Editionen auswählen, und Lizenzen für Windows Vista sind sowohl für die 32-Bit-als auch für die 64-Bit-Edition des Betriebssystems gültig. Außerdem sind viele 64-Bit-Treiber in der Box verfügbar, und Gerätehersteller müssen im Rahmen des Windows-Zertifizierungsprogramms sowohl native 32-Bit-als auch 64-Bit-Treiber bereitstellen.

Alle diese Faktoren erhöhen die bereit Stellungen der 64-Bit-Editionen von Windows erheblich. Wenn neue Computer mit mehr als 2 GB physischem RAM ausgeliefert werden, verringert sich der Anreiz, ein 32-Bit-Betriebssystem zu verwenden, zugunsten der 64-Bit-Editionen erheblich. Die 64-Bit-Technologie 32 unterstützt vollständigen 32-Bit-Code vollständig, obwohl systemeigene 64-Bit-Implementierungen erforderlich sind, um den neuen 64-Bit-Speicherplatz in vollem Umfang zu nutzen. Jede 32-Bit-Anwendung sollte eine 64-Bit-Kompatibilität als Mindestanzahl von Lieferanforderungen aufweisen, und die Erfüllung dieser Anforderung ist eine Grundvoraussetzung für die Kompatibilität mit Windows Vista. Inkompatibilitäten treten in der Regel durch die Verwendung von 16-Bit-Code auf, der für das Betriebssystem Windows 3,1 entworfen wurde, oder das Installieren von Treibern, die nicht in systemeigenen 32-Bit-und 64-Bit-Formularen

Weitere Informationen zur 64-Bit-Technologie finden Sie unter [64-Bit-Programmierung für Spieleentwickler](/windows/desktop/DxTechArts/sixty-four-bit-programming-for-game-developers).

</dd> <dt>

<span id="Should_game_developers_still_be_publishing_games_for_Windows_95__Windows_98_or_Windows_ME_"></span><span id="should_game_developers_still_be_publishing_games_for_windows_95__windows_98_or_windows_me_"></span><span id="SHOULD_GAME_DEVELOPERS_STILL_BE_PUBLISHING_GAMES_FOR_WINDOWS_95__WINDOWS_98_OR_WINDOWS_ME_"></span>**Sollten Spieleentwickler weiterhin Spiele für Windows 95, Windows 98 oder Windows Me veröffentlichen?**
</dt> <dd>

Nicht mehr aus zwei Gründen: Leistung und Featuresatz.

Wenn die minimale CPU-Geschwindigkeit, die für Ihr Spiel erforderlich ist, 1,2 GHz oder höher beträgt (was bei High Performance-Titeln häufiger vorkommt), wird die Mehrheit der berechtigten Computer unter Windows XP ausgeführt. Wenn Computer mit einer CPU-Geschwindigkeit von über 1,2 GHz verkauft wurden, wurde Windows XP von fast allen Herstellern als Standardbetriebssystem installiert. Dies bedeutet, dass in Windows XP viele Features gefunden werden, die die Spieleentwickler von heute wie folgt nutzen:

-   Verbessertes Multitasking: Dies führt zu einer besseren, reibungsloseren Darstellung von Videos, Audiodateien und spielen.
-   Stabileres Videotreiber Modell, das ein einfacheres Debuggen, ein glatteres Spiel spielen und eine bessere Leistung ermöglicht.
-   Einfachere Konfiguration für das Netzwerk: Dies ermöglicht den einfacheren Zugriff auf Spiele mit mehreren spielen.
-   Unterstützung für DMA-Übertragungen standardmäßig von Festplatten. Dies führt zu einem reibungsloseren, schnelleren Laden von Anwendungen.
-   Windows-Fehlerberichterstattung: Dies führt zu einem stabileren Betriebssystem, Treibern und Anwendungen.
-   Unicode-Unterstützung, wodurch Lokalisierungs Probleme erheblich vereinfacht werden.
-   Bessere Sicherheit und Stabilität: Dies führt zu einer besseren Verbrauchererfahrung.
-   Bessere Unterstützung für moderne Hardware, von der die meisten keine Windows 98-Treiber mehr verwenden.
-   Verbesserte Speicherverwaltung: Dies führt zu einer besseren Stabilität und Sicherheit.
-   Verbessertes NTFS-Dateisystem, das besser gegen Ausfälle resistent ist und eine bessere Leistung mit Sicherheitsfeatures bietet.

</dd> <dt>

<span id="Should_game_developers_still_be_publishing_games_for_Windows_2000_"></span><span id="should_game_developers_still_be_publishing_games_for_windows_2000_"></span><span id="SHOULD_GAME_DEVELOPERS_STILL_BE_PUBLISHING_GAMES_FOR_WINDOWS_2000_"></span>**Sollten Spieleentwickler weiterhin Spiele für Windows 2000 veröffentlichen?**
</dt> <dd>

Nicht mehr. Zusätzlich zu den unter den genannten Gründen, in denen **Spieleentwickler weiterhin Spiele für Windows 95, Windows 98 oder Windows Me veröffentlichen**, bietet Windows 2000 nicht die folgenden Features:

-   Windows XP unterstützt erweiterte Prozessor Features, wie z. b. Hyper-Threading, Multi-Core und x64.
-   Windows XP unterstützt parallele Komponenten, durch die Konflikte bei der Anwendungs Versionsverwaltung erheblich reduziert werden.
-   Windows XP unterstützt den No-Execute-Speicherschutz, der das verhindern bösartiger Programme und das Debuggen erleichtert.
-   Windows XP bietet verbesserte Unterstützung für erweiterte AGP-und PCI Express-basierte Grafikkarten.
-   Windows XP unterstützt die schnelle Benutzerumschaltung, Remote Desktop und Remote Unterstützung, wodurch die Produktsupport Kosten gesenkt werden können.
-   Leistungs Tools wie Pix (im DirectX Developer SDK) unterstützen Windows 2000 nicht mehr.

Kurz gesagt, wurde Windows 2000 nie als consumerbetriebssystem entworfen oder vermarktet.

</dd> <dt>

<span id="What_are_the_differences_between_the_various_editions_of_Windows_Vista__How_do_they_impact_my_DirectX_application_"></span><span id="what_are_the_differences_between_the_various_editions_of_windows_vista__how_do_they_impact_my_directx_application_"></span><span id="WHAT_ARE_THE_DIFFERENCES_BETWEEN_THE_VARIOUS_EDITIONS_OF_WINDOWS_VISTA__HOW_DO_THEY_IMPACT_MY_DIRECTX_APPLICATION_"></span>**Worin bestehen die Unterschiede zwischen den verschiedenen Editionen von Windows Vista? Wie wirken sich diese auf meine DirectX-Anwendung aus?**
</dt> <dd>

Die Windows Vista-Familie umfasst fünf Editionen:

-   Windows Vista Home Basic
-   Windows Vista Home Premium
-   Windows Vista Business
-   Windows Vista Enterprise
-   Windows Vista Ultimate

Home Basic und Home Premium sind kundenorientierte Versionen mit Features wie Familien Sicherheit (früher als Jugendschutz bezeichnet) und Home Premium umfasst Media Center. Business und Enterprise sind Editionen mit Unternehmens Niveau und Features wie Domänen Beitritt und Remotedesktop/Terminal Dienste. Die Ultimate Edition kombiniert alle Features der Consumer-und Corporate-Editionen in einer Version. Alle Editionen sind sowohl in der 32-Bit-Version (x86) als auch in der 64-Bit-Edition (x64) enthalten, und Benutzer können die gleiche Produkt Kennung für beide Plattformen verwenden.

Die Technologie, die den verschiedenen Editionen zugrunde liegt, ist identisch, und Sie verfügen alle über dieselbe Version der DirectX-Laufzeit und anderer Komponenten. Die Editionen haben jedoch geringfügige Unterschiede in Bezug auf Spiele:

-   Games Explorer ist in allen Editionen vorhanden, aber die Spiele Verknüpfung im Startmenü ist nur in den Home Basic, Home Premium und Ultimate enthalten. Games Explorer kann weiterhin in allen Editionen gefunden werden (indem Sie auf Start klicken, auf alle Programme zeigen und dann auf Games klicken) und die igameexplorer-Schnittstelle für alle Editionen funktioniert.
-   Die in Windows enthaltenen Spiele sind für Unternehmen und Unternehmen standardmäßig nicht verfügbar, können jedoch vom Administrator aktiviert werden.
-   Die Familien Sicherheit und die Spiel Bewertung zeigen weder das Verhalten von Unternehmen noch Unternehmen an oder haben keinerlei Auswirkung auf das Verhalten von Unternehmen oder Unternehmen, und Sie sind beim Beenden einer Domäne auf Ultimate deaktiviert.

Die Einstellungen der Benutzerkontensteuerung sind für alle Editionen identisch, Sie können jedoch durch Gruppenrichtlinie Einstellungen für die Domäne in den Bereichen Business, Enterprise und Ultimate überschrieben werden. Beispielsweise kann die Richtlinien Einstellung Benutzerkontensteuerung: Verhalten der Eingabeaufforderung für erhöhte Rechte für Standardbenutzer so festgelegt werden, dass Anforderungen für erhöhte Rechte in vielen Geschäfts Einstellungen automatisch verweigert werden, um die Sicherheit zu erhöhen. viele Benutzer in diesen Umgebungen werden immer als Standardbenutzer ausgeführt, ohne dass Sie selbst als Administrator ausgeführt werden können. Jedes Programm (z. b. ein Installationsprogramm), das Administratorrechte erfordert, entweder aufgrund der Legacy-Setup-Erkennung oder durch ein Manifest, das die angeforderte Ausführungs Ebene als "requisionministrator" angibt, wird in solchen Situationen immer nicht gestartet. Andere Richtlinien Einstellungen, wie z. b. die Benutzerkontensteuerung: nur ausführbare Dateien herauf Stufen, die signiert und validiert sind, können die Funktionsfähigkeit des Installers auch verhindern, wenn Sie die ausführbare Datei nicht mit Authenticode signieren.

Diese Arten von Richtlinien Änderungen können auf eine beliebige Edition von Windows Vista angewendet werden, Sie sind jedoch eher auf Computern, die einer Domäne hinzugefügt werden.

</dd> <dt>

<span id="What_are_the_differences_between_the_various_editions_of_Windows_7__How_do_they_impact_my_DirectX_application__"></span><span id="what_are_the_differences_between_the_various_editions_of_windows_7__how_do_they_impact_my_directx_application__"></span><span id="WHAT_ARE_THE_DIFFERENCES_BETWEEN_THE_VARIOUS_EDITIONS_OF_WINDOWS_7__HOW_DO_THEY_IMPACT_MY_DIRECTX_APPLICATION__"></span>**Worin bestehen die Unterschiede zwischen den verschiedenen Editionen von Windows 7? Wie wirken sich diese auf meine DirectX-Anwendung aus?** 
</dt> <dd>

Die meisten Windows 7-Benutzer verfügen wahrscheinlich über eine von zwei Editionen: Windows 7 Home Premium, für Privat Benutzer oder Windows 7 Professional, für Geschäfts Benutzer und Entwickler. Für große Unternehmen gibt es eine Volumen lizenzierte Windows 7 Enterprise Edition, die alle Windows 7-Features umfasst. Windows 7 Ultimate ist die Retail-Entsprechung dieser Edition.

Die Starter Edition von Windows 7 ist weltweit für OEMs verfügbar und wird voraussichtlich mit Netbooks, ultralow-Power Notebook-Computern bereitgestellt. Windows 7 Home Basic ist nur in aufstrebenden Märkten verfügbar.

Beachten Sie, dass alle Editionen von Windows 7 (außer Starter Edition) für die Versionen 32-Bit (x86) und 64-Bit (x64) verfügbar sind und alle Einzelhandels Pakete von Windows 7 Medien für beide Versionen enthalten. Wie bei Windows Vista können Benutzer auch auf beiden Plattformen dieselbe Einzelhandelsprodukt Kennung verwenden.

Die zugrunde liegende Technologie in den verschiedenen Editionen ist identisch, und alle Editionen haben dieselbe Version der DirectX-Laufzeit und anderer Komponenten. Sie haben einige Unterschiede in Bezug auf die Spiele Features:

-   Games Explorer ist in allen Editionen vorhanden, aber die Spiele Verknüpfung im Startmenü ist in Windows 7 Professional und Enterprise standardmäßig ausgeblendet. Spiele-Explorer finden Sie weiterhin im Startmenü (durch Klicken auf "alle Programme" und dann auf "Spiele"), und die Verknüpfung "direkte Spiele" kann vom Benutzer aktiviert werden.
-   Die in Windows enthaltenen Spiele sind unter Windows 7 Professional und Enterprise standardmäßig nicht verfügbar, können jedoch vom Administrator aktiviert werden.
-   Familien Sicherheit und Spiel Bewertungen sind in allen Editionen verfügbar. Sie sind jedoch unter Windows 7 Professional, Enterprise und Ultimate deaktiviert, wenn das Betriebssystem einer Domäne Beitritt. Wie bei Windows Vista Ultimate kann dieses Feature auf Computern, die einer Domäne beigetreten sind, erneut aktiviert werden.

Die Einstellungen der Benutzerkontensteuerung (User Account Control, UAC) können von Gruppenrichtlinie Einstellungen auf Windows 7 Professional-, Enterprise-und Ultimate-Editionen, ähnlich wie Windows Vista, beeinträchtigt werden. Weitere Informationen finden Sie **unter Worin bestehen die Unterschiede zwischen den verschiedenen Editionen von Windows Vista? Wie wirken sich diese auf meine DirectX-Anwendung aus?**

</dd> <dt>

<span id="Will_DirectX_10_be_available_for_Windows_XP__"></span><span id="will_directx_10_be_available_for_windows_xp__"></span><span id="WILL_DIRECTX_10_BE_AVAILABLE_FOR_WINDOWS_XP__"></span>**Ist DirectX 10 für Windows XP verfügbar?** 
</dt> <dd>

Nein. Windows Vista, das über DirectX 10 verfügt, umfasst eine aktualisierte DirectX-Laufzeit, die auf der Laufzeit in Windows XP SP2 (DirectX 9.0 c) basiert und Änderungen für die Verwendung des neuen Windows Display Driver Model (WDDM) und des neuen audiotreibertreibers sowie anderer Updates im Betriebssystem umfasst. Zusätzlich zu Direct3D 9 unterstützt Windows Vista zwei neue Schnittstellen, wenn die richtige Video Hardware und die richtigen Treiber vorhanden sind: Direct3D9Ex und Direct3D10.

Da diese neuen Schnittstellen auf der WDDM-Technologie basieren, sind Sie in früheren Versionen von Windows nie verfügbar. Alle anderen Änderungen, die an DirectX-Technologien für Windows Vista vorgenommen werden, sind auch für die neue Version von Windows spezifisch. Der Name DirectX 10 ist insofern irreführend, als dass viele Technologien, die im DirectX SDK (XACT, xinput, D3DX) enthalten sind, nicht von dieser Versionsnummer abgedeckt werden. Daher hat das verweisen auf die Versionsnummer der DirectX-Laufzeit als Ganzes einen Großteil der Bedeutung verloren, auch für 9.0 c. Das DirectX-Diagnose Tool (DXdiag.exe) unter Windows Vista meldet DirectX 10, aber dies bezieht sich nur auf Direct3D 10.

</dd> <dt>

<span id="Will_DirectX_11_be_available_for_Windows_Vista_or_Windows_XP__"></span><span id="will_directx_11_be_available_for_windows_vista_or_windows_xp__"></span><span id="WILL_DIRECTX_11_BE_AVAILABLE_FOR_WINDOWS_VISTA_OR_WINDOWS_XP__"></span>**Ist DirectX 11 für Windows Vista oder Windows XP verfügbar?** 
</dt> <dd>

DirectX 11 ist in Windows 7 integriert und steht als Update für Windows Vista zur Verfügung (siehe <https://go.microsoft.com/fwlink/p/?linkid=160189> ). Dies umfasst die API Direct3D 11, DirectX Graphics Infrastructure (DXGI) 1,1, 10level9 Feature Levels, Windows Advanced rasterization Platform (Warp) 10 Software Rendering Device, Direct2D, DirectWrite und ein Update für die Direct3D 10,1-API zur Unterstützung von 10level9 und Warp 10.

Aus den gleichen Gründen, die in der vorangegangenen Frage aufgeführt sind (ist **DirectX 10 für Windows XP verfügbar?** ), Direct3D 11 und verwandte APIs sind unter Windows XP nicht verfügbar.

</dd> <dt>

<span id="What_Happened_to_DirectShow__I_can_t_find_it_in_the_DirectX_SDK._"></span><span id="what_happened_to_directshow__i_can_t_find_it_in_the_directx_sdk._"></span><span id="WHAT_HAPPENED_TO_DIRECTSHOW__I_CAN_T_FIND_IT_IN_THE_DIRECTX_SDK._"></span>**Was ist mit DirectShow passiert? Ich kann es im DirectX SDK nicht finden.** 
</dt> <dd>

DirectShow wurde seit April 2005 aus dem DirectX SDK entfernt. Sie können die Header, Bibliotheken, Tools und Beispiele für DirectShow im Windows Software Development Kit (ehemals Platform SDK) abrufen. DirectSetup im DirectX SDK unterstützt weiterhin die Neuverteilung der Systemkomponenten von DirectShow, und die neuesten Komponenten sind bereits unter den folgenden Betriebssystemen installiert: Microsoft Windows XP Service Pack 2, Windows XP Professional x64 Edition, Windows Server 2003 Service Pack 1 und Windows Vista.

</dd> <dt>

<span id="What_changes_were_made_to_the_DirectX_runtime_for_Windows_Vista__"></span><span id="what_changes_were_made_to_the_directx_runtime_for_windows_vista__"></span><span id="WHAT_CHANGES_WERE_MADE_TO_THE_DIRECTX_RUNTIME_FOR_WINDOWS_VISTA__"></span>**Welche Änderungen wurden an der DirectX-Laufzeit für Windows Vista vorgenommen?** 
</dt> <dd>

Die primären Änderungen wurden vorgenommen, um die neue WDDM zu unterstützen. Ausführliche Informationen zum neuen Treibermodell, zu den Auswirkungen auf Direct3D 9 und den beiden neuen Grafik Schnittstellen Direct3D 9Ex und Direct3D 10 finden Sie unter [Grafik-APIs in Windows](/windows/desktop/direct3darticles/graphics-apis-in-windows-vista). Neue Grafik-APIs für Windows 7 – Direct3D 11, Direct2D, DirectWrite, DXGI 1,1 und ein aktualisiertes Direct3D 10.1 – sind als Update für Windows Vista verfügbar (siehe <https://go.microsoft.com/fwlink/p/?linkid=160189> ).

Windows Vista Service Pack 1 enthält eine aktualisierte Version der DirectX-Laufzeit. Dieses Update erweitert die Unterstützung von Windows Vista um Direct3D 10,1 und bietet neue optionale Hardware Features. (Alle Hardware, die Direct3D 10,1 unterstützen kann, unterstützt auch vollständig alle Features von Direct3D 10.)

DirectSound wurde aktualisiert, um die Funktionen des neuen Windows Vista-audiotreiberstapels verfügbar zu machen, der Software Puffer mit mehreren Kanälen unterstützt. Die API für den beibehaltenen Modus Direct3D wurde vollständig aus Windows Vista entfernt. Außerdem wurde die DirectPlay-Stimme entfernt, ebenso wie das NAT-Hilfsobjekt von DirectPlay und die Aktions Mapper-Benutzeroberfläche von DirectInput. Unterstützung für die DirectX 7-und DirectX 8-Schnittstellen für Visual Basic 6,0 ist unter Windows Vista nicht verfügbar.

</dd> <dt>

<span id="What_changes_were_made_to_the_DirectX_runtime_for_Windows_7__"></span><span id="what_changes_were_made_to_the_directx_runtime_for_windows_7__"></span><span id="WHAT_CHANGES_WERE_MADE_TO_THE_DIRECTX_RUNTIME_FOR_WINDOWS_7__"></span>**Welche Änderungen wurden an der DirectX-Laufzeit für Windows 7 vorgenommen?** 
</dt> <dd>

Windows 7 umfasst alle in Windows Vista gefundenen DirectX-Laufzeitkomponenten und fügt Direct3D 11, DXGI 1,1, 10level9-featureebenen, das WARP10-Software Gerät, Direct2D, DirectWrite und ein Update für Direct3D 10,1 zur Unterstützung von 10level9 und WARP10 hinzu. Weitere Informationen finden Sie unter [Grafik-APIs in Windows](/windows/desktop/direct3darticles/graphics-apis-in-windows-vista).

Alle anderen Komponenten sind mit Windows Vista identisch. Zusätzlich wird die systemeigene Unterstützung von 64-Bit (x64) für die zentrale DirectMusic-API für das Zeitstempel-MIDI verwendet. Die Leistungs Ebene von DirectMusic bleibt veraltet und steht nur für 32-Bit-Anwendungen unter Windows 7 für die Anwendungs Kompatibilität zur Verfügung. Beachten Sie, dass die native Unterstützung von DirectMusic in 64-Bit unter Windows Vista nicht verfügbar ist.

</dd> <dt>

<span id="I_think_I_have_found_a_driver_bug__what_do_I_do__"></span><span id="i_think_i_have_found_a_driver_bug__what_do_i_do__"></span><span id="I_THINK_I_HAVE_FOUND_A_DRIVER_BUG__WHAT_DO_I_DO__"></span>**Ich denke, ich habe einen Treiber Fehler gefunden. Was kann ich tun?** 
</dt> <dd>

Vergewissern Sie sich zunächst, dass Sie die Ergebnisse mit dem Verweis Raster geprüft haben. Überprüfen Sie dann die Ergebnisse mit der neuesten WHQL Certified-Version des IHVs-Treibers. Sie können den WHQL-Status mithilfe der getadapteridentifier ()-Methode in der IDirect3D9-Schnittstelle Programm gesteuert überprüfen, indem Sie das D3DENUM \_ WHQL \_ Level-Flag übergeben.

</dd> <dt>

<span id="Why_do_I_get_so_many_error_messages_when_I_try_to_compile_the_samples__"></span><span id="why_do_i_get_so_many_error_messages_when_i_try_to_compile_the_samples__"></span><span id="WHY_DO_I_GET_SO_MANY_ERROR_MESSAGES_WHEN_I_TRY_TO_COMPILE_THE_SAMPLES__"></span>**Warum erhalte ich so viele Fehlermeldungen, wenn ich versuche, die Beispiele zu kompilieren?** 
</dt> <dd>

Der Include-Pfad ist wahrscheinlich nicht ordnungsgemäß festgelegt. Viele Compiler, einschließlich Microsoft Visual C++, enthalten eine frühere Version des SDK. Wenn Ihr Includepfad den Standard Compiler beispielsweise Verzeichnisse zuerst durchsucht, erhalten Sie falsche Versionen der Header Dateien. Um dieses Problem zu beheben, stellen Sie sicher, dass die Pfade Pfad und Bibliothek einschließen so festgelegt sind, dass Sie zuerst die Microsoft DirectX-Include-und-Bibliothekspfade Weitere Informationen finden Sie auch in der dxreadme.txt-Datei im SDK. Wenn Sie das DirectX SDK installieren und Visual C++ verwenden, kann das Installationsprogramm optional die Includepfade für Sie einrichten.

</dd> <dt>

<span id="I_get_linker_errors_about_multiple_or_missing_symbols_for_globally_unique_identifiers__GUIDs___what_do_I_do__"></span><span id="i_get_linker_errors_about_multiple_or_missing_symbols_for_globally_unique_identifiers__guids___what_do_i_do__"></span><span id="I_GET_LINKER_ERRORS_ABOUT_MULTIPLE_OR_MISSING_SYMBOLS_FOR_GLOBALLY_UNIQUE_IDENTIFIERS__GUIDS___WHAT_DO_I_DO__"></span>**Ich erhalte Linker-Fehler über mehrere oder fehlende Symbole für Global Unique Identifier (GUIDs). Was kann ich tun?** 
</dt> <dd>

Die verschiedenen GUIDs, die Sie verwenden, sollten nur einmal definiert werden. Die Definition für die GUID wird eingefügt, wenn Sie \# das Initguid-Symbol definieren, bevor Sie die DirectX-Header Dateien einschließen. Daher sollten Sie sicherstellen, dass dies nur für eine Kompilierungseinheit auftritt. Eine Alternative zu dieser Methode besteht darin, eine Verknüpfung mit der dxguid. lib-Bibliothek zu verknüpfen, die Definitionen für alle DirectX-GUIDs enthält. Wenn Sie diese Methode verwenden (was empfohlen wird), sollten Sie nie \# das Initguid-Symbol definieren.

</dd> <dt>

<span id="Can_I_cast_a_pointer_to_a_DirectX_interface_to_a_lower_version_number__"></span><span id="can_i_cast_a_pointer_to_a_directx_interface_to_a_lower_version_number__"></span><span id="CAN_I_CAST_A_POINTER_TO_A_DIRECTX_INTERFACE_TO_A_LOWER_VERSION_NUMBER__"></span>**Kann ich einen Zeiger auf eine DirectX-Schnittstelle in eine niedrigere Versionsnummer umwandeln?** 
</dt> <dd>

Nein. DirectX-Schnittstellen sind COM-Schnittstellen. Dies bedeutet, dass es nicht erforderlich ist, dass höher nummerierte Schnittstellen von den entsprechenden niedrigeren nummerierten Schnittstellen abgeleitet werden. Daher besteht die einzige sichere Möglichkeit zum Abrufen einer anderen Schnittstelle zu einem DirectX-Objekt darin, die QueryInterface-Methode der Schnittstelle zu verwenden. Diese Methode ist Teil der standardmäßigen IUnknown-Schnittstelle, von der alle COM-Schnittstellen abgeleitet werden müssen.

</dd> <dt>

<span id="Can_I_mix_the_use_of_DirectX_9_components_and_DirectX_8_or_earlier_components_within_the_same_application__"></span><span id="can_i_mix_the_use_of_directx_9_components_and_directx_8_or_earlier_components_within_the_same_application__"></span><span id="CAN_I_MIX_THE_USE_OF_DIRECTX_9_COMPONENTS_AND_DIRECTX_8_OR_EARLIER_COMPONENTS_WITHIN_THE_SAME_APPLICATION__"></span>**Kann ich die Verwendung von DirectX 9-Komponenten und DirectX 8 oder früheren Komponenten in derselben Anwendung mischen?** 
</dt> <dd>

Sie können verschiedene Komponenten einer abweichenden Version beliebig kombinieren. Beispielsweise können Sie DirectInput 8 mit Direct3D 9 in derselben Anwendung verwenden. Im Allgemeinen ist es jedoch nicht möglich, unterschiedliche Versionen derselben Komponente innerhalb derselben Anwendung zu mischen. Sie können DirectDraw 7 z. b. nicht mit Direct3D 9 mischen (da es sich dabei tatsächlich um dieselbe Komponente handelt, wie DirectDraw in Direct3D ab DirectX 8 subsudiert wurde). Es gibt jedoch Ausnahmen, wie z. b. die Verwendung von Direct3D 9 und Direct3D 10 in derselben Anwendung, die zulässig ist.

</dd> <dt>

<span id="Can_I_mix_the_use_of_Direct3D_9_and_Direct3D_10_within_the_same_application__"></span><span id="can_i_mix_the_use_of_direct3d_9_and_direct3d_10_within_the_same_application__"></span><span id="CAN_I_MIX_THE_USE_OF_DIRECT3D_9_AND_DIRECT3D_10_WITHIN_THE_SAME_APPLICATION__"></span>**Kann ich die Verwendung von Direct3D 9 und Direct3D 10 innerhalb derselben Anwendung kombinieren?** 
</dt> <dd>

Ja, Sie können diese Versionen von Direct3D in derselben Anwendung verwenden.

</dd> <dt>

<span id="What_do_the_return_values_from_the_Release_or_AddRef_methods_mean__"></span><span id="what_do_the_return_values_from_the_release_or_addref_methods_mean__"></span><span id="WHAT_DO_THE_RETURN_VALUES_FROM_THE_RELEASE_OR_ADDREF_METHODS_MEAN__"></span>**Was bedeuten die Rückgabewerte der Release-oder adressf-Methoden?** 
</dt> <dd>

Der Rückgabewert ist der aktuelle Verweis Zähler des Objekts. Die com-Spezifikation gibt jedoch an, dass Sie sich nicht darauf verlassen sollten. der Wert ist in der Regel nur für Debugzwecke verfügbar. Die von Ihnen beobachteten Werte sind möglicherweise unerwartet, da verschiedene andere Systemobjekte möglicherweise Verweise auf die von Ihnen erstellten DirectX-Objekte enthalten. Aus diesem Grund sollten Sie keinen Code schreiben, der die Freigabe wiederholt aufruft, bis der Verweis Zähler 0 (null) ist, da das Objekt dann freigegeben werden kann, obwohl eine andere Komponente möglicherweise noch auf Sie verweist.

</dd> <dt>

<span id="Does_it_matter_in_which_order_I_release_DirectX_interfaces__"></span><span id="does_it_matter_in_which_order_i_release_directx_interfaces__"></span><span id="DOES_IT_MATTER_IN_WHICH_ORDER_I_RELEASE_DIRECTX_INTERFACES__"></span>**Ist es wichtig, in welcher Reihenfolge ich DirectX-Schnittstellen freigebe?** 
</dt> <dd>

Es sollte keine Rolle spielen, da COM-Schnittstellen Verweis gezählt werden. In einigen Versionen von DirectX gibt es jedoch einige bekannte Fehler in der releasereihenfolge der Schnittstellen. Aus Sicherheitsgründen empfiehlt es sich, Schnittstellen nach Möglichkeit in umgekehrter Reihenfolge zu veröffentlichen.

</dd> <dt>

<span id="What_is_a_smart_pointer_and_should_I_use_it__"></span><span id="what_is_a_smart_pointer_and_should_i_use_it__"></span><span id="WHAT_IS_A_SMART_POINTER_AND_SHOULD_I_USE_IT__"></span>**Was ist ein intelligenter Zeiger und sollte ich ihn verwenden?** 
</dt> <dd>

Ein intelligenter Zeiger ist eine C++-Vorlagen Klasse, die zum Kapseln von Zeiger Funktionen entworfen wurde. Insbesondere gibt es standardmäßige intelligente Zeiger Klassen, die für das Kapseln von COM-Schnittstellen Zeigern konzipiert sind. Diese Zeiger führen automatisch QueryInterface anstelle einer Typumwandlung aus, und Sie verarbeiten Adressaten und Freigaben für Sie. Ob Sie diese verwenden sollten, ist größtenteils eine Frage des Geschmacks. Wenn Ihr Code viele Kopien von Schnittstellen Zeigern mit mehreren Adressen und Releases enthält, können intelligente Zeiger den Code ggf. und weniger fehleranfällig machen. Andernfalls können Sie ohne Sie ausführen. Visual C++ enthält einen intelligenten Microsoft com-Standard Zeiger, der in der Header Datei "comdef. h" definiert ist (suchen Sie \_ in der-Hilfe nach com PTR \_ t).

</dd> <dt>

<span id="I_have_trouble_debugging_my_DirectX_application__any_tips__"></span><span id="i_have_trouble_debugging_my_directx_application__any_tips__"></span><span id="I_HAVE_TROUBLE_DEBUGGING_MY_DIRECTX_APPLICATION__ANY_TIPS__"></span>**Ich habe Probleme beim Debuggen meiner DirectX-Anwendung, Tipps?** 
</dt> <dd>

Das häufigste Problem beim Debuggen von DirectX-Anwendungen ist das Debuggen, während eine DirectDraw-Oberfläche gesperrt ist. Diese Situation kann eine "Win16 Lock" auf Microsoft Windows 9X-Systemen verursachen, die das Zeichnen des Debugger-Fensters verhindert. Wenn das D3DLOCK \_ nosyslock-Flag beim Sperren der Oberfläche angegeben wird, kann dies normalerweise vermieden werden. Windows 2000 wird von diesem Problem nicht beeinträchtigt. Beim Entwickeln einer Anwendung ist es sinnvoll, mit der Debugversion der DirectX-Laufzeit (die bei der Installation des SDKs ausgewählt ist) ausgeführt zu werden, die eine Parameter Validierung ausführt und nützliche Meldungen an die Debugger-Ausgabe ausgibt.

</dd> <dt>

<span id="What_s_the_correct_way_to_check_return_codes__"></span><span id="what_s_the_correct_way_to_check_return_codes__"></span><span id="WHAT_S_THE_CORRECT_WAY_TO_CHECK_RETURN_CODES__"></span>**Wie sieht die richtige Methode zum Überprüfen von Rückgabecodes aus?** 
</dt> <dd>

Verwenden Sie die Makros erfolgreich und failed. DirectX-Methoden können mehrere Erfolgs-und Fehlercodes zurückgeben, also eine einfache:

``` syntax
== D3D_OK
```

ein ähnlicher Test ist nicht immer ausreichend.

</dd> <dt>

<span id="How_do_I_disable_ALT_TAB_and_other_task_switching__"></span><span id="how_do_i_disable_alt_tab_and_other_task_switching__"></span><span id="HOW_DO_I_DISABLE_ALT_TAB_AND_OTHER_TASK_SWITCHING__"></span>**Gewusst wie die Optionen Alt + Tab und anderer Aufgaben Wechsel deaktivieren?** 
</dt> <dd>

Nicht! Spiele müssen in der Lage sein, den Aufgaben Wechsel ordnungsgemäß durchzuführen, so wie es dies bewirkt: Alt + Tab, Remote Desktop Verbindungen, schnelle Benutzerumschaltung, Nutzungs Grenzwerte für Eltern Kontrollen und viele andere Ereignisse.

Gleichzeitig werden zwei häufige Quellen der versehentlichen Aufgaben Umschaltung bei Spielen mit Tastatur zentrischen Steuerungs Schemas durch Drücken der Windows-Taste und durch Aktivieren der Barrierefreiheits Funktion "StickyKeys" mit der Umschalttaste versehen. Informationen zu diesen Fällen durch Deaktivierung der Funktionalität finden Sie unter den unter [Deaktivieren von Tastenkombinationen in spielen](/windows/desktop/DxTechArts/disabling-shortcut-keys-in-games)beschriebenen Techniken.

</dd> <dt>

<span id="Is_there_a_recommended_book_explaining_COM__"></span><span id="is_there_a_recommended_book_explaining_com__"></span><span id="IS_THERE_A_RECOMMENDED_BOOK_EXPLAINING_COM__"></span>**Gibt es ein empfohlenes Buch, das com erläutert?** 
</dt> <dd>

*In com* von Dale Rogerson, veröffentlicht von Microsoft Press, ist eine hervorragende Einführung in com. Eine ausführlichere Betrachtung von com, das von Longman veröffentlichte Book Essentials *com* von Don, wird ebenfalls dringend empfohlen.

</dd> <dt>

<span id="What_is_managed_code__"></span><span id="what_is_managed_code__"></span><span id="WHAT_IS_MANAGED_CODE__"></span>**Was ist verwalteter Code?** 
</dt> <dd>

Verwalteter Code ist Code, dessen Ausführung von der .NET Framework Common Language Runtime (CLR) verwaltet wird. Er bezieht sich auf einen Vertrag der Zusammenarbeit zwischen nativ ausgeführter Code und Laufzeit. Dieser Vertrag gibt an, dass die Laufzeit zu einem beliebigen Zeitpunkt der Ausführung eine ausführende CPU beenden und Informationen für die aktuelle CPU-Anweisungs Adresse abrufen kann. Informationen, die Abfrage fähig sein müssen, beziehen sich in der Regel auf den Lauf Zeit Zustand, wie z. b. Register oder Stapel Speicherinhalte.

Bevor der Code ausgeführt wird, wird die Il in systemeigenen ausführbaren Code kompiliert. Da diese Kompilierung von der verwalteten Ausführungsumgebung ausgeführt wird (oder durch einen Laufzeit-fähigen Compiler, der das Ziel der verwalteten Ausführungsumgebung ist), kann die verwaltete Ausführungsumgebung gewährleisten, was der Code tun soll. Es können Traps und geeignete Garbage Collection Hooks, Ausnahmebehandlung, Typsicherheit, Array Begrenzungen und Indexüberprüfung usw. eingefügt werden. Ein solcher Compiler stellt z. b. sicher, dass Stapel Rahmen und alles recht genau angeordnet werden, damit die Garbage Collector im Hintergrund in einem separaten Thread ausgeführt werden kann, wobei ständig die aktive aufrufsstapel durchlaufen und alle Stamm Elemente nachverfolgt werden. Da die Il über eine Art Sicherheit verfügt, behält die Ausführungs-Engine die Garantie der Typsicherheit bei, wodurch eine ganze Klasse von Programmierfehlern vermieden wird, die häufig zu Sicherheitslücken führen.

Anders als bei der nicht verwalteten Welt: nicht verwaltete ausführbare Dateien sind im Grunde ein binäres Bild, x86-Code, der in den Arbeitsspeicher geladen wird. Der Programm Counter wird dort abgelegt, und das ist das letzte Betriebssystem. Es gibt Schutzmaßnahmen hinsichtlich der Speicherverwaltung und der Port-e/a und so weiter, aber das System weiß nicht, was die Anwendung tut. Daher kann es keine Garantie dafür geben, was geschieht, wenn die Anwendung ausgeführt wird.

</dd> <dt>

<span id="What_books_are_there_about_general_Windows_programming__"></span><span id="what_books_are_there_about_general_windows_programming__"></span><span id="WHAT_BOOKS_ARE_THERE_ABOUT_GENERAL_WINDOWS_PROGRAMMING__"></span>**Welche Bücher gibt es mit allgemeiner Windows-Programmierung?** 
</dt> <dd>

Viele. Beide werden jedoch dringend empfohlen:

-   Programmieren von Fenstern von Charles Petzold (Microsoft Press)
-   Programmieren von Anwendungen für Windows von Jeffrey Richter (Microsoft Press)

</dd> <dt>

<span id="How_do_I_debug_using_the_Windows_symbol_files__"></span><span id="how_do_i_debug_using_the_windows_symbol_files__"></span><span id="HOW_DO_I_DEBUG_USING_THE_WINDOWS_SYMBOL_FILES__"></span>**Gewusst wie Debuggen mit den Windows-Symbol Dateien aus?** 
</dt> <dd>

Microsoft veröffentlichte Symbole für alle System-DLLs (und einige andere). Um darauf zuzugreifen, fügen Sie dem Symbol Pfad in den Projekteinstellungen in Visual Studio Folgendes hinzu:

``` syntax
srv*https://msdl.microsoft.com/download/symbols
```

um Symbole lokal zwischenzuspeichern, verwenden Sie die folgende Syntax:

``` syntax
srv*c:\cache*https://msdl.microsoft.com/download/symbols
```

Dabei ist c: \\ Cache ein lokales Verzeichnis zum Zwischenspeichern von Symbol Dateien.

</dd> </dl>

## <a name="direct3d-questions"></a>Direct3D Fragen

### <a name="general-direct3d-questions"></a>Allgemeine Direct3D Fragen

<dl> <dt>

<span id="Where_can_I_find_information_about_3D_graphics_techniques__"></span><span id="where_can_i_find_information_about_3d_graphics_techniques__"></span><span id="WHERE_CAN_I_FIND_INFORMATION_ABOUT_3D_GRAPHICS_TECHNIQUES__"></span>**Wo finde ich Informationen zu 3D-Grafiktechniken?** 
</dt> <dd>

Das Standardbuch des Subjekts ist Computer Grafik: Prinzipien und Praxis von Foley, van Dam et al. Es ist eine nützliche Ressource für alle Benutzer, die die mathematischen Grundlagen von Geometrie-, Rasterung-und Beleuchtungstechniken verstehen möchten. Die häufig gestellten Fragen zur Comp-Gruppe comp. Graphics. Algorithmen enthalten auch nützliches Material.

</dd> <dt>

<span id="Does_Direct3D_emulate_functionality_not_provided_by_hardware__"></span><span id="does_direct3d_emulate_functionality_not_provided_by_hardware__"></span><span id="DOES_DIRECT3D_EMULATE_FUNCTIONALITY_NOT_PROVIDED_BY_HARDWARE__"></span>**Werden Direct3D Emulierung nicht von Hardware bereitgestellt?** 
</dt> <dd>

Das ist unterschiedlich. Direct3D verfügt über eine voll ausgestattete Pipeline zur Verarbeitung von Software Scheitel Punkten (einschließlich Unterstützung für benutzerdefinierte Scheitelpunkt-Shader). Für Vorgänge auf Pixelebene wird jedoch keine Emulation bereitgestellt. Anwendungen müssen die entsprechenden Caps-Bits überprüfen und die ValidateDevice-API verwenden, um die Unterstützung zu ermitteln.

</dd> <dt>

<span id="Is_there_a_software_rasterizer_included_with_Direct3D__"></span><span id="is_there_a_software_rasterizer_included_with_direct3d__"></span><span id="IS_THERE_A_SOFTWARE_RASTERIZER_INCLUDED_WITH_DIRECT3D__"></span>**Gibt es einen Software-Raster, der in Direct3D enthalten ist?** 
</dt> <dd>

Nicht für Leistungs Anwendungen. Für die Treiber Validierung wird ein verweisrasterizer bereitgestellt, die Implementierung ist jedoch auf Genauigkeit und keine Leistung ausgelegt. Direct3D unterstützt Plug-in-softwarerasterizer.

</dd> <dt>

<span id="How_can_I_perform_color_keying_with_DirectX_graphics__"></span><span id="how_can_i_perform_color_keying_with_directx_graphics__"></span><span id="HOW_CAN_I_PERFORM_COLOR_KEYING_WITH_DIRECTX_GRAPHICS__"></span>**Wie kann ich die Farb Erstellung mit DirectX-Grafiken durchführen?** 
</dt> <dd>

Die Farb Erstellung wird nicht direkt unterstützt. stattdessen müssen Sie Alpha Blending zum Emulieren von Farben verwenden. Die Funktion D3DXCreateTextureFromFileEx () kann verwendet werden, um dies zu vereinfachen. Diese Funktion akzeptiert einen Schlüssel Farb Parameter und ersetzt alle Pixel aus dem Quell Bild, das die angegebene Farbe enthält, durch transparente schwarze Pixel in der erstellten Textur.

</dd> <dt>

<span id="Does_the_Direct3D_geometry_code_utilize_3DNow__and_or_Pentium_III_SIMD_instructions__"></span><span id="does_the_direct3d_geometry_code_utilize_3dnow__and_or_pentium_iii_simd_instructions__"></span><span id="DOES_THE_DIRECT3D_GEOMETRY_CODE_UTILIZE_3DNOW__AND_OR_PENTIUM_III_SIMD_INSTRUCTIONS__"></span>**Verwendet der Direct3D-Geometry-Code 3DNow!-und/oder Pentium III-SIMD-Anweisungen?** 
</dt> <dd>

Ja. Die Direct3D-Geometrie Pipeline hat mehrere verschiedene Codepfade, abhängig vom Prozessortyp, und Sie verwendet die speziellen Gleit Komma Operationen, die von 3DNow bereitgestellt werden. oder Pentium III-SIMD-Anweisungen, in denen diese verfügbar sind. Dies schließt die Verarbeitung von benutzerdefinierten Vertex-Shadern ein.

</dd> <dt>

<span id="How_do_I_prevent_transparent_pixels_being_written_to_the_z-buffer__"></span><span id="how_do_i_prevent_transparent_pixels_being_written_to_the_z-buffer__"></span><span id="HOW_DO_I_PREVENT_TRANSPARENT_PIXELS_BEING_WRITTEN_TO_THE_Z-BUFFER__"></span>**Gewusst wie verhindern, dass transparente Pixel in den z-Puffer geschrieben werden?** 
</dt> <dd>

Sie können Pixel mit einem Alpha Wert über oder unter einem bestimmten Schwellenwert herausfiltern. Dieses Verhalten können Sie mithilfe von "renderstates Alpha atestenable", "Alpha Aref" und "alphafunc" steuern.

</dd> <dt>

<span id="What_is_a_stencil_buffer__"></span><span id="what_is_a_stencil_buffer__"></span><span id="WHAT_IS_A_STENCIL_BUFFER__"></span>**Was ist ein Schablone-Puffer?** 
</dt> <dd>

Ein Schablone-Puffer ist ein zusätzlicher Puffer von pro Pixel, ähnlich wie ein z-Puffer. Tatsächlich befindet er sich in einigen der Bits eines z-Puffers. Allgemeine Schablone/z-Puffer Formate sind 15-Bit-z-und 1-Bit-Schablonen oder 24-Bit-z-und 8-Bit-Schablonen. Es ist möglich, einfache arithmetische Operationen für den Inhalt des Schablonen Puffers pro Pixel auszuführen, wenn Polygone gerendert werden. Beispielsweise kann der Schablonen Puffer inkrementiert oder dekrementiert werden, oder das Pixel kann zurückgewiesen werden, wenn der Schablonen Wert einen einfachen Vergleichstest nicht bestanden hat. Dies ist nützlich für Effekte, bei denen ein Bereich des Frame Puffers gekennzeichnet und dann nur der markierte (oder nicht markierte) Bereich gerendert wird. Gute Beispiele sind Volumetrische-Effekte wie schattenvolumes.

</dd> <dt>

<span id="How_do_I_use_a_stencil_buffer_to_render_shadow_volumes__"></span><span id="how_do_i_use_a_stencil_buffer_to_render_shadow_volumes__"></span><span id="HOW_DO_I_USE_A_STENCIL_BUFFER_TO_RENDER_SHADOW_VOLUMES__"></span>**Gewusst wie einen Schablonen Puffer zum Rendering von schattenvolumes verwenden?** 
</dt> <dd>

Der Schlüssel zu diesem und anderen volumetristencil-Puffer Effekten ist die Interaktion zwischen dem Schablonen Puffer und dem z-Puffer. Eine Szene mit einem Schatten Volume wird in drei Phasen gerendert. Zuerst wird die Szene ohne den Schatten wie gewohnt mit dem z-Puffer gerendert. Im nächsten Schritt wird der Schatten im Schablonen Puffer wie folgt markiert. Die Vorderseiten des Schatten Volumens werden mithilfe von nicht sichtbaren Polygonen gezeichnet, wobei z-Tests aktiviert sind, z-Schreibvorgänge jedoch deaktiviert und der Schablonen Puffer bei jedem Pixel, der den z-Test übergibt, inkrementiert wird. Die Hinterflächen des Schatten Datentyps werden ähnlich gerendert, aber der Schablonen Wert wird stattdessen herabgesetzt.

Sehen Sie sich nun ein einzelnes Pixel an. Wenn sich die Kamera nicht im Schatten Volume befindet, gibt es vier Möglichkeiten für den entsprechenden Punkt in der Szene. Wenn sich der Strahl von der Kamera bis zum Punkt nicht mit dem Schatten Volume überschneidet, werden keine Schatten Polygone dort gezeichnet, und der Schablonen Puffer ist noch 0 (null). Andernfalls, wenn der Punkt vor dem Schatten Volume liegt, werden die Schatten Polygone z-puffert, und die Schablone bleibt unverändert. Wenn sich die Punkte hinter dem Schatten Volume befinden, wird die gleiche Anzahl von Front-Shadow-Gesichtern als hintere Gesichter gerendert, und die Schablone ist 0 (null) und wird so oft wie dekrementiert erhöht.

Die endgültige Möglichkeit besteht darin, dass sich der Punkt innerhalb des Schatten Volumens befindet. In diesem Fall wird die Rückseite des Schatten Datentyps z-puffert, jedoch nicht die Vorderseite, sodass der Schablonen Puffer ein Wert ungleich 0 (null) ist. Das Ergebnis sind Teile des Frame Puffers, die sich im Schatten befinden, haben einen Schablonen Wert ungleich 0 (null). Um den Schatten tatsächlich zu erzeugen, wird die gesamte Szene mit einem Alpha gemischten Polygon gewaschen, das sich nur auf Pixel mit einem Schablonen Wert ungleich 0 auswirkt. Ein Beispiel für diese Technik finden Sie im Beispiel "Schatten Volume", das im DirectX SDK vorhanden ist.

</dd> <dt>

<span id="What_are_the_texel_alignment_rules__How_do_I_get_a_one-to-one_mapping__"></span><span id="what_are_the_texel_alignment_rules__how_do_i_get_a_one-to-one_mapping__"></span><span id="WHAT_ARE_THE_TEXEL_ALIGNMENT_RULES__HOW_DO_I_GET_A_ONE-TO-ONE_MAPPING__"></span>**Was sind die texausrichtungs Regeln? Gewusst wie eine eins-zu-Eins-Zuordnung erhalten?** 
</dt> <dd>

Dies wird in der Dokumentation zu Direct3D 9 ausführlich erläutert. Die Zusammenfassung der Zusammenfassungen besteht jedoch darin, dass Sie die Bildschirm Koordinaten um-0,5 eines Pixels überprüfen müssen, um die ordnungsgemäße Ausrichtung an Texels zu erhalten. Die meisten Karten entsprechen jetzt den texausrichtungsregeln, es gibt jedoch einige ältere Karten oder Treiber, die dies nicht tun. Um diese Fälle zu behandeln, empfiehlt es sich, den betreffenden Hardware Anbieter zu kontaktieren und aktualisierte Treiber oder die vorgeschlagene Problem Umgehung anzufordern. Beachten Sie, dass diese Regel in Direct3D 10 nicht mehr enthalten ist.

</dd> <dt>

<span id="What_is_the_purpose_of_the_D3DCREATE_PUREDEVICE_flag__"></span><span id="what_is_the_purpose_of_the_d3dcreate_puredevice_flag__"></span><span id="WHAT_IS_THE_PURPOSE_OF_THE_D3DCREATE_PUREDEVICE_FLAG__"></span>**Welchen Zweck hat das Flag "D3DCREATE \_ puredevice"?** 
</dt> <dd>

Verwenden Sie zum \_ Erstellen eines reinen Geräts das Flag D3DCREATE puredevice während der Erstellung des Geräts. Ein reines Gerät speichert den aktuellen Zustand (während der Zustandsänderungen) nicht, was häufig die Leistung verbessert. Dieses Gerät erfordert auch die Verarbeitung von Hardware Scheitel Punkten. Ein reines Gerät wird normalerweise verwendet, wenn die Entwicklung und das Debuggen abgeschlossen sind, und Sie möchten die beste Leistung erzielen.

Ein Nachteil eines reinen Geräts besteht darin, dass nicht alle Get-API-Aufrufe unterstützt werden \* . Dies bedeutet, dass Sie kein reines Gerät verwenden können, um den Pipeline Status abzufragen. Dies erschwert das Debuggen während der Ausführung einer Anwendung. Im folgenden finden Sie eine Liste aller Methoden, die von einem reinen Gerät deaktiviert werden.

-   [**IDirect3DDevice9:: getclipplane**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipplane)
-   [**IDirect3DDevice9:: getclipstatus**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getclipstatus)
-   [**IDirect3DDevice9:: getLight**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getlight)
-   [**IDirect3DDevice9:: getlightenable**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getlightenable)
-   [**IDirect3DDevice9:: getmaterial**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getmaterial)
-   [**IDirect3DDevice9:: getpixelshaderconstantf**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getpixelshaderconstantf)
-   [**IDirect3DDevice9:: getpixelshaderconstanti**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getpixelshaderconstanti)
-   [**IDirect3DDevice9:: getpixelshaderconstantb**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getpixelshaderconstantb)
-   [**IDirect3DDevice9::GetRenderState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getrenderstate)
-   [**IDirect3DDevice9:: getsamplerstate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getsamplerstate)
-   [**IDirect3DDevice9:: gettexturestagestate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-gettexturestagestate)
-   [**IDirect3DDevice9:: GetTransform**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-gettransform)
-   [**IDirect3DDevice9:: getvertexshaderconstantf**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getvertexshaderconstantf)
-   [**IDirect3DDevice9:: getvertexshaderconstanti**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getvertexshaderconstanti)
-   [**IDirect3DDevice9:: getvertexshaderconstantb**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getvertexshaderconstantb)

Ein zweiter Nachteil eines reinen Geräts besteht darin, dass redundante Zustandsänderungen nicht gefiltert werden. Wenn Sie ein reines Gerät verwenden, sollte die Anwendung die Anzahl der Zustandsänderungen in der Renderschleife auf ein Mindestmaß reduzieren. Dies kann Filter Zustandsänderungen beinhalten, um sicherzustellen, dass die Zustände nicht mehrmals festgelegt werden. Dieser Kompromiss ist abhängig von der Anwendung. Wenn Sie mehr als 1000 Set-Aufrufe pro Frame verwenden, sollten Sie die Vorteile der Redundanz Filterung in Erwägung ziehen, die automatisch von einem nicht reinen Gerät durchgeführt wird.

Wie bei allen Leistungsproblemen besteht die einzige Möglichkeit, zu ermitteln, ob Ihre Anwendung mit einem reinen Gerät besser funktioniert, darin, die Leistung Ihrer Anwendung mit einem reinen und nicht reinen Gerät zu vergleichen. Ein reines Gerät hat die Möglichkeit, eine Anwendung zu beschleunigen, indem der CPU-Aufwand der API verringert wird. Seien Sie jedoch vorsichtig! In einigen Szenarien verlangsamt ein reines Gerät Ihre Anwendung (aufgrund der zusätzlichen CPU-Arbeit, die durch redundante Zustandsänderungen verursacht wird). Wenn Sie nicht sicher sind, welcher Gerätetyp für Ihre Anwendung am besten geeignet ist und Sie keine redundanten Änderungen in der Anwendung filtern, verwenden Sie ein nicht reines Gerät.

</dd> <dt>

<span id="How_do_I_enumerate_the_display_devices_in_a_multi-monitor_system__"></span><span id="how_do_i_enumerate_the_display_devices_in_a_multi-monitor_system__"></span><span id="HOW_DO_I_ENUMERATE_THE_DISPLAY_DEVICES_IN_A_MULTI-MONITOR_SYSTEM__"></span>**Gewusst wie die Anzeigegeräte in einem System mit mehreren Monitoren aufzuzählen?** 
</dt> <dd>

Die Enumeration kann durch eine einfache Iteration durch die Anwendung mithilfe von Methoden der IDirect3D9-Schnittstelle durchgeführt werden. Aufrufen von getadaptercount, um die Anzahl der Anzeige Adapter im System zu ermitteln. Aufrufen von GetAdapterMonitor, um zu bestimmen, mit welchem physischen Monitor ein Adapter verbunden ist (diese Methode gibt einen Hmonitor zurück, den Sie in der Win32-API getmonitorinfo verwenden können, um Informationen über den physischen Monitor zu ermitteln). Das Ermitteln der Merkmale eines bestimmten Anzeige Adapters oder das Erstellen eines Direct3D-Geräts auf diesem Adapter ist so einfach wie das übergeben der entsprechenden Adapter Nummer anstelle von D3DADAPTER \_ Default beim Aufrufen von GetDeviceCaps, createdevice oder anderen Methoden.

</dd> <dt>

<span id="What_happened_to_Fixed_Function_Bumpmapping_in_D3D9__"></span><span id="what_happened_to_fixed_function_bumpmapping_in_d3d9__"></span><span id="WHAT_HAPPENED_TO_FIXED_FUNCTION_BUMPMAPPING_IN_D3D9__"></span>**Was ist mit der Fixed Function Bumpmapping in d3d9 passiert?** 
</dt> <dd>

Ab Direct3D 9 haben wir die Überprüfung auf Karten gestrafft, die nur > 2 gleichzeitige Texturen unterstützen können. Bei bestimmten älteren Karten sind nur drei Textur Phasen verfügbar, wenn Sie einen bestimmten Alpha modulieren-Vorgang verwenden. Die am häufigsten verwendeten Verwendungsmöglichkeiten für die drei Stufen sind Prägung Bumpmapping, und Sie können dies weiterhin mit d3d9 tun.

Das Height-Feld muss im Alphakanal gespeichert werden und wird verwendet, um den lichtbeitrag zu modulieren, d. h.:

``` syntax
// Stage 0 is the base texture, with the height map in the alpha channel
m_pd3dDevice->SetTexture(0, m_pEmbossTexture );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_TEXCOORDINDEX, 0 );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLOROP,   D3DTOP_MODULATE );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLORARG1, D3DTA_TEXTURE );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_COLORARG2, D3DTA_DIFFUSE );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_ALPHAOP,   D3DTOP_SELECTARG1 );
m_pd3dDevice->SetTextureStageState(0, D3DTSS_ALPHAARG1, D3DTA_TEXTURE );
if( m_bShowEmbossMethod )
{
 // Stage 1 passes through the RGB channels (SELECTARG2 = CURRENT), and 
 // does a signed add with the inverted alpha channel. 
 // The texture coords associated with Stage 1 are the shifted ones, so 
 // the result is:
 //    (height - shifted_height) * tex.RGB * diffuse.RGB
   m_pd3dDevice->SetTexture( 1, m_pEmbossTexture );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_TEXCOORDINDEX, 1 );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_COLOROP, D3DTOP_SELECTARG2 );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG1, D3DTA_TEXTURE );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_COLORARG2, D3DTA_CURRENT );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_ALPHAOP, D3DTOP_ADDSIGNED );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_ALPHAARG1, D3DTA_TEXTURE|D3DTA_COMPLEMENT );
   m_pd3dDevice->SetTextureStageState( 1, D3DTSS_ALPHAARG2, D3DTA_CURRENT );

   // Set up the alpha blender to multiply the alpha channel 
   // (monochrome emboss) with the src color (lighted texture)
   m_pd3dDevice->SetRenderState( D3DRS_ALPHABLENDENABLE, TRUE );
   m_pd3dDevice->SetRenderState( D3DRS_SRCBLEND,  D3DBLEND_SRCALPHA );
   m_pd3dDevice->SetRenderState( D3DRS_DESTBLEND, D3DBLEND_ZERO );
}
```

Dieses Beispiel wird zusammen mit anderen älteren Beispielen nicht mehr in der aktuellen SDK-Version ausgeliefert und wird nicht in zukünftigen SDK-Releases ausgeliefert.

</dd> </dl>

### <a name="geometry-vertex-processing"></a>Geometrie Verarbeitung (Scheitelpunkt)

<dl> <dt>

<span id="Vertex_streams_confuse_me_how_do_they_work__"></span><span id="vertex_streams_confuse_me_how_do_they_work__"></span><span id="VERTEX_STREAMS_CONFUSE_ME_HOW_DO_THEY_WORK__"></span>**Vertex-Streams verwechseln mich, wie funktionieren Sie?** 
</dt> <dd>

Direct3D assembliert jeden Scheitelpunkt, der aus einem oder mehreren vertexstreams in den Verarbeitungsbereich der Pipeline eingespeist wird. Wenn nur ein vertexstream vorhanden ist, entspricht das alte vor DirectX 8-Modell, in dem Vertices aus einer einzelnen Quelle stammen. Bei DirectX 8 können unterschiedliche Scheitelpunkt Komponenten aus unterschiedlichen Quellen stammen. Beispielsweise könnte ein Vertex-Puffer Positionen und normale enthalten, während ein zweiter Farbwert und Texturkoordinaten enthält.

</dd> <dt>

<span id="What_is_a_vertex_shader__"></span><span id="what_is_a_vertex_shader__"></span><span id="WHAT_IS_A_VERTEX_SHADER__"></span>**Was ist ein Vertex-Shader?** 
</dt> <dd>

Ein Vertex-Shader ist eine Prozedur für die Verarbeitung eines einzelnen Scheitel Punkts. Sie wird mit einer einfachen assemblyähnlichen Sprache definiert, die von der D3DX Utility Library in einem Tokenstream assembliert wird, den Direct3D akzeptiert. Der Vertex-Shader nimmt als Eingabe einen einzelnen Scheitelpunkt und einen Satz konstanter Werte an. Er gibt eine Scheitelpunkt Position (im Clip Bereich) und optional einen Satz von Farben und Texturkoordinaten aus, die bei der rasterisierung verwendet werden. Beachten Sie, dass bei einem benutzerdefinierten Vertexshader die Vertex-Komponenten keine Semantik mehr haben, auf die Sie durch Direct3D angewendet werden, und Vertices einfach beliebige Daten sind, die von dem von Ihnen erstellten Vertex-Shader interpretiert werden.

</dd> <dt>

<span id="Does_a_vertex_shader_perform_perspective_division_or_clipping__"></span><span id="does_a_vertex_shader_perform_perspective_division_or_clipping__"></span><span id="DOES_A_VERTEX_SHADER_PERFORM_PERSPECTIVE_DIVISION_OR_CLIPPING__"></span>**Führt ein Vertex-Shader eine perspektivische Division oder Clipping durch?** 
</dt> <dd>

Nein. Der Vertex-Shader gibt eine homogene Koordinate für die transformierte Scheitelpunkt Position im Clip Raum aus. Die Bereichs Einteilung und das Clipping werden automatisch nach dem Shader ausgeführt.

</dd> <dt>

<span id="Can_I_generate_geometry_with_a_vertex_shader__"></span><span id="can_i_generate_geometry_with_a_vertex_shader__"></span><span id="CAN_I_GENERATE_GEOMETRY_WITH_A_VERTEX_SHADER__"></span>**Kann ich Geometrie mit einem Vertex-Shader generieren?** 
</dt> <dd>

Scheitel Punkte können von einem Scheitelpunkt-Shader nicht erstellt oder zerstört werden. Er arbeitet jeweils auf einem einzelnen Scheitelpunkt, wobei ein nicht verarbeiteter Scheitelpunkt als Eingabe und Ausgabe eines einzelnen Vertex verarbeitet wird. Sie kann daher zum Bearbeiten vorhandener Geometrie (Anwenden von Deformationen oder zum Durchführen von Skinning-Vorgängen) verwendet werden, aber es ist nicht möglich, neue Geometrie pro SE zu generieren

</dd> <dt>

<span id="Can_I_apply_a_custom_vertex_shader_to_the_results_of_the_fixed-function_geometry_pipeline__or_vice-versa___"></span><span id="can_i_apply_a_custom_vertex_shader_to_the_results_of_the_fixed-function_geometry_pipeline__or_vice-versa___"></span><span id="CAN_I_APPLY_A_CUSTOM_VERTEX_SHADER_TO_THE_RESULTS_OF_THE_FIXED-FUNCTION_GEOMETRY_PIPELINE__OR_VICE-VERSA___"></span>**Kann ich einen benutzerdefinierten Vertex-Shader auf die Ergebnisse der Geometrie Pipeline mit fester Funktion (oder umgekehrt) anwenden?** 
</dt> <dd>

Nein. Sie müssen eine oder die andere auswählen. Wenn Sie einen benutzerdefinierten Vertex-Shader verwenden, sind Sie für die Ausführung der gesamten Vertex-Transformation verantwortlich.

</dd> <dt>

<span id="Can_I_use_a_custom_vertex_shader_if_my_hardware_does_not_support_it__"></span><span id="can_i_use_a_custom_vertex_shader_if_my_hardware_does_not_support_it__"></span><span id="CAN_I_USE_A_CUSTOM_VERTEX_SHADER_IF_MY_HARDWARE_DOES_NOT_SUPPORT_IT__"></span>**Kann ich einen benutzerdefinierten Vertex-Shader verwenden, wenn die Hardware ihn nicht unterstützt?** 
</dt> <dd>

Ja. Die Direct3D Software Vertex-Verarbeitungs-Engine unterstützt vollständig benutzerdefinierte Scheitelpunkt-Shader mit einem überraschend hohen Leistungsgrad.

</dd> <dt>

<span id="How_do_I_determine_if_the_hardware_supports_my_custom_vertex_shader__"></span><span id="how_do_i_determine_if_the_hardware_supports_my_custom_vertex_shader__"></span><span id="HOW_DO_I_DETERMINE_IF_THE_HARDWARE_SUPPORTS_MY_CUSTOM_VERTEX_SHADER__"></span>**Gewusst wie ermitteln, ob die Hardware meinen benutzerdefinierten Vertex-Shader unterstützt?** 
</dt> <dd>

Geräte, die Vertex-Shader in der Hardware unterstützen können, müssen das Feld D3DCAPS9:: VertexShaderVersion ausfüllen, um die Versions Ebene des Vertex-Shader anzugeben, den Sie unterstützen. Jedes Gerät, das eine bestimmte Ebene des Vertex-Shader unterstützt, muss alle juristischen Vertex-Shader unterstützen, die die Spezifikation für diese Ebene oder darunter erfüllen.

</dd> <dt>

<span id="How_many_constant_registers_are_available_for_vertex_shaders__"></span><span id="how_many_constant_registers_are_available_for_vertex_shaders__"></span><span id="HOW_MANY_CONSTANT_REGISTERS_ARE_AVAILABLE_FOR_VERTEX_SHADERS__"></span>**Wie viele Konstante Register sind für Vertex-Shader verfügbar?** 
</dt> <dd>

Geräte, die vs 1,0-Vertex-Shader unterstützen, müssen mindestens 96 Konstante Register unterstützen. Geräte unterstützen möglicherweise mehr als diese Mindestanzahl und können dies über das Feld D3DCAPS9:: maxvertexshaderalst melden.

</dd> <dt>

<span id="Can_I_share_position_data_between_vertices_with_different_texture_coordinates__"></span><span id="can_i_share_position_data_between_vertices_with_different_texture_coordinates__"></span><span id="CAN_I_SHARE_POSITION_DATA_BETWEEN_VERTICES_WITH_DIFFERENT_TEXTURE_COORDINATES__"></span>**Kann ich Positionsdaten zwischen Scheitel Punkten mit unterschiedlichen Texturkoordinaten freigeben?** 
</dt> <dd>

Das übliche Beispiel für diese Situation ist ein Cube, in dem Sie für jedes Gesicht eine andere Textur verwenden möchten. Leider ist die Antwort Nein, es ist derzeit nicht möglich, die Scheitelpunkt Komponenten unabhängig voneinander zu indizieren. Auch bei mehreren Scheitelpunkt Datenströmen werden alle Streams miteinander indiziert.

</dd> <dt>

<span id="When_I_submit_an_indexed_list_of_primitives__does_Direct3D_process_all_of_the_vertices_in_the_buffer__or_just_the_ones_I_indexed__"></span><span id="when_i_submit_an_indexed_list_of_primitives__does_direct3d_process_all_of_the_vertices_in_the_buffer__or_just_the_ones_i_indexed__"></span><span id="WHEN_I_SUBMIT_AN_INDEXED_LIST_OF_PRIMITIVES__DOES_DIRECT3D_PROCESS_ALL_OF_THE_VERTICES_IN_THE_BUFFER__OR_JUST_THE_ONES_I_INDEXED__"></span>**Wenn ich eine indizierte Liste von primitiven Sende, verarbeitet Direct3D alle Scheitel Punkte im Puffer oder nur die Indizes, die ich indiziert habe?** 
</dt> <dd>

Wenn Sie die Software Geometrie Pipeline verwenden, wandelt Direct3D zuerst alle Scheitel Punkte in den von Ihnen übermittelten Bereich um, anstatt Sie bei der Indizierung "Bedarfs gesteuert" zu transformieren. Bei dichten Daten (d. h. bei Verwendung der meisten Scheitel Punkte) ist dies effizienter, insbesondere wenn SIMD-Anweisungen verfügbar sind. Wenn Ihre Daten spärlich gepackt sind (d. h. viele Scheitel Punkte werden nicht verwendet), sollten Sie die Daten neu anordnen, um zu viele redundante Transformationen zu vermeiden. Wenn Sie die Hardware Geometrie Beschleunigung verwenden, werden Vertices in der Regel nach Bedarf transformiert, wenn Sie erforderlich sind.

</dd> <dt>

<span id="What_is_an_index_buffer__"></span><span id="what_is_an_index_buffer__"></span><span id="WHAT_IS_AN_INDEX_BUFFER__"></span>**Was ist ein Index Puffer?** 
</dt> <dd>

Ein Index Puffer entspricht genau einem Scheitelpunkt Puffer, stattdessen enthält er jedoch Indizes für die Verwendung in DrawIndexedPrimitive-aufrufen. Es wird dringend empfohlen, nach Möglichkeit Index Puffer anstelle von unformatierten, von der Anwendung belegten Arbeitsspeicher zu verwenden, und zwar aus denselben Gründen wie Scheitelpunkt Puffer.

</dd> <dt>

<span id="I_notice_that_32-bit_indices_are_a_supported_type__can_I_use_them_on_all_devices__"></span><span id="i_notice_that_32-bit_indices_are_a_supported_type__can_i_use_them_on_all_devices__"></span><span id="I_NOTICE_THAT_32-BIT_INDICES_ARE_A_SUPPORTED_TYPE__CAN_I_USE_THEM_ON_ALL_DEVICES__"></span>**Beachten Sie, dass 32-Bit-Indizes ein unterstützter Typ sind. kann ich diese auf allen Geräten verwenden?** 
</dt> <dd>

Nein. Sie müssen das Feld D3DCAPS9:: MaxVertexIndex überprüfen, um den maximalen Indexwert zu bestimmen, der vom Gerät unterstützt wird. Dieser Wert muss größer als 2 bis 16. Strom-1 (0xFFFF) sein, damit Index Puffer vom Typ D3DFMT \_ INDEX32 unterstützt werden. Beachten Sie außerdem, dass einige Geräte 32-Bit-Indizes unterstützen, aber einen maximalen Indexwert kleiner als 2 bis zum 32. Strom-1 (0xFFFFFFFF) unterstützen. in diesem Fall muss die Anwendung das vom Gerät gemeldete Limit berücksichtigen.

</dd> <dt>

<span id="Does_S_W_vertex_processing_support_64_bit__"></span><span id="does_s_w_vertex_processing_support_64_bit__"></span><span id="DOES_S_W_VERTEX_PROCESSING_SUPPORT_64_BIT__"></span>**Unterstützt die S/W-Vertexverarbeitung das 64-Bit?** 
</dt> <dd>

Es ist eine optimierte s/w-Scheitelpunkt Pipeline für x64 vorhanden, Sie ist jedoch nicht für ia64 vorhanden.

</dd> </dl>

### <a name="performance-tuning"></a>Leistungsoptimierung

<dl> <dt>

<span id="How_can_I_improve_the_performance_of_my_Direct3D_application__"></span><span id="how_can_i_improve_the_performance_of_my_direct3d_application__"></span><span id="HOW_CAN_I_IMPROVE_THE_PERFORMANCE_OF_MY_DIRECT3D_APPLICATION__"></span>**Wie kann ich die Leistung meiner Direct3D-Anwendung verbessern?** 
</dt> <dd>

Im folgenden finden Sie die wichtigsten Bereiche, die Sie beim Optimieren der Leistung untersuchen können:

<dl> <dt>

<span id="Batch_size_"></span><span id="batch_size_"></span><span id="BATCH_SIZE_"></span>**Batch Größe** 
</dt> <dd>

Direct3D ist für große Batches von primitiven optimiert. Die mehr Polygone, die in einem einzelnen-Befehl gesendet werden können, desto besser. Eine gute Faustregel besteht darin, durchschnittlich 1000 Vertices pro primitiver aufzurufen. Unterhalb dieser Stufe erzielen Sie wahrscheinlich nicht die optimale Leistung, und Sie können zu abnehmenden Rückgaben und potenziellen Konflikten mit neben läufigkeits Überlegungen kommen (siehe unten).

</dd> <dt>

<span id="State_changes_"></span><span id="state_changes_"></span><span id="STATE_CHANGES_"></span>**Statusänderungen** 
</dt> <dd>

Das Ändern des Rendering-Zustands kann ein kostspieliger Vorgang sein, insbesondere beim Ändern der Textur. Aus diesem Grund ist es wichtig, so viel wie möglich die Anzahl der pro Frame vorgenommenen Zustandsänderungen zu minimieren. Versuchen Sie außerdem, die Änderungen des Scheitel Punkts oder des Index Puffers zu minimieren.

> [!Note]  
> Ab DirectX 8 ist die Kosten für das Ändern des Scheitelpunkt Puffers nicht mehr so teuer wie bei früheren Versionen. es ist aber dennoch empfehlenswert, nach Möglichkeit Vertex-Puffer Änderungen zu vermeiden.

 

</dd> <dt>

<span id="Concurrency"></span><span id="concurrency"></span><span id="CONCURRENCY"></span>**Concurrency**
</dt> <dd>

Wenn Sie die gleichzeitige Ausführung von Rendering mit anderer Verarbeitung anordnen können, werden Sie die Systemleistung voll ausschöpfen. Dieses Ziel kann einen Konflikt mit dem Ziel der Reduzierung von renderstate-Änderungen verursachen. Sie müssen ein Gleichgewicht zwischen der Batch Verarbeitung erreichen, um Zustandsänderungen zu reduzieren und Daten frühzeitig an den Treiber zu übertragen, um Parallelität zu erzielen. Die Verwendung mehrerer Scheitelpunkt Puffer im Roundrobin-Verfahren kann bei der Parallelität helfen.

</dd> <dt>

<span id="Texture_uploads_"></span><span id="texture_uploads_"></span><span id="TEXTURE_UPLOADS_"></span>**Textur Uploads** 
</dt> <dd>

Das Hochladen von Texturen auf das Gerät beansprucht Bandbreite und verursacht einen Bandbreiten Wettbewerb mit Scheitelpunkt Daten. Daher ist es wichtig, dass Sie sich nicht über den Texturspeicher für den Commit überschreiben, wodurch das zwischen Speicherungs Schema gezwungen wird, übermäßige Mengen von Texturen für jeden Frame

</dd> <dt>

<span id="Vertex_and_index_buffers_"></span><span id="vertex_and_index_buffers_"></span><span id="VERTEX_AND_INDEX_BUFFERS_"></span>**Vertex-und Index Puffer** 
</dt> <dd>

Sie sollten immer Vertex-und Index Puffer verwenden, anstatt nur einfache Blöcke der von der Anwendung belegten Arbeitsspeicher zu verwenden. Die Sperr Semantik für Scheitelpunkt-und Index Puffer kann mindestens einen redundanten Kopiervorgang vermeiden. Bei manchen Treibern kann der Vertex-oder Index Puffer in einem besser optimalen Arbeitsspeicher (vielleicht im Video-oder AGP-Speicher) für den Zugriff durch die Hardware platziert werden.

</dd> <dt>

<span id="State_macro_blocks_"></span><span id="state_macro_blocks_"></span><span id="STATE_MACRO_BLOCKS_"></span>**State-Makroblöcke** 
</dt> <dd>

Diese wurden in DirectX 7,0 eingeführt. Sie stellen einen Mechanismus bereit, mit dem eine Reihe von Zustandsänderungen (einschließlich Beleuchtung, Material und Matrix Änderungen) in einem Makro aufgezeichnet werden können, das dann von einem einzelnen-Befehl wiedergegeben werden kann. Das hat zwei Vorteile:

-   Sie reduzieren den aufrufungsaufwand, indem Sie anstelle von vielen einen einzigen Rückruf erstellen.
-   Ein fähiger Treiber kann die Zustandsänderungen vorab analysieren und vorkompilieren, sodass er viel schneller an die Grafikhardware übermittelt werden kann.

Zustandsänderungen können weiterhin teuer sein, aber durch die Verwendung von Zustands Makros können zumindest einige der Kosten gesenkt werden. Verwenden Sie nur ein einzelnes Direct3D-Gerät. Wenn Sie mehrere Ziele Renderingziele benötigen, verwenden Sie "*". Wenn Sie eine Anwendung mit mehreren 3D-Fenstern erstellen, verwenden Sie die API "kreateadditionalswapchain". Die Laufzeit ist für ein einzelnes Gerät optimiert, und es gibt eine beträchtliche Geschwindigkeit bei der Verwendung mehrerer Geräte.

</dd> </dl> </dd> <dt>

<span id="Which_primitive_types__strips__fans__lists_and_so_on__should_I_use__"></span><span id="which_primitive_types__strips__fans__lists_and_so_on__should_i_use__"></span><span id="WHICH_PRIMITIVE_TYPES__STRIPS__FANS__LISTS_AND_SO_ON__SHOULD_I_USE__"></span>**Welche primitiven Typen (Streifen, Lüfter, Listen usw.) sollte ich verwenden?** 
</dt> <dd>

In den Scheitel Punkten für echte Daten Features, die von mehreren Polygonen gemeinsam genutzt werden, sind viele Netze aufgetreten. Um die Leistung zu maximieren, ist es wünschenswert, die Duplizierung in Vertices zu verringern, die transformiert und über den Bus an das renderinggerät Es ist klar, dass durch die Verwendung einfacher Dreiecks Listen keine Scheitelpunkt Freigabe erzielt wird, sodass Sie die beste Methode ist. Die Auswahl erfolgt dann zwischen der Verwendung von Streifen und Lüfter, die eine bestimmte konnektivitätsbeziehung zwischen Polygonen und der Verwendung indizierter Listen implizieren. Wenn die Daten natürlich in "Streifen" und "Fans" fallen, sind diese die am besten geeignete Wahl, da Sie die an den Treiber gesendeten Daten minimieren. Das Zerlegen von Netzen in Streifen und Lüfter führt jedoch häufig zu einer großen Anzahl separater Teile, was eine große Anzahl von drawprimitiven aufrufen impliziert. Aus diesem Grund besteht die effizienteste Methode in der Regel in der Verwendung eines einzelnen drawindexedprimitiven Aufrufes mit einer Dreiecks Liste. Ein zusätzlicher Vorteil der Verwendung einer indizierten Liste besteht darin, dass ein Vorteil auch dann erzielt werden kann, wenn aufeinander folgende Dreiecke nur einen einzigen Scheitelpunkt gemeinsam verwenden. Zusammengefasst: Wenn Ihre Daten natürlich in große Bänder oder Lüfter fallen, verwenden Sie Bänder oder Lüfter. Verwenden Sie andernfalls indizierte Listen.

</dd> <dt>

<span id="How_do_you_determine_the_total_texture_memory_a_card_has__excluding_AGP_memory__"></span><span id="how_do_you_determine_the_total_texture_memory_a_card_has__excluding_agp_memory__"></span><span id="HOW_DO_YOU_DETERMINE_THE_TOTAL_TEXTURE_MEMORY_A_CARD_HAS__EXCLUDING_AGP_MEMORY__"></span>**Wie bestimmen Sie den gesamten Texturspeicher, der in einer Karte vorhanden ist, ohne den AGP-Speicher?** 
</dt> <dd>

[**IDirect3DDevice9:: getavailabletexturemem**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-getavailabletexturemem) gibt den gesamten verfügbaren Arbeitsspeicher zurück, einschließlich AGP. Die Zuweisung von Ressourcen auf der Grundlage einer Annahme, wie viel Video Arbeitsspeicher Sie haben, ist keine gute Idee. Was ist beispielsweise, wenn die Karte unter einer Unified Memory-Architektur (UMA) ausgeführt wird oder die Texturen komprimiert werden kann? Möglicherweise ist mehr Speicherplatz verfügbar, als Sie vielleicht denken. Erstellen Sie Ressourcen, und suchen Sie nach "nicht genügend Arbeitsspeicher"-Fehlern, und Skalieren Sie Sie dann auf die Texturen zurück. Beispielsweise können Sie die obersten MIP-Ebenen Ihrer Texturen entfernen.

</dd> <dt>

<span id="What_s_a_good_usage_pattern_for_vertex_buffers_if_I_m_generating_dynamic_data__"></span><span id="what_s_a_good_usage_pattern_for_vertex_buffers_if_i_m_generating_dynamic_data__"></span><span id="WHAT_S_A_GOOD_USAGE_PATTERN_FOR_VERTEX_BUFFERS_IF_I_M_GENERATING_DYNAMIC_DATA__"></span>**Was ist ein gutes Verwendungs Muster für Vertex-Puffer, wenn ich dynamische Daten generiere?** 
</dt> <dd>

1.  Erstellen Sie einen Scheitelpunkt Puffer mithilfe der Nutzungs Kennzeichen D3DUSAGE \_ Dynamic und D3DUSAGE \_ schreibonly und des \_ standardpoolflags D3DPOOL. (Geben Sie auch D3DUSAGE \_ an. Software processing bei Verwendung der Verarbeitung von Software Scheitel Punkten.)
2.  I = 0.
3.  Legen Sie State (Texturen, renderstates usw.) fest.
4.  Überprüfen Sie, ob im Pufferspeicher Platz vorhanden ist, z. b. I + M <= N? (Wobei M die Anzahl der neuen Scheitel Punkte ist).
5.  Wenn ja, Sperren Sie VB mit D3DLOCK \_ noüberschreibung. Dies weist Direct3D und den Treiber an, dass Sie Scheitel Punkte hinzufügen werden und nicht die Änderungen ändern, die Sie zuvor im Batch verarbeitet haben. Daher wird ein DMA-Vorgang nicht unterbrochen, wenn ein DMA-Vorgang ausgeführt wurde. Wenn Nein, gehe zu 11.
6.  Füllen Sie die M-Scheitel Punkte bei I aus.
7.  Entsperren.
8.  Aufrufen von \[ indizierten \] primitiven zeichnen. Verwenden Sie für nicht indizierte primitive I als startVertex-Parameter. Stellen Sie für indizierte primitive sicher, dass die Indizes auf den richtigen Teil des Vertexpuffers zeigen (es ist möglicherweise am einfachsten, den basevertexindex-Parameter des setindexes-Aufrufs zu verwenden, um dies zu erreichen).
9.  I + = M.
10. Gehe zu 3.
11. OK, das ist nicht genügend Speicherplatz. wir beginnen mit einem neuen VB. Wir möchten nicht dieselbe verwenden, da möglicherweise ein DMA-Vorgang ausgeführt wird. Wir kommunizieren mit diesem Direct3D und dem Treiber, indem wir denselben VB mit dem D3DLOCK \_ DISCARD-Flag sperren. Dies bedeutet, dass Sie einen neuen Zeiger erhalten können, da ich mit dem alten und nicht wirklich auf den alten Inhalt achten muss. "
12. I = 0.
13. Gehe zu 4 (oder 6).

</dd> <dt>

<span id="Why_do_I_have_to_specify_more_information_in_the_D3DVERTEXELEMENT9_structure__"></span><span id="why_do_i_have_to_specify_more_information_in_the_d3dvertexelement9_structure__"></span><span id="WHY_DO_I_HAVE_TO_SPECIFY_MORE_INFORMATION_IN_THE_D3DVERTEXELEMENT9_STRUCTURE__"></span>**Warum muss ich weitere Informationen in der D3DVERTEXELEMENT9-Struktur angeben?** 
</dt> <dd>

Ab Direct3D 9 ist die vertexstreamdeklaration nicht mehr nur ein DWORD-Array, sondern ist nun ein Array von D3DVERTEXELEMENT9-Strukturen. Die Common Language Runtime verwendet die zusätzlichen Semantik und Verwendungs Informationen, um den Inhalt der vertexstreams an Vertex-Shader-Eingabe Register/-Variablen zu binden. Bei Direct3D 9 sind Scheitelpunkt Deklarationen von Vertex-Shadern entkoppelt. dadurch ist es einfacher, Shader mit Geometrien verschiedener Formate zu verwenden, da die Laufzeit nur die Daten bindet, die der Shader benötigt.

Die neuen Vertex-Deklarationen können entweder mit der Fixed-Funktions Pipeline oder mit Shadern verwendet werden. Bei der Fixed-Funktions Pipeline ist das Aufrufen von setvertexshader nicht erforderlich. Wenn Sie jedoch zur Fixed-Funktions Pipeline wechseln und zuvor einen Vertex-Shader verwendet haben, nennen Sie setvertexshader (null). Wenn dies der Fall ist, müssen Sie auch setfvf aufrufen, um den FVF-Code zu deklarieren.

Beim Verwenden von Vertex-Shadern wird setvertexshader mit dem Vertex-Shader-Objekt aufgerufen. Außerdem wird setfvf aufgerufen, um eine Scheitelpunkt Deklaration einzurichten. Dabei werden die Informationen verwendet, die in der "f" implizit sind. Setvertexdeclaration kann anstelle von setfvf aufgerufen werden, da Sie Scheitelpunkt Deklarationen unterstützt, die nicht mit einer FVF ausgedrückt werden können.

</dd> </dl>

### <a name="d3dx-utility-library"></a>D3DX-Hilfsprogrammbibliothek

<dl> <dt>

<span id="What_file_formats_are_supported_by_the_D3DX_image_file_loader_functions__"></span><span id="what_file_formats_are_supported_by_the_d3dx_image_file_loader_functions__"></span><span id="WHAT_FILE_FORMATS_ARE_SUPPORTED_BY_THE_D3DX_IMAGE_FILE_LOADER_FUNCTIONS__"></span>**Welche Dateiformate werden von den D3DX-Bild Datei Ladefunktionen unterstützt?** 
</dt> <dd>

Die D3DX-Abbild Datei-Lade Programmfunktionen unterstützen BMP, TGA, JPG, DIB, ppm und DDS-Dateien.

</dd> <dt>

<span id="The_text_rendering_functions_in_D3DX_don_t_seem_to_work__what_am_I_doing_wrong__"></span><span id="the_text_rendering_functions_in_d3dx_don_t_seem_to_work__what_am_i_doing_wrong__"></span><span id="THE_TEXT_RENDERING_FUNCTIONS_IN_D3DX_DON_T_SEEM_TO_WORK__WHAT_AM_I_DOING_WRONG__"></span>**Die textrenderingfunktionen in D3DX scheinen nicht zu funktionieren. Was kann ich falsch tun?** 
</dt> <dd>

Ein häufiger Fehler bei der Verwendung der ID3DXFont::D rawtext-Funktionen ist die Angabe einer Alpha-Komponente (null) für den Color-Parameter. Dies führt zu einem vollständig transparenten (d. h. unsichtbar) Text. Stellen Sie bei vollständig undurchsichtigem textsicher, dass die Alpha Komponente des Color-Parameters vollständig ausgelastet ist (255).

</dd> <dt>

<span id="How_can_I_save_the_contents_of_a_surface_or_texture_to_a_file__"></span><span id="how_can_i_save_the_contents_of_a_surface_or_texture_to_a_file__"></span><span id="HOW_CAN_I_SAVE_THE_CONTENTS_OF_A_SURFACE_OR_TEXTURE_TO_A_FILE__"></span>**Wie kann ich den Inhalt einer Oberfläche oder Textur in einer Datei speichern?** 
</dt> <dd>

Das DirectX 8,1 SDK hat zwei Funktionen zur D3DX-Bibliothek hinzugefügt, speziell für diesen Zweck: D3DXSaveSurfaceToFile () und D3DXSaveTextureToFile (). Diese Funktionen unterstützen das Speichern eines Bilds in einer Datei im BMP-oder DDS-Format. In früheren Versionen müssen Sie die Oberfläche Sperren und die Bilddaten lesen und dann in eine Bitmapdatei schreiben. Informationen zum Schreiben einer Funktion zum Speichern von Bitmaps finden Sie unter [Speichern eines Bilds](/windows/desktop/gdi/storing-an-image).

Alternativ könnte GDI+ verwendet werden, um das Bild in einer Vielzahl von Formaten zu speichern. hierfür sind jedoch zusätzliche Unterstützungs Dateien erforderlich, die mit der Anwendung verteilt werden müssen.

</dd> <dt>

<span id="How_can_I_make_use_of_the_High_Level_Shader_Language__HLSL__in_my_game__"></span><span id="how_can_i_make_use_of_the_high_level_shader_language__hlsl__in_my_game__"></span><span id="HOW_CAN_I_MAKE_USE_OF_THE_HIGH_LEVEL_SHADER_LANGUAGE__HLSL__IN_MY_GAME__"></span>**Wie kann ich die High Level Shader Language (HLSL) in meinem Spiel verwenden?** 
</dt> <dd>

Es gibt drei Möglichkeiten, wie Sie die Microsoft High Level Shader Language (HLSL) in Ihre Game-Engine integrieren können:

-   Kompilieren Sie Ihre Shader-Quelle in eine Scheitelpunkt-oder Pixel Schattierungs Assembly (über das Befehlszeilen-Hilfsprogramm fxc.exe), und verwenden Sie D3DXAssembleShader () zur Laufzeit. Auf diese Weise kann sogar ein DirectX 8-Spiel die Leistungsfähigkeit von HLSL nutzen.
-   Verwenden Sie D3DXCompileShader (), um die Shader-Quelle in den Tokenstream und das Konstante Tabellen Formular zu kompilieren. Laden Sie zur Laufzeit den Tokenstream und die Konstante Tabelle, und rufen Sie auf dem Gerät "", um die Shader zu erstellen.
-   Die einfachste Möglichkeit zum Einrichten und Ausführen von besteht darin, das D3DX Effects-System durch Aufrufen von D3DXCreateEffectFromFile () oder D3DXCreateEffectFromResource () mit ihrer Wirkungs Datei zu nutzen.

</dd> <dt>

<span id="What_is_the_purpose_of_the_new_shader_compiler_flag__"></span><span id="what_is_the_purpose_of_the_new_shader_compiler_flag__"></span><span id="WHAT_IS_THE_PURPOSE_OF_THE_NEW_SHADER_COMPILER_FLAG__"></span>**Wozu dient das neue Shader-Compilerflag?** 
</dt> <dd>

Ab dem DirectX SDK vom Dezember 2006 wurde der neue HLSL-Compiler, der für Direct3D 10 entwickelt wurde, für Direct3D 9-Ziele aktiviert. Der neue Compiler unterstützt keine PS \_ 1 \_ x-Ziele und ist nun der Standard Compiler für alle Direct3D HLSL-Shader. Ein Flag für die Abwärtskompatibilität kann verwendet werden, um zu erzwingen, dass PS \_ 1 \_ x-Ziele als PS \_ 2 0-Ziele kompiliert werden \_ .

Anwendungen, die den Legacy Compiler verwenden möchten, können dies weiterhin tun, indem Sie zur Laufzeit ein Flag bereitstellen (siehe [**Compilerflags**](/windows/desktop/direct3d9/d3dxshader-flags)), oder indem Sie bei der Verwendung von FXC einen Switch angeben.

</dd> <dt>

<span id="What_is_the_correct_way_to_get_shaders_from_an_Effect__"></span><span id="what_is_the_correct_way_to_get_shaders_from_an_effect__"></span><span id="WHAT_IS_THE_CORRECT_WAY_TO_GET_SHADERS_FROM_AN_EFFECT__"></span>**Was ist die richtige Methode, um Shader von einem Effekt zu erhalten?** 
</dt> <dd>

Verwenden Sie D3DXCreateEffect, um eine ID3DXEffect zu erstellen, und verwenden Sie dann getpassdebug zum Abrufen eines D3DXPASS- \_ abgebers. Diese Struktur enthält Zeiger auf den Scheitelpunkt und die Pixel-Shader.

Verwenden Sie ID3DXEffectCompiler:: getpassde nicht. Von dieser Methode zurückgegebene Scheitelpunkt-und Pixel-Shader-Handles sind NULL.

</dd> <dt>

<span id="What_is_the_HLSL_noise___intrinsic_for__"></span><span id="what_is_the_hlsl_noise___intrinsic_for__"></span><span id="WHAT_IS_THE_HLSL_NOISE___INTRINSIC_FOR__"></span>**Wofür ist das HLSL-Rauschen () intrinsisch?** 
</dt> <dd>

Die intrinsische Rausch Funktion generiert Perlin-Rauschen, wie von Ken Perlin definiert. Die HLSL-Funktion kann derzeit nur zum Auffüllen von Texturen in Textur-Shadern verwendet werden, da die aktuelle h/w die Methode nicht nativ unterstützt. Textur-Shader werden bei der kontexturierung mit den D3DXFill \* Texture ()-Funktionen verwendet, die nützliche Hilfsfunktionen sind, um während der Ladezeit prozedurale definierte Texturen zu generieren.

</dd> <dt>

<span id="How_do_I_detect_whether_to_use_pixel_shader_model_2.0_or_2.a__"></span><span id="how_do_i_detect_whether_to_use_pixel_shader_model_2.0_or_2.a__"></span><span id="HOW_DO_I_DETECT_WHETHER_TO_USE_PIXEL_SHADER_MODEL_2.0_OR_2.A__"></span>**Gewusst wie erkennen, ob das Pixel Shader-Modell 2,0 oder 2. a verwendet werden soll?** 
</dt> <dd>

Sie können die Funktionen D3DXGetPixelShaderProfile () und D3DXGetPixelShaderProfile () verwenden, die eine Zeichenfolge zurückgeben, die festlegt, welches HLSL-Profil am besten für das ausgeführte Gerät geeignet ist.

</dd> <dt>

<span id="How_do_I_access_the_Parameters_in_my_Precompiled_Effects_Shaders__"></span><span id="how_do_i_access_the_parameters_in_my_precompiled_effects_shaders__"></span><span id="HOW_DO_I_ACCESS_THE_PARAMETERS_IN_MY_PRECOMPILED_EFFECTS_SHADERS__"></span>**Gewusst wie auf die Parameter in meinen vorkompilierten Effekten-Shadern zugreifen?** 
</dt> <dd>

Über die ID3DXConstantTable-Schnittstelle, die verwendet wird, um auf die Konstante Tabelle zuzugreifen. Diese Tabelle enthält die Variablen, die von den sprach-Shadern und-Effekten auf hoher Ebene verwendet werden.

</dd> <dt>

<span id="Is_there_a_way_to_add_user_data_to_an_effect_or_other_resource__"></span><span id="is_there_a_way_to_add_user_data_to_an_effect_or_other_resource__"></span><span id="IS_THERE_A_WAY_TO_ADD_USER_DATA_TO_AN_EFFECT_OR_OTHER_RESOURCE__"></span>**Gibt es eine Möglichkeit, Benutzerdaten einem Effekt oder einer anderen Ressource hinzuzufügen?** 
</dt> <dd>

Ja, um private Daten festzulegen, rufen Sie setprivatedata auf (preal ist das D3D Texture-Objekt, pspoof ist das umschließende Textur Objekt).

``` syntax
hr = pReal->SetPrivateData(IID_Spoof, &pSpoof, 
            sizeof(IDirect3DResource9*), 0)));
```

So suchen Sie den umschließenen Zeiger:

``` syntax
    IDirect3DResource9* pSpoof;
    DWORD dwSize = sizeof(pSpoof);
    hr = pReal->GetPrivateData(IID_Spoof, (void*) &pSpoof, &dwSize);
```

</dd> <dt>

<span id="Why_does_rendering_of_an_ID3DXMesh_object_slow_down_significantly_after_I_define_subsets__"></span><span id="why_does_rendering_of_an_id3dxmesh_object_slow_down_significantly_after_i_define_subsets__"></span><span id="WHY_DOES_RENDERING_OF_AN_ID3DXMESH_OBJECT_SLOW_DOWN_SIGNIFICANTLY_AFTER_I_DEFINE_SUBSETS__"></span>**Warum wird das Rendern eines ID3DXMesh-Objekts nach dem Definieren von Teilmengen erheblich verlangsamt?** 
</dt> <dd>

Sie haben das Mesh wahrscheinlich nicht optimiert, nachdem die Gesichts Attribute definiert wurden. Wenn Sie Attribute angeben und dann ID3DXMesh::D rawsubset () aufzurufen, muss diese Methode eine Suche des Netzes für alle Gesichter durchführen, die die angeforderten Attribute enthalten. Außerdem sind die gerenderten Gesichter wahrscheinlich in einem zufälligen Zugriffsmuster, sodass der Scheitelpunkt Cache nicht genutzt wird. Nachdem Sie die Gesichts Attribute für Ihre Teilmengen definiert haben, müssen Sie die Methoden ID3DXMesh:: Optimization oder ID3DXMesh:: OptimizeInPlace und eine Optimierungsmethode von D3DXMESHOPT \_ attrsort oder eine stärkere Methode angeben. Beachten Sie, dass Sie für eine optimale Leistung die Optimierung mit dem D3DXMESHOPT \_ vertexcache-Flag durchführt, das auch die Scheitel Punkte für die optimale vertexcache-Auslastung neu anordnen. Das für ein D3DX-Mesh generierte "faceency"-Array hat drei Einträge pro Gesicht, aber einige Gesichter haben möglicherweise keine angrenzenden Gesichter an allen drei Kanten. Wie wird diese codiert? Einträge, bei denen keine angrenzenden Gesichter vorhanden sind, werden als 0xffffffff codiert.

</dd> <dt>

<span id="I_ve_heard_a_lot_about_Pre-computed_Radiance_Transfer__PRT___where_can_I_learn_more__"></span><span id="i_ve_heard_a_lot_about_pre-computed_radiance_transfer__prt___where_can_i_learn_more__"></span><span id="I_VE_HEARD_A_LOT_ABOUT_PRE-COMPUTED_RADIANCE_TRANSFER__PRT___WHERE_CAN_I_LEARN_MORE__"></span>**Ich habe viel über die vorab berechnete Strahlen Übertragung (PRT) gehört. wo kann ich mehr erfahren?** 
</dt> <dd>

PRT ist ein neues Feature von D3DX, das im SDK-Update für den Sommer 2003 hinzugefügt wurde. Sie ermöglicht das Rendering komplexer Beleuchtungsszenarien, wie z. b. globale lluminierung, weiche shadoinieren und untergeordnete Oberflächen Punkte in Echtzeit. Das SDK enthält Dokumentation und Beispiele dazu, wie Sie die Technologie in Ihr Spiel integrieren können. Die Beispiel Beispiele PRT Demo Sample und localdebuformableprt veranschaulichen die Verwendung des Simulators für pro Scheitelpunkt-bzw. Pixel Beleuchtungs Szenarios. Weitere Informationen zu diesem und anderen Themen finden Sie auch auf der Webseite von Peter Pike Sloan.

</dd> <dt>

<span id="How_can_I_render_to_a_texture_and_make_use_of_Anti_Aliasing__"></span><span id="how_can_i_render_to_a_texture_and_make_use_of_anti_aliasing__"></span><span id="HOW_CAN_I_RENDER_TO_A_TEXTURE_AND_MAKE_USE_OF_ANTI_ALIASING__"></span>**Wie kann ich eine Textur in eine Textur darstellen und Antialiasing verwenden?** 
</dt> <dd>

Erstellen Sie ein Multisampling-Renderziel mithilfe von Direct3DDevice9:: dashaterendertarget. Nachdem die Szene in dieses Renderziel gerendert wurde, wird Sie von der Szene in eine renderzieltextur kopiert. Wenn Sie Änderungen an der Offscreen-Textem vornehmen (z. b. ein-oder Wiederherstellung), kopieren Sie Sie zurück in den Hintergrund Puffer, bevor Sie ().

</dd> </dl>

## <a name="directsound-questions"></a>Fragen zu DirectSound

<dl> <dt>

<span id="Why_do_I_get_a_burst_of_static_when_my_application_starts_up__I_notice_this_problem_with_other_applications_too._"></span><span id="why_do_i_get_a_burst_of_static_when_my_application_starts_up__i_notice_this_problem_with_other_applications_too._"></span><span id="WHY_DO_I_GET_A_BURST_OF_STATIC_WHEN_MY_APPLICATION_STARTS_UP__I_NOTICE_THIS_PROBLEM_WITH_OTHER_APPLICATIONS_TOO._"></span>**Warum erhalte ich einen Burst, wenn meine Anwendung gestartet wird? Dieses Problem ist auch bei anderen Anwendungen zu erkennen.** 
</dt> <dd>

Sie haben wahrscheinlich die Debugversion DirectX-Laufzeit installiert. Die Debugversion der Laufzeit füllt Puffer mit statischer Reihenfolge aus, um Entwicklern beim Abfangen von Fehlern mit nicht initialisierten Puffern zu helfen. Der Inhalt eines DirectSound-Puffers kann nach der Erstellung nicht garantiert werden. insbesondere können Sie nicht davon ausgehen, dass ein Puffer mit nulgerout ist.

</dd> <dt>

<span id="Why_I_am_experiencing_a_delay_in_between_changing_an_effects_parameters_and_hearing_the_results__"></span><span id="why_i_am_experiencing_a_delay_in_between_changing_an_effects_parameters_and_hearing_the_results__"></span><span id="WHY_I_AM_EXPERIENCING_A_DELAY_IN_BETWEEN_CHANGING_AN_EFFECTS_PARAMETERS_AND_HEARING_THE_RESULTS__"></span>**Warum kommt es zu einer Verzögerung zwischen dem Ändern von Effekt Parametern und dem hören der Ergebnisse?** 
</dt> <dd>

Änderungen an den Effekt Parametern werden nicht immer sofort in DirectX 8 durchgeführt. Aus Effizienzgründen verarbeitet DirectSound in einem Puffer, beginnend mit dem Wiedergabe Cursor, 100 Millisekunden für Audiodaten, bevor der Puffer wiedergegeben wird. Diese Vorverarbeitung erfolgt nach allen folgenden aufrufen:

``` syntax
IDirectSoundBuffer8::SetCurrentPosition
IDirectSoundBuffer8::SetFX
IDirectSoundBuffer8::Stop
IDirectSoundBuffer8::Unlock
```

Seit DirectX 9 behandelt ein neuer FX-Verarbeitungs Algorithmus, der die Auswirkungen Just-in-Time verarbeitet, dieses Problem und hat die Latenz reduziert. Der Algorithmus wurde dem IDirectSoundBuffer8::P Lay ()-aufrufsamt einem zusätzlichen Thread hinzugefügt, der die Auswirkungen direkt vor dem Schreib Cursor verarbeitet. Sie können Parameter jederzeit festlegen und funktionieren wie erwartet. Beachten Sie jedoch, dass es bei einem Spiel Puffer zu einer geringfügigen Verzögerung (in der Regel 100 ms) kommt, bevor Sie die Parameter Änderung hören, da das Audiogerät zwischen den Play-und Write-Cursorn (und etwas mehr Auffüll Zeichen) zu diesem Zeitpunkt bereits verarbeitet wurde.

</dd> <dt>

<span id="How_do_I_detect_if_DSound_is_installed__"></span><span id="how_do_i_detect_if_dsound_is_installed__"></span><span id="HOW_DO_I_DETECT_IF_DSOUND_IS_INSTALLED__"></span>**Gewusst wie erkennen, ob DSound installiert ist?** 
</dt> <dd>

Wenn Sie "directsoundenumerate ()" nicht zum Auflisten der verfügbaren DSound-Geräte verwenden müssen, verknüpfen Sie Ihre Anwendung nicht mit "DSound. lib", und verwenden Sie Sie stattdessen über "coms cokreateinstance" (CLSID \_ DirectSound...), und initialisieren Sie das DSound-Objekt mithilfe von initialisieren (null) Wenn Sie directsoundenumerate () verwenden müssen, können Sie dsound.dll mithilfe von LoadLibrary ("dsound.dll") dynamisch laden. und greifen mithilfe von GetProcAddress ("directsoundenenumeratea/w") und GetProcAddress ("directsoundkreatea/W") und so weiter auf die zugehörigen Methoden zu.

</dd> <dt>

<span id="How_do_I_create_multichannel_audio_with_WAVEFORMATEXTENSIBLE__"></span><span id="how_do_i_create_multichannel_audio_with_waveformatextensible__"></span><span id="HOW_DO_I_CREATE_MULTICHANNEL_AUDIO_WITH_WAVEFORMATEXTENSIBLE__"></span>**Gewusst wie Sie Multichannel-Audiodaten mit WAVEFORMATEXTENSIBLE erstellen?** 
</dt> <dd>

Wenn Sie in den DirectSound-Hilfedateien keine Antwort auf Ihre Frage finden, gibt es einen guten Artikel mit weiteren Informationen, die bei mehreren channelaudiodaten und wellendateien verfügbar sind.

</dd> <dt>

<span id="How_can_I_use_the_DirectSound_Voice_Manager_with_property_sets_like_EAX__"></span><span id="how_can_i_use_the_directsound_voice_manager_with_property_sets_like_eax__"></span><span id="HOW_CAN_I_USE_THE_DIRECTSOUND_VOICE_MANAGER_WITH_PROPERTY_SETS_LIKE_EAX__"></span>**Wie kann ich den DirectSound Voice Manager mit Eigenschafts Sätzen wie EAX verwenden?** 
</dt> <dd>

Wenn Sie in DirectSound 9,0 einen Puffer duplizieren, ist es jetzt möglich, die IDirectSoundBuffer8-Schnittstelle für den doppelten Puffer zu erhalten, wodurch Sie Zugriff auf die Methode "acquirieresources" erhalten. Auf diese Weise können Sie dem dsbcaps locverzögerungs- \_ Flag einen Puffer mit einer Hardware Ressource zuordnen. Anschließend können Sie die EAX-Parameter für diesen Puffer festlegen, bevor Sie Play () aufrufen müssen.

</dd> <dt>

<span id="I_am_having_problems_with_unreliable_behavior_when_using_cursor_position_notifications._How_can_I_get_more_accurate_information__"></span><span id="i_am_having_problems_with_unreliable_behavior_when_using_cursor_position_notifications._how_can_i_get_more_accurate_information__"></span><span id="I_AM_HAVING_PROBLEMS_WITH_UNRELIABLE_BEHAVIOR_WHEN_USING_CURSOR_POSITION_NOTIFICATIONS._HOW_CAN_I_GET_MORE_ACCURATE_INFORMATION__"></span>**Bei der Verwendung von Cursor Positions Benachrichtigungen treten Probleme mit unzuverlässigem Verhalten auf. Wie kann ich genauere Informationen erhalten?** 
</dt> <dd>

Es gibt einige feine Fehler in verschiedenen Versionen von DirectSound, den Windows-kernaudiostapel und Audiotreiber, die Cursor Positions Benachrichtigungen unzuverlässig machen. Wenn Sie nicht auf eine bekannte HW/SW-Konfiguration abzielen, bei der Sie wissen, dass die Benachrichtigungen sich gut Verhalten, sollten Sie keine Cursor Positions Benachrichtigungen vermeiden. Bei der Positionsverfolgung ist GetCurrentPosition () ein sicheres Verfahren.

</dd> <dt>

<span id="I_am_suffering_from_performance_degradation_when_using_GetCurrentPosition__._What_can_I_do_to_improve_performance__"></span><span id="i_am_suffering_from_performance_degradation_when_using_getcurrentposition__._what_can_i_do_to_improve_performance__"></span><span id="I_AM_SUFFERING_FROM_PERFORMANCE_DEGRADATION_WHEN_USING_GETCURRENTPOSITION__._WHAT_CAN_I_DO_TO_IMPROVE_PERFORMANCE__"></span>**Bei der Verwendung von GetCurrentPosition () treten Leistungseinbußen auf. Was kann ich tun, um die Leistung zu verbessern?** 
</dt> <dd>

Jeder GetCurrentPosition ()-Aufruf für jeden Puffer verursacht einen Systemaufruf, und Systemaufrufe sollten minimiert werden, da es sich um eine große Komponente der CPU-Auslastung von DSound handelt. In NT (Win2K und XP) werden die Cursor in SW-Puffer (und die HW-Puffer auf einigen Geräten) in Schritten von 10 MS verschoben, sodass der Aufruf von GetCurrentPosition () alle 10 MS ideal ist. Ein häufiger Aufruf als alle 5 ms führt zu Leistungseinbußen.

</dd> <dt>

<span id="My_DirectSound_application_is_taking_up_too_much_CPU_time_or_is_performing_slowly._Is_there_anything_I_can_do_to_optimize_my_code__"></span><span id="my_directsound_application_is_taking_up_too_much_cpu_time_or_is_performing_slowly._is_there_anything_i_can_do_to_optimize_my_code__"></span><span id="MY_DIRECTSOUND_APPLICATION_IS_TAKING_UP_TOO_MUCH_CPU_TIME_OR_IS_PERFORMING_SLOWLY._IS_THERE_ANYTHING_I_CAN_DO_TO_OPTIMIZE_MY_CODE__"></span>**Meine DirectSound-Anwendung nimmt zu viel CPU-Zeit in Anspruch oder dauert langsam. Gibt es etwas, was ich tun kann, um den Code zu optimieren?** 
</dt> <dd>

Es gibt mehrere Möglichkeiten, die Leistung Ihres AudioCodes zu verbessern:

-   Nennen Sie GetCurrentPosition nicht zu oft. Jeder GetCurrentPosition ()-Aufruf für jeden Puffer verursacht einen Systemaufruf, und Systemaufrufe sollten minimiert werden, da es sich um eine große Komponente der CPU-Auslastung von DSound handelt. In NT (Win2K und XP) werden die Cursor in SW-Puffer (und die HW-Puffer auf einigen Geräten) in Schritten von 10 MS verschoben, sodass der Aufruf von GetCurrentPosition () alle 10 MS ideal ist. Ein häufiger Aufruf als alle 5 ms führt zu einer Leistungsminderung.
-   Verwenden Sie eine separate, niedrigere Framerate für Audiodaten. Heutzutage können viele Windows-Spiele 100 Frames pro Sekunde überschreiten. in den meisten Fällen ist es nicht erforderlich, die 3D-Audioparameter mit der gleichen Framerate zu aktualisieren. Wenn Sie Ihre Audiodaten mit jedem zweiten oder dritten Grafik Rahmen oder mit jeweils 30 ms verarbeiten, kann die Anzahl von audioaufrufen in der gesamten Anwendung erheblich reduziert werden, ohne die Audioqualität zu verringern.
-   Verwenden Sie DS3D verzögert \_ für 3D-Objekte. Die meisten Soundkarten reagieren sofort auf Parameteränderungen, und in einem einzelnen Frame können sich viele Änderungen ändern, insbesondere dann, wenn Sie die Position oder Ausrichtung des listenerers ändern. Dies bewirkt, dass die Soundkarte/CPU viele unnötige Berechnungen durchführt. eine weitere schnelle und universelle Optimierung besteht darin, einige Parameteränderungen abzuschieben und am Ende des Frames einen Commit auszuführen.

    oder verwenden Sie zumindest setallparameters anstelle einzelner Set3DParamX-Aufrufe für Puffer.

    Ebenso sollten Sie mindestens den Aufruf von setallparamenter-aufrufen für 3D-Puffer anstelle der einzelnen Set3DParamX-Aufrufe verwenden. Versuchen Sie einfach, Systemaufrufe möglichst gering zu halten.

-   Keine redundanten Aufrufe vornehmen; Speichern und sortieren Sie eine Liste von Wiedergabe aufrufen. Häufig gibt es in einem audioaktualisierungs Rahmen zwei Anforderungen, neue Sounds wiederzugeben. Wenn die Anforderungen beim Eintreffen verarbeitet werden, könnte der erste neue Sound gestartet werden und dann den zweiten angeforderten Sound sofort ersetzen. Dies ergibt redundante Berechnungen, einen unnötigen Wiedergabe Aufrufvorgang und einen unnötigen halte Vorgang. Es empfiehlt sich, eine Liste von Anforderungen zu speichern, damit neue Sounds wiedergegeben werden können, sodass die Liste sortiert werden kann, und nur die Stimmen, die abgespielt werden sollten, werden tatsächlich wiedergegeben.

    Außerdem sollten Sie lokale Kopien der 3D-und EAX-Parameter für jede Audioquelle speichern. Wenn eine Anforderung zum Festlegen eines Parameters auf einen bestimmten Wert erstellt wird, können Sie überprüfen, ob sich der Wert tatsächlich vom letzten festgelegten Wert unterscheidet. Wenn dies nicht der Fall ist, muss der-Befehl nicht durchgeführt werden.

    Obwohl der Soundkartentreiber dieses Szenario wahrscheinlich erkennt und die (gleiche) Berechnung nicht erneut durchführt, muss der audiobefehl den Audiotreiber (über einen Ring Übergang) erreichen, und dies ist bereits ein langsamer Vorgang.

</dd> <dt>

<span id="When_I_stream_a_buffer_it_tends_to_glitch_and_perform_poorly._What_s_the_best_way_to_stream_a_buffer__"></span><span id="when_i_stream_a_buffer_it_tends_to_glitch_and_perform_poorly._what_s_the_best_way_to_stream_a_buffer__"></span><span id="WHEN_I_STREAM_A_BUFFER_IT_TENDS_TO_GLITCH_AND_PERFORM_POORLY._WHAT_S_THE_BEST_WAY_TO_STREAM_A_BUFFER__"></span>**Wenn ein Puffer gestreamt wird, wird der Vorgang tendenziell nicht ordnungsgemäß durchgeführt. Was ist die beste Möglichkeit zum Streamen eines Puffers?** 
</dt> <dd>

Beim Streaming von Audiodaten in einen Puffer gibt es zwei grundlegende Algorithmen: After-Write-Cursor (AWC) und before-Play-Cursor (BPC). AWC minimiert die Latenz zu den Kosten für das glitchen, während bpc das Gegenteil ist. Da es in der Regel keine interaktiven Änderungen am Streaming gibt, ist diese Art der Latenz selten ein Problem für Spiele und ähnliche Anwendungen. Daher ist bpc der geeignetere Algorithmus. In AWC können Sie bei jedem Ausführen Ihres streamingthreads die Daten in den Schleifen Puffern bis zu N MS über die Schreib Cursor hinaus (in der Regel n = 40 oder so, um Windows-Planungs Jitter zu ermöglichen). In bpc schreiben Sie immer so viele Daten wie möglich in die Puffer und füllen Sie mit ihren Wiedergabe Cursorn (oder möglicherweise 32 Bytes vor, um Treiber zu unterbinden, die den Wiedergabe Cursor nicht ordnungsgemäß melden).

Verwenden Sie bpc, um das Durchführen von Daten zu imitieren, und verwenden Sie Puffer, die 100 MS oder größer sind, auch wenn Ihre Spiele nicht auf der Testhardware unterwegs sind, sondern auf einem Computer.

</dd> <dt>

<span id="I_am_playing_the_same_sounds_over_and_over_very_often_and_very_quickly_and_sometimes_they_don_t_play_properly__or_the_Play___call_takes_a_long_time._What_should_I_do__"></span><span id="i_am_playing_the_same_sounds_over_and_over_very_often_and_very_quickly_and_sometimes_they_don_t_play_properly__or_the_play___call_takes_a_long_time._what_should_i_do__"></span><span id="I_AM_PLAYING_THE_SAME_SOUNDS_OVER_AND_OVER_VERY_OFTEN_AND_VERY_QUICKLY_AND_SOMETIMES_THEY_DON_T_PLAY_PROPERLY__OR_THE_PLAY___CALL_TAKES_A_LONG_TIME._WHAT_SHOULD_I_DO__"></span>**Ich werde dieselben Sounds häufig und sehr schnell wiedergeben, und manchmal werden Sie nicht ordnungsgemäß abgespielt, oder der Play ()-Aufruf dauert sehr lange. Was soll ich tun?** 
</dt> <dd>

Die Start Latenz (unterscheidet sich von der oben erwähnten streaminginglatenz) kann im Fall einiger Hardware ein Problem sein (der Play ()-Aufruf dauert manchmal einige Zeit auf bestimmten Soundkarten). Wenn Sie diese Latenz wirklich verringern möchten, sollten Sie für Twitch-Sounds (Schuss-, hinterbrechungs-und so weiter) sorgen, dass einige Puffer immer Schleifen und wiedergeben. Wenn Sie einen Twitch-Sound wiedergeben müssen, wählen Sie einen freien Puffer aus, sehen Sie sich an, wo sein Schreib Cursor ist, und fügen Sie den Sound direkt hinter dem Schreib Cursor in den Puffer ein. Bei einigen Soundkarten tritt beim querysupport für verzögerte Eigenschaften, die von mir unterstützt werden, Fehler auf. Gibt es eine Problem Umgehung? Sie können einfach querysupport für die nicht verzögerten Versionen der Eigenschaften verwenden und verzögerte Einstellungen trotzdem verwenden. Das Problem kann auch durch die neuesten Treiber für Treiber behoben werden.

</dd> <dt>

<span id="How_do_I_encode_WAV_files_into_WMA__"></span><span id="how_do_i_encode_wav_files_into_wma__"></span><span id="HOW_DO_I_ENCODE_WAV_FILES_INTO_WMA__"></span>**Gewusst wie WAV-Dateien in WMA codieren?** 
</dt> <dd>

Weitere Informationen finden Sie in der Dokumentation zum Windows Media Encoder unter: Windows Media Encoder 9-Serie.

</dd> <dt>

<span id="How_do_I_decode_MP3_files_with_DirectSound__"></span><span id="how_do_i_decode_mp3_files_with_directsound__"></span><span id="HOW_DO_I_DECODE_MP3_FILES_WITH_DIRECTSOUND__"></span>**Gewusst wie Sie die Decodierung von MP3-Dateien mit DirectSound?** 
</dt> <dd>

DirectSound unterstützt die MP3-Decodierung nicht nativ. Sie können die Dateien im voraus selbst decodieren (mit einem ACM-Codec eines DirectShow-Filters), oder Sie können nur DirectShow selbst verwenden, was die Decodierung für Sie ausführen kann. Anschließend können Sie die resultierenden PCM-Audiodaten in Ihre DirectSound-Puffer kopieren.

</dd> </dl>

## <a name="directx-extensions-for-alias-maya"></a>DirectX-Erweiterungen für Alias Maya

<dl> <dt>

<span id="Why_aren_t_my_NURBS_showing_up__"></span><span id="why_aren_t_my_nurbs_showing_up__"></span><span id="WHY_AREN_T_MY_NURBS_SHOWING_UP__"></span>**Warum werden meine nursb nicht angezeigt?** 
</dt> <dd>

Nursb werden nicht unterstützt. Sie können Sie in Polygon-Meshes konvertieren.

</dd> <dt>

<span id="Why_aren_t_my_SUBDs_showing_up_"></span><span id="why_aren_t_my_subds_showing_up_"></span><span id="WHY_AREN_T_MY_SUBDS_SHOWING_UP_"></span>**Warum werden meine subds nicht angezeigt?**
</dt> <dd>

Subds werden nicht unterstützt. Sie können Sie in Polygon-Meshes konvertieren.

</dd> <dt>

<span id="Why_does_my_animation_in_the_X_file_look_different_than_the_animation_in_the_preview_window__"></span><span id="why_does_my_animation_in_the_x_file_look_different_than_the_animation_in_the_preview_window__"></span><span id="WHY_DOES_MY_ANIMATION_IN_THE_X_FILE_LOOK_DIFFERENT_THAN_THE_ANIMATION_IN_THE_PREVIEW_WINDOW__"></span>**Warum sieht meine Animation in der X-Datei anders aus als die Animation im Vorschau Fenster?** 
</dt> <dd>

Das Vorschaufenster ist nicht im strengsten Sinne von Bedeutung. Es spielt keine Animation, sondern synchronisiert mit dem aktuellen Zustand der Maya-Szene. Wenn Animation exportiert wird, werden die Matrizen bei jeder Transformation in Skalierungs-, Rotations-(Quaternion) und Übersetzungs Komponenten (häufig als srts bezeichnet) zerlegt. Srts sind besser erwünscht als Matrizen, da Sie gut interpolieren, eine kompaktere Form der Daten bereitstellen und unabhängig voneinander komprimiert werden können. Nicht alle Matrizen können in srts unterteilt werden. Wenn Sie nicht zusammengesetzt werden können, sind die resultierenden srts unbekannt, sodass kleine Fehler in der Animation erkannt werden können. Die beiden Features in Maya, die bei der Zerlegung häufig Probleme verursachen, sind zerrt und Off-Center-Drehungen oder-Skalen. Wenn dieses Problem auftritt, weil Sie offline-oder Skalierungen verwenden, sollten Sie ggf. zusätzliche Transformationen hinzufügen, um die Hierarchieebene zu erhöhen.

Wenn D3DX Animation srts unterstützt, sieht es wie folgt aus:

``` syntax
[S]x[R]x[T]
```

Die Maya-Matrizen sind viel komplizierter und erfordern eine beträchtliche Menge an zusätzlichem Prozess, der wie folgt aussieht:

``` syntax
[SpInv]x[S]x[Sh]x[Sp]x[St]x[RpInv]x[Ro]x[R]x[Rp]x[Rt]x[T]
```

</dd> <dt>

<span id="I_skinned_my_mesh_with_RigidSkin_but_the_mesh__or_portion__isn_t_moving._Why__"></span><span id="i_skinned_my_mesh_with_rigidskin_but_the_mesh__or_portion__isn_t_moving._why__"></span><span id="I_SKINNED_MY_MESH_WITH_RIGIDSKIN_BUT_THE_MESH__OR_PORTION__ISN_T_MOVING._WHY__"></span>**Ich habe mein Mesh mit "rigidskin", aber das Mesh (oder den Teil) nicht verschoben. Dafür?** 
</dt> <dd>

Das starre Skin von Maya wird zurzeit nicht unterstützt. Verwenden Sie Smooth Skin.

</dd> <dt>

<span id="Where_has_all_of_my_IK_gone_in_the_X-file__"></span><span id="where_has_all_of_my_ik_gone_in_the_x-file__"></span><span id="WHERE_HAS_ALL_OF_MY_IK_GONE_IN_THE_X-FILE__"></span>**Wo ist all mein IK in der X-Datei geblieben?** 
</dt> <dd>

X-Dateien unterstützen IK nicht. Stattdessen werden die IK-Lösungen in die in der X-Datei gespeicherten Frames integriert.

</dd> <dt>

<span id="Why_do_none_of_my_materials_colors_show_up_except_DirectXShaders__"></span><span id="why_do_none_of_my_materials_colors_show_up_except_directxshaders__"></span><span id="WHY_DO_NONE_OF_MY_MATERIALS_COLORS_SHOW_UP_EXCEPT_DIRECTXSHADERS__"></span>**Warum werden keine eigenen Materialien mit Ausnahme von directxshaders angezeigt?** 
</dt> <dd>

Die DirectX-Erweiterungen für Maya unterstützen derzeit nur directxshader-Materialien für Vorschau und Export. In einer zukünftigen Version werden möglicherweise andere Materialien unterstützt.

</dd> </dl>

## <a name="xinput-questions"></a>Fragen zu xinput

<dl> <dt>

<span id="Can_I_use_DirectInput_to_read_the_triggers__"></span><span id="can_i_use_directinput_to_read_the_triggers__"></span><span id="CAN_I_USE_DIRECTINPUT_TO_READ_THE_TRIGGERS__"></span>**Kann ich die Trigger mithilfe von DirectInput lesen?** 
</dt> <dd>

Ja, aber Sie fungieren als dieselbe Achse. Daher können Sie die Trigger nicht unabhängig mit DirectInput lesen. Bei Verwendung von xinput geben die Trigger separate Werte zurück.

Weitere Informationen dazu, warum DirectInput die Trigger als eine Achse interpretiert, finden [Sie unter Verwenden des Xbox 360-Controllers mit DirectInput](/windows/desktop/xinput/xinput-and-directinput).

</dd> <dt>

<span id="How_many_controllers_does_XInput_support__"></span><span id="how_many_controllers_does_xinput_support__"></span><span id="HOW_MANY_CONTROLLERS_DOES_XINPUT_SUPPORT__"></span>**Wie viele Controller unterstützt xinput?** 
</dt> <dd>

Xinput unterstützt vier Controller, die gleichzeitig angeschlossen sind.

</dd> <dt>

<span id="Does_XInput_support_non-common_controllers__"></span><span id="does_xinput_support_non-common_controllers__"></span><span id="DOES_XINPUT_SUPPORT_NON-COMMON_CONTROLLERS__"></span>**Unterstützt xinput nicht gemeinsame Controller?** 
</dt> <dd>

Nein, das ist nicht der Fall.

</dd> <dt>

<span id="Are_common_controllers_available_through_DirectInput__"></span><span id="are_common_controllers_available_through_directinput__"></span><span id="ARE_COMMON_CONTROLLERS_AVAILABLE_THROUGH_DIRECTINPUT__"></span>**Sind allgemeine Controller über DirectInput verfügbar?** 
</dt> <dd>

Ja, Sie können über DirectInput auf allgemeine Controller zugreifen.

</dd> <dt>

<span id="How_do_I_get_force_feedback_on_the_common_controllers__"></span><span id="how_do_i_get_force_feedback_on_the_common_controllers__"></span><span id="HOW_DO_I_GET_FORCE_FEEDBACK_ON_THE_COMMON_CONTROLLERS__"></span>**Gewusst wie erhalten Sie ein Erzwingungs Feedback zu den allgemeinen Controllern?** 
</dt> <dd>

Verwenden Sie die Funktion " [**xinputsetstate**](/windows/desktop/api/xinput/nf-xinput-xinputsetstate) ".

</dd> <dt>

<span id="Why_does_my_default_audio_device_change__"></span><span id="why_does_my_default_audio_device_change__"></span><span id="WHY_DOES_MY_DEFAULT_AUDIO_DEVICE_CHANGE__"></span>**Warum ändert sich das standardmäßige Audiogerät?** 
</dt> <dd>

Beim Herstellen einer Verbindung mit dem Headset fungiert das Headset des Controllers als Standard-USB-Audiogerät. wenn es verbunden ist, wird Windows automatisch so geändert, dass dieses USB-Audiogerät als Standard verwendet wird. Da der Benutzer wahrscheinlich nicht alle Audiodaten über das Headset durchläuft, muss er Sie manuell an die ursprüngliche Einstellung anpassen.

</dd> <dt>

<span id="How_do_I_control_the_lights_on_the_controller__"></span><span id="how_do_i_control_the_lights_on_the_controller__"></span><span id="HOW_DO_I_CONTROL_THE_LIGHTS_ON_THE_CONTROLLER__"></span>**Gewusst wie die Beleuchtung auf dem Controller steuern?** 
</dt> <dd>

Die Lichter auf dem Controller werden vom Betriebssystem vorgegeben und können nicht geändert werden.

</dd> <dt>

<span id="How_do_I_access_the_Xbox_360_button_in_my_applications__"></span><span id="how_do_i_access_the_xbox_360_button_in_my_applications__"></span><span id="HOW_DO_I_ACCESS_THE_XBOX_360_BUTTON_IN_MY_APPLICATIONS__"></span>**Gewusst wie auf die Schaltfläche Xbox 360 in "meine Anwendungen" zugreifen?** 
</dt> <dd>

Diese Schaltfläche ist für die zukünftige Verwendung reserviert.

</dd> <dt>

<span id="Where_do_I_get_drivers__"></span><span id="where_do_i_get_drivers__"></span><span id="WHERE_DO_I_GET_DRIVERS__"></span>**Wo erhalte ich Treiber?** 
</dt> <dd>

Die Treiber werden über Windows Update verfügbar sein.

</dd> <dt>

<span id="How_is_controller_ID_determined__"></span><span id="how_is_controller_id_determined__"></span><span id="HOW_IS_CONTROLLER_ID_DETERMINED__"></span>**Wie wird die Controller-ID bestimmt?** 
</dt> <dd>

Beim Starten von xinput wird die ID nicht deterministisch von der xinput-Engine und den Controllern bestimmt, die angeschlossen sind. Wenn Controller angeschlossen sind, während eine xinput-Anwendung ausgeführt wird, weist das System den neuen Controller als niedrigste verfügbare Zahl zu. Wenn ein Controller getrennt ist, wird die Nummer wieder verfügbar gemacht.

</dd> <dt>

<span id="How_do_I_get_the_audio_devices_for_the_controller__"></span><span id="how_do_i_get_the_audio_devices_for_the_controller__"></span><span id="HOW_DO_I_GET_THE_AUDIO_DEVICES_FOR_THE_CONTROLLER__"></span>**Gewusst wie Sie die Audiogeräte für den Controller?** 
</dt> <dd>

Verwenden Sie die Funktion " [**xinputgetdsoundaudiodeviceguids**](/windows/desktop/api/xinput/nf-xinput-xinputgetdsoundaudiodeviceguids) ". Weitere Informationen finden Sie im Beispiel Audiocontroller.

</dd> <dt>

<span id="What_should_I_do_when_a_controller_is_unplugged__"></span><span id="what_should_i_do_when_a_controller_is_unplugged__"></span><span id="WHAT_SHOULD_I_DO_WHEN_A_CONTROLLER_IS_UNPLUGGED__"></span>**Was soll ich tun, wenn ein Controller nicht mehr verfügbar ist?** 
</dt> <dd>

Wenn der Controller von einem Player verwendet wurde, sollten Sie das Spiel anhalten, bis der Controller wieder verbunden ist, und der Player drückt eine Schaltfläche, um zu signalisieren, dass er zum Anhalten bereit ist.

</dd> </dl>

 

 