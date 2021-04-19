---
description: Beschreibung, wie ein Fenster durch seine Funktion für den Tablet PC identifiziert wird.
ms.assetid: 513e0c9d-4c9e-4e7c-8314-bd7603489e89
title: Identifizieren eines Fensters anhand seiner Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497f660d6690bd4dc37c252f82f2408da3e3655d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353098"
---
# <a name="identifying-a-window-by-its-function"></a>Identifizieren eines Fensters anhand seiner Funktion

Identifizieren Sie jede Art von Fenster, indem Sie Ihr eine eindeutige Fenster Klasse zuweisen. Vermeiden Sie eine einzelne Fenster Klasse, die für eine Vielzahl von Funktionen verwendet wird.

Barrierefreiheits Hilfen müssen über diese Identifikation verfügen, damit unterschiedliche Fenster in derselben Anwendung behandelt werden können. Möglicherweise gibt es separate Anweisungen für die Handhabung dieser Fenster, z. b. das ankündigen bestimmter Bereiche, wenn sich der Inhalt ändert.

Wenn Sie keine separaten Fenster Klassen verwenden können, können Sie die Unterschiede über Microsoft <entity type="reg"/> Active Accessibility <entity type="reg"/> oder ggf. durch eine private Fenster Meldung, die Sie auf Ihrer Website dokumentieren, verfügbar machen.

Weitere Informationen zum verfügbar machen von Fenster Klassen mithilfe Active Accessibility finden Sie im Abschnitt zur [Barrierefreiheit](/windows/desktop/accessibility) .

 

 
