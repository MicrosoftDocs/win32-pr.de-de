---
title: Bibliotheksdateien und Compilereinstellungen
description: Bibliotheksdateien und Compilereinstellungen
ms.assetid: ae043b1e-1d61-4d5a-be98-54f899fa24ed
keywords:
- Windows Media-Format-SDK, Bibliotheksdateien
- Windows Media-Format-SDK, Compilereinstellungen
- Windows Media-Format-SDK, Header Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 079636c8f01decdcfb90e36641e26c62354a7893
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104474560"
---
# <a name="library-files-and-compiler-settings"></a>Bibliotheksdateien und Compilereinstellungen

Zum Entwickeln einer Anwendung mit dem Windows Media-Format SDK müssen Sie Microsoft Visual C++ Version 6,0 oder höher verwenden. Die einzige Programmiersprache, die für die Entwicklung geeignet ist, sind C++ und C.

Der Inhalt der verschiedenen Header Dateien, die in diesem SDK enthalten sind, wird in der folgenden Tabelle beschrieben.



| Headerdatei                 | BESCHREIBUNG                                                                                                                                                                                                                                         |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| asferr. h                    | Definiert Fehlercodes im Zusammenhang mit ASF-Datei Vorgängen. Dieser Header ist in wmsdk. h enthalten.                                                                                                                                                            |
| drmexternals. h              | Definiert Strukturen, Enumerationen und Konstanten, die für Digital Rights Management (DRM) verwendet werden. Fügen Sie diesen Header ein, wenn Sie eine Anwendung schreiben, die DRM verwendet.                                                                                            |
| dshowasf. h                  | Definiert die Microsoft DirectShow-qasf-Filter. Fügen Sie diesen Header ein, wenn Sie eine DirectShow-Anwendung schreiben, die ASF-Dateien erstellt oder liest. Weitere Informationen finden Sie unter [DirectShow-und Windows-Medien](directshow-and-windows-media.md).               |
| msnettobj. h                  | Definiert die [**irmgetlicense**](irmgetlicense.md) -Schnittstelle, die in einer der Laufzeitbibliotheken implementiert ist, die mit dem Windows Media Format SDK installiert werden.                                                                                     |
| nserror. h                   | Definiert Fehlercodes für Windows Media-Technologien. Nur eine Teilmenge dieser Fehlercodes ist für das Windows Media-Format-SDK relevant. Dieser Header ist in wmsdk. h enthalten.                                                                            |
| wmdxva. h                    | Schließt andere Header und Definitionen ein, die erforderlich sind, um die Microsoft DirectX-Video Beschleunigung für die Wiedergabe von Windows Media-basierten Inhalten Weitere Informationen finden Sie unter [Aktivieren der DirectX-Video Beschleunigung](enabling-directx-video-acceleration.md). |
| wmnetsourcecreator. h        | Enthält Informationen, die zum Erstellen von Plug-Ins für Netzwerk Quellen erforderlich sind.                                                                                                                                                                                      |
| wmsbuffer. h                 | Definiert die Schnittstellen, die von Puffer Objekten verwendet werden. Fügen Sie diesen Header ein, wenn Sie eigene Puffer für das Lesen von Dateien erstellen.                                                                                                                                 |
| wmsdk. h                     | Der Haupt Header für Anwendungen, die das Windows Media-Format-SDK verwenden. Dieser Header enthält keine Definitionen, enthält jedoch "asferr. h", "nserror. h", "Windows. h" und "wmsdkidl. h". Schließen Sie diesen Header für alle Anwendungen ein, die dieses SDK verwenden.                     |
| wmsdkidl. h                  | Definiert die Schnittstellen, Funktionen, Strukturen, Enumerationen und Konstanten für die meisten Objekte des Windows Media Format SDK. Dieser Header ist in wmsdk. h enthalten.                                                                             |
| wmsinternaladminnetsource. h | Definiert die Schnittstellen von Netzwerk Quellen-Plug-ins.                                                                                                                                                                                                  |
| wmsysprf. h                  | Definiert die Konstanten für die Systemprofile. Fügen Sie diesen Header in Anwendungen ein, die Systemprofile nach Bezeichner laden.                                                                                                                         |



 

Um das Windows Media-Format-SDK verwenden zu können, muss der Compiler ordnungsgemäß konfiguriert sein. Die Konfiguration unterscheidet sich für die Erstellung im Debugmodus als für den Releasemodus. Konfigurieren Sie die Einstellung gemäß der folgenden Tabelle. Alle diese Einstellungen sind im Dialogfeld Projekteinstellungen konfiguriert. Um zum Dialogfeld zu gelangen, wählen Sie im Menü **Projekt** die Option **Einstellungen** aus.



