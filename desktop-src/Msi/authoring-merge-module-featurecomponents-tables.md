---
description: Eine leere FeatureComponents-Tabelle ist in jedem Mergemodul erforderlich. Diese leere Tabelle stellt ein Schema für das Mergetool bereit, wenn die MSI-Datei des Ziels nicht über eine eigene FeatureComponents-Tabelle verfügt.
ms.assetid: 19463fc7-8362-4943-8907-22c38f66fe25
title: Erstellen von FeatureComponents-Tabellen für Mergemodule
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3522f32f91a66df93e9096bf9c528f8d00e11f6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350184"
---
# <a name="authoring-merge-module-featurecomponents-tables"></a>Erstellen von FeatureComponents-Tabellen für Mergemodule

Eine leere [FeatureComponents-Tabelle](featurecomponents-table.md) ist in jedem Mergemodul erforderlich. Diese leere Tabelle stellt ein Schema für das Mergetool bereit, wenn die MSI-Datei des Ziels nicht über eine eigene FeatureComponents-Tabelle verfügt.

Wenn, und nur wenn, in der MSI-Datei des Ziels keine FeatureComponents-Tabelle vorhanden ist, verwendet das Merge-Tool die leere Tabelle, die im Modul enthalten ist. In diesem Fall erstellt das Merge-Tool eine doppelte Tabelle in der MSI-Ziel Datei und fügt Zeilen hinzu, die die neuen Komponenten im Mergemodul den Funktionen im Installationspaket der Anwendung zuordnen.

 

 



