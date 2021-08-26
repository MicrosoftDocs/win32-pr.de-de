---
title: Bibliotheksdateien und Einstellungen
description: Bibliotheksdateien und Einstellungen
ms.assetid: ae043b1e-1d61-4d5a-be98-54f899fa24ed
keywords:
- Windows Medienformat-SDK, Bibliotheksdateien
- Windows Medienformat-SDK, Compilereinstellungen
- Windows Medienformat-SDK, Headerdateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176f6c7acb9516e8c7ac38a067091bcbb0c8f7cf49cfdb9e65b396768158b233
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930660"
---
# <a name="library-files-and-compiler-settings"></a>Bibliotheksdateien und Einstellungen

Um eine Anwendung mit dem Windows Media Format SDK zu entwickeln, müssen Sie Microsoft Visual C++ Version 6.0 oder höher verwenden. Die einzigen Programmiersprachen, die für die Entwicklung geeignet sind, sind C++ und C.

Der Inhalt der verschiedenen Headerdateien, die in diesem SDK enthalten sind, wird in der folgenden Tabelle beschrieben.



| Headerdatei                 | Beschreibung                                                                                                                                                                                                                                         |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| asferr.h                    | Definiert Fehlercodes im Zusammenhang mit ASF-Dateivorgängen. Dieser Header ist in wmsdk.h enthalten.                                                                                                                                                            |
| drmexternals.h              | Definiert Strukturen, Enumerationen und Konstanten, die für die Verwaltung digitaler Rechte (Digital Rights Management, DRM) verwendet werden. Schließen Sie diesen Header ein, wenn Sie eine Anwendung schreiben, die DRM verwendet.                                                                                            |
| dshowasf.h                  | Definiert die Microsoft DirectShow QASF-Filter. Schließen Sie diesen Header ein, wenn Sie eine DirectShow-Anwendung schreiben, die ASF-Dateien erstellt oder liest. Weitere Informationen finden Sie unter [DirectShow und Windows Media](directshow-and-windows-media.md).               |
| msnetobj.h                  | Definiert die [**IRMGetLicense-Schnittstelle,**](irmgetlicense.md) die in einer der Laufzeitbibliotheken implementiert ist, die mit dem Windows Media Format SDK installiert sind.                                                                                     |
| nserror.h                   | Definiert Fehlercodes für Windows Media Technologies. Nur eine Teilmenge dieser Fehlercodes ist für das Windows Media Format SDK relevant. Dieser Header ist in wmsdk.h enthalten.                                                                            |
| wmdxva.h                    | Enthält andere Header und Definitionen, die erforderlich sind, um die Microsoft DirectX-Videobeschleunigung für die Wiedergabe Windows medienbasierten Inhalten zu aktivieren. Weitere Informationen finden Sie unter [Aktivieren der DirectX-Videobeschleunigung.](enabling-directx-video-acceleration.md) |
| wmnetsourcecreator.h        | Enthält Informationen, die zum Erstellen von Netzwerkquellen-Plug-Ins erforderlich sind.                                                                                                                                                                                      |
| wmsbuffer.h                 | Definiert die schnittstellen, die von Pufferobjekten verwendet werden. Schließen Sie diesen Header ein, wenn Sie eigene Puffer zum Lesen von Dateien erstellen.                                                                                                                                 |
| wmsdk.h                     | Der Hauptheader für Anwendungen, die das Windows Media Format SDK verwenden. Dieser Header enthält keine Definitionen, sondern asferr.h, nserror.h, windows.h und wmsdkidl.h. Schließen Sie diesen Header für alle Anwendungen ein, die dieses SDK verwenden.                     |
| wmsdkidl.h                  | Definiert die Schnittstellen, Funktionen, Strukturen, Enumerationen und Konstanten für die meisten Objekte des Windows Media Format SDK. Dieser Header ist in wmsdk.h enthalten.                                                                             |
| wmsinternaladminnetsource.h | Definiert die Schnittstellen von Netzwerkquellen-Plug-Ins.                                                                                                                                                                                                  |
| wmsysprf.h                  | Definiert die Konstanten für die Systemprofile. Schließen Sie diesen Header in Anwendungen ein, die Systemprofile nach Bezeichner laden.                                                                                                                         |



 

Damit Sie das Windows Media Format SDK verwenden können, muss Ihr Compiler ordnungsgemäß konfiguriert sein. Die Konfiguration für das Erstellen im Debugmodus ist anders als für den Releasemodus. Konfigurieren Sie Ihre Einstellung gemäß der folgenden Tabelle. Alle diese Einstellungen werden im Dialogfeld Project Einstellungen konfiguriert. Um zum Dialogfeld zu kommen, wählen Sie **Einstellungen** **Menü** Project aus.



