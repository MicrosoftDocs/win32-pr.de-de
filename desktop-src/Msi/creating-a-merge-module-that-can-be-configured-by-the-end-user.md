---
description: Verwenden Sie zum Erstellen von Mergemodulen die allgemeinen Richtlinien, die im Thema Erstellen von Mergemodulen beschrieben werden.
ms.assetid: 9d5e60dc-9133-4c6e-9a47-dd341f2757fa
title: Erstellen eines Mergemoduls, das vom End-User konfiguriert werden kann
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2db6ff7bd85fb1b6704fc2452c488b8a3bbc06b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216759"
---
# <a name="creating-a-merge-module-that-can-be-configured-by-the-end-user"></a>Erstellen eines Mergemoduls, das vom End-User konfiguriert werden kann

Verwenden Sie zum Erstellen von Mergemodulen die allgemeinen Richtlinien, die im Thema [Erstellen von Mergemodulen](authoring-merge-modules.md) beschrieben werden. Außerdem müssen Sie Folgendes ausführen, um ein Mergemodul zu erstellen, das vom Endbenutzer des Moduls konfiguriert werden kann:

-   Endbenutzer müssen über Mergemod.dll Version 2,0 verfügen, um das Modul zu konfigurieren. Benutzer mit früheren Versionen von Mergemod.dll können das Modul anwenden, aber Sie erhalten stets die Standardeinstellungen.
-   Fügen Sie dem Mergemodul eine [ModuleConfiguration-Tabelle](moduleconfiguration-table.md) hinzu, um die Elemente zu identifizieren, die von einem Endbenutzer konfiguriert werden können. Fügen Sie für jedes konfigurierbare Element einen Datensatz in dieser Tabelle hinzu. Diese Elemente werden in die Vorlagen ersetzt, die in der [ModuleSubstitution-Tabelle](modulesubstitution-table.md)angegeben sind. Geben Sie einen Namen für jedes konfigurierbare Element in das Feld Name ein. Geben Sie das Format, den Typ und den semantischen Kontext für jedes Element in den Spalten "Format", "Typ" und "ContextData" ein. Weitere Informationen finden Sie unter [semantische Typen](semantic-types.md). Geben Sie im Feld DefaultValue einen Standardwert für das Element ein, das das [spezielle cmsm-Format](cmsm-special-format.md)verwendet.
-   Fügen Sie dem Mergemodul eine [ModuleSubstitution-Tabelle](modulesubstitution-table.md) hinzu. Jeder Datensatz in dieser Tabelle entspricht einer Ersetzung von einem oder mehreren konfigurierbaren Elementen in einem Feld der mergemoduldatenbank. Geben Sie die Tabelle, die Zeile und die Spalte des Felds ein, das die Ersetzung empfängt. Geben Sie eine Formatierungs Vorlage für die Ersetzung in die Spalte Wert ein, indem Sie das [spezielle cmsm-Format](cmsm-special-format.md)verwenden.
-   Fügen Sie der Überprüfungs [Tabelle](-validation-table.md) für die Tabellen "ModuleSubstitution" und "ModuleConfiguration" Datensätze hinzu.
-   Fügen Sie der Tabelle [moduleignoretable](moduleignoretable-table.md) der Tabelle [ModuleSubstitution](modulesubstitution-table.md) und der Tabelle [ModuleConfiguration](moduleconfiguration-table.md)Datensätze hinzu. Dadurch wird sichergestellt, dass das Modul für Benutzer mit Versionen von Mergemod.dll mit früheren Versionen als Version 2,0 kompatibel ist.

 

 



