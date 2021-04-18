---
description: Die Speicherung von hart codierten Zeichen folgen in der Registrierung ist Teil eines Lokalisierungs Modells vor Windows Vista.
ms.assetid: 70185942-7d32-4151-a4e1-f71cf45e87af
title: Verwenden von Registrierungs Zeichenfolgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287f6e1420aae0ff41c386e19852bebbd1a322c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351589"
---
# <a name="using-registry-string-redirection"></a>Verwenden von Registrierungs Zeichenfolgen

Die Speicherung von hart codierten Zeichen folgen in der Registrierung ist Teil eines Lokalisierungs Modells vor Windows Vista. Sie wird von MUI nicht unterstützt. Im aktuellen Modell wird die Benutzeroberfläche für das Betriebssystem in sprachspezifischen Ressourcen Dateien oberhalb einer sprach neutralen Basis ausgeführt. Die Komponenten des Betriebssystems verwenden die Registrierung auf sprachneutrale Weise.

MUI verwendet nur umgeleitete Registrierungs Zeichenfolgen, die von Win32 PE-Ressourcen in der Ressourcen Datei der Basis Sprache definiert werden. Die Umleitung wird separat definiert, z. b. in einer INF-Datei. Diese Art von Speicher ermöglicht es dem Ressourcen Lader, beim Laden von Ressourcen Modulen automatisch die richtigen Sprachressourcen auszuwählen.

> [!Note]  
> Dieses Thema bezieht sich nur auf Win32 PE-Ressourcen. Bei Verwendung von nicht-Win32 PE-Ressourcen müssen Sie ggf. eine angepasste Registrierung für die Registrierungs Zeichenfolge bereitstellen.

 

## <a name="create-a-language-neutral-resource"></a>Erstellen einer Language-Neutral Ressource

Eine MUI-Anwendung, die unter Windows Vista und höher ausgeführt wird, verwendet eine sprachneutrale Zeichen folgen Ressource, um den Zugriff auf sprachspezifische Zeichen folgen zuzulassen, die in einer Zeichen folgen Ressourcen Tabelle gespeichert sind. Anwendungscode, der diese Werte aus der Registrierung liest, wird im Abschnitt Laden eines Language-Neutral Registrierungs Werts untersuchen von [umgeleiteten](locating-redirected-strings.md)Zeichen folgen beschrieben.

Die Daten für einen sprach neutralen Registrierungs Wert haben das Format " `@<PE-path>,-<stringID>[;<comment>]` ", wobei Folgendes gilt:

-   *PE-Path* gibt den Pfad der ausführbaren Datei an. Sie können den Pfad mithilfe einer Umgebungsvariablen, z. b .% Program Files%, angeben, um die Bereitstellung zu unterstützen. Eine Alternative zum Erstellen des Zeichen folgen Verweises besteht darin, die Dateipfad Informationen auszulassen. In diesem Fall muss Ihre Anwendung über eine bestimmte Möglichkeit verfügen, z. b. einen anderen Registrierungs Wert, um Ihr eigenes Installationsverzeichnis zu kommunizieren.
-   *stringID* gibt den numerischen Ressourcen Bezeichner der relevanten Zeichen folgen Ressource an, die wie jede andere lokalisierbare Zeichen folgen Ressource implementiert wird.
-   der *Kommentar* gibt optionale Informationen zum Debuggen oder zur besseren Lesbarkeit des Registrierungs Werts an. Die Registrierungs-API-Funktionen ignorieren den Kommentar beim Laden der Zeichenfolge.

> [!Note]  
> Die Daten für den Registrierungs Wert machen keinen expliziten Verweis auf die sprachspezifische Ressourcen Datei. Die richtige Datei wird zur Laufzeit basierend auf den aktuellen Spracheinstellungen der Benutzeroberfläche festgelegt.

 

Ein Registrierungs Wert wird ohne Leerzeichen zwischen "," und "-" eingegeben. Ein korrekter Registrierungs Wert lautet wie folgt:

`shell32.dll,-22912`

Ein falscher Registrierungs Wert ist:

`shell32.dll, -22912`

Ein Beispiel aus Windows Vista ist der Registrierungs Wert mit den folgenden Daten:

`@%SystemRoot%\system32\input.dll,-5020`

## <a name="create-resources-for-shortcut-strings"></a>Erstellen von Ressourcen für Tastenkombinationen

