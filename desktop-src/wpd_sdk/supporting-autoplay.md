---
description: Unterstützen von AutoPlay
ms.assetid: e91334d9-9041-4cb8-a6d0-0e2371800064
title: Unterstützen von AutoPlay
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 467a4f6289492177beab0469a181297b13accfce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758455"
---
# <a name="supporting-autoplay"></a>Unterstützen von AutoPlay

AutoPlay ist ein Feature der Shell, mit dem Anwendungen gestartet werden, die bestimmten Geräten zugeordnet sind. Abhängig von den aktuellen Einstellungen für die automatische Wiedergabe führt diese Funktion eine von mehreren Aktionen aus, z. b. das darstellen einer Liste verfügbarer handleranwendungen, das Anzeigen einer Standardordner Ansicht von Dateien usw.

In Windows Vista wurde das AutoPlay-Feature so erweitert, dass ein WPD-Gerät eine Liste der unterstützten Inhaltstypen bereitstellen kann. Ebenso können WPD-Anwendungen Inhaltstypen registrieren, die Sie unterstützen. Beispielsweise kann sich ein Assistent zum Erfassen von Fotos als Handler für ein beliebiges WPD-Gerät registrieren, das Bilder bereitstellt, und eine Multimedia-Anwendung kann als Handler für jedes Gerät registriert werden, das Audiodateien oder Videodateien speichert.

Anwendungen registrieren handlerspezifische Informationen durch das Schreiben von Einträgen in den Schlüssel **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ autoplayhandlers \\ Handlers** Key. Mithilfe eines WPD-Anwendungs Handlers (mit dem Namen MyWpdApplication.exe) als Beispiel kann die Anwendung die folgenden Werte unter einem Handler **\\ \\ mywpdapplicationhandler** -Schlüssel einfügen.



| Wert          | Typ            | Daten                                                 |
|----------------|-----------------|------------------------------------------------------|
| Aktion         | REG- \_ SZ         | Durchsuchen von Inhalt auf tragbaren Geräten.                  |
| Clsidforcancel | REG- \_ SZ         | {00000000-0000-0000-0000-000000000000}               |
| DefaultIcon    | REG \_ Expand \_ SZ | % System Drive% \\ Multimedia \\ WPD \\MyWpdApplication.exe |
| InitCmdLine    | REG- \_ SZ         | /AutoPlay                                            |
| ProgID         | REG- \_ SZ         | Mywpdapplikation. mywpdapplicationautoplay            |
| Anbieter       | REG- \_ SZ         | Mywpdapplikation                                     |



 

Weitere Informationen zu den AutoPlay-Registrierungs Schlüsseln und-Werten unter der **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ autoplayhandlers \\ Handlers** Key finden Sie in der entsprechenden Dokumentation auf MSDN.

### <a name="the-wpd-autoplay-scheme"></a>Das WPD-AutoPlay-Schema

Das WPD-AutoPlay-Schema ist in das Windows Vista-Feature für die automatische Wiedergabe integriert. Dies geschieht durch die Unterstützung von drei Kategorien für die automatische Wiedergabe, die in der folgenden Tabelle beschrieben werden.



| Category | BESCHREIBUNG                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------|
| `Source`   | Ein WPD-Gerät kann als Quelle des Inhalts behandelt werden (d. h., der Inhalt kann vom Gerät übertragen werden).        |
| Senke     | Ein WPD-Gerät kann als Ziel für den Inhalt behandelt werden (d. h., der Inhalt kann auf das Gerät übertragen werden).    |
| Funktion | Ein WPD-Gerät unterstützt eine programmierbare oder steuerbare Funktion (z. b. zum Senden und empfangen von SMS-Nachrichten). |



 

