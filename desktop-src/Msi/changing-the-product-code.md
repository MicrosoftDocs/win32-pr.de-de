---
description: Der Produktcode ist eine GUID, bei der es sich um die Prinzipal Identifizierung einer Anwendung oder eines Produkts handelt. Siehe Produkt Codes.
ms.assetid: 4de84885-587d-405f-ba85-d62e09e8ba92
title: Ändern des Produktcodes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0272f1901ef60342f01f4db091e7a4e62b28e30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042152"
---
# <a name="changing-the-product-code"></a>Ändern des Produktcodes

Der Produktcode ist eine GUID, bei der es sich um die Prinzipal Identifizierung einer Anwendung oder eines Produkts handelt. Siehe [Produkt Codes](product-codes.md).

Ein Update, das die folgenden Richtlinien erfüllt, erfordert im Allgemeinen keine Änderung des Produktcodes und kann als [kleines Update](small-updates.md)behandelt werden, oder wenn die Version geändert werden soll, als [geringfügige](minor-upgrades.md)Aktualisierung:

-   Das Update kann die Funktionskomponenten Struktur vergrößern oder verkleinern, aber die vorhandene Hierarchie von Features und Komponenten, die in den Tabellen [Feature](feature-table.md) und [FeatureComponents](featurecomponents-table.md) beschrieben werden, darf nicht neu organisiert werden. Der vorhandenen Funktionskomponenten Struktur kann ein neues Feature hinzugefügt werden. Wenn eine übergeordnete Funktion entfernt wird, müssen auch alle untergeordneten Funktionen der entfernten Funktion entfernt werden.
-   Mit dem Update kann eine neue Komponente zu einem neuen oder vorhandenen Feature hinzugefügt werden.
-   Das Update darf den Komponenten Code einer beliebigen Komponente nicht ändern. Folglich muss bei einem kleinen Update oder einem geringfügigen Upgrade nie der Name der Schlüsseldatei einer Komponente geändert werden, da dies eine Änderung des Komponenten Codes erfordern würde.
-   Der Name der MSI-Datei des Installationspakets darf nicht durch das Update geändert werden. Stattdessen sollte der Paketcode geändert werden, da er das Paket ändert. Beachten Sie, dass das Update die Tabellen, benutzerdefinierten Aktionen und Dialogfelder in der MSI-Datei ändern kann, ohne den Dateinamen zu ändern.
-   Mit dem Update können Dateien, Registrierungsschlüssel oder Verknüpfungen von Komponenten, die nicht von zwei oder mehr Features gemeinsam genutzt werden, hinzugefügt, entfernt oder geändert werden. Wenn das Update eine Datei mit Versions Angabe ändert, muss die Version der Datei in der [Dateitabelle](file-table.md)inkrementiert werden. Wenn beim Update Ressourcen entfernt werden, sollten auch die Tabellen [RemoveFile](removefile-table.md) und [removeregistry](removeregistry-table.md) aktualisiert werden, um nicht verwendete Dateien, Registrierungsschlüssel oder Verknüpfungen zu entfernen, die bereits installiert wurden.
-   Das Update einer Komponente, die von zwei oder mehr Features gemeinsam genutzt wird, muss abwärts kompatibel mit allen Anwendungen und Features sein, die die Komponente verwenden. Das Update kann die Ressource einer freigegebenen Komponente (z. b. Dateien, Registrierungseinträge und Verknüpfungen) ändern, solange die Änderungen abwärts kompatibel sind. Es wird nicht empfohlen, Dateien, Registrierungseinträge oder Verknüpfungen aus einer freigegebenen Komponente hinzuzufügen oder zu entfernen.
-   Ein kleines Update wird als Windows Installer [Patchpaket](patch-packages.md)ausgeliefert. (Eine vollständige Produkt-CD-ROM wird in der Regel nicht mit einem kleinen Update bereitgestellt.)

Der Produktcode muss geändert werden, wenn für das Update Folgendes zutrifft:

-   Vorhandene Installationen von ursprünglichen und aktualisierten Produkten auf demselben System müssen möglich sein.
-   Der Name der MSI-Datei wurde geändert.
-   Der Komponenten Code einer vorhandenen Komponente hat sich geändert.
-   Eine Komponente wird aus einer vorhandenen Funktion entfernt.
-   Eine vorhandene Funktion wurde in einem untergeordneten Element eines vorhandenen Features erstellt.
-   Eine vorhandene untergeordnete Funktion wurde aus der übergeordneten Funktion entfernt.

Beachten Sie, dass das Ändern des Produktcodes nicht erforderlich ist, wenn Sie ein neues untergeordnetes Feature hinzufügen, das ausschließlich aus neuen Komponenten besteht.

Neue untergeordnete Funktionen können erstellt werden, indem "msidbfeatureattributesfollowparent" und "msidbfeatureattributesuidisallowmissing" in das Feld "Attribute" der [Funktions Tabelle](feature-table.md)eingeschlossen werden. Wenn beim geringfügigen Upgrade nur neue untergeordnete Funktionen hinzugefügt werden, ist REINSTALL = ALL ausreichend, um die Installation der neuen untergeordneten Funktionen zu erzwingen. Weitere Informationen finden Sie unter [Steuern von Funktionsauswahl Zuständen](controlling-feature-selection-states.md).

Ein neues untergeordnetes Feature ist möglicherweise für den Benutzer ausgeblendet. Um den Installationsstatus einer neuen untergeordneten Funktion mit ihrem übergeordneten Feature zu synchronisieren, legen Sie die Bits "msidbfeatureattributesfollowparent" und "msidbfeatureattributesuidisallowmissing" für die untergeordnete Funktion fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Eigenschaften](about-properties.md)
</dt> <dt>

[Verwenden von Eigenschaften](using-properties.md)
</dt> <dt>

[Eigenschafts Verweis](property-reference.md)
</dt> </dl>

 

 