Wenn die MUI-Anwendung den Namen in der shellbenutzerschnittstelle anzeigt, wird für das Anwendungssymbol eine infotip-Zeichenfolge angezeigt. Sie sollten Zeichen folgen Ressourcen für den anzeigen amen der Anwendung und die zugehörige infotip-Zeichenfolge für jede unterstützte Sprache erstellen. Wenn die Ressourcen bereit sind, kann Ihre Anwendung die Zeichen folgen verwenden, wie im Abschnitt Verwenden der Shell-API zum Laden von Verknüpfungs Zeichenfolgen aus dem Registrierungs Abschnitt untersuchen von [umgeleiteten](locating-redirected-strings.md)Zeichen folgen beschrieben.

### <a name="prepare-resources-for-a-shortcut-created-with-windows-installer"></a>Vorbereiten von Ressourcen für eine Verknüpfung, die mit Windows Installer erstellt wurde

Wenn Sie Windows Installer (MSI) verwenden, um eine Verknüpfung zu erstellen, enthalten Zeichen folgen Ressourcen den anzeigen Amen und die Beschreibung der Verknüpfung. In der [MSI](../msi/shortcut-table.md)-Verknüpfungs Tabelle wird auf die Ressourcen-DLL in den entsprechenden Spalten verwiesen, und die Ressourcen Bezeichner für den Kontext anzeigen Amen und die Beschreibung werden in den entsprechenden Spalten des Ressourcen Bezeichners verwendet.

Damit die Anwendungs Verknüpfung ordnungsgemäß mit der MUI-Ressourcen Technologie funktioniert, sollten Sie die folgenden Punkte beachten, wenn Sie die Verknüpfungs Zeichenfolgen vorbereiten:

-   Verwenden Sie entweder Umgebungsvariablen oder einen relativen Pfad, um die dll zu registrieren. Sie können @% SystemRoot% System32shell32.dll angeben, solange \\ \\ der Registrierungs Zeichenfolgentyp "reg \_ Expand SZ" lautet \_ . Der Zeichen folgen Ressourcen Bezeichner für "Text Document" in Shell32.dll ist 12345.
-   Verwenden Sie keine Leerzeichen um die Symbole "," und "-". Ein richtiges Beispiel ist "shell32.dll,-22912".
-   Verwenden Sie keinen kurzen Dateinamen. Diese Art von Name funktioniert nicht mit dem Ressourcen Lade Modul.

### <a name="prepare-resources-for-a-shortcut-using-inf-format"></a>Vorbereiten von Ressourcen für eine Verknüpfung mit dem INF-Format

Wenn Sie das INF-Dateiformat verwenden, um Verknüpfungs Zeichenfolgen zu erstellen, sollte die Ressourcen Datei die folgenden Registrierungs Einstellungen erstellen. Bei diesen Anweisungen wird davon ausgegangen, dass die profileitems-Syntax der Setup-API verwendet wird.

1.  Ändern Sie den infotip-Wert, um auf den Verweis auf die Zeichen folgen Umleitung mit dem Pfad und dem Ressourcen Bezeichner zu verweisen.
2.  Fügen Sie den neuen Wert displayresource unter den Profilen für die profileitems-Installation hinzu.

Im folgenden Beispiel wird gezeigt, wie die Rechner Anwendung zum **Startmenü** hinzugefügt wird:


```C++
[CalcInstallItems]
"Name" = %Calc_DESC%
"CmdLine" = 11, calc.exe
"SubDir" = %Access_GROUP%
"WorkingDir" = 11

"InfoTip" = "@%systemroot%\system32\shell32.dll,-22531"

"DisplayResource" = "%systemroot%\system32\shell32.dll",22019
```



Verwenden Sie die unten gezeigte Syntax, wenn Sie mit INF dem **Startmenü** Elemente hinzufügen, z. b. einen Zugriffs Gruppenordner. Diese Syntax setzt voraus, dass die \[ Unterstützung von "startmenuitems" \] von Setup verwendet wird, ähnlich der Syntax in "syssetup. inf".


```C++
[StartMenuItems]
<description> = <binary>,<commandline>,<iconfile>,<iconnum>,<infotip>,<resDLL,resID>
```



Legen Sie den Wert *Infotipp* auf den Zeichen folgen Verweis " `@<path>,-resID` " fest.

