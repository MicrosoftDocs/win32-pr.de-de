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

Windows ist in lokalisierten Editionen für viele Sprachen verfügbar. Die englischsprachige Edition kann jedoch auch zum Ausführen von Anwendungen verwendet werden, die in anderen Sprachen als Englisch geschrieben sind. Dies gilt auch, wenn das für diese Sprachen verwendete Skript anders ist, als wenn Anwendungen in Griechisch oder Japanisch geschrieben werden. Diese Anwendungen erfordern eine Benutzeroberfläche mit Dialogfeldern, Symbolen und Hilfsprogrammen, die Informationen in der Anwendungssprache bereitstellen, die sich von der Sprache unterscheiden können, die in der aktuellen Windows verwendet wird.

Das Problem bei der Auswahl der Schriftart für eine Benutzeroberfläche ist offensichtlich. Beispielsweise ist die Shellschriftart, die auch als System- oder Standardschriftart bezeichnet wird, für Englisch (USA) Windows 98 MS Sans Serif, während die Shellschriftart für Griechisch (Windows 98) MS Sans Serif Griechisch ist. Für Japanisch (Japan) Windows 98 ist die Shellschriftart MS UI Ui. Diese Zeichensätze können nicht direkt einander zugeordnet werden. Wenn MS Sans Serif durch MS Sans Serif Griechisch ersetzt wird, wenn das -Locale auf Griechisch (Griechisch) festgelegt ist, können vorhandene Anwendungen nicht ordnungsgemäß ausgeführt werden oder in Systemmenüs, Dialogfeldern und Bearbeitungssteuerelementen griechisch angezeigt werden.

Windows dieses Problem mithilfe der logischen Schriftarten MS Shell Dlg und MS Shell Dlg 2 gelöst, um die Auswahl der geeigneten Schriftart für die Skriptanzeige zu ermöglichen. In diesem Abschnitt werden verschiedene Überlegungen zur Programmierung bei der Verwendung logischer Schriftarten zum Implementieren von Dialogfeldern, Menüs und deren Verwendung für flexible Benutzeroberflächen behandelt, die auf allen unterstützten Windows-Betriebssystemen und in allen Sprachen gut angezeigt werden. Weitere Informationen finden Sie unter [Schriftarterstellung und -auswahl.](../gdi/font-creation-and-selection.md) Weitere Informationen [mehrsprachige Benutzeroberfläche](multilingual-user-interface.md) verwendung der mehrsprachige Benutzeroberfläche-Technologie (TECHNOLOGY) beim Erstellen von Benutzeroberflächen für Mehrsprachige Anwendungen finden Sie auch unter mehrsprachige Benutzeroberfläche.

## <a name="about-the-logical-fonts"></a>Informationen zu logischen Schriftarten

Bei den logischen Schriftarten MS Shell Dlg und MS Shell Dlg 2 handelt es sich im Wesentlichen um Gesichtsnamen, die für die Zuordnung verwendet werden, um die Unterstützung für Lokal-/Kulturen mit Zeichen zu ermöglichen, die nicht in Codepage 1252 enthalten sind, dem Windows-Zeichensatz für die USA und Westeuropa. MS Shell Dlg wird der Standardshellschriftart zugeordnet, die der aktuellen Kultur/dem aktuellen Windows zugeordnet ist, und unterstützt das klassische Windows Desktop-Look. Ms Shell Dlg 2 face name wurde in Windows 2000 eingeführt, um das Aussehen zu unterstützen, das mit Windows 2000 eingeführt wurde.

Wenn Ihre Anwendung z. B. MS Shell Dlg oder MS Shell Dlg 2 für ihre Dialogfelder verwendet, kann sich ein Lokalisierungsteam, das Ressourcen in griechisch-Sprache für Ihre Anwendung erstellt, auf die Übersetzung von Text konzentrieren. Sie müssen sich nicht um Probleme wie den Unterschied zwischen MS Sans Serif und MS Sans Serif (Griechisch) befassen.

> [!Note]  
> Die von MS Shell Dlg und MS Shell Dlg 2 generierten Schriftarten unterscheiden sich je nach Windows Versionen. Daher sollten Sie sicherstellen, dass Ihre Benutzeroberflächenelemente auf allen Plattformen gut angezeigt werden.

 

## <a name="handle-hard-coded-font-names"></a>Behandeln Hard-Coded Schriftartnamen

