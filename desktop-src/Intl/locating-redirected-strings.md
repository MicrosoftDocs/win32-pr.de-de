---
description: In diesem Thema wird erläutert, wie Sie umgeleitete Registrierungs Zeichenfolgen suchen. Weitere Informationen finden Sie unter Verwenden der Umleitung von Registrierungs Zeichenfolgen.
ms.assetid: 03d1512f-35a6-4b3a-9a0e-97e17bd9b126
title: Suchen umgeleitet-Zeichen folgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f11600ad57c04de54d914c2c876b67967dfa1467
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368161"
---
# <a name="locating-redirected-strings"></a>Suchen umgeleitet-Zeichen folgen

In diesem Thema wird erläutert, wie Sie umgeleitete Registrierungs Zeichenfolgen suchen. Weitere Informationen finden Sie unter [Verwenden der Umleitung von Registrierungs Zeichenfolgen](using-registry-string-redirection.md).

## <a name="load-a-language-neutral-registry-value"></a>Laden eines Language-Neutral Registrierungs Werts

Unter Windows Vista und höher verwendet die MUI-Anwendung einen sprach neutralen Registrierungs Wert, um den Zugriff auf sprachspezifische Zeichen folgen zu ermöglichen, die in einer Zeichen folgen-Ressourcen Tabelle gespeichert sind. Weitere Informationen finden Sie unter Erstellen einer Language-Neutral Ressource in [mithilfe der Umleitung von Registrierungs Zeichenfolgen](using-registry-string-redirection.md).

Anwendungscode, der den sprach neutralen Wert aus der Registrierung liest, sollte die Zeichen folgen in der richtigen Sprache der Benutzeroberfläche durch Aufrufen von [**regloadmuistringw**](/windows/win32/api/winreg/nf-winreg-regloadmuistringa)laden. Wenn Sie diese Funktion verwenden, muss sich die Anwendung nicht explizit mit dem Laden von Ressourcen befassen.

Wenn Sie eine vorhandene Anwendung auf die sprachneutrale Verwendung der Registrierung aktualisieren, behalten Sie in der Regel die vorhandenen Zeichen folgen Werte, die auf Englisch oder in einer anderen Sprache in der Registrierung lokalisiert sind, als Fallbacks und aus Gründen der Abwärtskompatibilität. Wenn eine Literalzeichenfolge in der Registrierung beibehalten wird, kann die Anwendung auf die Literalzeichenfolge zurückgreifen, wenn ein Rückruf von [**regloadmuistringw**](/windows/win32/api/winreg/nf-winreg-regloadmuistringa) fehlschlägt. Sie müssen entscheiden, wie ein solcher Fallback implementiert werden soll, da MUI eine solche Implementierung nicht unterstützt.

## <a name="use-shell-api-to-set-shortcut-strings-from-the-registry"></a>Verwenden der shellapi zum Festlegen von Verknüpfungs Zeichenfolgen aus der Registrierung

Die Anwendung kann die Shell-API verwenden, um Zeichen folgen für Verknüpfungen zu erstellen, mit denen Dateien oder Ordner im **Startmenü** oder auf dem Desktop verknüpft werden. Weitere Informationen finden Sie unter Erstellen von Ressourcen für Tastenkombinationen in [mithilfe der Umleitung von Registrierungs Zeichenfolgen](using-registry-string-redirection.md).

Die Anwendung kann [**shsetlocalizedname**](/windows/win32/api/shellapi/nf-shellapi-shsetlocalizedname) verwenden, um den MUI-kompatiblen anzeigen Amen für eine Verknüpfung zu laden. Zum Festlegen des zugeordneten infotip sollte [**IShellLink:: setDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) verwendet werden. Die Aufrufe registrieren die Zeichen folgen bei der Registrierung. Sehen Sie sich die folgenden Beispiele an, für die "HKCR" den Stamm Registrierungsschlüssel der HKEY- \_ Klassen darstellt \_ :


```C++
HKCR,"CLSID\%CLSID_AntiSpyware%",,,"Windows AntiSpyware"

HKCR,"CLSID\%CLSID_AntiSpyware%","LocalizedString",,"@%ProgramFiles%\Windows AntiSpyware\MSASCui.exe,-104"

HKCR,"CLSID\%CLSID_AntiSpyware%","InfoTip",,"@%ProgramFiles%\Windows AntiSpyware\MSASCui.exe,-208"
```



Die erste Zeile stellt eine nicht lokalisierte Literalzeichenfolge für die Fall Back-und Abwärtskompatibilität bereit. In der zweiten Zeile wird die MUI-kompatible Methode zum Registrieren des anzeigen Amens angezeigt. Diese Zeile gibt den Zeichen folgen Bezeichner 104 an, der in Msascui.exe (für Windows XP) oder in der zugehörigen sprachspezifischen Datei (für Windows Vista) gespeichert ist. Dieser Zeichen folgen Bezeichner entspricht "meine Netzwerk Orte". In der dritten Zeile des Beispiels wird die infotip-Registrierung behandelt. % CLSID \_ AntiSpyware% gibt eine Umgebungsvariable an, die die GUID darstellt, die mit dem Klassen Bezeichner dieser Komponente übereinstimmt.