Der Anzeige Name wird durch die Werte " *ResDll* " und " *RESID* " bestimmt. Der Wert *RESID* gibt den Ressourcen Bezeichner für eine Zeichen folgen Ressource an, die der sprach neutralen Datei zugeordnet ist. Der *ResDll* -Wert gibt den Pfad zu der sprach neutralen Datei an.

## <a name="create-resources-for-friendly-document-type-names"></a>Erstellen von Ressourcen für benutzerfreundliche Dokumenttyp Namen

Sie müssen Anzeige Name-und infotip-Zeichen folgen für die Anwendung als Zeichen folgen Ressourcen implementieren. Damit benutzerfreundliche Dokumenttyp Namen auf die Sprache der Benutzeroberfläche reagieren können, muss die Anwendung die Namen mit dem Wert friendlytyid unter dem Programm Bezeichner-Schlüssel für den Dateityp registrieren. Der Standardwert für den programmbezeichnerschlüssel sollte beibehalten werden, um die Abwärtskompatibilität zu gewährleisten. Weitere Informationen über den Zugriff auf die Namen Ihrer Anwendung finden Sie in den Typnamen der Abfrage freundlichen Dokumente im Registrierungs Abschnitt der [Suche nach umgeleiteten](locating-redirected-strings.md)Zeichen folgen.

Die jeweilige Aufgabe umfasst die folgenden Schritte:

1.  Implementieren Sie den anzeigen Amen und die infotip-Zeichen folgen als sprachspezifische Zeichen folgen Ressourcen.
2.  Fügen Sie den Wert friendlytyadapame unter dem Dokumenttyp-Registrierungsschlüssel hinzu. Die Daten für den Wert entsprechen dem Muster " `@<path>,-<resID>` ", wobei " *path* " angibt, dass die ausführbare Datei und die *RESID* der Ressourcen Bezeichner einer lokalisierbaren Zeichen folgen Ressource sind, die dieser ausführbaren Datei
3.  Geben Sie den infotip-Registrierungs Wert gemäß dem Format " `@<path>,-<resID>` " an.

Das folgende Beispiel zeigt die Registrierungs Einstellungen für eine txt-Datei:


```C++
HKCR\.txt
@="txtfile"
"Content Type"="text/plain"

HKCR\txtfile
@="Text Document"

"FriendlyTypeName" = "@%systemroot%\system32\shell32.dll,-12345"

"InfoTip" = "@%systemroot%\system32\shell32.dll,-12346"
```



## <a name="provide-resources-for-shell-verb-action-strings"></a>Bereitstellen von Ressourcen für shellverb-Aktions Zeichenfolgen

Aktions Zeichenfolgen für bestimmte Verben (z. b. "Öffnen" und "Bearbeiten") werden im Popup Menü angezeigt, wenn der Benutzer mit der rechten Maustaste auf eine Datei in Windows-Explorer klickt. Die Anwendung muss keine Zeichen folgen für gängige Shellverben angeben, da die Shell über eigene MUI-aktivierte Standardwerte für diese Verben verfügt. Sie sollten jedoch lokalisierbare Zeichen folgen Ressourcen für Zeichen folgen bereitstellen, die ungewöhnliche Verben darstellen.

Unter den Betriebssystemen vor Windows XP werden Zeichen folgen für Shellverben in der Registrierung mit der folgenden Syntax gerendert, wobei *Verb* den tatsächlichen Verb Namen angibt:


```C++
HKCR\<progid>\shell\<verb>
@ = <friendly-name>
```



Hier sehen Sie ein Beispiel:


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
```



Unter Windows XP und höher können Sie eine dereferenzierungsstufe verwenden, um eine Aktions Zeichenfolge von der Benutzeroberflächen Sprache abhängig zu machen. Diese Betriebssysteme unterstützen einen MUIVerb-Wert für die Definition einer MUI-kompatiblen Zeichenfolge. Im folgenden finden Sie ein Beispiel für einen Registrierungs Eintrag für ein ungewöhnliches Verb:


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
"MUIVerb" = "@%systemroot%\system32\sample.exe,-9875"
```



Ihre MUI-Anwendung sollte außerdem in der Lage sein, den alten Standardwert als lokalisierbare Zeichenfolge zu registrieren, wie unten dargestellt:


```C++
HKCR\Sample.app\shell\Disc
@ = "@%systemroot%\system32\sample.exe,-9875"
```



> [!Note]  
> Die Registrierung des alten Standardwerts wird nicht empfohlen, da für Windows XP und höher unter Windows XP und höher eine andere Einrichtung als bei älteren Betriebssystemen erforderlich ist.

 

