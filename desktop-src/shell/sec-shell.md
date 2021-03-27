---
description: Dieses Thema enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit der Windows-Shell.
ms.assetid: eca31652-2659-456d-b082-c84d6fd39094
title: 'Überlegungen zur Sicherheit: Microsoft Windows Shell'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b11a965a36a403b57a3e5229fc758a4ce37252
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753048"
---
# <a name="security-considerations-microsoft-windows-shell"></a>Überlegungen zur Sicherheit: Microsoft Windows Shell

Dieses Thema enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit der Windows-Shell. Dieses Dokument kann nicht alles bereitstellen, was Sie über Sicherheitsprobleme wissen müssen – verwenden Sie es stattdessen als Ausgangspunkt und Verweis für diesen speziellen Technologiebereich.

Die Shell steuert eine Reihe wichtiger Aspekte des Systems, einschließlich mehrerer, die potenzielle Sicherheitsrisiken darstellen, wenn Sie nicht ordnungsgemäß behandelt werden. In diesem Thema werden einige der gängigeren Probleme und deren Behebung in Ihren Anwendungen erläutert. Beachten Sie, dass Sicherheit nicht auf Internet basierte Exploits beschränkt ist. Auf freigegebenen Systemen, einschließlich Systemen, auf die über Terminal Dienste zugegriffen werden kann, müssen Sie sicherstellen, dass Benutzer nichts tun können, was anderen Benutzern das System möglicherweise schadet.

