---
description: Unterstützen der automatischen Wiedergabe
ms.assetid: e91334d9-9041-4cb8-a6d0-0e2371800064
title: Unterstützen der automatischen Wiedergabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83091191d8468b7ea3d34146e4a4c02e8cf5bf80cb3e49c72dc43bb092d10f76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083394"
---
# <a name="supporting-autoplay"></a>Unterstützen der automatischen Wiedergabe

Die automatische Wiedergabe ist ein Feature der Shell, das Anwendungen startet, die bestimmten Geräten zugeordnet sind. Abhängig von den aktuellen Einstellungen für die automatische Wiedergabe führt dieses Feature eine von mehreren Aktionen aus, z. B. das Anzeigen einer Liste der verfügbaren Handleranwendungen, das Anzeigen einer Standardordneransicht von Dateien usw.

In Windows Vista wurde die AutoPlay-Funktion erweitert, sodass ein WPD-Gerät eine Liste der unterstützten Inhaltstypen bereitstellen kann. Auf ähnliche Weise können WPD-Anwendungen Inhaltstypen registrieren, die sie unterstützen. Beispielsweise kann sich ein Fotoerfassungs-Assistent als Handler für jedes WPD-Gerät registrieren, das Bilder bereitstellt, und eine Multimediaanwendung kann sich als Handler für jedes Gerät registrieren, auf dem Audio- oder Videodateien gespeichert werden.

Anwendungen registrieren handlerspezifische Informationen, indem sie Einträge in den **Handlerschlüssel HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion Explorer \\ \\ AutoplayHandlers \\** schreiben. Mithilfe eines WPD-Anwendungshandlers (mit dem Namen MyWpdApplication.exe) kann die Anwendung beispielsweise die folgenden Werte unter einem **\\ \\ Handlers MyWpdApplicationHandler-Schlüssel** einfügen.



| Wert          | Typ            | Daten                                                 |
|----------------|-----------------|------------------------------------------------------|
| Aktion         | REG \_ SZ         | Durchsuchen von Inhalten auf portablen Geräten                  |
| CLSIDForCancel | REG \_ SZ         | {00000000-0000-0000-0000-000000000000}               |
| DefaultIcon    | REG \_ EXPAND \_ SZ | %SystemDrive% \\ multimedia \\ wpd \\MyWpdApplication.exe |
| InitCmdLine    | REG \_ SZ         | /AutoPlay                                            |
| ProgID         | REG \_ SZ         | MyWpdApplication.MyWpdApplicationAutoPlay            |
| Anbieter       | REG \_ SZ         | MyWpdApplication                                     |



 

Weitere Informationen zu den Registrierungsschlüsseln und -werten der AutoPlay-Registrierung finden Sie unter **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion Explorer \\ \\ AutoplayHandlers \\ Handlers Key** in der entsprechenden Dokumentation auf MSDN.

### <a name="the-wpd-autoplay-scheme"></a>Das WPD-Schema für die automatische Wiedergabe

Das WPD AutoPlay-Schema lässt sich in das Feature Windows Vista AutoPlay integrieren. Dazu werden drei AutoPlay-Kategorien unterstützt, die in der folgenden Tabelle beschrieben werden.



| Kategorie | BESCHREIBUNG                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------------------|
| `Source`   | Ein WPD-Gerät kann als Inhaltsquelle behandelt werden (d. b. der Inhalt kann vom Gerät übertragen werden).        |
| Senke     | Ein WPD-Gerät kann als Ziel für Inhalte behandelt werden (d. b. der Inhalt kann auf das Gerät übertragen werden).    |
| Funktion | Ein WPD-Gerät unterstützt eine programmierbare oder steuerbare Funktion (z. B. kann es SMS-Nachrichten senden und empfangen). |



 

Anwendungen registrieren sich für die entsprechende Quell-, Senken- und/oder Funktionskategorie, indem sie Einträge in den Abschnitt AutoPlay der Systemregistrierung schreiben. Diese Einträge werden unter dem **WPD-Schlüssel HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion Explorer \\ \\ AutoplayHandlers \\ EventHandlers \\** angezeigt. Unter dem WPD-Schlüssel befinden sich die Schlüssel **Function**, **Sink** und **Source.** Unter jedem dieser Schlüssel befindet sich eine GUID, die einer WPD-Funktionskategorie oder einem Inhaltstyp entspricht.

