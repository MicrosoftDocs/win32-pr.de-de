---
description: Jede Windows Installer Funktion verwendet eine oder mehrere Windows Installer Komponenten, und Features können Komponenten gemeinsam verwenden.
ms.assetid: 7ab4b359-e729-4ca5-8ef3-fa8e988be6da
title: Angeben von Feature-Component Beziehungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a05ff15f4c735ac7d081c16f49f1aafe555a96db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372862"
---
# <a name="specifying-feature-component-relationships"></a>Angeben von Feature-Component Beziehungen

Jede [Windows Installer Funktion](windows-installer-features.md) verwendet eine oder mehrere [Windows Installer Komponenten](windows-installer-components.md), und Features können Komponenten gemeinsam verwenden. Die [FeatureComponents-Tabelle](featurecomponents-table.md) definiert die Beziehung zwischen Features und Komponenten. Weitere Informationen finden Sie in der Übersicht über die [Kern Tabellen](core-tables-group.md) und [Komponenten und Features](components-and-features.md) in der Windows Installer Übersicht. In diesem Abschnitt fügen Sie der Tabelle "FeatureComponents" des Notepad-Beispiels Informationen hinzu.

Öffnen Sie MNP2000.msi mit dem Datenbank-Editor, und geben Sie die folgenden Daten in die leere FeatureComponents-Tabelle ein.

[FeatureComponents-Tabelle](featurecomponents-table.md)



| Funktion\_ | Komponente\_ |
|-----------|-------------|
| Ball  | Ball    |
| Konzert   | Konzert     |
| Abhängigkeit     | Abhängigkeit       |
| Verbandes  | Verbandes    |
| Hilfe      | Hilfe        |
| January   | January     |
| Newyears  | Newyears    |
| Editor   | Editor     |
| Infodatei    | Editor     |



 

[Fortsetzen](adding-registry-information.md)

 

 



