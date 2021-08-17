---
description: Storage hart codierten Zeichenfolgen in der Registrierung ist Teil eines Windows Vista-Lokalisierungsmodells.
ms.assetid: 70185942-7d32-4151-a4e1-f71cf45e87af
title: Verwenden der Umleitung von Registrierungszeichenfolgen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30f0804d0586f8340e5a84e9da9c82ca39ffc30b55f72f4695d5216cbb26aab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118389416"
---
# <a name="using-registry-string-redirection"></a>Verwenden der Umleitung von Registrierungszeichenfolgen

Storage hart codierten Zeichenfolgen in der Registrierung ist Teil eines Windows Vista-Lokalisierungsmodells. Dies wird von DER -DATEI nicht unterstützt. Im aktuellen Modell wird die Benutzeroberfläche für das Betriebssystem in sprachspezifischen Ressourcendateien zusätzlich zu einer sprachneutralen Basis ausgeführt. Die Komponenten des Betriebssystems verwenden die Registrierung sprachneutral.

BEI DER WERDEN nur umgeleitete Registrierungszeichenfolgen verwendet, die von Win32 PE-Ressourcen in der Ressourcendatei der Basissprache definiert werden. Die Umleitung wird separat definiert, z. B. in einer INF-Datei. Mit dieser Art von Speicher kann das Ressourcenlademodul beim Laden des Ressourcenmoduls automatisch die richtigen Sprachressourcen auswählen.

> [!Note]  
> Dieses Thema bezieht sich nur auf Win32 PE-Ressourcen. Wenn Sie Nicht-Win32 PE-Ressourcen verwenden, müssen Sie bei Bedarf eine angepasste Umleitung der Registrierungszeichenfolge bereitstellen.

 

## <a name="create-a-language-neutral-resource"></a>Erstellen einer Language-Neutral Ressource

Eine unter Windows Vista und höher ausgeführte ANWENDUNG verwendet eine sprachneutrale Zeichenfolgenressource, um den Zugriff auf sprachspezifische Zeichenfolgen zu ermöglichen, die in einer Zeichenfolgenressourcentabelle gespeichert sind. Anwendungscode, der diese Werte aus der Registrierung liest, wird im Abschnitt Laden eines Language-Neutral-Registrierungswerts unter Suchen von umgeleiteten [Zeichenfolgen beschrieben.](locating-redirected-strings.md)

Die Daten für einen sprachneutralen Registrierungswert haben das Format `@<PE-path>,-<stringID>[;<comment>]` " ", wobei:

-   *PE-path* gibt den Pfad der ausführbaren Datei an. Sie können den Pfad mithilfe einer Umgebungsvariablen wie %ProgramFiles% angeben, um die Bereitstellung zu unterstützen. Eine Alternative zum Erstellen eines Zeichenfolgenverweises besteht in der Auslassung der Dateipfadinformationen. In diesem Fall muss Ihre Anwendung über einige Mittel verfügen, z. B. einen anderen Registrierungswert, um ihr eigenes Installationsverzeichnis zu kommunizieren.
-   *stringID* gibt den numerischen Ressourcenbezeichner der relevanten Zeichenfolgenressource an, die genau wie jede andere lokalisierbare Zeichenfolgenressource implementiert wird.
-   *comment* gibt optionale Informationen zum Debuggen oder zur Lesbarkeit des Registrierungswerts an. Die Registrierungs-API-Funktionen ignorieren den Kommentar beim Laden der Zeichenfolge.

> [!Note]  
> Die Daten für den Registrierungswert verweisen nicht explizit auf die sprachspezifische Ressourcendatei. Die richtige Datei wird zur Laufzeit basierend auf den aktuellen Spracheinstellungen der Benutzeroberfläche bestimmt.

 

Ein Registrierungswert wird ohne Leerzeichen zwischen "," und "-" eingegeben. Der richtige Registrierungswert ist:

`shell32.dll,-22912`

Ein falscher Registrierungswert ist:

`shell32.dll, -22912`

Ein Beispiel aus Windows Vista ist der Registrierungswert mit den folgenden Daten:

`@%SystemRoot%\system32\input.dll,-5020`

## <a name="create-resources-for-shortcut-strings"></a>Erstellen von Ressourcen für Verknüpfungszeichenfolgen