| Einstellung                                                                 | Debugwert                                                                              | Releasewert                                                                           |
|-------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| (Registerkarte C/C++, Kategorie = Codegenerierung) Verwenden der Laufzeitbibliothek            | Debuggen einer Multithread-DLL                                                                  | Multithread-DLL                                                                       |
| (Registerkarte "Link", Kategorie = Allgemein) Alle Standardbibliotheken ignorieren (Kontrollkästchen) | Ausgewählt                                                                                 | Ausgewählt                                                                                |
| (Registerkarte "Link", Kategorie = Allgemein) Objekt-/Bibliotheksmodule                   | Schließen Sie Msvcrtd.lib ein, und Wmvcore.lib.Do libc.lib oder andere Varianten nicht enthalten.<br/> | Schließen Sie Msvcrt.lib ein, Wmvcore.lib.Do libc.lib oder andere Varianten nicht enthalten.<br/> |



 

Wenn Sie Microsoft Visual Studio .NET verwenden, wurden die Einstellungen an verschiedene Speicherorte geändert, wie in der folgenden Tabelle gezeigt. Alle diese Einstellungen werden im Dialogfeld **Eigenschaftenseiten** konfiguriert. Um zum Dialogfeld zu kommen, klicken Sie  mit der rechten Maustaste  auf ihr Projekt im Projektmappen-Explorer, und wählen Sie im Kontextmenü Eigenschaften aus.



| Einstellung                                                                  | Debugwert                                                                              | Releasewert                                                                           |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| (Konfigurationseigenschaften/ C/C++ / Codegenerierung) Laufzeitbibliothek     | Multithread-Debug-DLL (/MDd)                                                          | Multithread-DLL (/MD)                                                                |
| (Konfigurationseigenschaften/Linker/Eingabe) Zusätzliche Abhängigkeiten      | Schließen Sie Msvcrtd.lib ein, und Wmvcore.lib.Do libc.lib oder andere Varianten nicht enthalten.<br/> | Schließen Sie Msvcrt.lib ein, Wmvcore.lib.Do libc.lib oder andere Varianten nicht enthalten.<br/> |
| (Konfigurationseigenschaften/Linker/Eingabe) Alle Standardbibliotheken ignorieren | Ja                                                                                      | Ja                                                                                     |



 

Wenn Sie das Laden von Wmvcore.dll oder einer anderen DLL verzögern möchten, verwenden Sie die Linkoption /DELAYLOAD in Microsoft Visual C++ 6.0 oder verzögert geladene DLLs in Microsoft Visual C++ .NET.

Darüber hinaus müssen Sie die Verzeichnisse für die Bibliotheken und Header des Windows Media Format SDK hinzufügen. Um die Verzeichniseinstellungen für Visual C++ 6.0 zu finden, klicken Sie im Menü **Extras** auf **Optionen** und dann auf **die Registerkarte** Verzeichnisse. Wenn Sie Visual C++ .NET  verwenden, klicken Sie im Menü **Extras** auf Optionen, und wählen Sie dann projekte/VC++ Verzeichnisse in der Optionsliste aus. Fügen Sie Verzeichnisse wie in der folgenden Tabelle gezeigt hinzu. Wenn Sie das Installationsverzeichnis für das Windows Media Format SDK geändert haben, ist Ihr Pfad anders.



| Verzeichnistyp | Standardpfad                 |
|----------------|------------------------------|
| Includedateien  | C: \\ WMSDK \\ WMFSDK11 \\ include |
| Bibliotheksdateien  | C: \\ WMSDK \\ WMFSDK11 \\ lib     |



 

Wenn Sie das Platform SDK verwenden, werden die Standardpfade wie folgt angezeigt:



| Verzeichnistyp | Standardpfad                                              |
|----------------|-----------------------------------------------------------|
| Includedateien  | C: \\ Programme \\ Microsoft SDsK \\ Windows \\ v6.0 \\ Include |
| Bibliotheksdateien  | C: \\ Programme \\ Microsoft SDsK \\ Windows \\ v6.0 \\ Lib     |



 

Vor dem Aufrufen einer der Erstellungsfunktionen sollte COM mit einem Aufruf von **Coinitialize** oder **CoinitializeEx initialisiert werden.** Es kann entweder das FreeThreadingmodell oder das Apartmentthreadingmodell verwendet werden, aber das Apartmentthreadingmodell erzwingt Threadingeinschränkungen für die Anwendung. Weitere Informationen zum Microsoft Component Object Model (COM) finden Sie auf der COM-Seite auf [der Microsoft-Website](../com/the-component-object-model.md).

**Hinweis** Anwendungen, die dateien wiedergeben oder erstellen, die durch digitale Rights Management (DRM) geschützt sind, erfordern eine individualisierte statische Bibliothek, die separat von Microsoft abgerufen werden muss. Weitere Informationen finden Sie im Windows Media Licensing Form auf der [Microsoft-Website](https://www.microsoft.com/licensing/default). Wenn Sie die DRM-Bibliothek verwenden, sollten Sie keinen Link zu Wmvcore.lib erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erste Schritte**](getting-started.md)
</dt> </dl>

 

