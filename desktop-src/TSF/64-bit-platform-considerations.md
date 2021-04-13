---
title: 64-Bit-Überlegungen
description: Mit der zunehmenden Verfügbarkeit von 64-Bit-Fenstern erwarten Benutzer, dass Eingabemethoden, wie z. b. Internationale Tastaturen in verschiedenen Sprachen oder Eingabemethoden-Editoren (IMEs) in ostasiatischen Sprachen, ordnungsgemäß mit 32-Bit-und 64-Bit-Anwendungen funktionieren.
ms.assetid: 6a99ad45-202c-4fbb-9707-341bc9fde21e
keywords:
- Text Dienst Framework (TSF), 64-Bit-Windows
- TSF (Text Dienst Framework), 64-Bit-Windows
- Text Services, 64-Bit-Windows
- 64-Bit-Windows
- Text Services-Framework (TSF), Eingabemethoden-Editor (IME)
- TSF (Text Dienste-Framework), Eingabemethoden-Editor (IME)
- Text Dienste, Eingabemethoden-Editor (IME)
- Eingabemethoden-Editor (IME)
- IME (Eingabemethoden-Editor)
- Text Dienst Framework (TSF), internationale Tastaturen
- TSF (Text Dienst Framework), internationale Tastaturen
- Text Dienste, internationale Tastaturen
- Internationale Tastaturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 045ec699c7a433f15b92467e3072d30acbf01936
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390482"
---
# <a name="64-bit-considerations"></a>64-Bit-Überlegungen

Mit der zunehmenden Verfügbarkeit von 64-Bit-Fenstern erwarten Benutzer, dass Eingabemethoden, wie z. b. Internationale Tastaturen in verschiedenen Sprachen oder Eingabemethoden-Editoren (IMEs) in ostasiatischen Sprachen, ordnungsgemäß mit 32-Bit-und 64-Bit-Anwendungen funktionieren. Wenn Sie Eingabemethoden Komponenten oder Text Dienste für Microsoft Windows entwickeln, ist es wichtig, dass Sie 64-Bit-Windows als potenzielle Zielplattform für Ihr Produkt in Erwägung gezogen.

Da IMEs und Text Dienste (auf der Grundlage des Text Dienst-Frameworks) in der Regel als DLLs (Dynamic-Link Libraries) implementiert werden, ist es wichtig zu beachten, dass DLLs speziell für die Verwendung in 32-Bit-Umgebungen oder in 64-Bit-Umgebungen erstellt werden. eine DLL, die für die Verwendung in 32-Bit-Umgebungen erstellt wurde, kann von 64-Bit-Anwendungen nicht verwendet werden und umgekehrt.

> [!Note]  
> WOW64 mindern diese bitspezifische dll-Einschränkung nicht. Weitere Informationen zu WOW64 finden Sie unter [Ausführen von 32-Bit-Anwendungen](/windows/desktop/WinProg64/running-32-bit-applications).

 

In diesem Thema werden wichtige Entwurfs Überlegungen für die Entwicklung von IMEs und Text Diensten für die Verwendung auf 64-Bit-Windows erläutert.

## <a name="64-bit-considerations-for-imes"></a>64-Bit-Überlegungen für IMEs

In diesem Abschnitt werden die besonderen Aspekte beschrieben, die beim Entwickeln von IMEs für die Verwendung mit 64-Bit-Windows berücksichtigt werden. Weitere Informationen zu IMEs finden Sie unter [Eingabemethoden-Editor](/previous-versions/windows/desktop/dnacc/input-method-editor-and-text-services-framework-accessibility).

## <a name="building-32-bit-and-64-bit-versions-of-an-ime"></a>Entwickeln von 32-Bit-und 64-Bit-Versionen von IME

