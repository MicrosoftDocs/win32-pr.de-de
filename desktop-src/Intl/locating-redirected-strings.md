---
description: In diesem Thema werden Programmieranweisungen zum Suchen von umgeleiteten Registrierungszeichenfolgen erläutert. Weitere Informationen finden Sie unter Verwenden der Registrierungszeichenfolgenumleitung.
ms.assetid: 03d1512f-35a6-4b3a-9a0e-97e17bd9b126
title: Suchen von umgeleiteten Zeichenfolgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9c4e1a46b2c12af839e4c5b562eba18a80c8e814e5a6071dca925a14a46d0ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788480"
---
# <a name="locating-redirected-strings"></a>Suchen von umgeleiteten Zeichenfolgen

In diesem Thema werden Programmieranweisungen zum Suchen von umgeleiteten Registrierungszeichenfolgen erläutert. Weitere Informationen finden Sie unter [Verwenden der Registrierungszeichenfolgenumleitung.](using-registry-string-redirection.md)

## <a name="load-a-language-neutral-registry-value"></a>Laden eines Language-Neutral Registrierungswerts

Unter Windows Vista und höher verwendet die PROGRAMM-Anwendung einen sprachneutralen Registrierungswert, um den Zugriff auf sprachspezifische Zeichenfolgen zu ermöglichen, die in einer Zeichenfolgenressourcentabelle gespeichert sind. Weitere Informationen finden Sie unter Erstellen einer Language-Neutral-Ressource in [Using Registry String Redirection](using-registry-string-redirection.md).

Anwendungscode, der den sprachneutralen Wert aus der Registrierung liest, sollte die Zeichenfolgen in der richtigen Benutzeroberflächensprache laden, indem [**RegLoadMUIStringW aufruft.**](/windows/win32/api/winreg/nf-winreg-regloadmuistringa) Wenn Sie diese Funktion verwenden, muss sich Ihre Anwendung nicht explizit mit dem Laden von Ressourcen befassen.

Wenn Sie eine vorhandene Anwendung auf die sprachneutrale Verwendung der Registrierung aktualisieren, behalten Sie in der Regel die vorhandenen Zeichenfolgenwerte, lokalisiert in Englisch oder in einer anderen einzelnen Sprache in der Registrierung, als Fallbacks und aus Gründen der Abwärtskompatibilität bei. Wenn eine Literalzeichenfolge in der Registrierung gespeichert wird, kann die Anwendung auf die literale Zeichenfolge zurückfallen, wenn ein Aufruf von [**RegLoadMUIStringW fehlschlägt.**](/windows/win32/api/winreg/nf-winreg-regloadmuistringa) Sie müssen entscheiden, wie ein solches Fallback implementiert werden soll, da DIES keine Unterstützung für eine solche Implementierung bietet.

## <a name="use-shell-api-to-set-shortcut-strings-from-the-registry"></a>Verwenden der Shell-API zum Festlegen von Verknüpfungszeichenfolgen aus der Registrierung

Ihre Anwendung kann die Shell-API verwenden, um Zeichenfolgen für Verknüpfungen zu erstellen, die Dateien oder Ordner im **Startmenü** oder auf dem Desktop verknüpfen. Weitere Informationen finden Sie unter Erstellen von Ressourcen für Verknüpfungszeichenfolgen in [Using Registry String Redirection](using-registry-string-redirection.md).

Die Anwendung kann [**SHSetLocalizedName**](/windows/win32/api/shellapi/nf-shellapi-shsetlocalizedname) verwenden, um den BEZEICHNUNG-konformen Anzeigenamen für eine Verknüpfung zu laden. Sie sollte [**IShellLink::SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription) verwenden, um den zugeordneten InfoTip festlegen. Die Aufrufe registrieren die Zeichenfolgen bei der Registrierung. Betrachten Sie die folgenden Beispiele, für die "HKCR" den HKEY \_ CLASSES \_ ROOT-Registrierungsschlüssel darstellt:


```C++
HKCR,"CLSID\%CLSID_AntiSpyware%",,,"Windows AntiSpyware"

HKCR,"CLSID\%CLSID_AntiSpyware%","LocalizedString",,"@%ProgramFiles%\Windows AntiSpyware\MSASCui.exe,-104"

HKCR,"CLSID\%CLSID_AntiSpyware%","InfoTip",,"@%ProgramFiles%\Windows AntiSpyware\MSASCui.exe,-208"
```



Die erste Zeile stellt aus Gründen der Fallback- und Abwärtskompatibilität eine nicht lokalisierte Literalzeichenfolge zur Unterstützung von Fallbacks und Abwärtskompatibilitäten zurVerfingung von Literalzeichenfolgen zur Veralten. Die zweite Zeile zeigt die MIT-kompatible Methode zum Registrieren des Anzeigenamens. Diese Zeile gibt den Zeichenfolgenbezeichner 104 an, der in Msascui.exe (für Windows XP) oder in der zugehörigen sprachspezifischen Datei (für Windows Vista) gespeichert ist. Dieser Zeichenfolgenbezeichner entspricht "My Network Places". Die dritte Zeile im Beispiel verarbeitet die InfoTip-Registrierung. %CLSID AntiSpyware% gibt eine Umgebungsvariable an, die die GUID darstellt, die dem \_ Klassenbezeichner dieser Komponente entspricht.