Wenn die SHELL-Anwendung ihren Namen auf der Shell-Benutzeroberfläche anzeigt, wird eine InfoTip-Zeichenfolge für das Anwendungssymbol angezeigt. Sie sollten Zeichenfolgenressourcen für den Anzeigenamen Ihrer Anwendung und die zugehörige InfoTip-Zeichenfolge für jede unterstützte Sprache erstellen. Wenn die Ressourcen bereit sind, kann Ihre Anwendung die Zeichenfolgen wie im Abschnitt Verwenden der Shell-API zum Laden von Verknüpfungszeichenfolgen aus der Registrierung unter Suchen von umgeleiteten Zeichenfolgen [beschrieben verwenden.](locating-redirected-strings.md)

### <a name="prepare-resources-for-a-shortcut-created-with-windows-installer"></a>Vorbereiten von Ressourcen für eine Verknüpfung, die mit dem Windows erstellt wurde

Wenn Sie einen Windows Installer (MSI) verwenden, um eine Verknüpfung zu erstellen, enthalten Zeichenfolgenressourcen den Anzeigenamen und die Beschreibung der Verknüpfung. In der [MSI-Verknüpfungstabelle](../msi/shortcut-table.md)wird in den entsprechenden Spalten auf die Ressourcen-DLL verwiesen, und die Ressourcenbezeichner für den Kontextanzeigenamen und die Beschreibung werden in den entsprechenden Ressourcenbezeichnerspalten verwendet.

Damit die Anwendungsverknüpfung ordnungsgemäß mit der TECHNOLOGY-Ressourcentechnologie funktioniert, beachten Sie beim Vorbereiten der Verknüpfungszeichenfolgen folgende Punkte:

-   Verwenden Sie entweder Umgebungsvariablen oder einen relativen Pfad, um die DLL zu registrieren. Sie können @%systemroot% system32shell32.dll, solange der Registrierungszeichenfolgentyp \\ \\ REG EXPAND SZ \_ \_ ist. Der Zeichenfolgenressourcenbezeichner für "Textdokument" in Shell32.dll ist 12345.
-   Verwenden Sie keine Leerzeichen um die Symbole "," und "-". Ein korrektes Beispiel ist "shell32.dll,-22912".
-   Verwenden Sie keinen kurzen Dateinamen. Dieser Namenstyp funktioniert nicht mit dem Ressourcenlader.

### <a name="prepare-resources-for-a-shortcut-using-inf-format"></a>Vorbereiten von Ressourcen für eine Verknüpfung im INF-Format

Wenn Sie das INF-Dateiformat verwenden, um Verknüpfungszeichenfolgen zu erstellen, sollte die Ressourcendatei die folgenden Registrierungseinstellungen vornehmen. Bei diesen Anweisungen wird davon ausgegangen, dass die ProfileItems-Syntax der Setup-API verwendet wird.

1.  Ändern Sie den InfoTip-Wert so, dass er mithilfe des Pfads und des Ressourcenbezeichners auf den Zeichenfolgenumleitungsverweis verweist.
2.  Fügen Sie den neuen Wert DisplayResource unter den ProfileItems-Installationsabschnitten hinzu.

Das folgende Beispiel zeigt das Hinzufügen der Anwendung Calculator zum **Startmenü:**


```C++
[CalcInstallItems]
"Name" = %Calc_DESC%
"CmdLine" = 11, calc.exe
"SubDir" = %Access_GROUP%
"WorkingDir" = 11

"InfoTip" = "@%systemroot%\system32\shell32.dll,-22531"

"DisplayResource" = "%systemroot%\system32\shell32.dll",22019
```



Verwenden Sie die unten gezeigte Syntax, wenn Sie INF verwenden, um Dem Startmenü Elemente hinzuzufügen, z. B. **einen** Ordner "Zugriffsgruppe". Diese Syntax setzt die Verwendung der StartMenuItems-Unterstützung von Setup voraus, ähnlich der Syntax, die \[ \] in Syssetup.inf verwendet wird.


```C++
[StartMenuItems]
<description> = <binary>,<commandline>,<iconfile>,<iconnum>,<infotip>,<resDLL,resID>
```



Legen Sie den Wert *infotip* auf den Zeichenfolgenverweis " `@<path>,-resID` " fest.