Die Verwendung von Unicode ermöglicht Anwendungen den Umgang mit Tausenden von verschiedenen Zeichen, aber die meisten Schriftarten decken nicht den ganzen Unicode-Zeichensatz ab. Ihre Anwendungen sollten keine Hartcodeschriftartnamen verwenden. Ein Grund ist, dass die hart codierte Codierung eines Schriftartnamens, der Zeichen für eine Sprache und keine Zeichen für eine andere Sprache anzeigt, dazu führt, dass der lokalisierte Text in der zweiten Sprache falsch angezeigt wird. Ein weiterer Grund, Schriftartnamen nicht hart zu codieren, ist, dass die gewünschte Schriftart möglicherweise nicht auf das Betriebssystem geladen wird, das Anwendungstext zeigt.

Die beste Möglichkeit, Schriftartnamen zu behandeln, ist, sie als lokalisierbare Ressourcen zu betrachten. Die Verwendung einer logischen Schriftart löst das Problem der Ausführung Ihrer Schnittstelle mit einer beliebigen Sprache in Windows NT oder Windows 2000 für jede Sprache. Wenn Sie einen Schriftartnamen als lokalisierbare Ressource festlegen, kann Ihr Lokalisierer die Schriftart für die lokalisierte Benutzeroberfläche ändern.

## <a name="handle-hard-coded-font-sizes"></a>Handle Hard-Coded Schriftgraden

Einige Skripts sind komplex und erfordern eine große Anzahl von Pixeln, um ordnungsgemäß angezeigt zu werden. Beispielsweise werden die meisten englischen Zeichen in einem 5x7-Raster angezeigt, aber japanische Zeichen benötigen mindestens ein 16x16-Raster, um klar zu erkennen. Während Chinesisch ein 24 x 24-Raster benötigt, benötigt Thailändisch nur 8 Pixel für die Breite, aber mindestens 22 Pixel für die Höhe. Es ist leicht zu verstehen, dass einige Zeichen bei einem kleinen Schriftgrad möglicherweise nicht lesbar sind.

Die Benutzeroberfläche Ihrer Anwendung sollte Schriftgrößen als lokalisierbare Ressourcen behandeln. Die Verwendung einer logischen Schriftart löst das Problem der Ausführung Ihrer Schnittstelle mit einer beliebigen Sprache in Windows NT oder Windows 2000 für jede Sprache. Wenn Sie einen Schriftgrad als lokalisierbare Ressource festlegen, kann Ihr Lokalisierer die Schriftart für die lokalisierte Benutzeroberfläche ändern.

## <a name="map-the-logical-fonts"></a>Zuordnen der logischen Schriftarten

Jede der logischen Schriftarten wird durch einen Eintrag in der Registrierung der entsprechenden Shellschriftart für das derzeit aktive Locale zugeordnet. Wenn eine der logischen Schriftarten verwendet wird, Windows zur Schriftart für das aktuell ausgewählte Locale zur Laufzeit wechseln. Dieser Vorgang ermöglicht die korrekte Anzeige der englischen (USA) Windows-Benutzeroberfläche sowie von Zeichen, die nicht auf der Codepage 1252 enthalten sind. Daher können lokalisierte Anwendungen derzeit auf der englischen Version (USA) von Windows ausgeführt werden.

Jeder Windows ordnet MS Shell Dlg und MS Shell Dlg 2 einer entsprechenden physischen Schriftart zu, basierend auf der definierten Sprache für Nicht-Unicode-Programme, wie unter [NLS-Terminologie beschrieben.](nls-terminology.md) Die tatsächlichen Zuordnungen werden im Registrierungsschlüssel HKEY \_ LOCAL MACHINE Software Microsoft Windows NT Current Version \_ \\ \\ \\ \\ \\ FontSubstitutes gespeichert.

### <a name="font-mapping-on-windows-me9895"></a>Schriftartzuordnung auf Windows Me/98/95

MS Shell Dlg ist in der Regel einer codepagespezifischen Version von MS Sans Serif verfügbar.

### <a name="font-mapping-on-windows-nt-40"></a>Schriftartzuordnung auf Windows NT 4.0

MS Shell Dlg wird MS Sans Serif für West- und Mitteleigen, Griechisch, Türkisch, Türkisch, Türkisch und Sprachen mithilfe kyrillischer Skripts zu ms sans Serif karten. MS UI Ui Für Japanisch; Gulim für Koreanisch; Simsun für vereinfachtes Chinesisch; PMinglu für traditionelles Chinesisch; Etc.

