---
description: Ihre globalisierte Anwendung muss eine Vielzahl von Benutzeroberflächen Elementen definieren, z. b. Menüs, Dialogfelder, Hilfe Zeichenfolgen und andere Elemente, die als lokalisierte Ressourcen dargestellt werden.
ms.assetid: 4d8b769d-0830-4e4e-b284-ce0b21dfe5d4
title: MUI-Ressourcenverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeed59c4b835e2c93e5f4cfc9988509349d8b0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347020"
---
# <a name="mui-resource-management"></a>MUI-Ressourcenverwaltung

Ihre globalisierte Anwendung muss eine Vielzahl von Benutzeroberflächen Elementen definieren, z. b. Menüs, Dialogfelder, Hilfe Zeichenfolgen und andere Elemente, die als lokalisierte Ressourcen dargestellt werden. Die Sprache der Benutzeroberfläche wird zu einer der Einstellungen für die Anwendung. In diesem Abschnitt wird die MUI-Ressourcen Technologie beschrieben, die Sie zum Erstellen Ihrer Anwendungs Ressourcen verwenden sollten.

## <a name="features-of-the-mui-resource-technology"></a>Features der MUI-Ressourcen Technologie

Die in Windows Vista und höher verfügbar gemachte MUI-Ressourcen Technologie weist die folgenden Eigenschaften auf:

-   Sprachspezifische Ressourcen Dateien werden getrennt von der Anwendungscode Binärdatei gespeichert, sodass sich eine Codeänderung nicht auf die Ressourcen auswirkt.
-   Die Ressourcen für mehrere Sprachen können in einer einzelnen Installation oder in separaten Installationen für jede Sprache bereitgestellt werden.
-   Eine Ressource wird geladen und entsprechend der Sprache der Anwendung angezeigt, die vom Benutzer festgelegt wurde.

Diese Technologie verknüpft die Ressourcen, die in sprachspezifischen Dateien definiert sind, mit einer bestimmten Version einer sprach neutralen Datei (LN). Bei der LN-Datei handelt es sich um eine Win32 PE-Datei, die den Anwendungscode Binär und sprachneutrale Ressourcen darstellt. Die Zuordnung von Dateien verwendet eine Prüfsumme, die in den Ressourcen Konfigurationsdaten in allen zugeordneten Dateien widergespiegelt wird. Das Ressourcen Lade Modul verwendet die Prüfsumme, um zu überprüfen, ob die Dateien dieselbe Version der erforderlichen Ressourcen enthalten. Außerdem wird die Sprache in der sprachspezifischen Datei mit dem zugehörigen Ordnernamen überprüft. Das Lade Modul lädt eine Ressourcen Datei nicht, wenn die entsprechende Zuordnung nicht eingerichtet wurde.

Insbesondere wird die Haupt Prüfsumme aus den Haupt-und neben Versionsnummern einer Datei und dem Dateinamen (Groß-/Kleinschreibung) berechnet, die von der Versions Ressource abgerufen werden. Diese Prüfsumme sollte zwischen RTM-und Service Pack-Versionen derselben Komponente nicht geändert werden. Außerdem wird eine Dienst Checksumme verwendet, um die entsprechende Version der zu ladenden sprachspezifischen Ressourcen Datei zu bestimmen. Diese Prüfsumme wird basierend auf den lokalisierbaren Ressourcen in der Datei berechnet.

MUI liefert zwei Ressourcen Dienstprogramme, mit denen Sie Ressourcen Dateien für Ihre Anwendung vorbereiten können. Mit einem MUI-spezifischen Dienstprogramm, das als Mut bezeichnet wird, können Sie eine ln-Datei und zugehörige sprachspezifische Ressourcen Dateien erstellen. Unter Windows Vista und höher wurde der Windows RC-Compiler ebenfalls so geändert, dass diese Dateien gemäß der MUI-Ressourcen Technologie erstellt werden. Syntax und Details zu diesen Tools finden Sie unter [Ressourcen Dienstprogramme](resource-utilities.md).

## <a name="ln-file"></a>LN-Datei

Die LN-Datei für eine MUI-Anwendung enthält ausführbaren Code und sprachneutrale Ressourcen, die von allen Sprachversionen der Anwendung gemeinsam genutzt und installiert werden.

## <a name="language-specific-resource-file"></a>Ressourcen Datei Language-Specific

Eine sprachspezifische Ressourcen Datei enthält normalerweise Benutzeroberflächen-Zeichen folgen und andere Elemente, für die eine Lokalisierung für eine bestimmte Sprache erforderlich ist. Ihre MUI-Anwendung verwendet eine sprachspezifische Ressourcen Datei pro unterstützter Sprache. Die LN-Datei für die Anwendung ist für jede sprachspezifische Ressourcen Datei identisch.

Wenn sprachspezifische Dateien mithilfe der MUI-Ressourcen Technologie erstellt werden, verfügen Sie über die Erweiterung ". MUI" und werden wie folgt behandelt:

-   Die sprachspezifischen Dateien, die einer bestimmten LN-Datei zugeordnet sind, haben den gleichen Dateinamen, der durch Hinzufügen der Erweiterung ". MUI" zum vollständigen Dateinamen (mit Erweiterung) der entsprechenden LN-Datei gebildet wird. Beispielsweise enthält eine ln-Datei mit dem Namen "Myfile.dll" sprachspezifische Dateien mit dem Namen "Myfile.dll. MUI".
-   Die sprachspezifischen Dateien befinden sich in den Unterordnern des Ordners, der die LN-Datei enthält. Jeder Ordnername spiegelt die Sprache wider.

## <a name="resource-configuration-data"></a>Ressourcen Konfigurationsdaten

Um einer LN-Datei die sprachspezifischen Dateien zuzuordnen, verwendet die MUI-Ressourcen Technologie Ressourcen Konfigurationsdaten, einschließlich der Prüfsumme. Die ressourcenbuildprozedur speichert diese Informationen in einem RC-Konfigurations Abschnitt jeder LN und sprachspezifischen Datei. Eine lesbare Form dieser Informationen ist über das Dienstprogramm "muject" verfügbar. Weitere Informationen finden Sie unter [Ressourcen Dienstprogramme](resource-utilities.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen über mehrsprachige Benutzeroberfläche](about-multilingual-user-interface.md)
</dt> <dt>

[Ressourcen Hilfsprogramme](resource-utilities.md)
</dt> </dl>

 

 