Der Anzeigename wird durch die *ResDLL- und* *resID-Werte* bestimmt. Der *resID-Wert* gibt den Ressourcenbezeichner für eine Zeichenfolgenressource an, die der sprachneutralen Datei zugeordnet ist. Der *resDLL-Wert* gibt den Pfad zur sprachneutralen Datei an.

## <a name="create-resources-for-friendly-document-type-names"></a>Erstellen von Ressourcen für benutzerfreundliche Dokumenttypnamen

Sie müssen Denknamen und InfoTip-Zeichenfolgen für Ihre Anwendung als Zeichenfolgenressourcen implementieren. Damit benutzerfreundliche Dokumenttypnamen auf die Benutzeroberflächensprache reagieren können, muss die Anwendung die Namen mithilfe des FriendlyTypeName-Werts unter dem Programmbezeichnerschlüssel für den Dateityp registrieren. Der Standardwert für den Programmbezeichnerschlüssel sollte beibehalten werden, um abwärtskompatibel zu bleiben. Informationen zum Zugreifen auf die Namen aus Ihrer Anwendung finden Sie im Abschnitt Abfragefreundliche Dokumenttypnamen im Abschnitt Registrierung unter Suchen von umgeleiteten [Zeichenfolgen.](locating-redirected-strings.md)

Die spezifische Arbeit umfasst die folgenden Schritte:

1.  Implementieren Sie den Benutzernamen und infotip-Zeichenfolgen als sprachspezifische Zeichenfolgenressourcen.
2.  Fügen Sie unter dem Registrierungsschlüssel des Dokumenttyps den Wert FriendlyTypeName hinzu. Die Daten für den Wert folgen dem Muster " ", wobei path die ausführbare Datei angibt und resID der Ressourcenbezeichner einer lokalisierbaren Zeichenfolgenressource ist, die `@<path>,-<resID>` dieser ausführbaren Datei zugeordnet ist.  
3.  Geben Sie den InfoTip-Registrierungswert im Format "" `@<path>,-<resID>` an.

Das folgende Beispiel zeigt die Registrierungseinstellungen für eine .txt Datei:


```C++
HKCR\.txt
@="txtfile"
"Content Type"="text/plain"

HKCR\txtfile
@="Text Document"

"FriendlyTypeName" = "@%systemroot%\system32\shell32.dll,-12345"

"InfoTip" = "@%systemroot%\system32\shell32.dll,-12346"
```



## <a name="provide-resources-for-shell-verb-action-strings"></a>Bereitstellen von Ressourcen für Shellverb-Aktionszeichenfolgen

Aktionszeichenfolgen für bestimmte Verben, z. B. "öffnen" und "bearbeiten", werden im Popupmenü angezeigt, das angezeigt wird, wenn der Benutzer im Explorer mit der rechten Maustaste auf eine Datei Windows klickt. Ihre Anwendung muss keine Zeichenfolgen für allgemeine Shellverben angeben, da die Shell über eigene STANDARD-fähige Standardeinstellungen für diese Verben verfügt. Sie sollten jedoch lokalisierbare Zeichenfolgenressourcen für Zeichenfolgen bereitstellen, die ungewöhnliche Verben darstellen.

Bei xp-Windows werden Zeichenfolgen für Shellverben in der Registrierung mithilfe der folgenden Syntax gerendert, wobei *verb* den tatsächlichen Verbnamen angibt:


```C++
HKCR\<progid>\shell\<verb>
@ = <friendly-name>
```



Ein Beispiel:


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
```



Bei Windows XP und höher können Sie eine Deskriptionsebene verwenden, um eine Aktionszeichenfolge von der Sprache der Benutzeroberfläche abhängig zu machen. Diese Betriebssysteme unterstützen einen ZEICHENFOLGEVerb-Wert für die Definition einer MIT DER KOMPATIBLEN Zeichenfolge. Hier ist ein Beispiel für einen Registrierungseintrag für ein ungewöhnliches Verb:


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
"MUIVerb" = "@%systemroot%\system32\sample.exe,-9875"
```



IhreSTELLUNG-Anwendung sollte auch in der Lage sein, den alten Standardwert als lokalisierbare Zeichenfolge zu registrieren, wie unten dargestellt:


```C++
HKCR\Sample.app\shell\Disc
@ = "@%systemroot%\system32\sample.exe,-9875"
```