Für das oben gezeigte Beispiel ruft die Anwendung [**shsetlocalizedname**](/windows/win32/api/shellapi/nf-shellapi-shsetlocalizedname) auf, um den Pfad der ausführbaren Datei für die ersten beiden Parameter anzugeben, und gibt *idsres* als "@% Program Files% \\ Windows AntiSpyware \\MSASCui.exe, 104" an. Ein Aufrufen von [**IShellLink:: setDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription)gibt den Pfad für den infotip als "@% Program Files% \\ Windows AntiSpyware \\MSASCui.exe, 208" an.

## <a name="query-friendly-document-type-names-in-the-registry"></a>Abfragen von anzeigen Amen für Dokumenttyp in der Registrierung

Informationen zur Ressourcen Erstellung für benutzerfreundliche Dokumenttyp Namen finden Sie unter Erstellen von Ressourcen für benutzerfreundliche Dokumenttyp Namen in [mithilfe der Umleitung von Registrierungs Zeichenfolgen](using-registry-string-redirection.md). Um einen anzeigen Amen für Dokumente abzufragen, sollte die Anwendung [**iqueryassociations:: init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init)verwenden, gefolgt von einem [**iqueryassociations:: GetString**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-getstring)-aufrufen. Der **iqueryassociations:: init** -Aufrufe gibt den Dokumenttyp an, z. b. ". txt". Beim Aufrufen von **iqueryassociations:: GetString** muss als Zeichen folgen Bezeichner "assocstr \_ friendlydocname" angegeben werden.

## <a name="register-microsoft-management-console-snap-in-strings-not-read-from-the-registry"></a>Microsoft Management Console-Snap-in-Zeichen folgen registrieren, die nicht aus der Registrierung gelesen werden

Ihre Anwendung kann ein Microsoft Management Console (MMC)-Snap-in verwenden, um die Verwaltungsaufgaben zu hosten. Die meisten Zeichen folgen werden mithilfe der Registrierungs Einstellungen, die unter Erstellen von Zeichen folgen Ressourcen für Microsoft Management Snap-Ins Console beschrieben werden, mithilfe der [Umleitung von Registrierungs Zeichenfolgen](using-registry-string-redirection.md)als Ressourcen behandelt Allerdings registrieren einige Snap-Ins Registrierungs Zeichenfolgen-Werte, die von MMC nicht aus der Registrierung gelesen werden können. In diesem Fall muss das Snap-in die Werte mithilfe der [**ISnapinAbout**](/windows/win32/api/mmc/nn-mmc-isnapinabout) -Schnittstelle abrufen, die MUI-kompatibel ist.

## <a name="set-the-display-name-and-description-for-a-windows-service-from-the-registry"></a>Legen Sie den anzeigen Amen und die Beschreibung für einen Windows-Dienst aus der Registrierung fest.

Wenn Ihre MUI-Anwendung einen Windows-Dienst verwendet, muss der Anzeige Name und die Beschreibung des dienstanwendungs angezeigt werden. Die zugehörigen Ressourcen werden unter [Verwenden der Umleitung von Registrierungs Zeichenfolgen](using-registry-string-redirection.md)unter "Erstellen von Zeichen folgen Ressourcen für einen Windows-Dienst" erläutert.

Um den anzeigen amen des Diensts festzulegen, ruft die MUI-Anwendung " [**kreateservice**](/windows/win32/api/winsvc/nf-winsvc-createservicea) " oder " [**ChangeServiceConfig**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga)" auf. Der Name ist eine Zeichenfolge im Format " `@<PE-path>,-<stringID>[;<comment>]` ". Wenn Ihr Dienst z. b. durch eine DLL-Datei mit dem Pfad% Program Files% \\ % myPath% \\MyDll.dll implementiert wird und der Zeichen folgen Bezeichner des sprachspezifischen anzeigen Amens 347 lautet, wird der-Parameter als " `@%ProgramFiles%\\%MyPath%\\MyDll.dll,-347` " angegeben. Die doppelten umgekehrten Schrägstriche ( \\ \\ ) sind erforderlich, da C/C++ den umgekehrten Schrägstrich als Escapezeichen in Zeichen folgen verwendet.

Um die sprachspezifische Dienst Beschreibung festzulegen, sollte die MUI-Anwendung den **lpdescription** -Member einer [**Dienst \_ Beschreibungs**](/windows/win32/api/winsvc/ns-winsvc-service_descriptiona) Struktur so angeben, dass eine Zeichenfolge der Form " `@<PE-path>,-<stringID>[;<comment>]` " angegeben wird. dabei wird auf den entsprechenden Zeichen folgen Bezeichner verwiesen. Dann ruft die Anwendung [**ChangeServiceConfig2**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfig2a) mit dem *dwinfolevel* -Parameter auf, der als Dienst Konfigurations Beschreibung angegeben ist, \_ und der \_ Parameter *lpInfo* , der als **Dienst \_ Beschreibungs** Struktur angegeben ist

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Suchen von Win32 PE-Ressourcen](locating-win32-pe-resources.md)
</dt> <dt>

[Verwenden von Registrierungs Zeichenfolgen](using-registry-string-redirection.md)
</dt> </dl>

 

 