In der folgenden Tabelle sind die GUIDs aufgeführt, die sich unter dem **Funktionsschlüssel** in der Registrierung finden, und es wird die Funktionskategorie identifiziert, die den einzelnen GUIDs entspricht.



| WPD-Funktionskategorie                           | Registrierungsschlüssel (GUID)                    |
|---------------------------------------------------|----------------------------------------|
| WPD \_ FUNCTIONAL \_ CATEGORY \_ ALL                    | {2D8A6512-A74C-448E-BA8A-F4AC07C49399} |
| WPD \_ FUNCTIONAL \_ CATEGORY \_ AUDIO \_ CAPTURE         | {3F2A1919-C7C2-4A00-855D-F57CF06DEBBB} |
| WPD \_ FUNCTIONAL \_ CATEGORY \_ DEVICE                 | {08EA466B-E3A4-4336-A1F3-A44D2B5C438C} |
| WPD \_ FUNCTIONAL \_ CATEGORY \_ NETWORK \_ CONFIGURATION | {48F4DB72-7C6A-4AB0-9E1A-470E3CDBF26A} |
| \_WPD FUNCTIONAL \_ CATEGORY RENDERING INFORMATION \_ (WPD-FUNKTIONSKATEGORIERENDERINGINFORMATIONEN) \_ | {08600BA4-A7BA-4A01-AB0E-0065D0A356D3} |
| WPD \_ FUNCTIONAL \_ CATEGORY \_ SMS                    | {0044A0B1-C1E9-4AFD-B358-A62C6117C9CF} |
| WPD \_ FUNCTIONAL \_ CATEGORY \_ STILL \_ IMAGE \_ CAPTURE  | {613CA327-AB93-4900-B4FA-895BB5874B79} |
| SPEICHER \_ DER WPD-FUNKTIONSKATEGORIE \_ \_                | {23F05BBC-15DE-4C2A-A55B-A9AF5CE412EF} |
| WPD \_ FUNCTIONAL \_ CATEGORY \_ VIDEO \_ CAPTURE         | {E23E5F6B-7243-43AA-8DF1-0EB3D968A918} |



 

In der folgenden Tabelle sind die GUIDS unter der **Senke** und den **Quellschlüsseln** in der Registrierung aufgeführt und der Inhaltstyp identifiziert, der den einzelnen GUIDs entspricht.