-   [Ordnungsgemäße Installation der Anwendung](#installing-your-application-properly)
-   [Shlwapi](#shlwapi)
-   [AutoVervollständigen](#autocomplete)
-   [ShellExecute, ShellExecuteEx und verwandte Funktionen](#shellexecute-shellexecuteex-and-related-functions)
-   [Verschieben und Kopieren von Dateien](#moving-and-copying-files)
-   [Schreiben sicherer Namespace Erweiterungen](#writing-secure-namespace-extensions)
-   [Sicherheitswarnungen](#security-alerts)
-   [Zugehörige Themen](#related-topics)

## <a name="installing-your-application-properly"></a>Ordnungsgemäße Installation der Anwendung

Die Mehrzahl potenzieller shellsicherheitsprobleme können durch eine ordnungsgemäße Installation der Anwendung behoben werden.

-   Installieren Sie die Anwendung unter dem Ordner "Programme". 

    | Betriebssystem                             | Standort                                                                                                                                                                                                                                   |
    |----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Windows XP, Windows Server 2003 und früher | CSIDL- \_ Programm \_ Dateien                                                                                                                                                                                                                      |
    | Windows Vista und höher                      | Folderid \_ Program Files, folderid \_ ProgramFilesX86, folderid \_ ProgramFilesX64, folderid \_ programfilescommon, folderid \_ ProgramFilesCommonX86 oder folderid \_ ProgramFilesCommonX64. Einzelheiten finden Sie unter [**KNOWNFOLDERID**](knownfolderid.md) . |

    

     

-   Speichern Sie Benutzerdaten nicht im Ordner "Programme".

    Verwenden Sie den entsprechenden Datenordner für Daten, die allen Benutzern gemeinsam sind.

    

    | Betriebssystem                             | Standort               |
    |----------------------------------------------|------------------------|
    | Windows XP, Windows Server 2003 und früher | Allgemeine CSIDL- \_ \_ AppData |
    | Windows Vista und höher                      | Folderid- \_ programmdata  |

    

     

    Verwenden Sie den entsprechenden Ordner für Benutzerdaten für Daten, die zu einem bestimmten Benutzer gehören.

    

    | Betriebssystem                             | Standort                                                   |
    |----------------------------------------------|------------------------------------------------------------|
    | Windows XP, Windows Server 2003 und früher | CSIDL \_ AppData, CSIDL \_ Personal und andere.               |
    | Windows Vista und höher                      | Folderid \_ roamingappdata, folderid \_ -Dokumente und andere. |

    

     

-   Wenn Sie an einem anderen Speicherort als dem Ordner "Programme" installieren müssen, stellen Sie sicher, dass Sie Zugriffs Steuerungs Listen (ACLs) ordnungsgemäß festlegen, damit Benutzer nicht auf ungeeignete Teile des Dateisystems zugreifen können. Alle Daten, die für einen bestimmten Benutzer spezifisch sind, sollten über eine ACL verfügen, die verhindert, dass andere Benutzer darauf zugreifen können.
-   Wenn Sie Dateizuordnungen einrichten, stellen Sie sicher, dass Sie die Befehlszeile ordnungsgemäß angeben. Verwenden Sie einen voll qualifizierten Pfad, und packen Sie alle Elemente, die Leerzeichen enthalten, in Anführungszeichen. Umbruch von Befehlsparametern in separaten Anführungszeichen. Andernfalls wird die Zeichenfolge möglicherweise falsch analysiert, und die Anwendung wird nicht ordnungsgemäß gestartet. Hier werden zwei Beispiele für ordnungsgemäß formatierte Befehlszeilen angezeigt.

    ```
    "C:\Program Files\MyApp\MyApp.exe" "%1" "%2"
    C:\MyAppDir\MyApp\MyApp.exe "%1"
    ```

    

> [!Note]  
> Der Speicherort der Standard Installationsordner kann von System zu System abweichen. Um den Speicherort eines Standard Ordners für ein bestimmtes Windows Vista-oder ein späteres System zu erhalten, wenden Sie [**shgetknownfolderpath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetknownfolderpath) mit dem entsprechenden [**KNOWNFOLDERID**](knownfolderid.md) -Wert an. In Windows XP, Windows Server 2003 oder früheren Systemen, rufe Sie [**shgetfolderlocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) oder [**SHGetFolderPath**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderpatha) mit dem entsprechenden [**CSIDL**](csidl.md) -Wert auf.

 

## <a name="shlwapi"></a>Shlwapi

Die Shell Lightweight API (shlwapi) umfasst eine Reihe von Funktionen zur Zeichen folgen Bearbeitung. Wenn diese Funktionen nicht ordnungsgemäß verwendet werden, kann dies zu unerwarteten abgeschnittene Zeichen folgen führen, ohne dass eine Benachrichtigung über die zurückgegebene abgeschnittene In den folgenden Fällen sollten die shlwapi-Funktionen nicht verwendet werden. Die aufgeführten Alternativen Funktionen, die weniger Risiken darstellen, sollten an ihrer Stelle verwendet werden.



| Shlwapi-Funktion                                                 | Alternative Funktion                                                                                             |
|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| " [**Strauch**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw)", "[**strauncat** "](/windows/desktop/api/Shlwapi/nf-shlwapi-strncata)              | [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**stringcbcat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata) und verwandte Funktionen             |
| " [**Strincpy**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw)", " [ **straucpyn** "](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw)             | [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**stringcbcopy**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya) und verwandte Funktionen         |
| [**wnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa), [ **wvnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa) | [**StringCchPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfa), [**stringcbprintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa) und verwandte Funktionen |



 

Legen Sie mit Funktionen wie [**pathrelativepathto**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathrelativepathtoa) , die einen Dateipfad zurückgeben, die Größe des Puffers immer auf Max \_ . Pfad Zeichen fest. Dadurch wird sichergestellt, dass der Puffer groß genug ist, um den größtmöglichen Dateipfad und ein abschließendes NULL-Zeichen zu speichern.

Weitere Informationen zu den alternativen Zeichen folgen Funktionen finden Sie unter [Informationen zu "tresafe. h](../menurc/strsafe-ovw.md)".

## <a name="autocomplete"></a>AutoVervollständigen

Verwenden Sie die Funktion "Auto Vervollständigen" nicht für Kenn Wörter.

## <a name="shellexecute-shellexecuteex-and-related-functions"></a>ShellExecute, ShellExecuteEx und verwandte Funktionen

Es gibt mehrere Shellfunktionen, mit denen Sie Anwendungen starten können: [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa), [**winexec**](/windows/win32/api/winbase/nf-winbase-winexec)und [**shkreateprocessasuserw**](/windows/desktop/api/Shellapi/nf-shellapi-shcreateprocessasuserw). Stellen Sie sicher, dass Sie eine eindeutige Definition der Anwendung angeben, die ausgeführt werden soll.

-   Wenn Sie den Pfad der ausführbaren Datei bereitstellen, geben Sie den voll qualifizierten Pfad an. Verwenden Sie die Shell nicht, um nach der Datei zu suchen.
-   Wenn Sie eine Befehlszeilen Zeichenfolge bereitstellen, die Leerzeichen enthält, schließen Sie die Zeichenfolge in Anführungszeichen ein. Andernfalls interpretiert der Parser möglicherweise ein einzelnes Element, das Leerzeichen als mehrere Elemente enthält.

## <a name="moving-and-copying-files"></a>Verschieben und Kopieren von Dateien

Ein Schlüssel für die Systemsicherheit ist das ordnungsgemäße Zuweisen von ACLs. Sie können auch verschlüsselte Dateien verwenden. Stellen Sie sicher, dass beim Verschieben oder Kopieren von Dateien die richtige ACL zugewiesen wird und dass Sie nicht versehentlich entschlüsselt wurden. Dies umfasst auch das Verschieben von Dateien in den **Papierkorb** und innerhalb des Dateisystems. Verwenden Sie [**IFileOperation**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifileoperation) (Windows Vista oder höher) oder [**SHFileOperation**](/windows/desktop/api/Shellapi/nf-shellapi-shfileoperationa) (Windows XP und früher). Verwenden Sie nicht " [**muvefile**](/windows/win32/api/winbase/nf-winbase-movefile)", wodurch möglicherweise nicht die erwartete ACL für die Zieldatei festgelegt wird.

## <a name="writing-secure-namespace-extensions"></a>Schreiben sicherer Namespace Erweiterungen

Shell-Namespace Erweiterungen sind eine leistungsstarke und flexible Möglichkeit, um dem Benutzerdaten zur Verfügung zu stellen. Allerdings können Sie einen Systemfehler verursachen, wenn Sie nicht ordnungsgemäß geschrieben wurden. Beachten Sie dabei einige wichtige Punkte:

-   Gehen Sie nicht davon aus, dass Daten wie Bilder ordnungsgemäß formatiert sind.
-   Gehen Sie nicht davon aus, dass \_ der maximale Pfad der Anzahl von *Bytes* in einer Zeichenfolge entspricht. Dabei handelt es sich um die Anzahl der *Zeichen*.

## <a name="security-alerts"></a>Sicherheitswarnungen

In der folgenden Tabelle werden einige Features aufgelistet, die ggf. die Sicherheit Ihrer Anwendungen beeinträchtigen können.



| Feature                                                                        | Minderung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea), [ **ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) | Suchvorgänge, die davon abhängen, dass eine Reihe von Standard Speicherorten zum Suchen nach einer bestimmten Datei überprüft wird, können in einem Spoofing-Angriff verwendet werden. Verwenden Sie einen voll qualifizierten Pfad, um sicherzustellen, dass Sie auf die gewünschte Datei zugreifen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**StrCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw)                                                       | Das erste Argument, *psz1*, muss groß genug sein, um *psz2* und das schließende ' \\ 0 ' aufzunehmen. andernfalls kann ein Pufferüberlauf auftreten. Verwenden Sie stattdessen eine der folgenden Alternativen. [**Stringcbcat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**stringcbcr Ex**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**stringcbcr n**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatna), [**stringcb-netX**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**stringcch|**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)Ex, [**stringcchkat}**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatna)oder [**stringcchkatkatx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa).                                                                                                                                                             |
| [**Strauch**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa)                                               | Es ist nicht garantiert, dass die endgültige Zeichenfolge mit NULL endet. Verwenden Sie stattdessen eine der folgenden Alternativen. [**Stringcbcat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**stringcbcr Ex**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**stringcbcr n**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatna), [**stringcb-netX**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**stringcch|**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)Ex, [**stringcchkat}**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatna)oder [**stringcchkatkatx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa).                                                                                                                                                                                                                                  |
| [**"Erw"**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw)                                           | Es ist nicht garantiert, dass die endgültige Zeichenfolge mit NULL endet. Verwenden Sie stattdessen eine der folgenden Alternativen. [**Stringcb-Ex**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**stringcbcr-x**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**stringcch| Ex**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)oder [**stringcchcr-x**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa).                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**StrCpy**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw)                                                       | Das erste Argument, *psz1*, muss groß genug sein, um *psz2* und das schließende ' \\ 0 ' aufzunehmen. andernfalls kann ein Pufferüberlauf auftreten. Verwenden Sie stattdessen eine der folgenden Alternativen. [**Stringcbcopy**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya), [**stringcbcopyex**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyexa), [**stringcbcopyn**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyna), [**stringcbcopynetx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopynexa), [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**stringcchcopyex**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa), [**stringcchcopyn**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyna)oder [**stringcchcopynetx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopynexa).                                                                                                                                             |
| [**"Straucpyn"**](/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw)                                                     | Es ist nicht garantiert, dass die kopierte Zeichenfolge auf NULL endet. Verwenden Sie stattdessen eine der folgenden Alternativen. [**Stringcbcopy**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopya), [**stringcbcopyex**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyexa), [**stringcbcopyn**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyna), [**stringcbcopynetx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopynexa), [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**stringcchcopyex**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa), [**stringcchcopyn**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyna), [**stringcchcopynetx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopynexa).                                                                                                                                                                                                                    |
| [**StrDup**](/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa)                                                       | [](/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa) Bei der über Bildung wird angenommen, dass *lpsz* eine auf NULL endenden Zeichenfolge ist. Außerdem ist die zurückgegebene Zeichenfolge nicht garantiert NULL-terminiert. Verwenden Sie stattdessen eine der folgenden Alternativen. [**Stringcbcat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**stringcbcopyex**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyexa), [**stringcbcopyn**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopyna), [**stringcbcopynetx**](/windows/win32/api/strsafe/nf-strsafe-stringcbcopynexa), [**StringCchCopy**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopya), [**stringcchcopyex**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyexa), [**stringcchcopyn**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopyna)oder [**stringcchcopynetx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcopynexa).                                                                                                                              |
| [**StrNCat**](/windows/desktop/api/Shlwapi/nf-shlwapi-strncata)                                                     | Das erste Argument, *pszfront*, muss groß genug sein, um *pszback* und das schließende ' \\ 0 ' aufzunehmen. andernfalls kann ein Pufferüberlauf auftreten. Beachten Sie, dass das letzte Argument, *cchmax*, die Anzahl der Zeichen ist, die in *pszfront* kopiert werden sollen, nicht notwendigerweise die Größe von *pszfront* in Bytes. Verwenden Sie stattdessen eine der folgenden Alternativen. [**Stringcbcat**](/windows/win32/api/strsafe/nf-strsafe-stringcbcata), [**stringcbcr Ex**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatexa), [**stringcbcr n**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatna), [**stringcb-netX**](/windows/win32/api/strsafe/nf-strsafe-stringcbcatnexa), [**StringCchCat**](/windows/win32/api/strsafe/nf-strsafe-stringcchcata), [**stringcch|**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatexa)Ex, [**stringcchkat}**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatna)oder [**stringcchkatkatx**](/windows/win32/api/strsafe/nf-strsafe-stringcchcatnexa). |
| [**wnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa)                                                 | Es ist nicht garantiert, dass die kopierte Zeichenfolge auf NULL endet. Verwenden Sie stattdessen eine der folgenden Alternativen. [**Stringcbprintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa), [**stringcbprintfex**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfexa), [**stringcbvprintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfa), [**stringcbvprintfex**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfexa), [**StringCchPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfa), [**stringcchprintfex**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfexa), [**stringcchvprintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfa)oder [**stringcchvprintfex**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfexa).                                                                                                                                                                                 |
| [**wvnsprintf**](/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa)                                               | Es ist nicht garantiert, dass die kopierte Zeichenfolge auf NULL endet. Verwenden Sie stattdessen eine der folgenden Alternativen. [**Stringcbprintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfa), [**stringcbprintfex**](/windows/win32/api/strsafe/nf-strsafe-stringcbprintfexa), [**stringcbvprintf**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfa), [**stringcbvprintfex**](/windows/win32/api/strsafe/nf-strsafe-stringcbvprintfexa), [**StringCchPrintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfa), [**stringcchprintfex**](/windows/win32/api/strsafe/nf-strsafe-stringcchprintfexa), [**stringcchvprintf**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfa)oder [**stringcchvprintfex**](/windows/win32/api/strsafe/nf-strsafe-stringcchvprintfexa).                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Microsoft Security](https://www.microsoft.com/security/default.aspx)
</dt> <dt>

[Security Developer Center](https://msdn.microsoft.com/security/)
</dt> <dt>

[Microsoft Solution Accelerators](/previous-versions/tn-archive/cc936627(v=technet.10))
</dt> <dt>

[Sicherheits-TechCenter](https://technet.microsoft.com/security/default.aspx)
</dt> <dt>

[Informationen zu "strausafe. h"](../menurc/strsafe-ovw.md)
</dt> </dl>

 

 
