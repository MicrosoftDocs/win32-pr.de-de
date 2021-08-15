---
description: Verwenden von MS Shell Dlg und MS Shell Dlg 2
ms.assetid: ac3b57a6-5b92-4366-ad71-c501cec60997
title: Verwenden von MS Shell Dlg und MS Shell Dlg 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c29b6f45267ee9f123e5a6dddcd044d667fbe4553af8b3f580edd633b2293ef2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118389507"
---
# <a name="using-ms-shell-dlg-and-ms-shell-dlg-2"></a>Verwenden von MS Shell Dlg und MS Shell Dlg 2

Windows ist in lokalisierten Editionen für viele Sprachen verfügbar. Die Edition in englischer Sprache kann jedoch auch zum Ausführen von Anwendungen verwendet werden, die in anderen Sprachen als Englisch geschrieben sind. Dies gilt auch, wenn das für diese Sprachen verwendete Skript anders ist, als wenn Anwendungen auf Griechisch oder Japanisch geschrieben werden. Diese Anwendungen erfordern eine Benutzeroberfläche mit Dialogfeldern, Symbolen und Hilfsprogrammen, die Informationen in der Anwendungssprache bereitstellen, die sich möglicherweise von der Sprache unterscheiden, die in der aktuellen Windows Benutzeroberfläche verwendet wird.

Das Problem beim Auswählen der Schriftart für eine Benutzeroberfläche ist offensichtlich. Beispielsweise ist die Shellschriftart, die auch als System- oder Standardschriftart bezeichnet wird, für Englisch (USA) Windows 98 MS Sans Serif, während die Shellschriftart für Griechisch (Griechisch) Windows 98 MS Sans Serif Griechisch ist. Für Japanisch (Japan) Windows 98 ist die Shellschriftart MS UI-Format. Diese Zeichensätze können nicht direkt einander zugeordnet werden. Das Ersetzen von MS Sans Serif durch MS Sans Serif Griechisch, wenn das Gebietsschema auf Griechisch (Griechisch) festgelegt ist, lässt nicht zu, dass vorhandene Anwendungen ordnungsgemäß ausgeführt werden oder dass griechisch zeichen in Systemmenüs, Dialogfeldern und Bearbeitungssteuerelementen angezeigt werden.

Windows löst dieses Problem, indem die logischen Schriftarten MS Shell Dlg und MS Shell Dlg 2 verwendet werden, um die Auswahl der geeigneten Schriftart für die Skriptanzeige zu ermöglichen. In diesem Abschnitt werden verschiedene Programmierüberlegungen zur Verwendung der logischen Schriftarten zum Implementieren von Dialogfeldern, Menüs und ähnlichem für flexible Benutzeroberflächen behandelt, die auf allen unterstützten Windows Betriebssystemen und in allen Sprachen gut angezeigt werden. Weitere Informationen finden Sie unter [Schriftarterstellung und -auswahl.](../gdi/font-creation-and-selection.md) Unter [mehrsprachige Benutzeroberfläche](multilingual-user-interface.md) wird auch die Verwendung der TECHNOLOGIE mehrsprachige Benutzeroberfläche (MEHRSPRACHIGE BENUTZEROBERFLÄCHE) beim Erstellen von Benutzeroberflächen für Ihre mehrsprachigen Anwendungen erörtert.

## <a name="about-the-logical-fonts"></a>Informationen zu logischen Schriftarten

Die logischen Schriftarten MS Shell Dlg und MS Shell Dlg 2 sind im Wesentlichen Gesichtsnamen, die für die Zuordnung verwendet werden, um unterstützung für Gebietsschemas/Kulturen zu ermöglichen, die Zeichen enthalten, die nicht in Codepage 1252 enthalten sind, der Windows Zeichensatz für die USA und Westeuropa. MS Shell Dlg wird der Standardschriftart der Shell zugeordnet, die der aktuellen Kultur/dem aktuellen Gebietsschema zugeordnet ist, und unterstützt die klassische Windows Desktopdarstellung. Der Gesichtsname von MS Shell Dlg 2 wurde in Windows 2000 eingeführt, um das mit Windows 2000 eingeführte Aussehen zu unterstützen.

Wenn Ihre Anwendung beispielsweise MS Shell Dlg oder MS Shell Dlg 2 für die Dialogfelder verwendet, kann sich ein Lokalisierungsteam, das Ressourcen in griechisch-sprache für Ihre Anwendung erstellt, auf die Übersetzung von Text konzentrieren. Sie müssen sich nicht um Probleme wie die Unterscheidung zwischen MS Sans Serif und MS Sans Serif Griechisch kümmern.

