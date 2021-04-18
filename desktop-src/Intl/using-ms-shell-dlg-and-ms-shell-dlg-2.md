---
description: Verwenden von MS Shell Dlg und MS Shell Dlg 2
ms.assetid: ac3b57a6-5b92-4366-ad71-c501cec60997
title: Verwenden von MS Shell Dlg und MS Shell Dlg 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad43f972e776151551fa312ce2bd8ed6d19be58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106354851"
---
# <a name="using-ms-shell-dlg-and-ms-shell-dlg-2"></a>Verwenden von MS Shell Dlg und MS Shell Dlg 2

Windows ist in lokalisierten Editionen für viele Sprachen verfügbar. Die englischsprachige Edition kann jedoch auch zum Ausführen von Anwendungen verwendet werden, die in anderen Sprachen als Englisch geschrieben sind. Dies gilt auch, wenn das Skript, das für diese Sprachen verwendet wird, anders ist, als wenn Anwendungen in Griechisch oder Japanisch geschrieben werden. Diese Anwendungen erfordern eine Benutzeroberfläche mit Dialogfeldern, Symbolen und Dienstprogrammen, die Informationen in der Anwendungs Sprache bereitstellen, die sich möglicherweise von der Sprache unterscheiden, die in der aktuellen Windows-Benutzeroberfläche verwendet wird.

Das Problem beim Auswählen der Schriftart für eine Benutzeroberfläche ist offensichtlich. Beispielsweise ist die Shell-Schriftart, die auch als System-oder Standard Schriftart bezeichnet wird, für Englisch (USA) Windows 98 MS Sans Serif, während die Shell-Schriftart für Griechisch (Griechenland) Windows 98 MS Sans Serif Greek ist. Für Japanisch (Japan) Windows 98 ist die Shell-Schriftart MS UI Gothic. Diese Zeichensätze können nicht direkt einander zugeordnet werden. Wenn Sie MS Sans Serif durch MS Sans Serif Greek ersetzen, wenn das Gebiets Schema auf Griechisch (Griechenland) festgelegt ist, können vorhandene Anwendungen nicht ordnungsgemäß ausgeführt werden oder griechische Zeichen in Systemmenüs, Dialogfeldern und Bearbeitungs Steuerelementen anzeigen.

Windows löst dieses Problem, indem es die logischen Schriftarten MS Shell Dlg und MS Shell Dlg 2 verwendet, um die entsprechende Schriftart für die Skript Anzeige auszuwählen. In diesem Abschnitt werden verschiedene Programmier Überlegungen für die Verwendung der logischen Schriftarten zum Implementieren von Dialogfeldern, Menüs und ähnliches für flexible Benutzeroberflächen behandelt, die für alle unterstützten Windows-Betriebssysteme und in allen Sprachen gut angezeigt werden. Weitere Informationen finden Sie unter [Erstellen und](../gdi/font-creation-and-selection.md)auswählen von Schriftarten. Weitere Informationen zur Verwendung der MUI-Technologie (mehrsprachige Benutzeroberfläche) bei der Erstellung von Benutzeroberflächen für mehrsprachige Anwendungen finden Sie unter [mehrsprachige Benutzeroberfläche](multilingual-user-interface.md) .

## <a name="about-the-logical-fonts"></a>Informationen zu logischen Schriftarten

Die logischen Schriftarten MS Shell Dlg und MS Shell Dlg 2 sind im wesentlichen Gesichts Namen, die für die Zuordnung verwendet werden, um Unterstützung für Gebiets Schemas/Kulturen mit Zeichen zu ermöglichen, die nicht in der Codepage 1252 enthalten sind, dem Windows-Zeichensatz für die USA und Westeuropa MS Shell Dlg wird der standardmäßigen shellschriftart zugeordnet, die der aktuellen Kultur bzw. dem Gebiets Schema zugeordnet ist, und unterstützt die klassische Windows-Desktop Suche. Der Gesichts Name von MS Shell Dlg 2 wurde in Windows 2000 eingeführt, um das in Windows 2000 eingeführte aussehen zu unterstützen.

Wenn Ihre Anwendung z. b. MS Shell Dlg oder MS Shell Dlg 2 für die zugehörigen Dialogfelder verwendet, kann sich ein Lokalisierungsteam, das die griechischen Sprachressourcen für Ihre Anwendung erstellt, auf die Übersetzung von Text konzentrieren. Sie müssen sich nicht um Probleme kümmern, wie z. b. den Unterschied zwischen MS Sans Serif und MS Sans Serif Greek.

