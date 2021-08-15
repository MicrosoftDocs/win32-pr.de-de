---
title: 64-Bit-Überlegungen
description: Mit der zunehmenden Verfügbarkeit von 64-Bit-Windows erwarten Benutzer, dass Eingabemethoden wie internationale Tastaturen in verschiedenen Sprachen oder Eingabemethoden-Editoren (INPUT Method Editors, IMEs) in ostasiatischen Sprachen ordnungsgemäß mit 32-Bit- und 64-Bit-Anwendungen funktionieren.
ms.assetid: 6a99ad45-202c-4fbb-9707-341bc9fde21e
keywords:
- Textdienstframework (TSF), 64-Bit-Windows
- TSF (Textdienstframework),64-Bit-Windows
- Textdienste, 64-Bit-Windows
- 64-Bit-Windows
- Textdienstframework (TSF), Eingabemethoden-Editor (IME)
- TSF (Textdienstframework),Eingabemethoden-Editor (IME)
- Textdienste, Eingabemethoden-Editor (IME)
- Eingabemethoden-Editor (IME)
- IME (Eingabemethoden-Editor)
- Textdienstframework (TSF), internationale Tastaturen
- TSF (Textdienstframework),internationale Tastaturen
- Textdienste, internationale Tastaturen
- internationale Tastaturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de076721f1be036f0e5db6ea74b52a50060b9f0742621188a799ef6c824f677a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118880096"
---
# <a name="64-bit-considerations"></a>64-Bit-Überlegungen

Mit der zunehmenden Verfügbarkeit von 64-Bit-Windows erwarten Benutzer, dass Eingabemethoden wie internationale Tastaturen in verschiedenen Sprachen oder Eingabemethoden-Editoren (INPUT Method Editors, IMEs) in ostasiatischen Sprachen ordnungsgemäß mit 32-Bit- und 64-Bit-Anwendungen funktionieren. Beim Entwickeln von Eingabemethodenkomponenten oder Textdiensten für Microsoft Windows ist es wichtig, 64-Bit-Windows als potenzielle Zielplattform für Ihr Produkt zu betrachten.

Da IMEs und Textdienste (basierend auf dem Textdienstframework) in der Regel als Dynamic Link Libraries (DLLs) implementiert werden, ist es wichtig zu beachten, dass DLLs speziell für die Verwendung in 32-Bit- oder 64-Bit-Umgebungen erstellt wurden. Eine DLL, die für die Verwendung in 32-Bit-Umgebungen erstellt wurde, kann nicht von 64-Bit-Anwendungen verwendet werden und umgekehrt.

> [!Note]  
> WOW64 mindert diese bitspezifische DLL-Einschränkung nicht. Informationen zu WOW64 finden Sie unter [Ausführen von 32-Bit-Anwendungen.](/windows/desktop/WinProg64/running-32-bit-applications)

 

In diesem Thema werden wichtige Entwurfsüberlegungen für die Entwicklung von IMEs und Textdiensten für die Verwendung auf 64-Bit-Windows erläutert.

## <a name="64-bit-considerations-for-imes"></a>64-Bit-Überlegungen für IMEs

In diesem Abschnitt werden die besonderen Überlegungen zum Erstellen von IMEs für die Verwendung mit 64-Bit-Windows beschrieben. Informationen zu IMEs finden Sie unter [Eingabemethoden-Editor.](/previous-versions/windows/desktop/dnacc/input-method-editor-and-text-services-framework-accessibility)

## <a name="building-32-bit-and-64-bit-versions-of-an-ime"></a>Erstellen von 32-Bit- und 64-Bit-Versionen einer IME