> [!Note]  
> Die von MS Shell Dlg und MS Shell Dlg 2 generierten Schriftarten unterscheiden sich in verschiedenen Windows Versionen. Daher sollten Sie sicherstellen, dass Ihre Benutzeroberflächenelemente auf allen Plattformen gut angezeigt werden.

 

## <a name="handle-hard-coded-font-names"></a>Behandeln Hard-Coded Schriftartnamen

Die Verwendung von Unicode ermöglicht Anwendungen den Umgang mit Tausenden von verschiedenen Zeichen, aber die meisten Schriftarten decken nicht den gesamten Unicode-Zeichensatz ab. Ihre Anwendungen sollten keine Schriftartnamen hart codieren. Ein Grund dafür ist, dass die Hartcodierung eines Schriftartnamens, der Zeichen für eine Sprache und keine Zeichen für eine andere Sprache anzeigt, dazu führt, dass der lokalisierte Text in der zweiten Sprache falsch angezeigt wird. Ein weiterer Grund, schriftartnamen nicht hartzu codieren, ist, dass die gewünschte Schriftart möglicherweise nicht auf dem Betriebssystem geladen wird, das Anwendungstext anzeigt.

Die beste Möglichkeit, Schriftartnamen zu behandeln, besteht darin, sie als lokalisierbare Ressourcen zu betrachten. Die Verwendung einer logischen Schriftart löst das Problem, dass Ihre Schnittstelle mit einer beliebigen Sprache auf Windows NT oder Windows 2000 für jede Sprache ausgeführt wird. Wenn Sie einen Schriftartnamen als lokalisierbare Ressource festlegen, kann der Lokalisierer die Schriftart für die lokalisierte Benutzeroberfläche ändern.

## <a name="handle-hard-coded-font-sizes"></a>Behandeln Hard-Coded Schriftgraden

Einige Skripts sind komplex und erfordern eine große Anzahl von Pixeln, um ordnungsgemäß angezeigt zu werden. Beispielsweise werden die meisten englischen Zeichen in einem 5x7-Raster angezeigt, aber japanische Zeichen benötigen mindestens ein 16 x 16-Raster, um deutlich sichtbar zu sein. Während Chinesisch ein 24x24-Raster benötigt, benötigt Thai nur 8 Pixel für die Breite, aber mindestens 22 Pixel für die Höhe. Es ist leicht zu verstehen, dass einige Zeichen bei einem kleinen Schriftgrad möglicherweise nicht lesbar sind.

Die Benutzeroberfläche Ihrer Anwendung sollte Schriftgrade als lokalisierbare Ressourcen behandeln. Die Verwendung einer logischen Schriftart löst das Problem, dass Ihre Schnittstelle mit einer beliebigen Sprache auf Windows NT oder Windows 2000 für jede Sprache ausgeführt wird. Wenn Sie einen Schriftgrad als lokalisierbare Ressource festlegen, kann Ihr Lokalisierer die Schriftart für die lokalisierte Benutzeroberfläche ändern.

## <a name="map-the-logical-fonts"></a>Zuordnen der logischen Schriftarten

Jede der logischen Schriftarten wird durch einen Eintrag in der Registrierung der entsprechenden Shellschriftart für das derzeit aktive Gebietsschema zugeordnet. Wenn eine der logischen Schriftarten verwendet wird, wechselt Windows zur Laufzeit zur Schriftart für das aktuell ausgewählte Gebietsschema. Dieser Vorgang ermöglicht die korrekte Anzeige der englischen (USA) Windows Benutzeroberfläche sowie Zeichen, die nicht in Codepage 1252 enthalten sind. Daher können derzeit lokalisierte Anwendungen ohne Änderungen auf der englischen Version (USA) von Windows ausgeführt werden.

Jeder Windows Computer ordnet MS Shell Dlg und MS Shell Dlg 2 einer entsprechenden physischen Schriftart zu, basierend auf der definierten Sprache für Nicht-Unicode-Programme, die in [NLS-Terminologie](nls-terminology.md)beschrieben wird. Die tatsächlichen Zuordnungen werden im Registrierungsschlüssel HKEY \_ LOCAL MACHINE Software Microsoft Windows NT Current Version \_ \\ \\ \\ \\ \\ FontSubstitutes gespeichert.

### <a name="font-mapping-on-windows-me9895"></a>Schriftartzuordnung auf Windows Me/98/95

MS Shell Dlg wird in der Regel einer codepagespezifischen Version von MS Sans Serif zugeordnet.

### <a name="font-mapping-on-windows-nt-40"></a>Schriftartzuordnung auf Windows NT 4.0