| Einstellung                                                                 | Debugwert                                                                              | Releasewert                                                                           |
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| (Registerkarte C/C++, Kategorie = Code Generierung) Verwenden der Lauf Zeit Bibliothek            | Multithread-DLL Debuggen                                                                  | Multithread-DLL                                                                       |
| (Registerkarte "Link", Kategorie = Allgemein) Alle Standardbibliotheken ignorieren (Kontrollkästchen) | Ausgewählt                                                                                 | Ausgewählt                                                                                |
| (Registerkarte "Link", Kategorie = Allgemein) Objekt-/Bibliotheksmodule                   | Schließen Sie msvcrtd. lib und Wmvcore.lib.do nicht include libc. lib oder irgendeine Variation ein.<br/> | Schließen Sie msvcrt. lib und Wmvcore.lib.do nicht include libc. lib oder irgendeine Variation ein.<br/> |



 

Wenn Sie Microsoft Visual Studio .NET verwenden, wurden die Einstellungen in verschiedene Speicherorte geändert, wie in der folgenden Tabelle dargestellt. Alle diese Einstellungen werden im Dialogfeld **Eigenschaften Seiten** konfiguriert. Um zum Dialogfeld zu gelangen, klicken Sie im Bereich **Projektmappen-Explorer** mit der rechten Maustaste auf das Projekt, und wählen Sie im Kontextmenü **Eigenschaften** aus.



| Einstellung                                                                  | Debugwert                                                                              | Releasewert                                                                           |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| (Konfigurations Eigenschaften/C/C++/Code Generierung) Lauf Zeit Bibliothek     | Multithreaded-Debug-DLL (/MDd)                                                          | Multithread-DLL (/MD)                                                                |
| (Konfigurations Eigenschaften/Linker/Eingabe) Zusätzliche Abhängigkeiten      | Schließen Sie msvcrtd. lib und Wmvcore.lib.do nicht include libc. lib oder irgendeine Variation ein.<br/> | Schließen Sie msvcrt. lib und Wmvcore.lib.do nicht include libc. lib oder irgendeine Variation ein.<br/> |
| (Konfigurations Eigenschaften/Linker/Eingabe) Alle Standardbibliotheken ignorieren | Ja                                                                                      | Ja                                                                                     |



 

Wenn Sie das Laden von Wmvcore.dll oder einer anderen dll verzögern möchten, verwenden Sie die Link-Option/DELAYLOAD in Microsoft Visual C++ 6,0 oder verzögerte geladene DLLs in Microsoft Visual C++ .net.

Außerdem müssen Sie die Verzeichnisse für die Bibliotheken und Header des Windows Media Format SDK einschließen. Klicken Sie zum Suchen der Verzeichnis Einstellungen für Visual C++ 6,0 im **Menü Extras** auf **Optionen**, und klicken Sie dann auf die Registerkarte **Verzeichnisse** . Wenn Sie Visual C++ .NET verwenden, klicken Sie im **Menü Extras** auf **Optionen** , und wählen Sie dann in der Liste Optionen die Option Projekte/VC + +-Verzeichnisse aus. Fügen Sie Verzeichnisse hinzu, wie in der folgenden Tabelle gezeigt. Wenn Sie das Installationsverzeichnis für das Windows Media-Format-SDK geändert haben, wird der Pfad anders angezeigt.



| Verzeichnistyp | Standardpfad                 |
|----------------|------------------------------|
| Includedateien  | C: \\ wmsdk \\ WMFSDK11 \\ include |
| Bibliotheksdateien  | C: \\ wmsdk \\ WMFSDK11 \\ lib     |



 

Wenn Sie das Platform SDK verwenden, werden die Standard Pfade wie folgt angezeigt:



| Verzeichnistyp | Standardpfad                                              |
|----------------|-----------------------------------------------------------|
| Includedateien  | C: \\ Programmdateien \\ Microsoft sdsk \\ Windows \\ v 6.0 \\ include |
| Bibliotheksdateien  | C: \\ Programmdateien \\ Microsoft sdsk \\ Windows \\ v 6.0 \\ lib     |



 

Vor dem Aufrufen einer der Erstellungs Funktionen muss com mit einem Aufruf von **CoInitialize** oder **CoInitializeEx** initialisiert werden. Es kann entweder das kostenlose Threading Modell oder das Apartment-Threading Modell verwendet werden, aber das Apartment Threading Modell erzwingt Threading Einschränkungen für die Anwendung. Weitere Informationen zum Microsoft Component Object Model (com) finden Sie auf der Seite "com" auf der [Microsoft](../com/the-component-object-model.md)-Website.

**Hinweis** Anwendungen, die Dateien wiedergeben oder erstellen, die durch Digital Rights Management (DRM) geschützt sind, erfordern eine individualisierte statische Bibliothek, die separat von Microsoft abgerufen werden muss. Weitere Informationen finden Sie im Windows Media Licensing-Formular auf der [Microsoft-Website](https://www.microsoft.com/licensing/default). Wenn Sie die DRM-Bibliothek verwenden, sollten Sie nicht mit Wmvcore. lib verknüpfen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Einstieg**](getting-started.md)
</dt> </dl>

 