Aufgrund des bereits erwähnten 32-Bit-oder 64-Bit-Kompatibilitäts Problems mit DLLs müssen einige Vorsichtsmaßnahmen ergriffen werden, um sicherzustellen, dass die IMEs mit jeder Anwendung (32-Bit oder 64-Bit), die unter 64-Bit-Windows ausgeführt wird, transparent funktioniert. Die empfohlene Lösung, mit der ihr IME transparent mit 32-Bit-und 64-Bit-Anwendungen auf einer 64-Bit-Plattform ausgeführt werden kann, ist die Erstellung und Installation paralleler 32-Bit-und 64-Bit-Versionen der IME-DLL. In der Regel erstellen Entwickler parallele DLLs aus einer einzelnen Quelle, indem Sie die Einstellungen der Zielplattform in ihrer Buildumgebung anpassen. Weitere Informationen zu den Single-Sourcing-32-Bit-und 64-Bit-Anwendungen finden Sie unter [vorbereiten für 64-Bit-Windows](/windows/desktop/WinProg64/getting-ready-for-64-bit-windows).

## <a name="side-by-side-installation-of-64-bit-and-32-bit-input-method-editors"></a>Parallele Installation von 64-Bit-und 32-Bit-Eingabemethoden-Editoren

Entwickler von IMEs und Text Diensten sollten sich über die in diesem Thema beschriebenen 64-Bit-Überlegungen bewusst sein. Glücklicherweise müssen sich Endbenutzer dieser Dienste nicht mit diesen Implementierungs spezifischen Details befassen. Eine Funktion von 64-Bit-Fenstern ist die Möglichkeit, die Notwendigkeit von 64-Bit-und 32-Bit-spezifischen Versionen der IME-DLLs von Endbenutzern auszublenden. Wenn beide Versionen von IME ordnungsgemäß installiert sind, erkennt 64-Bit-Windows das vorhanden sein von 64-Bit-und 32-Bit-Versionen von IME und präsentiert diese bitspezifischen IMEs dem Endbenutzer als einzelnen *logischen* IME. Wenn ein Endbenutzer ein IME verwenden muss, wählt 64-Bit-Windows transparent die Version des IME (32-Bit oder 64-Bit) aus, die für die jeweiligen Umstände geeignet ist.

Damit parallele Installationen von 64-Bit-und 32-Bit-IMEs ordnungsgemäß funktionieren (d. h., um die beiden plattformspezifischen DLLs als einzelne logische IME für den Benutzer darzustellen), müssen die folgenden Bedingungen erfüllt sein:

-   Entwickler müssen plattformspezifische Versionen (einen für 32-Bit-Windows und einen für 64-Bit-Windows) der IME-DLL erstellen.
-   Die 32-Bit-und 64-Bit-DLLs müssen denselben Dateinamen haben.
-   Die Installationsverzeichnis Anforderungen müssen befolgt werden. Weitere Informationen finden Sie unter Installationsverzeichnis Anforderungen.

Parallele Installationen von 32-Bit-und 64-Bit-IME-DLLs verwenden denselben Registrierungsschlüssel zum Speichern von Konfigurationsdaten (einschließlich des dll-Datei namens):


```C++
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layouts
```



Die Funktion " [**imminstalkalk**](/windows/desktop/api/imm/nf-imm-imminstallimea) " wird verwendet, um diesen Registrierungsschlüssel zu erstellen. Das Setup-und Installationsprogramm für einen IME muss diese Funktion zum Registrieren des IME als unterstütztes Tastaturlayout aufruft. Die **imminstalkalk** -Funktion sollte nur einmal aufgerufen werden, entweder von der 32-Bit-oder 64-Bit-Version der IME-DLL.

## <a name="mismatched-ime-dlls"></a>Nicht übereinstimmende IME-DLLs

Die Installation von nur der 32-Bit-Version einer IME auf 64-Bit-Windows wird weder empfohlen noch unterstützt. Wenn eine 64-Bit-Anwendung versucht, eine 32-Bit-Version zu laden, schlägt der IME automatisch fehl, wenn die Anwendung versucht, das zugehörige Tastaturlayout zu laden.

> [!IMPORTANT]
>
> Wenn ein 64-Bit-Anwendungs-/32-Bit-IME-Konflikt Fehler auftritt, wird kein Warn Dialogfeld angezeigt.

 

