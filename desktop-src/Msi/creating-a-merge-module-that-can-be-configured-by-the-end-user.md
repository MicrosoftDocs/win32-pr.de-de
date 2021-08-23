---
description: Verwenden Sie zum Erstellen von Mergemodulen die allgemeinen Richtlinien, die im Thema Erstellen von Mergemodulen beschrieben werden.
ms.assetid: 9d5e60dc-9133-4c6e-9a47-dd341f2757fa
title: Erstellen eines Mergemoduls, das vom End-User
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0d1b4ffebe21659d33640c3872e9e6c7875518654b86d256ea4b858444ef39e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948134"
---
# <a name="creating-a-merge-module-that-can-be-configured-by-the-end-user"></a>Erstellen eines Mergemoduls, das vom End-User

Verwenden Sie zum Erstellen von Mergemodulen die allgemeinen Richtlinien, die im Thema [Erstellen von Mergemodulen](authoring-merge-modules.md) beschrieben werden. Darüber hinaus müssen Sie folgende Schritte ausführen, um ein Mergemodul zu erstellen, das vom Endbenutzer des Moduls konfiguriert werden kann:

-   Endbenutzer benötigen Mergemod.dll Version 2.0, um Ihr Modul zu konfigurieren. Benutzer mit früheren Versionen von Mergemod.dll können das Modul anwenden, erhalten jedoch immer die Standardeinstellungen.
-   Fügen Sie dem Mergemodul eine [ModuleConfiguration-Tabelle](moduleconfiguration-table.md) hinzu, um die Elemente zu identifizieren, die von einem Endbenutzer konfiguriert werden können. Fügen Sie in dieser Tabelle einen Datensatz für jedes konfigurierbare Element hinzu. Diese Elemente werden durch die Vorlagen ersetzt, die in der [Tabelle ModuleSubsdatenbank](modulesubstitution-table.md)angegeben sind. Geben Sie einen Namen für jedes konfigurierbare Element in das Feld Name ein. Geben Sie das Format, den Typ und den semantischen Kontext für jedes Element in den Spalten Format, Typ und ContextData ein. Weitere Informationen finden Sie unter [Semantische Typen.](semantic-types.md) Geben Sie im Feld DefaultValue einen Standardwert für das Element im [CMSM-Sonderformat ein.](cmsm-special-format.md)
-   Fügen Sie dem Mergemodul eine [Tabelle ModuleSubsdatenbank](modulesubstitution-table.md) hinzu. Jeder Datensatz in dieser Tabelle entspricht einer Ersetzung von einem oder mehreren konfigurierbaren Elementen in ein Feld der Mergemoduldatenbank. Geben Sie die Tabelle, Zeile und Spalte des Felds ein, das die Ersetzung empfängt. Geben Sie eine Formatierungsvorlage für die Ersetzung in die Spalte Wert ein, indem Sie das [CMSM-Sonderformat verwenden.](cmsm-special-format.md)
-   Fügen Sie der [Validierungstabelle](-validation-table.md) Datensätze für die Tabellen ModuleSubsconfiguration und ModuleConfiguration hinzu.
-   Fügen Sie der [Tabelle ModuleIgnoreTable](moduleignoretable-table.md) Datensätze für die [Tabelle ModuleSubs routing](modulesubstitution-table.md) und die Tabelle [ModuleConfiguration hinzu.](moduleconfiguration-table.md) Dadurch wird sichergestellt, dass das Modul für Benutzer kompatibel ist, die über Versionen von Mergemod.dll verfügen, die älter als Version 2.0 sind.

 

 