> [!Note]  
> Die von MS Shell Dlg und MS Shell Dlg 2 generierten Schriftarten unterscheiden sich in verschiedenen Windows-Versionen. Daher sollten Sie sicherstellen, dass die Benutzeroberflächen Elemente auf allen Plattformen gut angezeigt werden.

 

## <a name="handle-hard-coded-font-names"></a>Behandeln von Hard-Coded Schriftart Namen

Die Verwendung von Unicode ermöglicht es Anwendungen, Tausende von unterschiedlichen Zeichen zu behandeln, aber die meisten Schriftarten decken nicht den gesamten Unicode-Zeichensatz ab. Bei Ihren Anwendungen sollten Schriftart Namen nicht hart codiert werden. Ein Grund hierfür ist, dass die hart Codierung eines Schriftart namens, der Zeichen für eine Sprache anzeigt, und nicht von Zeichen für eine andere Sprache bewirkt, dass der lokalisierte Text in der zweiten Sprache falsch angezeigt wird. Ein weiterer Grund für die fest Codierung von Schriftart Namen ist, dass die gewünschte Schriftart möglicherweise nicht auf dem Betriebssystem geladen wird, das den Anwendungs Text anzeigt.

Die beste Möglichkeit, Schriftart Namen zu behandeln, besteht darin, Sie als lokalisierbare Ressourcen zu betrachten. Durch die Verwendung einer logischen Schriftart wird das Problem der Ausführung Ihrer Schnittstelle mit einer beliebigen Sprache unter Windows NT oder Windows 2000 für jede Sprache gelöst. Das Festlegen eines Schriftart namens als lokalisierbare Ressource ermöglicht es dem Lokalisierer, die Schriftart für die lokalisierte Benutzeroberfläche zu ändern.

## <a name="handle-hard-coded-font-sizes"></a>Behandeln von Hard-Coded Schriftart Größen

Einige Skripts sind komplex, und es ist erforderlich, dass eine große Anzahl von Pixeln ordnungsgemäß angezeigt wird. Die meisten englischen Zeichen werden z. b. in einem 5x7-Raster angezeigt, aber japanische Zeichen erfordern mindestens ein 16x16-Raster, um offensichtlich zu sein. Obwohl Chinesisch ein 24x24-Raster benötigt, benötigt Thai nur 8 Pixel für die Breite, aber mindestens 22 Pixel für die Höhe. Es ist leicht zu verstehen, dass einige Zeichen möglicherweise nur mit einem kleinen Schrift Grad lesbar sind.

Die Benutzeroberfläche der Anwendung sollte Schriftart Größen als lokalisierbare Ressourcen behandeln. Durch die Verwendung einer logischen Schriftart wird das Problem der Ausführung Ihrer Schnittstelle mit einer beliebigen Sprache unter Windows NT oder Windows 2000 für jede Sprache gelöst. Wenn Sie einen Schrift Grad als lokalisierbare Ressource festlegen, kann der Lokalisierer die Schriftart für die lokalisierte Benutzeroberfläche ändern.

## <a name="map-the-logical-fonts"></a>Zuordnen der logischen Schriftarten

Jede der logischen Schriftarten wird durch einen Eintrag in der Registrierung der entsprechenden shellschriftart für das derzeit aktive Gebiets Schema zugeordnet. Wenn eine der logischen Schriftarten verwendet wird, wechselt Windows zur Laufzeit für das aktuell ausgewählte Gebiets Schema zur Schriftart. Dieser Vorgang ermöglicht die korrekte Anzeige der Windows-Benutzeroberfläche (Englisch) (USA) sowie der Zeichen, die nicht in der Codepage 1252 enthalten sind. Auf diese Weise können lokalisierte Anwendungen zurzeit auf der englischen (USA) Version von Windows ohne Änderung ausgeführt werden.

Jeder Windows-Computer ordnet MS Shell Dlg und MS Shell Dlg 2 basierend auf der definierten Sprache für nicht-Unicode-Programme, die in der [nls-Terminologie](nls-terminology.md)beschrieben werden, einer entsprechenden physischen Schriftart zu. Die tatsächlichen Zuordnungen werden im Registrierungsschlüssel HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ Current Version \\ fontsubstitut gespeichert.

### <a name="font-mapping-on-windows-me9895"></a>Schriftart Zuordnung unter Windows Me/98/95

MS Shell Dlg ist im Allgemeinen einer Code Page spezifischen Version von MS Sans Serif zugeordnet.

### <a name="font-mapping-on-windows-nt-40"></a>Schriftart Zuordnung unter Windows NT 4,0

MS Shell Dlg wird MS Sans Serif für westliche und mitteleuropäische, Griechisch, Türkisch, Baltikum und Sprachen mithilfe von kyrillischen Skripts zugeordnet. MS UI Gothic für Japanisch; Gulim für Koreanisch; Simsun für vereinfachtes Chinesisch Pminglu für Chinesisch (traditionell); etc.

