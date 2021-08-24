---
description: Mit der Aktion UnregisterMIMEInfo wird die Registrierung von MIME-bezogenen Registrierungsinformationen beim System aufgehoben. Mit der Aktion wird die Registrierung von MIME-Informationen für Server aus der MIME-Tabelle aufgehoben, für die das entsprechende Feature derzeit für die Deinstallation ausgewählt ist.
ms.assetid: 9a5c12da-e78f-4c99-9b82-d41624593c61
title: UnregisterMIMEInfo-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e03ea1c50aa543615edc0ed875bd83b3338cdb261d09e01232e0fe76f7aa51ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810140"
---
# <a name="unregistermimeinfo-action"></a>UnregisterMIMEInfo-Aktion

Mit der Aktion UnregisterMIMEInfo wird die Registrierung von MIME-bezogenen Registrierungsinformationen beim System aufgehoben. Mit der Aktion wird die Registrierung von MIME-Informationen für Server aus der [MIME-Tabelle](mime-table.md) aufgehoben, für die das entsprechende Feature derzeit für die Deinstallation ausgewählt ist.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die Aktion UnregisterMIMEInfo muss nach der Aktion [InstallInitialize,](installinitialize-action.md) der Aktion [UnregisterClassInfo,](unregisterclassinfo-action.md) der Aktion [UnregisterExtensionInfo](unregisterextensioninfo-action.md) und vor der Aktion [RegisterMIMEInfo](registermimeinfo-action.md) erfolgen.

[RemoveRegistryValues](removeregistryvalues-action.md) muss in der Sequenz vor UnregisterMIMEInfo vorliegen.

Die Sequenzierung der Aktionen in der folgenden Gruppe ist eingeschränkt. Wenn eine Teilmenge dieser Aktionen zusammen in einer Sequenztabelle auftritt, müssen sie die gleiche relative Sequenzreihenfolge aufweisen wie gezeigt:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   UnregisterMIMEInfo
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

UnregisterMIMEInfo muss beispielsweise vor [RegisterExtensionInfo](registerextensioninfo-action.md) in der Sequenztabelle enthalten sein.

## <a name="actiondata-messages"></a>ActionData-Nachrichten



| Feld | Beschreibung der Aktionsdaten                    |
|-------|-----------------------------------------------|
| \[1\] | Bezeichner des nicht registrierten MIME-Inhaltstyps. |
| \[2\] | Erweiterung, die dem MIME-Inhaltstyp zugeordnet ist.  |



 

 

 