## <a name="create-resources-for-verb-protocol-and-auxusertype-strings"></a>Erstellen von Ressourcen für die Zeichen folgen Verb, Protocol und auxusertype

Sie sollten lokalisierbare Zeichen folgen Ressourcen für Verb-, Protokoll-und auxusertype-Zeichen folgen erstellen. Verwenden Sie die folgenden Registrierungs Einstellungen:


```C++
HKCR\CLSID\{<Your_CLSID>}\Verb\<number> @="<Your Verb>, <menu_flag>, <verb_flag>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...

HKCR\CLSID\{<Your_CLSID>}\AuxUserType\<number>
@="<Your Short Name>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID1"
...

HKCR\<Your_Name>\protocol\StdFileEditing\verb\<number>
@="<Your Verb>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...
```



Der für LocalizedString angegebene Wert enthält oder ersetzt den Wert für *Ihr Verb*, nicht die zwei Flagwerte.

Hier finden Sie eine Zusammenfassung, die Ihnen hilft, die richtigen Registrierungs Einstellungen sicherzustellen:

-   Wenn CLSID über einen \\ eininsertable-Schlüssel der HKCR CLSID \\ {CLSID} verfügt \\ , definieren Sie den CLSID-Standardwert mithilfe von HKCR \\ CLSID \\ {CLSID} \\ LocalizedString.
-   Wenn CLSID mindestens einen Unterschlüssel unter HKCR \\ CLSID \\ {CLSID} Verb aufweist \\ , definieren Sie jede einzelne Verb Zeichenfolge mithilfe von HKCR \\ CLSID \\ {CLSID} \\ Verb \\ xxx \\ LocalizedString.
-   Wenn die CLSID mindestens einen Unterschlüssel unter dem HKCR \\ {ProgID} \\ Protocol \\ stdfilebearbeitungs- \\ Verb aufweist, definieren Sie jede einzelne Verb Zeichenfolge mit dem HKCR \\ {ProgID} \\ Protocol \\ stdfilebearbeitungs \\ Verb \\ xxx \\ LocalizedString.
-   Wenn die CLSID mindestens einen aufgelisteten "auxusertype"-Unterschlüssel unter "HKCR \\ CLSID \\ {CLSID}" ist \\ , definieren Sie jeden "auxusertype"-Eintrag mit "HKCR \\ CLSID \\ {CLSID}" ( \\ \\ \\ LocalizedString).

## <a name="create-a-resource-for-the-uninstall-program"></a>Erstellen einer Ressource für das Deinstallationsprogramm

Um das Deinstallationsprogramm für die Anwendung zu registrieren, können Sie Registrierungs Werte im eindeutigen bezeichnerunter Schlüssel für die Anwendung unter dem Registrierungsschlüssel HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ Uninstall erstellen. Zu den festzulegenden Werten gehören: Display Name, Display Version, Publisher, ProductID, RegOwner, RegCompany, urlinfoabout, helptelefon, HelpLink, INSTALLLOCATION, InstallSource, InstallDate, Contact, comments, DisplayIcon, Info, urlupdateinfo.

> [!Note]  
> Um die MUI-Technologie für jeden Wert zu aktivieren, können Sie " \_ lokalisiert" an den Wertnamen anhängen.

 

Betriebssystemkomponenten müssen einen Wert für Display Name bereitstellen, \_ der auf eine MUI-spezifische Weise lokalisiert wird. Sie sollten den anzeigen Amen in einer DLL (z. b. Res.dll) als Zeichen folgen Ressource platzieren, vorausgesetzt, dass der Bezeichner 1245 lautet. Anschließend kann die Anwendung den anzeigen Amen als Display Name registrieren \_ , der mit dem Wert "@ \\res.DLL,-1245" lokalisiert wird. Alle anderen Registrierungs Einstellungen sollten unverändert beibehalten werden, einschließlich des ursprünglichen Werts für Display Name.

## <a name="create-resources-for-sound-events"></a>Erstellen von Ressourcen für Sound Ereignisse

In Windows werden bestimmte Ereignisse mit Audiodateien verknüpft, z. b. ein neues e-Mail-Benachrichtigungs Ereignis oder ein kritischer Akku Alarm Ereignis. Die Ereignis Namen müssen von der Benutzeroberfläche angezeigt werden und müssen die Globalisierung unterstützen. Daher sollten Sie eine lokalisierbare Zeichen folgen Ressource für die Beschreibung der einzelnen Ereignis Beschreibungen implementieren. Fügen Sie zusätzlich zu dem hart codierten Standardwert einen neuen Registrierungs Wert für jeden Ereignis Namen hinzu.