Aufgrund des zuvor erwähnten 32-Bit-/64-Bit-Kompatibilitätsproblems mit DLLs müssen einige Vorsichtsmaßnahmen ergriffen werden, um sicherzustellen, dass IMEs transparent mit jeder Anwendung (32-Bit oder 64-Bit) funktionieren, die auf 64-Bit-Windows ausgeführt wird. Die empfohlene Lösung, damit Ihre IME transparent mit 32-Bit- und 64-Bit-Anwendungen auf einer 64-Bit-Plattform funktioniert, besteht darin, parallele 32-Bit- und 64-Bit-Versionen der IME-DLL zu erstellen und zu installieren. In der Regel erstellen Entwickler parallele DLLs aus einer einzelnen Quelle, indem sie die Zielplattformeinstellungen in ihrer Buildumgebung anpassen. Weitere Informationen zu Singlesourcing-32-Bit- und 64-Bit-Anwendungen finden Sie unter [Vorbereiten auf 64-Bit-Windows](/windows/desktop/WinProg64/getting-ready-for-64-bit-windows).

## <a name="side-by-side-installation-of-64-bit-and-32-bit-input-method-editors"></a>Side-by-Side-Installation von 64-Bit- und 32-Bit-Eingabemethoden-Editoren

Entwickler von IMEs und Textdiensten sollten die in diesem Thema beschriebenen 64-Bit-Überlegungen beachten. Glücklicherweise müssen sich Endbenutzer dieser Dienste nicht um diese implementierungsspezifischen Details kümmern. Ein Feature von 64-Bit-Windows ist die Möglichkeit, die Notwendigkeit von 64-Bit- und 32-Bit-spezifischen Versionen der IME-DLLs für Endbenutzer auszublenden. Wenn beide Versionen des IME ordnungsgemäß parallel installiert sind, erkennt 64-Bit-Windows das Vorhandensein von 64-Bit- und 32-Bit-Versionen des IME und stellt diese bitspezifischen IMEs dem Endbenutzer als einzelne *logische* IME zur Verfügung. Wenn ein Endbenutzer eine IME verwenden muss, wählt 64-Bit-Windows transparent die Version des IME (32-Bit oder 64-Bit) aus, die für die jeweiligen Umstände geeignet ist.

