---
description: Die Aktion UnregisterProgIdInfo verwaltet die Aufhebung der Registrierung von OLE ProgId-Informationen mit dem System.
ms.assetid: c9837845-4ffc-4496-8330-11b46d27ec7a
title: UnregisterProgIdInfo-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6666e5648cba220dbb9bbc6e2d50c3959c1d73c98f97dcfd8c45cb3de8d94c82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786960"
---
# <a name="unregisterprogidinfo-action"></a>UnregisterProgIdInfo-Aktion

Die Aktion UnregisterProgIdInfo verwaltet die Aufhebung der Registrierung von OLE ProgId-Informationen mit dem System.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die Aktion UnregisterProgIdInfo muss nach der Aktion [InstallInitialize,](installinitialize-action.md) der Aktion [UnregisterClassInfo,](unregisterclassinfo-action.md) der Aktion [UnregisterExtensioninfo](unregisterextensioninfo-action.md) und vor der Aktion [RegisterProgIdInfo](registerprogidinfo-action.md) erfolgen.

[RemoveRegistryValues](removeregistryvalues-action.md) muss in der Sequenz vor UnregisterProgIdInfo vorliegen.

Die Sequenzierung der Aktionen in der folgenden Gruppe ist eingeschränkt. Wenn eine Teilmenge dieser Aktionen zusammen in einer Sequenztabelle auftritt, müssen sie die gleiche relative Sequenzreihenfolge aufweisen wie gezeigt:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensioninfo](unregisterextensioninfo-action.md)
-   UnregisterProgIdInfo
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

UnregisterProgIdInfo muss beispielsweise vor [UnregisterMIMEInfo](unregistermimeinfo-action.md) in der Sequenztabelle enthalten sein.

## <a name="actiondata-messages"></a>ActionData-Nachrichten



| Feld | Beschreibung der Aktionsdaten                |
|-------|-------------------------------------------|
| \[1\] | Programmbezeichner des registrierten Programms. |



 

## <a name="remarks"></a>Hinweise

Die Aktion UnregisterProgIdInfo entfernt ProgId-Informationen aus der Registrierung ([ProgId-Tabelle](progid-table.md)) für Features, die mit den Erweiterungsinformationen ([Erweiterungstabelle](extension-table.md)) oder den Klasseninformationen ([Klassentabelle](class-table.md)) verbunden sind und derzeit für die Deinstallation ausgewählt sind.

 

 