| WPD-Inhaltstyp                          | Registrierungsschlüssel (GUID)                    |
|-------------------------------------------|----------------------------------------|
| WPD \_ CONTENT \_ TYPE \_ ALL                   | {80E170D2-1055-4A3E-B952-82CC4F8A8689} |
| WPD \_ CONTENT \_ TYPE \_ APPOINTMENT           | {0FED060E-8793-4B1E-90C9-48AC389AC631} |
| \_WPD-INHALTSTYP \_ \_ AUDIO                 | {4AD2C85E-5E2D-45E5-8864-4F229E3C6CF0} |
| WPD \_ CONTENT \_ TYPE \_ AUDIO \_ ALBUM          | {AA18737E-5009-48FA-AE21-85F24383B4E6} |
| \_ \_ WPD-INHALTSTYPKALENDER \_              | {A1FD5967-6023-49A0-9DF1-F8060BE751B0} |
| \_ \_ WPD-INHALTSTYPZERTIFIKAT \_           | {DC3876E8-A948-4060-9050-GD77E8A3D87} |
| \_WPD-INHALTSTYP \_ \_ KONTAKT               | {EABA8313-4525-4707-9F0E-87C6808E9435} |
| \_WPD-INHALTSTYP \_ \_ \_ KONTAKTGRUPPE        | {346B8932-4C36-40D8-9415-1828291F9DE9} |
| \_ \_ \_ WPD-INHALTSTYPDOKUMENT              | {680ADF52-950A-4041-9B41-65E393648155} |
| \_WPD-INHALTSTYP \_ \_ E-MAIL                 | {8038044A-7E51-4F8F-883D-1D0623D14533} |
| \_ \_ \_ WPD-INHALTSTYPORDNER                | {27E2E392-A111-48E0-AB0C-E17705A05F85} |
| \_FUNKTIONALES OBJEKT DES WPD-INHALTSTYPS \_ \_ \_    | {99ED0160-17FF-4C44-9D98-1D7A6F941921} |
| GENERISCHE \_ \_ \_ WPD-INHALTSTYPDATEI \_         | {0085E0A6-8D34-45D7-BC5C-447E59C73D48} |
| GENERISCHE NACHRICHT DES \_ WPD-INHALTSTYPS \_ \_ \_      | {E80EAAF8-B2DB-4133-B67E-1BEF4B4A6E5F} |
| BILD \_ DES WPD-INHALTSTYPS \_ \_                 | {EF2107D5-A52A-4243-A26B-62D4176D7603} |
| WPD \_ CONTENT \_ TYPE \_ IMAGE \_ ALBUM          | {75793148-15F5-4A30-A813-54ED8A37E226} |
| WPD \_ CONTENT \_ TYPE \_ MEDIA \_ CAST           | {5E88B3CC-3E65-4E62-BFFF-229495253AB0} |
| \_ \_ WPD-INHALTSTYP \_ MEMO                  | {9CD20ECF-3B50-414F-A641-E473FFE45751} |
| WPD \_ CONTENT \_ TYPE \_ MIXED \_ CONTENT \_ ALBUM | {00F0C3AC-A593-49AC-9219-24ABCA5A2563} |
| WPD \_ CONTENT \_ TYPE \_ NETWORK \_ ASSOCIATION  | {031DA7EE-18C8-4205-847E-89A11261D0F3} |
| WIEDERGABELISTE DES \_ \_ WPD-INHALTSTYPS \_              | {1A33F7E4-AF13-48F5-994E-77369DFE04A3} |
| \_ \_ WPD-INHALTSTYPPROGRAMM \_               | {D269F96A-247C-4BFF-98FB-97F3C49220E6} |
| \_ \_ \_ WPD-INHALTSTYPABSCHNITT               | {821089F5-1D91-4DC9-BE3C-BBB1B35B18CE} |
| \_ \_ WPD-INHALTSTYPAUFGABE \_                  | {63252F2C-887F-4CB6-B1AC-D29855DCEF6C} |
| \_WPD-INHALTSTYP \_ \_ TV            | {60A169CF-F2AE-4E21-9375-9677F11C1C6E} |
| \_ \_ WPD-INHALTSTYP \_ NICHT ANGEGEBEN           | {28D8D31E-249C-454E-AABC-34883168E634} |
| WPD \_ CONTENT \_ TYPE \_ VIDEO                 | {9261B03C-3D78-4519-85E3-02C5E1F50BB9} |
| WPD \_ CONTENT \_ TYPE \_ VIDEO \_ ALBUM          | {012B0DB7-D4C1-45D6-B081-94B87779614F} |
| \_ \_ WPD-INHALTSTYP \_ \_ DRAHTLOSPROFIL     | {0BAC070A-9F5F-4DA4-A8F6-3DE44D68FD6C} |



 

Wenn eine Anwendung eine bestimmte Funktion, Quelle oder Senkenkategorie unterstützt, würde sie eine Zeichenfolge einfügen, die den Namen des Handlerschlüssels unter der GUID angibt, die die unterstützte Funktions- oder Inhaltstypkategorie identifiziert. Bei Verwendung von MyWpdApplication als Beispiel würde die Anwendung einen Eintrag unter dem ... **/EventHandlers/WPD/Function** oder **/Sink** oder **/Source-Schlüssel.** Dieser Eintrag hat das Formular "MyWpdApplicationHandler" und hat den Typ REG \_ SZ. Außerdem wird dieser Eintrag unter der GUID für die funktionalen Kategorien oder Inhaltstypen angezeigt, die von der Anwendung unterstützt werden.

 

 