Gehen Sie folgendermaßen vor, um ein Sound Ereignis zu aktivieren:

1.  Implementieren Sie die Beschreibung als lokalisierbare Zeichen folgen Ressource.
2.  Fügen Sie neben dem hart codierten Standardwert einen neuen Registrierungs Wert für den anzeigen Amen hinzu. Das zugehörige Registrierungs Layout wird unten angezeigt:


```C++
HKCR\AppEvents\EventLabels
<event_name>
    (Default) REG_SZ "<description>"
    DispFileName REG_EXPAND_SZ "@<path>,-<resID>"
```



Wenn die Shell den Wert von "dispfilename" nicht finden oder abrufen kann, wird die Standardbeschreibung verwendet.

## <a name="create-resources-for-keyboard-layout-strings"></a>Erstellen von Ressourcen für Tastatur Layout-Zeichen folgen

Wenn Ihre Anwendung ein Tastaturlayout implementiert, erfordert Sie eine lokalisierbare Zeichen folgen Ressource für den Namen des Layouts für die Bildschirm Anzeige, z. b. in Listen mit Tastaturlayouts. Jedes Tastaturlayout verfügt über einen Registrierungsschlüssel unter HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Tastatur Layouts.

Zu den Werten für diesen Schlüssel gehören Layouttext, ein lesbarer Name für die Abwärtskompatibilität und layoutanzeigename. Die für den layoutanzeigenamen angegebenen Daten sollten ein Zeichen folgen Verweis im Format " `@<path>,-resID` " sein, der auf eine lokalisierbare Zeichen folgen Ressource verweist, die dem Tastatur Layout zugeordnet ist.

Im folgenden finden Sie ein Beispiel für eine Registrierungs Einstellung für das Spanisch (Spanien)-Tastaturlayout:

`Layout Display Name=@%SystemRoot%\system32\input.dll,-5020`

## <a name="represent-ole-insert-object-common-dialog-strings"></a>Darstellung der allgemeinen Dialog Felder für OLE-Einfügevorgänge

