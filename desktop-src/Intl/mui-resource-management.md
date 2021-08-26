---
description: Ihre globalisierte Anwendung muss eine Vielzahl von Elementen der Benutzeroberfläche definieren, z. B. Menüs, Dialogfelder, Hilfezeichenfolgen und andere Elemente, die als lokalisierte Ressourcen dargestellt werden.
ms.assetid: 4d8b769d-0830-4e4e-b284-ce0b21dfe5d4
title: SOURCE-Ressourcenverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94c0b489d10ae28ca0fe7c659153b58c6ee7713e4eda4e1da9d96ffe16ae1a2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041270"
---
# <a name="mui-resource-management"></a>SOURCE-Ressourcenverwaltung

Ihre globalisierte Anwendung muss eine Vielzahl von Elementen der Benutzeroberfläche definieren, z. B. Menüs, Dialogfelder, Hilfezeichenfolgen und andere Elemente, die als lokalisierte Ressourcen dargestellt werden. Die Sprache der Benutzeroberfläche wird zu einer der Einstellungen für die Anwendung. In diesem Abschnitt wird die RESOURCES-Ressourcentechnologie beschrieben, die Sie zum Erstellen Ihrer Anwendungsressourcen verwenden sollten.

## <a name="features-of-the-mui-resource-technology"></a>Features der TECHNOLOGY-Ressourcentechnologie für DIE RESSOURCE

Die IN Windows Vista und höher verfügbar gemachte TECHNOLOGY DER RESSOURCE WEIST die folgenden Merkmale auf:

-   Sprachspezifische Ressourcendateien werden getrennt von der Binärdatei des Anwendungscodes gespeichert, sodass sich eine Codeänderung nicht auf die Ressourcen auswirkt.
-   Die Ressourcen für mehrere Sprachen können in einer einzelnen Installation oder in separaten Installationen für jede Sprache bereitgestellt werden.
-   Eine Ressource wird gemäß der Sprache der Anwendung geladen und angezeigt, wie vom Benutzer festgelegt.

Diese Technologie ordnet die in sprachspezifischen Dateien definierten Ressourcen einer bestimmten Version einer sprachneutralen Datei (LN) zu. Die LN-Datei ist eine Win32 PE-Datei, die die binären und sprachneutralen Ressourcen des Anwendungscodes darstellt. Die Zuordnung von Dateien verwendet eine Prüfsumme, die in den Ressourcenkonfigurationsdaten in allen zugeordneten Dateien widergespiegelt wird. Das Ressourcenladeprogramm verwendet die Prüfsumme, um zu überprüfen, ob die Dateien die gleiche Version der erforderlichen Ressourcen enthalten. Außerdem wird die Sprache in der sprachspezifischen Datei mit dem Ordnernamen überprüft. Das Ladeprogramm lädt keine Ressourcendatei, wenn die entsprechende Zuordnung nicht eingerichtet wurde.

Insbesondere wird die Hauptprüfsumme anhand der Haupt- und Nebenversionsnummer einer Datei und des Dateinamens (Groß-/Kleinschreibung beachten) berechnet, die von der Versionsressource abgerufen werden. Diese Prüfsumme darf sich nicht zwischen RTM- und Service Pack-Versionen derselben Komponente ändern. Darüber hinaus wird eine Dienstprüfsumme verwendet, um die geeignete Version der sprachspezifischen Ressourcendatei zu bestimmen, die geladen werden soll. Diese Prüfsumme wird basierend auf den lokalisierbaren Ressourcen in der Datei berechnet.

MITHILFE von TWO werden zwei Ressourcen-Hilfsprogramme erstellt, mit denen Sie Ressourcendateien für Ihre Anwendung vorbereiten können. Mit einem DIENSTPROGRAMM-spezifischen Hilfsprogramm namensRCT können Sie eine LN-Datei und zugehörige sprachspezifische Ressourcendateien erstellen. Auf Windows Vista und höher wurde auch der Windows RC-Compiler geändert, um diese Dateien gemäß der RESSOURCENtechnologie VON CAB zu erstellen. Syntax und Details zu diesen Tools finden Sie unter [Ressourcenhilfsprogramme.](resource-utilities.md)

## <a name="ln-file"></a>LN-Datei

Die LN-Datei für eine CSV-Anwendung enthält ausführbaren Code und sprachneutrale Ressourcen, die von allen Sprachversionen der Anwendung gemeinsam genutzt und installiert werden.

## <a name="language-specific-resource-file"></a>Language-Specific-Ressourcendatei

Eine sprachspezifische Ressourcendatei enthält normalerweise Benutzeroberflächenzeichenfolgen und andere Elemente, die eine Lokalisierung für eine bestimmte Sprache erfordern. Ihre LANGUAGE-Anwendung verwendet eine sprachspezifische Ressourcendatei pro unterstützter Sprache. Die LN-Datei für die Anwendung ist für jede sprachspezifische Ressourcendatei identisch.

Bei der Erstellung mithilfe der TECHNOLOGY OFC-Ressourcen verfügen sprachspezifische Dateien über die Erweiterung ".extensions" und werden wie folgt behandelt:

-   Die sprachspezifischen Dateien, die einer bestimmten LN-Datei zugeordnet sind, verwenden alle den gleichen Dateinamen, der durch Hinzufügen der Erweiterung ".extensions" zum vollständigen Dateinamen (mit Erweiterung) der entsprechenden LN-Datei gebildet wird. Eine LN-Datei mit dem Namen "Myfile.dll" enthält z. B. sprachspezifische Dateien mit dem Namen "Myfile.dll.dateierweiterung".
-   Die sprachspezifischen Dateien befinden sich in Unterordnern des Ordners, der die LN-Datei enthält. Jeder Ordnername gibt die Sprache an.

## <a name="resource-configuration-data"></a>Ressourcenkonfigurationsdaten

Um eine LN-Datei den sprachspezifischen Dateien zuzuordnen, verwendet die TECHNOLOGY OFC Ressourcenkonfigurationsdaten, einschließlich der Prüfsumme. Die Ressourcenbuildprozedur platziert diese Informationen in einem RC-Konfigurationsabschnitt jeder LN und sprachspezifischen Datei. Eine für Menschen lesbare Form dieser Informationen ist über das HILFSPROGRAMM UTILITYRCT verfügbar. Weitere Informationen finden Sie unter [Ressourcen-Hilfsprogramme.](resource-utilities.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen mehrsprachige Benutzeroberfläche](about-multilingual-user-interface.md)
</dt> <dt>

[Ressourcen-Hilfsprogramme](resource-utilities.md)
</dt> </dl>

 

 



