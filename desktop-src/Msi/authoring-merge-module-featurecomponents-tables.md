---
description: In jedem Mergemodul ist eine leere FeatureComponents-Tabelle erforderlich. Diese leere Tabelle stellt ein Schema für das Mergetool zur Verfügung, wenn .msi Zieldatei nicht über eine eigene FeatureComponents-Tabelle verfügt.
ms.assetid: 19463fc7-8362-4943-8907-22c38f66fe25
title: Erstellen von MergemodulfeaturesKomponententabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52b2da3e25d84f4f10edad6566edeba5a10d43c5617340d40c733aa23d31f4b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650299"
---
# <a name="authoring-merge-module-featurecomponents-tables"></a>Erstellen von MergemodulfeaturesKomponententabellen

In jedem Mergemodul ist eine leere [FeatureComponents-Tabelle](featurecomponents-table.md) erforderlich. Diese leere Tabelle stellt ein Schema für das Mergetool zur Verfügung, wenn .msi Zieldatei nicht über eine eigene FeatureComponents-Tabelle verfügt.

Wenn keine FeatureComponents-Tabelle in der Zieldatei vorhanden .msi verwendet das Mergetool die im Modul bereitgestellte leere Tabelle. In diesem Fall erstellt das Mergetool eine doppelte Tabelle in der Ziel-.msi-Datei und fügt Zeilen hinzu, die die neuen Komponenten im Mergemodul den Funktionen im Installationspaket der Anwendung zuordnen.

 

 