64-Bit-Überlegungen für Text Dienste

In diesem Abschnitt werden die besonderen Aspekte beim Aufbau von Text Diensten für die Verwendung in 64-Bit-Umgebungen beschrieben. Weitere Informationen zu Text Diensten und zum Text Dienst-Framework finden Sie unter [Text Services-Framework](text-services-framework.md).

## <a name="building-32-bit-and-64-bit-text-services"></a>Entwickeln von 32-Bit-und 64-Bit-Text Diensten

Ein Text Dienst wird als Component Object Model (com)-Objekt implementiert, das in einer DLL verfügbar gemacht wird. Folglich können 32-Bit/64-Bit-DLL-Konflikte mit Text Diensten auftreten, die auf 64-Bit-Windows installiert sind. Ebenso wie bei IMEs wird empfohlen, den Text Dienst so zu aktivieren, dass sowohl 32-Bit-als auch 64-Bit-Anwendungen auf einer 64-Bit-Plattform transparent funktionieren, indem Sie parallele 32-Bit-und 64-Bit-Versionen der Text Dienst-dll erstellen und installieren.

## <a name="side-by-side-installation-of-64-bit-and-32-bit-text-services"></a>Parallele Installation von 64-Bit-und 32-Bit-Text Diensten

Die folgenden Bedingungen müssen erfüllt sein, damit eine 32-Bit-Version und eine 64-Bit-Version eines Text dienstanders nebeneinander installiert und als einzelner, logischer Text Dienst dargestellt werden:

-   Beide Versionen des Text Dienstanbieter geben die gleiche Klassen-ID (CLSID) an, wenn Sie mit dem com-Subsystem registriert werden.
-   Beide Versionen des Text Dienstanbieter werden unabhängig voneinander registriert. Weitere Informationen finden Sie unter [Registrieren von com-Anwendungen](/windows/desktop/com/registering-com-applications).

Wenn ein 32-Bit-Text Dienst bei 64-Bit-Fenstern registriert ist, wird der Registrierungsvorgang transparent an den folgenden Registrierungsschlüssel umgeleitet:


```C++
HKEY_CLASS_ROOT\Wow6432Node\CLSID
```



[Registrierungs Redirector](/windows/desktop/WinProg64/registry-redirector)


```C++
HKEY_LOCAL_MACHINE\Software\Microsoft\CTF\TIP
```



[Itfinputprocessorprofiles](/windows/desktop/api/Msctf/nn-msctf-itfinputprocessorprofiles)-[Text Dienst Registrierung](text-service-registration.md)

Die 64-Bit-Version und die 32-Bit-Version eines Text Dienstanbieter werden möglicherweise gleichzeitig verwendet. In Fällen, in denen beide Versionen eines Text Dienstanbieter alle freigegebenen Objekte bearbeiten müssen, sollte die Koordination für den Zugriff auf freigegebene Objekte im Text Dienst entworfen werden. Jeder Text Dienst ist für das Verwalten von freigegebenen Objekten zuständig, die verwendet oder benötigt werden.

## <a name="installing-only-32-bit-text-services-on-64-bit-windows"></a>Installieren von nur 32-Bit-Text Diensten auf 64-Bit-Windows

Die Installation von nur der 32-Bit-Version eines Text Dienstanbieter auf einer 64-Bit-Windows-Plattform wird weder empfohlen noch unterstützt. Aufgrund der Registrierungs Zuordnung, die auf 64-Bit-Windows-Plattformen ausgeführt wird, kann eine 64-Bit-Anwendung die Dienste eines 32-Bit-Text Diensts über die **itfinputprocessorprofiles** -Schnittstelle auflisten. Wenn jedoch eine 64-Bit-Anwendung versucht, einen 32-Bit-Text Dienst zu laden, wird das Laden im Hintergrund fehlschlagen.