Damit die installation von 64-Bit- und 32-Bit-IMEs ordnungsgemäß funktioniert (d.amp;#160;B. um die beiden plattformspezifischen DLLs als einzelne logische IME für den Benutzer darzustellen), müssen die folgenden Bedingungen erfüllt sein:

-   Entwickler müssen plattformspezifische Versionen (eine für 32-Bit-Windows und eine für 64-Bit-Windows) der IME-DLL erstellen.
-   Die 32-Bit- und 64-Bit-DLLs müssen denselben Dateinamen haben.
-   Die Anforderungen an das Installationsverzeichnis müssen erfüllt werden. Weitere Informationen finden Sie unter Installationsverzeichnisanforderungen.

Parallele Installationen von 32-Bit- und 64-Bit-IME-DLLs verwenden denselben Registrierungsschlüssel zum Speichern von Konfigurationsdaten (einschließlich des DLL-Dateinamens):


```C++
HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\Keyboard Layouts
```



Die [**ImmInstallIME-Funktion**](/windows/desktop/api/imm/nf-imm-imminstallimea) wird verwendet, um diesen Registrierungsschlüssel zu erstellen. Das Setup- und Installationsprogramm für eine IME muss diese Funktion aufrufen, um die IME als unterstütztes Tastaturlayout zu registrieren. Die **ImmInstallIME-Funktion** sollte nur einmal aufgerufen werden, entweder aus der 32-Bit- oder 64-Bit-Version der IME-DLL.

## <a name="mismatched-ime-dlls"></a>Nicht übereinstimmende IME-DLLs

Es wird weder empfohlen noch unterstützt, nur die 32-Bit-Version einer IME auf 64-Bit-Windows zu installieren. Wenn eine 64-Bit-Anwendung versucht, eine 32-Bit-IME zu laden, schlägt die IME automatisch fehl, wenn die Anwendung versucht, das zugeordnete Tastaturlayout zu laden.

> [!IMPORTANT]
>
> Es wird kein Warndialogfeld oder keine Meldung angezeigt, wenn ein 64-Bit-Anwendungs-/32-Bit-IME-Konfliktfehler auftritt.

 

64-Bit-Überlegungen für Textdienste

In diesem Abschnitt werden die besonderen Überlegungen zum Erstellen von Textdiensten für die Verwendung in 64-Bit-Umgebungen beschrieben. Weitere Informationen zu Textdiensten und der Textdienstframework finden Sie unter [Textdienstframework](text-services-framework.md).

## <a name="building-32-bit-and-64-bit-text-services"></a>Erstellen von 32-Bit- und 64-Bit-Textdiensten

Ein Textdienst wird als com-Objekt (Component Object Model) implementiert, das für eine DLL verfügbar gemacht wird. Folglich können 32-Bit-/64-Bit-DLL-Konflikte mit Textdiensten auftreten, die auf 64-Bit-Windows installiert sind. Wie bei IMEs empfiehlt es sich, ihren Textdienst transparent mit 32-Bit- und 64-Bit-Anwendungen auf einer 64-Bit-Plattform zu arbeiten, indem Sie parallele 32-Bit- und 64-Bit-Versionen der Textdienst-DLL erstellen und installieren.

## <a name="side-by-side-installation-of-64-bit-and-32-bit-text-services"></a>Side-by-Side-Installation von 64-Bit- und 32-Bit-Textdiensten

Damit eine 32-Bit-Version und eine 64-Bit-Version eines Textdiensts nebeneinander installiert und dem Benutzer als einzelner, logischer Textdienst dargestellt werden, müssen die folgenden Bedingungen erfüllt sein:

-   Beide Versionen des Textdiensts geben den gleichen Klassenbezeichner (CLSID) an, wenn sie beim COM-Subsystem registriert werden.
-   Beide Versionen des Textdiensts werden unabhängig registriert. Weitere Informationen finden Sie unter [Registrieren von COM-Anwendungen.](/windows/desktop/com/registering-com-applications)

Wenn ein 32-Bit-Textdienst bei 64-Bit-Windows registriert ist, wird der Registrierungsvorgang transparent an den folgenden Registrierungsschlüssel umgeleitet:


```C++
HKEY_CLASS_ROOT\Wow6432Node\CLSID
```



[Registrierungsumleitung](/windows/desktop/WinProg64/registry-redirector)


```C++
HKEY_LOCAL_MACHINE\Software\Microsoft\CTF\TIP
```



[ITfInputProcessorProfiles-Textdienstregistrierung](/windows/desktop/api/Msctf/nn-msctf-itfinputprocessorprofiles)[](text-service-registration.md)

Die 64-Bit-Version und die 32-Bit-Version eines Textdiensts werden möglicherweise gleichzeitig verwendet. In Fällen, in denen beide Versionen eines Textdiensts freigegebene Objekte bearbeiten müssen, sollte die Koordination für den Zugriff auf freigegebene Objekte im Textdienst entworfen werden. Jeder Textdienst ist für die Verwaltung aller freigegebenen Objekte verantwortlich, die verwendet oder benötigt werden.

## <a name="installing-only-32-bit-text-services-on-64-bit-windows"></a>Nur 32-Bit-Textdienste auf 64-Bit-Windows

Es wird weder empfohlen noch unterstützt, nur die 32-Bit-Version eines Textdiensts auf einer 64-Bit-Windows-Plattform zu installieren. Aufgrund der Registrierungszuordnung, die auf 64-Bit-Windows-Plattformen erfolgt, kann eine 64-Bit-Anwendung die Dienste eines 32-Bit-Textdiensts über die **ITfInputProcessorProfiles-Schnittstelle aufzählen.** Wenn jedoch eine 64-Bit-Anwendung versucht, einen 32-Bit-Textdienst zu laden, schlägt das Laden automatisch fehl.

> [!IMPORTANT]
>
> Es wird kein Warndialogfeld oder keine Meldung angezeigt, wenn ein 64-Bit-Anwendungs-/32-Bit-Textdienstkonfliktfehler auftritt.

 

Weitere Überlegungen

## <a name="installation-directory-requirements"></a>Anforderungen an das Installationsverzeichnis

In diesem Abschnitt werden die Anforderungen für die Installation von IME- und Textdienstbinärdateien beschrieben. Wenn diese Anforderungen nicht erfüllt werden, funktioniert Ihr Textdienst oder IME möglicherweise nicht ordnungsgemäß.

**IME-DLLs**

Installieren Sie auf 64-Bit-Windows-Plattformen die 32-Bit- und 64-Bit-IME-DLLs in den folgenden Verzeichnissen:

-   Installieren Sie 32-Bit-IME-DLLs im Systemverzeichnis SysWOW64. Rufen [**Sie GetSystemWow64Directory**](/windows/desktop/api/wow64apiset/nf-wow64apiset-getsystemwow64directorya)oder [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) mit **CSIDL \_ SYSTEMX86** auf, um diesen Verzeichnispfad abzurufen. Wenn Sie [Windows Installer](/windows/desktop/Msi/about-windows-installer)verwenden, verwenden Sie alternativ die [**SystemFolder-Eigenschaft.**](/windows/desktop/Msi/systemfolder)
-   Installieren Sie 64-Bit-IME-DLLs im Systemverzeichnis System32. Rufen [**Sie GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya)oder **SHGetFolderPath** mit [CSIDL \_ SYSTEM](/windows/desktop/shell/csidl) auf, um diesen Verzeichnispfad abzurufen. Oder verwenden Sie für Windows Installer die [**System64Folder-Eigenschaft.**](/windows/desktop/Msi/system64folder)

**Textdienst-DLLs und zugehörige Binärdateien**

Installieren Sie auf 64-Bit-Windows-Plattformen die 32-Bit- und 64-Bit-Textdienst-DLLs sowie alle anderen Binärdateien im Zusammenhang mit Ihrem Textdienst oder IME in den folgenden Verzeichnissen:

-   Installieren Sie 32-Bit-Textdienst-DLLs und alle anderen 32-Bit-Binärdateien in einem Unterverzeichnis im Verzeichnis Programme (x86). Rufen Sie **SHGetFolderPath** mit **CSIDL \_ PROGRAM \_ FILESX86** auf, um diesen Verzeichnispfad abzurufen. Oder verwenden Sie für Windows Installer die [**ProgramFilesFolder-Eigenschaft.**](/windows/desktop/Msi/programfilesfolder)
-   Installieren Sie 64-Bit-Textdienst-DLLs und alle anderen 64-Bit-Binärdateien in einem Unterverzeichnis unter dem Verzeichnis Programme. Rufen **Sie SHGetFolderPath** mit **CSIDL \_ PROGRAM \_ FILES** auf, um diesen Verzeichnispfad abzurufen. Oder verwenden Sie für Windows Installer die [**ProgramFiles64Folder-Eigenschaft.**](/windows/desktop/Msi/programfiles64folder)

Wenn Sie zum Installieren des IME- oder Textdiensts kein Windows Installer-Paket verwenden, wird dringend empfohlen, dass Sie eine 64-Bit-Installationsanwendung verwenden. Der WOW64-Dateisystem-Redirector kann dazu führen, dass 32-Bit-Installationsprogramme Dateien in den falschen Verzeichnissen platzieren (z. B. kann die UMLEITUNG DES WOW64-Dateisystems dazu führen, dass Dateien, die für das Verzeichnis System32 vorgesehen sind, stattdessen im SysWOW64-Verzeichnis installiert werden). Wenn Sie ein 32-Bit-Installationsprogramm verwenden müssen, deaktivieren Sie die WOW64-Dateiumleitung während des Installationsvorgangs, um sicherzustellen, dass der Dateiumleitungsdienst während der Installation keine unbeabsichtigte Umleitung verursacht. Informationen zum WOW64-Dateisystem-Redirector finden Sie unter [Dateisystem-Redirector.](/windows/desktop/WinProg64/file-system-redirector) Informationen zum Deaktivieren oder Aktivieren der WOW64-Dateisystemumleitung finden Sie unter [**Wow64EnableWow64FsRedirection.**](/windows/desktop/api/winbase/nf-winbase-wow64enablewow64fsredirection)

> [!TIP]
>
> Vermeiden Sie hart codierte Installationspfade. Weitere Informationen finden Sie unter [Suchen von Verzeichnissen mithilfe der Anwendungsprogrammierschnittstelle nicht Hard-Coded Pfaden.](/previous-versions//ms675638(v=vs.85))

 

> [!IMPORTANT]
>
> Installieren Sie keine IME- oder Textdateien im speziellen Verzeichnis %WINDIR% \\ IME (standardmäßig c: \\ Windows \\ IME ). Dieses Verzeichnis enthält Systemdateien, die Textdienste und IMEs unterstützen. sie ist nicht für IME- oder Textdienstdateien von Drittanbietern vorgesehen, und die UMLEITUNG DES WOW64-Dateisystems wird für dieses Verzeichnis nicht unterstützt.

 

## <a name="dual-ctfmonexe-processes-run-on-64-bit-windows-platforms"></a>Dual-Ctfmon.exe-Prozesse werden auf 64-Bit-Windows-Plattformen ausgeführt

Der ctfmon.exe-Prozess verwaltet die Textdienstframework auf dem Desktop und stellt auch die Benutzeroberfläche der Sprachleiste bereit. Auf 64-Bit-Windows werden eine 32-Bit-Version und eine 64-Bit-Version des ctfmon.exe-Prozesses gleichzeitig ausgeführt. Der 64-Bit-ctfmon.exe-Prozess verwaltet 64-Bit-Textdienste, und ebenso verwaltet der 32-Bit-ctfmon.exe-Prozess 32-Bit-Textdienste.

## <a name="display-behavior-for-different-versions-of-the-language-bar-ui"></a>Anzeigeverhalten für verschiedene Versionen der Benutzeroberfläche der Sprachleiste

Auf 64-Bit-Windows wird nur die Sprachleistenbenutzeroberfläche angezeigt, die der 64-Bit-Version eines Textdiensts zugeordnet ist. In Fällen, in denen eine 32-Bit-Anwendung die 32-Bit-Version eines Textdiensts verwendet, fügt Windows automatisch die Benutzeroberfläche der Sprachleiste für den entsprechenden 64-Bit-Textdienst ein. Dadurch wird sichergestellt, dass keine besondere Arbeit erforderlich ist, damit 32-Bit-Textdienste in der 64-Bit-Version der Sprachleiste angezeigt werden.

## <a name="control-panel-considerations-on-64-bit-windows"></a>Systemsteuerung Überlegungen zu 64-Bit-Windows

64-Bit-Windows ermöglicht den Zugriff auf 32-Bit- und 64-Bit-Versionen von Textdiensten und IMEs über Systemsteuerung. Um auf Systemsteuerung für bestimmte Versionen von Textdiensten oder IMEs zu zugreifen, sehen Sie sich die folgenden Speicherorte an.

-   **Systemsteuerung für 32-Bit-Textdienste und IMEs:** Start -> Einstellungen -> Systemsteuerung -> x86-Systemsteuerung Symbole
-   **Systemsteuerung für 64-Bit-Textdienste und IMEs:** Start -> Einstellungen -> Systemsteuerung -> Regional- und Sprachoptionen

Möglicherweise sind einige Einstellungen nur über die 32-Bit-Systemsteuerung. Stellen Sie in diesen Fällen sicher, dass Benutzer Ihres Textdiensts oder IME dies wissen, indem Sie entsprechende Dokumentation bereitstellen oder Benutzeroberflächenhinweise in Ihrer 64-Bit-Einstellungsschnittstelle anbieten.

 

 