> [!Note]  
> Die Registrierung des alten Standardwerts wird nicht empfohlen, da ein anderes Setup auf Windows XP und höher erforderlich ist als das Setup, das unter früheren Betriebssystemen verwendet wird.

 

## <a name="create-resources-for-verb-protocol-and-auxusertype-strings"></a>Erstellen von Ressourcen für Verb-, Protokoll- und AuxUserType-Zeichenfolgen

Sie sollten lokalisierbare Zeichenfolgenressourcen für Verb-, Protokoll- und AuxUserType-Zeichenfolgen erstellen. Verwenden Sie die folgenden Registrierungseinstellungen:


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



Der für LocalizedString angegebene Wert enthält oder ersetzt nur den Wert für *Ihr Verb,* nicht die beiden Flagwerte.

Im Folgenden finden Sie eine Zusammenfassung, mit der Sie die richtigen Registrierungseinstellungen sicherstellen können:

-   Wenn CLSID über eine HKCR \\ CLSID \\ {clsid} Insertable Key verfügt, definieren Sie den \\ CLSID-Standardwert mithilfe von HKCR \\ CLSID \\ {clsid} \\ LocalizedString.
-   Wenn CLSID einen oder mehrere Unterschlüssel unter HKCR \\ CLSID {clsid} Verb enthält, definieren Sie jede einzelne \\ Verbzeichenfolge mithilfe von \\ HKCR \\ CLSID \\ {clsid} \\ Verb \\ xxx \\ LocalizedString.
-   Wenn CLSID über einen oder mehrere Unterschlüssel unter HKCR \\ {progid} Protocol Stdfileediting Verb verfügt, definieren Sie jede einzelne Verbzeichenfolge mit \\ \\ \\ hkcr \\ {progid} \\ Protocol \\ Stdfileediting \\ Verb \\ xxx \\ LocalizedString.
-   Wenn CLSID einen oder mehrere aufgelistete AuxUserType-Unterschlüssel unter HKCR \\ CLSID \\ {clsid} AuxUserType enthält, definieren Sie jeden \\ AuxUserType-Eintrag mithilfe von HKCR \\ CLSID \\ {clsid} \\ AuxUserType \\ xxx \\ LocalizedString.

## <a name="create-a-resource-for-the-uninstall-program"></a>Erstellen einer Ressource für das Deinstallationsprogramm

Um das Deinstallationsprogramm für die Anwendung zu registrieren, können Sie Registrierungswerte im Eindeutigen Bezeichnerunterschlüssel für die Anwendung unter dem Registrierungsschlüssel HKEY \_ LOCAL MACHINE Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion Uninstall \\ erstellen. Folgende Werte müssen festgelegt werden: DisplayName, DisplayVersion, Publisher, ProductID, RegOwner, RegCompany, UrlInfoAbout, HelpTelephone, HelpLink, InstallLocation, InstallSource, InstallDate, Contact, Comments, DisplayIcon, Readme, UrlUpdateInfo.

> [!Note]  
> Sie können "Lokalisiert" an den Wertnamen anfügen, um die TECHNOLOGY-Technologie für jeden \_ Wert zu aktivieren.

 

Betriebssystemkomponenten müssen einen Wert für DisplayName \_ Localized auf EINE BESTIMMTE Weise bereitstellen. Sie sollten den Anzeigenamen in einer DLL wie Res.dll als Zeichenfolgenressource platzieren, vorausgesetzt, der Bezeichner ist 1245. Anschließend kann die Anwendung den Anzeigenamen als DisplayName Localized mit dem Wert \_ "@ \\res.DLL,-1245" registrieren. Alle anderen Registrierungseinstellungen sollten beibehalten werden, wie sie sind, einschließlich des ursprünglichen Werts für DisplayName.

## <a name="create-resources-for-sound-events"></a>Erstellen von Ressourcen für Soundereignisse

Windows bestimmte Ereignisse sound-Dateien zu, z. B. einem New Mail Notification-Ereignis oder einem Critical Battery Alarm-Ereignis. Die Ereignisnamen müssen von der Benutzeroberfläche angezeigt werden und die Globalisierung unterstützen. Daher sollten Sie eine lokalisierbare Zeichenfolgenressource für die Beschreibung der einzelnen Ereignisbeschreibungen implementieren. Fügen Sie zusätzlich zum hart codierten Standardwert einen neuen Registrierungswert für jeden Ereignisnamen hinzu.