MS Shell Dlg wird MS Sans Serif für west- und mittelepäisch, Griechisch, Türkisch, Griechisch, Türkisch und Sprachen mithilfe eines kyrillischen Skripts zugeordnet. MS UI- (Ui) Für Japanisch; Gulim für Koreanisch; Simsun für Chinesisch (vereinfacht) PMinglu für chinesisch (traditionell) Etc.

### <a name="font-mapping-on-windows-2000-windows-xp-windows-server-2003-windows-vista-and-windows-7"></a>Schriftartzuordnung auf Windows 2000, Windows XP, Windows Server 2003, Windows Vista und Windows 7

Beide logischen Schriftarten werden Unicode-basierten TrueType-Schriftarten zugeordnet. MS Shell Dlg verwendet Microsoft Sans Serif (unterscheidet sich von MS Sans Serif), wenn die Installationssprache nicht Japanisch ist. MS Shell Dlg wird MS UI Components zugeordnet, wenn die Installationssprache Japanisch ist.

Auf Windows XP XP-SYSTEMS wird MS Shell Dlg nur dann ms ui(Ui), wenn das Gebietsschema des Systems und die Benutzeroberflächensprache auf Japanisch festgelegt sind. Andernfalls wird MS Shell Dlg Microsoft Sans Serif zugeordnet.

Auf Windows Vista und Windows 7 wird MS Shell Dlg MS UI Assemble zugeordnet, wenn die Standardsprache der Benutzeroberfläche des Computers (unabhängig von der Installationssprache) auf Japanisch festgelegt ist. MS Shell Dlg wird Microsoft Sans Serif zugeordnet, wenn die Standardsprache der Benutzeroberfläche des Computers auf eine andere Sprache als Japanisch festgelegt ist.

MS Shell Dlg 2 verwendet einfach die Schriftart Tahoma unabhängig von der Sprache. Der Hauptvorteil von Tahoma gegenüber Microsoft Sans Serif besteht darin, dass Tahoma über ein natives fett formatiertes Gesicht verfügt. Der Hauptnachteil besteht darin, dass ältere Betriebssysteme es möglicherweise nicht installiert haben und eine weniger attraktive Schriftart ersetzen können.

Zeichen, die nicht in Tahoma oder Microsoft Sans Serif implementiert sind, können in anderen Windows Schriftarten implementiert werden, die für die Textanzeige auf Benutzeroberflächen verwendet werden. Je nachdem, welche Steuerelemente oder APIs zum Anzeigen von Text verwendet werden, kann das System verschiedene Mechanismen wie [die Schriftartverknüpfung](https://msdn.microsoft.com/globalization/mt662331) verwenden, um solche Schriftarten automatisch für die Anzeige dieser Zeichen auszuwählen.

Anwendungen können Microsoft Sans Serif oder Tahoma explizit verwenden und die Dekonstruierungsebene für die Verwendung von MS Shell Dlg oder MS Shell Dlg 2 sparen. Aufgrund der Schriftartverknüpfung stellt die Angabe von Microsoft Sans Serif oder Tahoma entsprechende Glyphen für alle Sprachen bereit.

## <a name="use-ms-shell-dlg-for-a-non-english-application-on-windows-me9895"></a>Verwenden von MS Shell Dlg für eine nicht englische Anwendung auf Windows Me/98/95

Am Windows Me/98/95 ist MS Shell Dlg nicht für die Verwendung mit einer statischen, nicht englischen Benutzeroberfläche vorgesehen, die ausgeführt wird, wenn der Benutzer ein Gebietsschema mit einem anderen Windows Basiszeichensatz ausgewählt hat. In diesem Fall wird die Sprache der Benutzeroberfläche der Anwendung möglicherweise nicht mit der Schriftart unterstützt, die durch MS Shell Dlg ersetzt wird.

Wenn der Benutzer beispielsweise eine deutsche Version von Windows verwendet und eine Nicht-Unicode-Anwendung in griechisch-sprache installieren möchte, versucht der Benutzer, das Gebietsschema in Griechisch (Griechisch) zu ändern. Durch diese Aktion wird MS Shell Dlg auf eine griechisch-Schriftart zurückgesetzt, aber diese Schriftart enthält nicht alle Glyphen, die für die Anzeige auf Deutsch erforderlich sind. Daher werden alle Nicht-ASCII-Zeichen auf der Benutzeroberfläche der deutschen Sprache nicht ordnungsgemäß angezeigt. Um dieses Szenario zu unterstützen, muss eine Anwendung MS Shell Dlg auf eine Schriftart festlegen, die sowohl die westepäischen als auch die griechischfarbenen Glyphen enthält.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Internationale Schriftartenenumeration und -auswahl](using-international-fonts-and-text.md)
</dt> <dt>

[Multilingual User Interface](multilingual-user-interface.md)
</dt> </dl>

 

 