Sie können den anzeigen Amen eines OLE-einfügbar-Objekts als lokalisierbare Zeichen folgen Ressource implementieren, die dem Code zugeordnet ist, der das Objekt implementiert. Das [OLE-Dialogfeld "Objekt einfügen](/cpp/mfc/reference/coleinsertdialog-class) " erhält einen anzeigen Amen aus dem Registrierungsschlüssel HKCR \\ CLSID \\ { *<GUID>* }, wobei *GUID* den Klassen Bezeichner eines einfügbar OLE-Objekts identifiziert. Windows Vista und höher implementieren diesen Objekttyp auf lokalisierbare Weise. dabei wird ein MUI-kompatibler Anzeige Name verwendet, der die Anpassung an die Benutzeroberflächen Sprache ermöglicht. Im Gegensatz dazu implementieren Pre-Windows Vista-Betriebssysteme den anzeigen Amen für diesen Objekttyp mit dem Standardwert des entsprechenden Registrierungsschlüssels. In der Regel ist dieser Name entweder ein englischer Name (USA) oder ein Name in der Standardbenutzer Oberflächen Sprache des Systems.

> [!Note]  
> Nicht alle Objekte, die den unter Schlüsseln des Registrierungsschlüssels entsprechen, sind Insertable.

 

Der Standardwert des Schlüssels "HKCR \\ CLSID \\ { *<GUID>* }" sollte einen lesbaren Namen aus Gründen der Abwärtskompatibilität beibehalten. Er sollte jedoch auch den Wert von LocalizedString im Format " `@<path>,-ResID` " definieren, wobei Path die ausführbare Datei identifiziert, die das Objekt implementiert. Der Wert Resid gibt den Ressourcen Bezeichner der lokalisierbaren Zeichenfolge für den anzeigen Amen an.

Das Registrierungs Skript für das einfügbar Media Clip-Objekt enthält z. b. die folgenden Zeilen:


```C++
HKCR,"CLSID\%CLSID_Media_Clip%",,,"%default description%"
HKCR,"CLSID\%CLSID_Media_Clip%","LocalizedString",,"@%systemroot%\system32\mplay32.exe,-9217"
```



Die erste Zeile bietet Abwärtskompatibilität, indem eine einfache Text Zeichenfolge in der Registrierung als Standard Anzeige Name platziert wird. Die zweite Zeile ermöglicht den Zugriff auf den MUI-kompatiblen anzeigen Amen. Gibt den Zeichen folgen Bezeichner an, der in Mplay32.exe gespeichert ist. Die Zeichenfolge mit dem Bezeichner 9217 in Mplay32.exe kann den Zeichen folgen Ressourcen Werten für eine beliebige Anzahl von Sprachen zugeordnet werden. Der englische Name (USA) ist "Media Clip".

## <a name="create-string-resources-for-microsoft-management-console-snap-ins"></a>Erstellen von Zeichen folgen Ressourcen für die Microsoft Management Console Snap-Ins

Sie sollten für jedes MMC-Snap-in (Microsoft Management Console), das von ihrer MUI-Anwendung verwendet wird, eine lokalisierbare Zeichen folgen Ressource erstellen. Da ein Snap-in Teil einer Konsole ist, verfügt es über eine Benutzeroberfläche und muss globalisiert werden, um in mehreren Sprachen arbeiten zu können.

Zum größten Teil haben MMC-Snap-Ins dieselben Globalisierungs-und Lokalisierungs Probleme wie die MUI-Anwendung selbst. Ein MMC-Snap-in muss seinen Namen in der Registrierung für die Anzeige widerspiegeln. Der Registrierungs Eintrag sollte sowohl einen indirekten Verweis auf eine lokalisierbare Zeichen folgen Ressource als auch eine Literalzeichenfolge für die Abwärtskompatibilität enthalten.

Jedes MMC-Snap-in verfügt über einen Registrierungsschlüssel unter HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ MMC \\ SnapIns. Zu den Werten für diesen Schlüssel gehören namestring, ein lesbarer Name für die Abwärtskompatibilität und NameStringIndirect, der einen indirekten Verweis auf eine lokalisierbare Zeichen folgen Ressource angibt. Für NameStringIndirect sollten Sie einen Zeichen folgen Verweis im Format "" bereitstellen `@<path>,-resID` , das eine lokalisierbare Zeichen folgen Ressource darstellt.

Beispielsweise können Sie die folgende Einstellung für Mymmc.dll festlegen, wobei 12345 der Bezeichner der entsprechenden Zeichen folgen Ressource mit dem lokalisierbaren Namen des Snap-Ins ist:


```C++
NameStringIndirect=@%systemroot%@c:\windir\system32\mymmc.dll,-12345
```



Einige Snap-Ins registrieren andere Registrierungszeichen folgen Werte, die von MMC nicht aus der Registrierung gelesen werden. Weitere Informationen zur Verwendung dieser Werte finden Sie unter Registrieren von Microsoft Management Console Snap-In Zeichen folgen, die nicht aus der Registrierung gelesen wurden, beim Suchen von [umgeleiteten](locating-redirected-strings.md)Zeichen folgen.

## <a name="create-string-resources-for-a-windows-service"></a>Erstellen von Zeichen folgen Ressourcen für einen Windows-Dienst

Obwohl ein Windows-Dienst in der Regel nur wenige oder keine Benutzeroberfläche besitzt, muss er einen MUI-kompatiblen Namen anzeigen und in der Regel eine MUI-kompatible sprachspezifische Beschreibung bereitstellen. Der Registrierungsschlüssel, der einen Windows-Dienst beschreibt, unterstützt nur den Display Name-Wert für den Dienstnamen und den Beschreibungs Wert für die Dienst Beschreibung.

Die Einstellungen für den Windows-Dienst werden von der Anwendung hergestellt, wie unter Festlegen des anzeigen Amens und der Beschreibung für einen Windows-Dienst aus der Registrierung beim Suchen von [umgeleiteten](locating-redirected-strings.md)Zeichen folgen beschrieben. Wenn Ihre Anwendung die Registrierungs Werte für die Dienst Benutzeroberfläche nicht festgelegt hat, bleiben die Werte in der Registrierung auf Englisch festgelegt, auch wenn die Benutzeroberfläche in einer anderen Sprache vorhanden ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorbereiten von Ressourcen](preparing-resources.md)
</dt> <dt>

[Suchen umgeleitet-Zeichen folgen](locating-redirected-strings.md)
</dt> </dl>

 

 