Gehen Sie wie folgt vor, um ein Soundereignis zu aktivieren:

1.  Implementieren Sie die Beschreibung als lokalisierbare Zeichenfolgenressource.
2.  Fügen Sie zusätzlich zum hart codierten Standardwert einen neuen Registrierungswert für den Anzeigenamen hinzu. Das zugeordnete Registrierungslayout ist unten dargestellt:


```C++
HKCR\AppEvents\EventLabels
<event_name>
    (Default) REG_SZ "<description>"
    DispFileName REG_EXPAND_SZ "@<path>,-<resID>"
```



Wenn die Shell den Wert von DispFileName nicht finden oder abrufen kann, wird die Standardbeschreibung verwendet.

## <a name="create-resources-for-keyboard-layout-strings"></a>Erstellen von Ressourcen für Tastaturlayoutzeichenfolgen

Wenn Ihre Anwendung ein Tastaturlayout implementiert, ist eine lokalisierbare Zeichenfolgenressource für den Namen des Layouts für die Bildschirmanzeige erforderlich, z. B. in Listen von Tastaturlayouts. Jedes Tastaturlayout verfügt über einen Registrierungsschlüssel unter HKEY \_ LOCAL \_ MACHINE System \\ \\ CurrentControlSet \\ Control Keyboard \\ Layouts.

Zu den Werten für diesen Schlüssel gehören Layouttext, ein lesbarer Name für die Abwärtskompatibilität und Layoutanzeigename. Die für den Layoutanzeigenamen angegebenen Daten sollten ein Zeichenfolgenverweis im Format "" sein `@<path>,-resID` und auf eine lokalisierbare Zeichenfolgenressource verweisen, die dem Tastaturlayout zugeordnet ist.

Hier sehen Sie ein Beispiel für eine Registrierungseinstellung für das Tastaturlayout für Spanisch (Spanien):

`Layout Display Name=@%SystemRoot%\system32\input.dll,-5020`

## <a name="represent-ole-insert-object-common-dialog-strings"></a>Darstellen allgemeiner Dialogfeldzeichenfolgen für OLE Insert-Objekte

Sie können den Anzeigenamen eines einfügebaren OLE-Objekts als lokalisierbare Zeichenfolgenressource implementieren, die dem Code zugeordnet ist, der dieses Objekt implementiert. Das [Dialogfeld OLE Insert Object](/cpp/mfc/reference/coleinsertdialog-class) ruft einen Anzeigenamen aus dem Registrierungsschlüssel HKCR \\ CLSID \\ { } *<GUID>* ab, wobei *GUID* den Klassenbezeichner eines einfügebaren OLE-Objekts identifiziert. Windows Vista und höher implementieren diesen Objekttyp lokalisierbar und verwenden dabei einen MIT DEM-kompatiblen Anzeigenamen, der anpassungsfähige Anpassungen an der Sprache der Benutzeroberfläche ermöglicht. Im Gegensatz dazu implementieren Betriebssysteme vor Windows Vista den Anzeigenamen für diesen Objekttyp unter Verwendung des Standardwerts des entsprechenden Registrierungsschlüssels. In der Regel ist dieser Name entweder ein englischer Name (USA) oder ein Name in der Standardsprache der Benutzeroberfläche des Systems.

> [!Note]  
> Nicht alle Objekte, die Unterschlüsseln des Registrierungsschlüssels entsprechen, können eingefügt werden.

 

Der Standardwert des SCHLÜSSELS HKCR \\ CLSID { } sollte aus Gründen der \\ *<GUID>* Abwärtskompatibilität einen lesbaren Namen beibehalten. Sie sollte jedoch auch den LocalizedString-Wert im Format `@<path>,-ResID` "" definieren, wobei path die ausführbare Datei identifiziert, die das Objekt implementiert. Der ResID-Wert gibt den Ressourcenbezeichner der lokalisierbaren Zeichenfolge für den Anzeigenamen an.

Das Registrierungsskript für das einfügebare Medienclipobjekt enthält beispielsweise die folgenden Zeilen:


```C++
HKCR,"CLSID\%CLSID_Media_Clip%",,,"%default description%"
HKCR,"CLSID\%CLSID_Media_Clip%","LocalizedString",,"@%systemroot%\system32\mplay32.exe,-9217"
```