> [!IMPORTANT]
>
> Wenn ein 64-Bit-Anwendung/32-Bit-Text Dienst-Konflikt Fehler auftritt, wird kein Warn Dialogfeld oder keine Meldung angezeigt.

 

Weitere Überlegungen

## <a name="installation-directory-requirements"></a>Anforderungen an das Installationsverzeichnis

In diesem Abschnitt werden die Anforderungen für die Installation von IME-und Text-Dienst Binärdateien beschrieben. Wenn diese Anforderungen nicht befolgt werden, funktioniert der Text Dienst oder der IME möglicherweise nicht ordnungsgemäß.

**IME-DLLs**

Installieren Sie auf 64-Bit-Windows-Plattformen die 32-Bit-und 64-Bit-IME-DLLs in den folgenden Verzeichnissen:

-   Installieren Sie 32-Bit-IME-DLLs im System Verzeichnis syswow64; Rufen Sie [**GetSystemWow64Directory**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directorya)oder [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) mit **CSIDL \_ SYSTEMX86** auf, um diesen Verzeichnispfad abzurufen. Wenn Sie [Windows Installer](/windows/desktop/Msi/about-windows-installer)verwenden, verwenden Sie alternativ die [**System Folder**](/windows/desktop/Msi/systemfolder) -Eigenschaft.
-   Installieren Sie 64-Bit-IME-DLLs im Verzeichnis "System32 System". Rufen Sie [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)oder **SHGetFolderPath** mit dem [CSIDL- \_ System](/windows/desktop/shell/csidl) auf, um diesen Verzeichnispfad abzurufen. Oder verwenden Sie für Windows Installer die [**System64Folder**](/windows/desktop/Msi/system64folder) -Eigenschaft.

**Text Dienst-DLLs und zugehörige Binärdateien**

Installieren Sie auf 64-Bit-Windows-Plattformen die 32-Bit-und 64-Bit-Text Dienst-DLLs sowie alle anderen Binärdateien im Zusammenhang mit dem Text Dienst oder dem IME in den folgenden Verzeichnissen:

-   Installieren Sie 32-Bit-Text Dienst-DLLs und alle anderen 32-Bit-Binärdateien in einem Unterverzeichnis im Verzeichnis "Programme (x86)". Rufen Sie **SHGetFolderPath** mit dem **CSIDL- \_ Programm \_ FILESX86** auf, um diesen Verzeichnispfad abzurufen. Oder verwenden Sie für Windows Installer die [**ProgramFilesFolder**](/windows/desktop/Msi/programfilesfolder) -Eigenschaft.
-   Installieren Sie 64-Bit-Text Dienst-DLLs und alle anderen 64-Bit-Binärdateien in einem Unterverzeichnis unter dem Verzeichnis "Programme". Rufen Sie **SHGetFolderPath** mit **CSIDL- \_ Programm \_ Dateien** auf, um diesen Verzeichnispfad abzurufen. Oder verwenden Sie für Windows Installer die [**ProgramFiles64Folder**](/windows/desktop/Msi/programfiles64folder) -Eigenschaft.

Wenn Sie kein Windows Installer Paket verwenden, um den IME-oder Text Dienst zu installieren, wird eine 64-Bit-Installationsanwendung verwendet. Der WOW64 File System Redirector kann dazu führen, dass 32-Bit-Installationsprogramme Dateien in den falschen Verzeichnissen platzieren (z. b. kann die WOW64-Dateisystem Umleitung dazu führen, dass Dateien, die für das Verzeichnis System32 vorgesehen sind, stattdessen im syswow64-Verzeichnis installiert werden). Wenn Sie ein 32-Bit-Installationsprogramm verwenden müssen, deaktivieren Sie die WOW64-Datei Umleitung während des Installationsvorgangs, um sicherzustellen, dass der File-Redirector-Dienst während des Installationsvorgangs keine unbeabsichtigte Umleitung auslöst. Weitere Informationen zum Dateisystem-Redirector WOW64 finden Sie unter [Dateisystem-Redirector](/windows/desktop/WinProg64/file-system-redirector). Informationen dazu, wie Sie die WOW64-Dateisystem Umleitung deaktivieren oder aktivieren, finden Sie unter [**Wow64EnableWow64FsRedirection**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection).