Im oben gezeigten Beispiel ruft die Anwendung [**SHSetLocalizedName**](/windows/win32/api/shellapi/nf-shellapi-shsetlocalizedname) auf, um den Pfad der ausführbaren Datei für die ersten beiden Parameter anzugeben, und *idsRes* als "@%ProgramFiles% \\ Windows AntiSpyware \\MSASCui.exe,104". Ein Aufruf von [**IShellLink::SetDescription**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setdescription)gibt den Pfad für den InfoTip als "@%ProgramFiles% \\ Windows AntiSpyware \\MSASCui.exe,208" an.

## <a name="query-friendly-document-type-names-in-the-registry"></a>Abfragefreundliche Dokumenttypnamen in der Registrierung

Die Ressourcenerstellung für benutzerfreundliche Dokumenttypnamen wird unter Erstellen von Ressourcen für benutzerfreundliche Dokumenttypnamen in [Using Registry String Redirection (Verwenden der Registrierungszeichenfolgenumleitung) erläutert.](using-registry-string-redirection.md) Zum Abfragen eines benutzerfreundlichen Dokumentnamens sollte die Anwendung [**IQueryAssociations::Init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init)gefolgt von einem Aufruf von [**IQueryAssociations::GetString verwenden.**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-getstring) Der Aufruf von **IQueryAssociations::Init** gibt den Dokumenttyp an, z. B. ".txt". Der Aufruf von **IQueryAssociations::GetString** muss ASSOCSTR \_ FRIENDLYDOCNAME als Zeichenfolgenbezeichner angeben.

## <a name="register-microsoft-management-console-snap-in-strings-not-read-from-the-registry"></a>Registrieren Microsoft Management Console Snap-In-Zeichenfolgen, die nicht aus der Registrierung gelesen werden

Ihre Anwendung kann ein MICROSOFT MANAGEMENT CONSOLE-Snap-In (MMC) verwenden, um ihre Verwaltungsaufgaben zu hosten. Die meisten Zeichenfolgen werden als Ressourcen mithilfe der Registrierungseinstellungen behandelt, die unter Erstellen von Zeichenfolgenressourcen für Microsoft Management Console Snap-Ins in [Verwenden der Registrierungszeichenfolgenumleitung beschrieben werden.](using-registry-string-redirection.md) Einige Snap-Ins registrieren jedoch Registrierungszeichenfolgenwerte, die MMC nicht aus der Registrierung lesen kann. In diesem Fall muss das Snap-In die Werte mithilfe der [**ISnapinAbout-Schnittstelle**](/windows/win32/api/mmc/nn-mmc-isnapinabout) abrufen, die mit DER KOMPATIBEL ist.

## <a name="set-the-display-name-and-description-for-a-windows-service-from-the-registry"></a>Festlegen des Anzeigenamens und der Beschreibung für einen Windows Dienst aus der Registrierung

Wenn IhreSTELLUNG-Anwendung einen Windows verwendet, muss sie den Anzeigenamen und die Beschreibung des Diensts anzeigen. Die zugeordneten Ressourcen werden unter "Erstellen von Zeichenfolgenressourcen für einen Windows-Dienst" in [Using Registry String Redirection (Verwenden der Registrierungszeichenfolgenumleitung) erläutert.](using-registry-string-redirection.md)

Zum Festlegen des Anzeigenamens des Diensts ruft die ANWENDUNG FÜR DIE Anwendung [**CreateService**](/windows/win32/api/winsvc/nf-winsvc-createservicea) oder [**ChangeServiceConfig auf.**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfiga) Der Name ist eine Zeichenfolge der Form " `@<PE-path>,-<stringID>[;<comment>]` ". Wenn Ihr Dienst beispielsweise von einer .dll-Datei mit dem Pfad %ProgramFiles% %MyPath%MyDll.dll implementiert wird und der Zeichenfolgenbezeichner des sprachspezifischen Anzeigenamens \\ 347 ist, wird der Parameter als \\ " " `@%ProgramFiles%\\%MyPath%\\MyDll.dll,-347` angegeben. Die doppelten schrägen Schrägstriche ( ) sind erforderlich, da C/C++ den schrägen Schrägstrich als Escapezeichen \\ \\ in Zeichenfolgen verwendet.

Zum Festlegen der sprachspezifischen Dienstbeschreibung sollte die PROGRAMM-Anwendung den **lpDescription-Member** einer [**SERVICE \_ DESCRIPTION-Struktur**](/windows/win32/api/winsvc/ns-winsvc-service_descriptiona) auf eine Zeichenfolge vom Typ " " verweisen und auf den entsprechenden Zeichenfolgenbezeichner `@<PE-path>,-<stringID>[;<comment>]` verweisen. Anschließend ruft die Anwendung [**ChangeServiceConfig2**](/windows/win32/api/winsvc/nf-winsvc-changeserviceconfig2a) mit dem Parameter *dwInfoLevel* auf, der als SERVICE CONFIG DESCRIPTION angegeben ist, und dem Parameter \_ \_ *lpInfo,* der als **SERVICE \_ DESCRIPTION-Struktur angegeben** ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Suchen von Win32 PE-Ressourcen](locating-win32-pe-resources.md)
</dt> <dt>

[Verwenden der Umleitung von Registrierungszeichenfolgen](using-registry-string-redirection.md)
</dt> </dl>

 

 