Anwendungen registrieren sich für die geeignete Quell-, Senke-und/oder Funktions Kategorie durch das Schreiben von Einträgen in den Abschnitt "AutoPlay" der Systemregistrierung. Diese Einträge werden unter dem **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Explorer \\ autoplayhandlers \\ Eventhandlers \\ WPD** Key angezeigt. Unter dem WPD-Schlüssel befinden sich die **Funktionen**, die **Senke** und die **Quell** Schlüssel. Unter jedem dieser Schlüssel ist eine GUID, die einer WPD-Funktions Kategorie oder einem Inhaltstyp entspricht.

In der folgenden Tabelle sind die GUIDs aufgeführt, die unter dem **Funktions** Schlüssel in der Registrierung gefunden wurden, und die funktionale Kategorie identifiziert, die den einzelnen GUIDs entspricht.



| WPD-Funktions Kategorie                           | Registrierungsschlüssel (GUID)                    |
|---------------------------------------------------|----------------------------------------|
| WPD- \_ Funktions \_ Kategorie \_ alle                    | {2d8a6512-a74c-448e-ba8a-f 4ac07c49399} |
| WPD \_ \_ -Funktions Kategorie \_ - \_ Audioerfassung         | {3f2a1919-c7c2-4a00-855d-f57cf06debbb} |
| WPD \_ - \_ funktionskategoriegerät \_                 | {08ea466b-e3a4-4336-A1F 3-a44d2b5c438c} |
| Netzwerkkonfiguration der WPD- \_ Funktions \_ Kategorie \_ \_ | {48f & 4db72-7c6a-4AB0-9e1a-470e3cdbbba} |
| Informationen zur \_ Funktions \_ Kategorie \_ der WPD \_ | {08600ba4-a7ba-4a01-ab0e-0065d0a356d3} |
| WPD- \_ Funktions \_ Kategorie \_ SMS                    | {0044a0b1-c1e9-4afd-B358-a62c6117c9cf} |
| WPD- \_ Funktions \_ Kategorie \_ trotzdem \_ Image \_ Erfassung  | {613ca327-ab93-4900-b4fa-895bb5874b79} |
| Speicher für WPD- \_ Funktions \_ Kategorie \_                | {23f05bbc-15de-4c2a-a55b-a9af5ce412ef} |
| Video Erfassung der WPD- \_ Funktions \_ Kategorie \_ \_         | {E23E5F6B-7243-43AA-8DF1-0EB3D968A918} |



 

In der folgenden Tabelle werden die GUIDs unter der **Senke** und die **Quell** Schlüssel in der Registrierung aufgeführt und der Inhaltstyp identifiziert, der den einzelnen GUIDs entspricht.



