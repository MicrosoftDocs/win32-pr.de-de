---
description: Mit der registermimeinfo-Aktion werden MIME-bezogene Registrierungsinformationen beim System registriert.
ms.assetid: 2ba88b5f-bd8a-4572-af82-9c0b91b9b6d9
title: Registermimeinfo-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41130d9e595cc2d95557470f79c217f3c3235d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756468"
---
# <a name="registermimeinfo-action"></a>Registermimeinfo-Aktion

Mit der registermimeinfo-Aktion werden MIME-bezogene Registrierungsinformationen beim System registriert.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die registermimeinfo-Aktion muss nach der [InstallFiles](installfiles-action.md) -Aktion, der [unregistermimeinfo](unregistermimeinfo-action.md) -Aktion, der [RegisterClassInfo](registerclassinfo-action.md) -Aktion und der [RegisterExtensionInfo](registerextensioninfo-action.md) -Aktion erfolgen.

Die Sequenzierung der Aktionen in der folgenden Gruppe ist eingeschränkt. Wenn eine Teilmenge dieser Aktionen in einer Sequenz Tabelle enthalten ist, müssen Sie dieselbe relative Reihenfolge Reihenfolge aufweisen wie in der folgenden Abbildung:

-   [Unregisterclassinfo](unregisterclassinfo-action.md)
-   [Unregisterextensioninfo](unregisterextensioninfo-action.md)
-   [Unregisterprogidinfo](unregisterprogidinfo-action.md)
-   [Unregistermimeinfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [Registerprogidinfo](registerprogidinfo-action.md)
-   Registermimeinfo

So muss z. b. registermimeinfo in der Sequenz Tabelle auf [unregistermimeinfo](unregistermimeinfo-action.md) folgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                   |
|-------|----------------------------------------------|
| \[1\] | Der Bezeichner des registrierten MIME-Inhaltstyps.  |
| \[2\] | Erweiterung, die dem MIME-Inhaltstyp zugeordnet ist. |



 

## <a name="remarks"></a>Bemerkungen

Mit der registermimeinfo-Aktion werden alle MIME-Informationen für Server aus der [MIME-Tabelle](mime-table.md) , für die der zugehörige Klassen Server oder Erweiterungs Server zur Installation ausgewählt wurde, registriert.

 

 



