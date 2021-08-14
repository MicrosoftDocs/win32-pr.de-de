---
description: Sie können steuern, welche Featureinstallationsoptionen für Benutzer und Anwendungen zur Auswahl verfügbar sind, indem Sie die Tabelle Feature und Die Komponente erstellen.
ms.assetid: 3ce441e0-e709-415c-af64-b1ded7b04f6b
title: Steuern von Funktionsauswahlzuständen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd269e5b7b0c810df6f7f0909d56b98cdd1c54c9b51eacc40656fe48fc32f8e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379905"
---
# <a name="controlling-feature-selection-states"></a>Steuern von Funktionsauswahlzuständen

Sie können steuern, welche Featureinstallationsoptionen für Benutzer und Anwendungen ausgewählt werden können, indem Sie die [Featuretabelle](feature-table.md) und [die Komponententabelle](component-table.md)erstellen.

-   Um die Auswahl des Ankündigungszustands für ein Feature zu verhindern, schließen Sie **msidbFeatureAttributesDisallowAdvertise** in das Feld Attribute des Features in die [Featuretabelle](feature-table.md)ein.
-   Fügen Sie **msidbComponentAttributesLocalOnly** in die Attribute-Felder in der [Tabelle Komponente](component-table.md) für jede Komponente ein, die zum Feature gehört, um die Auswahl der Ausführungszustände aus der Quelle oder aus dem Netzwerk für ein Feature zu verhindern. Wenn ein Feature über keine Komponenten verfügt, stehen für das Feature immer die Optionen run-from-source und run-from-my-computer zur Verfügung.
-   Um die Auswahl des Ausführungszustands von "mein Computer" für ein Feature zu verhindern, schließen Sie **msidbComponentAttributesSourceOnly** für jede Komponente, die zum Feature gehört, in die Attribute-Felder der [Tabelle Komponente](component-table.md) ein. Wenn ein Feature über keine Komponenten verfügt, stehen für das Feature immer die Optionen run-from-source und run-from-my-computer zur Verfügung.
-   Neue untergeordnete Features können erstellt werden, indem **msidbFeatureAttributesFollowParent** und **msidbFeatureAttributesUIDisallowAbsent** in das Feld Attribute der [Featuretabelle](feature-table.md)eingeschlossen werden.

 

 