Die erste Zeile bietet Abwärtskompatibilität, indem eine einfache Textzeichenfolge in der Registrierung als Standardanzeigename platziert wird. Die zweite Zeile bietet Zugriff auf den ANZEIGEnamen, der MIT DEM KONFORM IST. Gibt den in Mplay32.exe gespeicherten Zeichenfolgenbezeichner an. Die Zeichenfolge mit dem Bezeichner 9217 in Mplay32.exe kann Zeichenfolgenressourcenwerten für eine beliebige Anzahl von Sprachen zugeordnet werden. Der englische Name (USA) lautet "Media Clip".

## <a name="create-string-resources-for-microsoft-management-console-snap-ins"></a>Erstellen von Zeichenfolgenressourcen für Microsoft Management Console Snap-Ins

Sie sollten eine lokalisierbare Zeichenfolgenressource für jedes mmc-Snap-In (Microsoft Management Console) erstellen, das von Ihrer MSI-Anwendung verwendet wird. Da ein Snap-In Teil einer Konsole ist, verfügt es über eine Benutzeroberfläche und muss globalisiert werden, damit es in mehreren Sprachen ausgeführt werden kann.

In den meisten Teilen lösen MMC-Snap-Ins die gleichen Globalisierungs- und Lokalisierungsprobleme aus wie die ANWENDUNG SELBST. Ein MMC-Snap-In muss seinen Namen in der Registrierung für die Anzeige widerspiegeln. Der Registrierungseintrag sollte aus Gründen der Abwärtskompatibilität sowohl einen indirekten Verweis auf eine lokalisierbare Zeichenfolgenressource als auch eine Literalzeichenfolge enthalten.

Jedes MMC-Snap-In verfügt über einen Registrierungsschlüssel unter HKEY \_ LOCAL MACHINE Software Microsoft \_ \\ \\ \\ MMC \\ SnapIns. Zu den Werten für diesen Schlüssel gehören NameString, die einen für Menschen lesbaren Namen aus Gründen der Abwärtskompatibilität angeben, und NameStringIndirect, die einen indirekten Verweis auf eine lokalisierbare Zeichenfolgenressource angeben. Für NameStringIndirect sollten Sie einen Zeichenfolgenverweis im Format " " bereitstellen, der `@<path>,-resID` eine lokalisierbare Zeichenfolgenressource darstellt.

Beispielsweise können Sie die folgende Einstellung für Mymmc.dll festlegen, wobei 12345 der Bezeichner der entsprechenden Zeichenfolgenressource ist, die den lokalisierbaren Namen des Snap-Ins enthält:


```C++
NameStringIndirect=@%systemroot%@c:\windir\system32\mymmc.dll,-12345
```



Einige Snap-Ins registrieren andere Registrierungszeichenfolgenwerte, die MMC nicht aus der Registrierung liest. Weitere Informationen zur Verwendung dieser Werte finden Sie unter Register Microsoft Management Console Snap-In Strings Not Read from the Registry in [Locating Redirected Strings](locating-redirected-strings.md).

## <a name="create-string-resources-for-a-windows-service"></a>Erstellen von Zeichenfolgenressourcen für einen Windows-Dienst

Obwohl ein Windows Dienst in der Regel nur wenig oder gar keine Benutzeroberfläche hat, muss er einen MIT DEM-kompatiblen Namen anzeigen und in der Regel eine sprachspezifische Beschreibung für die JEWEILIGE SPRACHE enthalten. Der Registrierungsschlüssel, der einen Windows Dienst beschreibt, unterstützt nur den DisplayName-Wert für den Dienstnamen und den Wert Description für die Dienstbeschreibung.

Einstellungen für den Windows-Dienst werden aus der Anwendung erstellt, wie unter Festlegen des Anzeigenamens und der Beschreibung für einen Windows-Dienst aus der Registrierung unter [Suchen von umgeleiteten Zeichenfolgen](locating-redirected-strings.md)beschrieben. Wenn Ihre Anwendung die Registrierungswerte für die Dienstbenutzerschnittstelle nicht festgelegt, bleiben die Werte in der Registrierung auf Englisch festgelegt, auch wenn sich die Benutzeroberfläche in einer anderen Sprache befindet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vorbereiten von Ressourcen](preparing-resources.md)
</dt> <dt>

[Suchen nach umgeleiteten Zeichenfolgen](locating-redirected-strings.md)
</dt> </dl>

 

 