> [!TIP]
>
> Vermeiden Sie hart codierte Installations Pfade. Weitere Informationen finden Sie unter [Suchen von Verzeichnissen mithilfe der Anwendungsprogrammierschnittstelle nicht Hard-Coded Pfade](/previous-versions//ms675638(v=vs.85))

 

> [!IMPORTANT]
>
> Installieren Sie keine IME-oder Text Dienst Dateien im speziellen Verzeichnis% windir% \\ IME (standardmäßig c: \\ Windows \\ IME). Dieses Verzeichnis enthält Systemdateien, die Text Dienste und IMEs unterstützen. Er ist nicht dafür vorgesehen, IME-oder Text Dienst Dateien von Drittanbietern zu enthalten, und die WOW64-Dateisystem Umleitung wird für dieses Verzeichnis nicht unterstützt.

 

## <a name="dual-ctfmonexe-processes-run-on-64-bit-windows-platforms"></a>Duale Ctfmon.exe Prozesse werden auf 64-Bit-Windows-Plattformen ausgeführt.

Der ctfmon.exe Prozess verwaltet das Text Dienst Framework auf dem Desktop und stellt auch die Benutzeroberfläche der sprach Leiste bereit. Auf 64-Bit-Fenstern werden eine 32-Bit-Version und eine 64-Bit-Version des ctfmon.exe Prozesses gleichzeitig ausgeführt. Der 64-Bit-ctfmon.exe Prozess verwaltet 64-Bit-Text Dienste und ebenso wie der 32-Bit-ctfmon.exe Prozess 32-Bit-Text Dienste.

## <a name="display-behavior-for-different-versions-of-the-language-bar-ui"></a>Anzeigeverhalten für verschiedene Versionen der sprach leisten-Benutzeroberfläche

Auf 64-Bit-Fenstern wird immer nur die sprach leisten-Benutzeroberfläche angezeigt, die mit der 64-Bit-Version eines Text Dienstanbieter verknüpft ist. In Fällen, in denen eine 32-Bit-Anwendung die 32-Bit-Version eines Text Dienstanbieter verwendet, fügt der 64-Bit-Windows automatisch die Benutzeroberfläche der sprach Leiste für den entsprechenden 64-Bit-Text Dienst ein. Dadurch wird sichergestellt, dass keine besondere Arbeit erforderlich ist, damit 32-Bit-Text Dienste in der 64-Bit-Version der sprach Leiste angezeigt werden.

## <a name="control-panel-considerations-on-64-bit-windows"></a>Überlegungen zur Systemsteuerung auf 64-Bit-Windows

64-Bit-Windows ermöglicht den Zugriff auf 32-Bit-und 64-Bit-Versionen von Text Diensten und IMEs über die Systemsteuerung. Um auf die Einstellungen der Systemsteuerung für bestimmte Versionen von Text Diensten oder IMEs zuzugreifen, sehen Sie sich die folgenden Speicherorte an.

-   **System Steuerungs Zugriff für 32-Bit-Text Dienste und-IMEs:** Start->-Einstellungen-> Systemsteuerung-> anzeigen von x86-System Steuerungs Symbolen
-   **System Steuerungs Zugriff für 64-Bit-Text Dienste und-IMEs:** Start->-Einstellungen-> Systemsteuerung-> Regions-und Sprachoptionen

Möglicherweise gibt es Situationen, in denen einige Einstellungen nur über die 32-Bit-Systemsteuerung verfügbar sein können. Vergewissern Sie sich in diesen Fällen, dass die Benutzer Ihres Text Dienstanbieter oder ihrer IME diese Informationen kennen, indem Sie die entsprechende Dokumentation bereitstellen oder Benutzeroberflächen Hinweise in der Schnittstelle für die 64-Bit-Einstellungen anbieten.

 

 