### <a name="font-mapping-on-windows-2000-windows-xp-windows-server-2003-windows-vista-and-windows-7"></a>Schriftart Zuordnung unter Windows 2000, Windows XP, Windows Server 2003, Windows Vista und Windows 7

Beide logischen Schriftarten werden Unicode-basierten TrueType-Schriftarten zugeordnet. MS Shell Dlg verwendet Microsoft Sans Serif (von MS Sans Serif unterschieden), wenn die Installationssprache nicht Japanisch ist. MS Shell Dlg wird MS UI Gothic zugeordnet, wenn die Installationssprache Japanisch ist.

Auf Windows XP-MUI-Systemen ist MS Shell Dlg nur dann MS UI Gothic zugeordnet, wenn das System Gebiets Schema und die Benutzeroberflächen Sprache auf Japanisch festgelegt sind. Andernfalls wird MS Shell Dlg Microsoft Sans Serif zugeordnet.

Unter Windows Vista und Windows 7 ist MS Shell Dlg der MS UI Gothic zugeordnet, wenn die Standardbenutzer Oberflächen Sprache des Computers auf Japanisch festgelegt ist (unabhängig von der Installationssprache). MS Shell Dlg wird Microsoft Sans Serif zugeordnet, wenn die Standardbenutzer Oberflächen Sprache des Computers auf eine andere Sprache als Japanisch festgelegt ist.

MS Shell Dlg 2 verwendet die Tahoma-Schriftart unabhängig von der Sprache. Der Hauptvorteil von Tahoma gegenüber Microsoft Sans Serif besteht darin, dass Tahoma eine systemeigene Fett formatierte Schriftart hat. Der Hauptnachteil besteht darin, dass ältere Betriebssysteme möglicherweise nicht installiert sind und eine weniger attraktive Schriftart ersetzen können.

Zeichen, die nicht in Tahoma oder Microsoft Sans Serif implementiert sind, können in anderen Windows-Schriftarten implementiert werden, die für die Anzeige von Text in Benutzeroberflächen verwendet werden. Abhängig davon, welche Steuerelemente oder APIs zum Anzeigen von Text verwendet werden, können verschiedene Mechanismen, wie z. b. die [Schriftart Verknüpfung](https://msdn.microsoft.com/globalization/mt662331) , vom System verwendet werden, um diese Schriftarten für die Anzeige dieser Zeichen automatisch auszuwählen.

Anwendungen können entweder Microsoft Sans Serif oder Tahoma explizit verwenden und den Grad der Dereferenzierung bei der Verwendung von MS Shell Dlg oder MS Shell Dlg 2 speichern. Aufgrund der Schriftart Verknüpfung bietet die Angabe von Microsoft Sans Serif oder Tahoma geeignete Symbole für alle Sprachen.

## <a name="use-ms-shell-dlg-for-a-non-english-application-on-windows-me9895"></a>Verwenden von MS Shell Dlg für eine nicht englischsprachige Anwendung unter Windows Me/98/95

Unter Windows Me/98/95 ist MS Shell Dlg nicht für die Verwendung mit einer statischen, nicht englischsprachigen Benutzeroberflächen Anwendung vorgesehen, die ausgeführt wird, wenn der Benutzer ein Gebiets Schema mit einem anderen Windows-Basis Zeichensatz ausgewählt hat. In diesem Fall wird die Sprache der Benutzeroberfläche der Anwendung möglicherweise nicht mit der Schriftart unterstützt, die für MS Shell Dlg ersetzt wird.

Wenn der Benutzer z. b. eine deutschsprachige Version von Windows verwendet und eine nicht-Unicode-Anwendung für Griechisch (Griechisch) installieren möchte, versucht der Benutzer, das Gebiets Schema in Griechisch (Griechenland) zu ändern. Durch diese Aktion wird MS Shell Dlg auf eine griechische Schriftart zurückgesetzt, aber diese Schriftart enthält nicht alle Symbole, die für die Anzeige in Deutsch erforderlich sind. Daher werden alle nicht-ASCII-Zeichen in der deutschsprachigen Benutzeroberfläche nicht ordnungsgemäß angezeigt. Um dieses Szenario zu unterstützen, muss eine Anwendung MS Shell Dlg auf eine Schriftart festlegen, die sowohl das westliche europäisch als auch das griechische Glyphs-Zeichen enthält.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Internationale Schriftart Enumeration und-Auswahl](using-international-fonts-and-text.md)
</dt> <dt>

[Multilingual User Interface](multilingual-user-interface.md)
</dt> </dl>

 

 
