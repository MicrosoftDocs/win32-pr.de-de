---
description: Der Produktcode ist eine GUID, die die Hauptidentifikation einer Anwendung oder eines Produkts ist. Weitere Informationen finden Sie unter Produktcodes.
ms.assetid: 4de84885-587d-405f-ba85-d62e09e8ba92
title: Ändern des Produktcodes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4567cbb014fa2f2002f0433a8e42c3a261ccb1af350f9b4e592a3bb5ff8a0216
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119340010"
---
# <a name="changing-the-product-code"></a>Ändern des Produktcodes

Der Produktcode ist eine GUID, die die Hauptidentifikation einer Anwendung oder eines Produkts ist. Weitere Informationen finden Sie unter [Produktcodes.](product-codes.md)

Ein Update, das die folgenden Richtlinien erfüllt, erfordert im Allgemeinen keine Änderung des Produktcodes und kann als [kleines Update](small-updates.md)behandelt werden, oder wenn die Version geändert werden soll, als [kleineres Upgrade:](minor-upgrades.md)

-   Das Update kann die Featurekomponentenstruktur vergrößern oder verkleinern, darf jedoch nicht die vorhandene Hierarchie von Features und Komponenten neu organisieren, die in den Tabellen [Feature](feature-table.md) und [FeatureComponents](featurecomponents-table.md) beschrieben werden. Sie kann der vorhandenen Funktionskomponentenstruktur ein neues Feature hinzufügen. Wenn ein übergeordnetes Feature entfernt wird, müssen auch alle untergeordneten Features der entfernten Funktion entfernt werden.
-   Das Update kann einer neuen oder vorhandenen Funktion eine neue Komponente hinzufügen.
-   Das Update darf den Komponentencode einer Komponente nicht ändern. Folglich darf ein kleines Update oder ein kleineres Upgrade nie den Namen der Schlüsseldatei einer Komponente ändern, da dies eine Änderung des Komponentencodes erfordern würde.
-   Das Update darf den Namen der .msi-Datei des Installationspakets nicht ändern. Stattdessen sollte der Paketcode geändert werden, da es das Paket ändert. Beachten Sie, dass dies bedeutet, dass das Update die Tabellen, benutzerdefinierten Aktionen und Dialoge in der .msi Datei ändern kann, ohne den Namen der Datei zu ändern.
-   Das Update kann Dateien, Registrierungsschlüssel oder Verknüpfungen von Komponenten hinzufügen, entfernen oder ändern, die nicht von zwei oder mehr Features gemeinsam genutzt werden. Wenn das Update eine Datei mit Versionsänderung ändert, muss die Version dieser Datei in der [Dateitabelle](file-table.md)inkrementiert werden. Wenn durch das Update Ressourcen entfernt werden, sollten auch die Tabellen [RemoveFile](removefile-table.md) und [RemoveRegistry](removeregistry-table.md) aktualisiert werden, um nicht verwendete Dateien, Registrierungsschlüssel oder Verknüpfungen zu entfernen, die bereits installiert wurden.
-   Das Update einer Komponente, die von zwei oder mehr Features gemeinsam genutzt wird, muss abwärtskompatibel mit allen Anwendungen und Features sein, die die Komponente verwenden. Das Update kann die Ressource einer freigegebenen Komponente wie Dateien, Registrierungseinträge und Verknüpfungen ändern, solange die Änderungen abwärtskompatibel sind. Es wird nicht empfohlen, dass das Update Dateien, Registrierungseinträge oder Verknüpfungen zu einer freigegebenen Komponente hinzu- oder entfernt.
-   Ein kleines Update wird als Windows [Installer-Patchpaket](patch-packages.md)ausgeliefert. (Ein vollständiges CD-ROM-Produkt wird in der Regel nicht mit einem kleinen Update bereitgestellt.)

Der Produktcode muss geändert werden, wenn einer der folgenden Punkte für das Update zutrifft:

-   Parallele Installationen von originalen und aktualisierten Produkten auf demselben System müssen möglich sein.
-   Der Name der .msi Datei wurde geändert.
-   Der Komponentencode einer vorhandenen Komponente wurde geändert.
-   Eine Komponente wird aus einem vorhandenen Feature entfernt.
-   Ein vorhandenes Feature wurde zu einem untergeordneten Element eines vorhandenen Features gemacht.
-   Ein vorhandenes untergeordnetes Feature wurde aus dem übergeordneten Feature entfernt.

Beachten Sie, dass das Hinzufügen eines neuen untergeordneten Features, das vollständig aus neuen Komponenten besteht, zu einem vorhandenen Feature keine Änderung des Produktcodes erfordert.

Neue untergeordnete Features können erstellt werden, indem msidbFeatureAttributesFollowParent und msidbFeatureAttributesUIDisallowAbsent in das Feld Attribute der [Featuretabelle](feature-table.md)eingeschlossen werden. Wenn das kleinere Upgrade nur neue untergeordnete Features hinzufügt, reicht REINSTALL=ALL aus, um die Installation der neuen untergeordneten Features zu erzwingen. Weitere Informationen finden Sie unter [Steuern von Funktionsauswahlzuständen.](controlling-feature-selection-states.md)

Ein neues untergeordnetes Feature kann für den Benutzer ausgeblendet werden. Um den Installationsstatus eines neuen untergeordneten Features mit dem übergeordneten Feature zu synchronisieren, legen Sie die Bits msidbFeatureAttributesFollowParent und msidbFeatureAttributesUIDisallowAbsent für das untergeordnete Feature fest.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Eigenschaften](about-properties.md)
</dt> <dt>

[Verwenden von Eigenschaften](using-properties.md)
</dt> <dt>

[Eigenschaftenverweis](property-reference.md)
</dt> </dl>

 

 