| WPD-Inhaltstyp                          | Registrierungsschlüssel (GUID)                    |
|-------------------------------------------|----------------------------------------|
| WPD \_ - \_ Inhaltstyp \_ alle                   | {80e170d2-1055-4a3e-b952-82cc4f 8a8689} |
| WPD \_ - \_ Inhaltstyp \_ Termin           | {0fed060e-8793-4b1e-90c9-48ac389ac631} |
| WPD \_ \_ -Inhaltstyp \_ Audiodatei                 | {4ad2c85e-5e2d-45e5-8864-4f229e3c6cf0} |
| Audioalbum für WPD \_ \_ -Inhaltstyp \_ \_          | {AA18737E-5009-48FA-AE21-85F24383B4E6} |
| WPD \_ - \_ Inhaltstyp \_ Kalender              | {A1FD5967-6023-49A0-9DF1-F8060BE751B0} |
| WPD \_ - \_ Inhaltstyp \_ Zertifikat           | {DC3876E8-A948-4060-9050-CBD77E8A3D87} |
| Kontakt zum WPD- \_ \_ Inhaltstyp \_               | {EABA8313-4525-4707-9F0E-87C6808E9435} |
| Kontaktgruppe für WPD- \_ \_ Inhaltstyp \_ \_        | {346b8932-4c36-40d8-9415-1828291"f" |
| Dokument für WPD- \_ \_ Inhaltstyp \_              | {680adb52-950a-4041-9b41-65e393648155} |
| e-Mail zum WPD \_ \_ -Inhaltstyp \_                 | {8038044a-7e51-4f-Datei -883d-1d0623d14533} |
| Ordner für WPD- \_ \_ Inhaltstyp \_                | {27e2e392-A111-48e0-ab0c-e17705a05f 85} |
| Funktions Objekt des WPD- \_ \_ Inhaltstyp \_ \_    | {99ed0160-17ff-4c44-9d98-1d7a6f941921} |
| generische Datei für WPD- \_ \_ Inhaltstyp \_ \_         | {0085e0a6-8d34-45d7-bc5c-447e59c73d48} |
| generische WPD- \_ \_ Inhaltstyp \_ \_ Nachricht      | {E80EAAF8-B2DB-4133-B67E-1bef 4b4a6e5f} |
| Bild für WPD- \_ \_ Inhaltstyp \_                 | {EF2107D5-A52A-4243-A26B-62d4176d7603} |
| Bild-Album für WPD- \_ \_ Inhaltstyp \_ \_          | {75793148-15F 5-4a30a813-54ed8a37e226} |
| WPD \_ - \_ Inhaltstyp \_ Medien Umwandlung \_           | {5e88b3cc-3e65-4e62-BFFF-229495253ab0} |
| WPD \_ - \_ Inhaltstyp \_ Memo                  | {9cd20ecf-3b50-414f-a641-e473ffe45751} |
| WPD \_ - \_ Inhaltstyp \_ gemischtes \_ Inhalts \_ Album | {00F 0c3ac-a593-49ac-9219-24abca5a2563} |
| Netzwerk Zuordnung für WPD- \_ \_ Inhaltstyp \_ \_  | {031da7ee-18c8-4205-847e-89a11261d0f 3} |
| WPD \_ - \_ Inhaltstyp \_ Wiedergabeliste              | {1a33f 7e4-AF13-48fi5-994e-77369dfe04a3} |
| WPD \_ - \_ Inhaltstyp \_ Programm               | {D269F96A-247C-4BFF-98FB-97F3C49220E6} |
| Abschnitt zum WPD- \_ \_ Inhaltstyp \_               | {821089f5-1d91-4dc9-be3c-bbb1b35b18ce} |
| WPD \_ - \_ Inhaltstyp \_ Aufgabe                  | {63252f & 2C-887f -4cb6-b1ac-d29855dcef6c} |
| WPD \_ - \_ Inhaltstyp \_ Fernsehen            | {60a169 CF-f2ae-4e21-9375-9677f11c1c6e} |
| WPD \_ - \_ Inhaltstyp \_ nicht angegeben           | {28d8d31e-249c-454e-aabc-34883168e634} |
| Video zum WPD- \_ \_ Inhaltstyp \_                 | {9261b03c-3d78-4519-85e3-02c5e1f50bb9} |
| Video zum WPD- \_ \_ Inhaltstyp \_ \_          | {012b0db7-d4c1-45d6-b081-94b87779614f} |
| WPD \_ - \_ Inhaltstyp \_ drahtlos \_ Profil     | {0bac070a-9F- -4da4-a8f 6-3debug d68f |



 

Wenn eine Anwendung eine bestimmte Funktion, Quelle oder Senke Kategorie unterstützt, würde Sie eine Zeichenfolge einfügen, die den Namen des handlerschlüssels unter der GUID angibt, die die unterstützte funktionale oder Inhaltstyp Kategorie identifiziert hat. Wenn Sie mywpdappliationals Beispiel verwenden, erstellt die Anwendung einen Eintrag unter... **/EventHandlers/WPD/Function**-, **/Sink**-oder **/Source** -Schlüssel. Dieser Eintrag hätte das Format "mywpdapplicationhandler" und den Typ "reg \_ SZ". Außerdem wird dieser Eintrag unter der GUID für die funktionalen Kategorien oder Inhaltstypen angezeigt, die von der Anwendung unterstützt werden.

 

 