### <a name="font-mapping-on-windows-2000-windows-xp-windows-server-2003-windows-vista-and-windows-7"></a>Schriftartzuordnung auf Windows 2000, Windows XP, Windows Server 2003, Windows Vista und Windows 7

Beide logischen Schriftarten sind Unicode-basierten TrueType-Schriftarten zuordnen. MS Shell Dlg verwendet Microsoft Sans Serif (im Unterschied zu MS Sans Serif), wenn die Installationssprache nicht Japanisch ist. MS Shell Dlg wird MS UI-Benutzeroberflächenzuordnungen, wenn die Installationssprache Japanisch ist.

Auf Windows XP XP XP-Systemen wird MS Shell Dlg nur dann ms ui ui(MS-UI)-Dlg(MS-UI-Ui)-Systemen angezeigt, wenn das System- und die Benutzeroberflächensprache auf Japanisch festgelegt sind. Andernfalls wird MS Shell Dlg Microsoft Sans Serif zu ordnet.

Unter Windows Vista und Windows 7 wird MS Shell Dlg ms UI-Benutzeroberflächen-Benutzeroberflächenzuordnungen, wenn die Standardsprache der Benutzeroberfläche des Computers (unabhängig von der Installationssprache) auf Japanisch festgelegt ist. MS Shell Dlg wird Microsoft Sans Serif zugestellt, wenn die Standardmäßige Benutzeroberflächensprache des Computers auf eine andere Sprache als Japanisch festgelegt ist.

MS Shell Dlg 2 verwendet einfach die Tahoma-Schriftart unabhängig von der Sprache. Der Hauptvorteil von Tahoma gegenüber Microsoft Sans Serif ist, dass Tahoma über ein natives fett formatierten Schriftgesicht verfügt. Sein Hauptnachteil ist, dass ältere Betriebssysteme es möglicherweise nicht installiert haben und eine weniger ansprechende Schriftart ersetzen können.

Zeichen, die nicht in Tahoma oder Microsoft Sans Serif implementiert sind, können in anderen Windows-Schriftarten implementiert werden, die für die Textanzeige in Benutzeroberflächen verwendet werden. Je nachdem, welche Steuerelemente oder APIs zum Anzeigen [](https://msdn.microsoft.com/globalization/mt662331) von Text verwendet werden, kann das System verschiedene Mechanismen wie Schriftartverknüpfungen verwenden, um solche Schriftarten automatisch für die Anzeige dieser Zeichen auszuwählen.

Anwendungen können entweder Microsoft Sans Serif oder Tahoma explizit verwenden und die Deskriptionsebene bei der Verwendung von MS Shell Dlg oder MS Shell Dlg 2 sparen. Aufgrund der Schriftartverknüpfung stellt die Angabe von Microsoft Sans Serif oder Tahoma geeignete Glyphen für alle Sprachen zur Verfügung.

## <a name="use-ms-shell-dlg-for-a-non-english-application-on-windows-me9895"></a>Verwenden von MS Shell Dlg für eine nicht englische Anwendung auf Windows Me/98/95

In Windows Me/98/95 ist MS Shell Dlg nicht für die Verwendung mit einer statischen, nicht englischsprachigen Benutzeroberflächenanwendung vorgesehen, die ausgeführt wird, wenn der Benutzer ein Locale mit einem anderen Windows-Basiszeichensatz ausgewählt hat. In diesem Fall wird die Benutzeroberflächensprache der Anwendung möglicherweise nicht mit der Schriftart unterstützt, die durch MS Shell Dlg ersetzt wird.

Wenn der Benutzer z. B. eine deutsche Version von Windows verwendet und eine Nicht-Unicode-Anwendung für Griechisch installieren möchte, versucht der Benutzer, das Lokale in Griechisch (Griechisch) zu ändern. Durch diese Aktion wird MS Shell Dlg auf eine schriftart für Griechisch zurückgesetzt, aber diese Schriftart enthält nicht alle Glyphen, die für die Anzeige auf Deutsch erforderlich sind. Daher werden alle Nicht-ASCII-Zeichen in der benutzeroberfläche für Deutsch nicht ordnungsgemäß angezeigt. Um dieses Szenario zu unterstützen, muss eine Anwendung MS Shell Dlg auf eine Schriftart festlegen, die sowohl die westeischen als auch die griechisch-Glyphen enthält.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Internationale Schriftartenenumeration und -auswahl](using-international-fonts-and-text.md)
</dt> <dt>

[Multilingual User Interface](multilingual-user-interface.md)
</dt> </dl>

 

 
