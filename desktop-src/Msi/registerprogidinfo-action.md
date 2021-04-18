---
description: Mit der registerprogidinfo-Aktion wird die Registrierung von OLE-ProgID-Informationen beim System verwaltet.
ms.assetid: f6fd4d0d-d2dc-4953-9402-314c7932746b
title: Registerprogidinfo-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c7d53ca4c4125c6ebfc4d089c1c5a0934f9a58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347566"
---
# <a name="registerprogidinfo-action"></a>Registerprogidinfo-Aktion

Mit der registerprogidinfo-Aktion wird die Registrierung von OLE-ProgID-Informationen beim System verwaltet.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die registerprogidinfo-Aktion muss nach der Aktion [InstallFiles](installfiles-action.md) , [unregisterprogidinfo](unregisterprogidinfo-action.md) Action, [RegisterClassInfo](registerclassinfo-action.md) und der [RegisterExtensionInfo](registerextensioninfo-action.md) -Aktion erfolgen.

Die Sequenzierung der Aktionen in der folgenden Gruppe ist eingeschränkt. Wenn eine Teilmenge dieser Aktionen in einer Sequenz Tabelle enthalten ist, müssen Sie dieselbe relative Reihenfolge Reihenfolge aufweisen wie in der folgenden Abbildung:

-   [Unregisterclassinfo](unregisterclassinfo-action.md)
-   [Unregisterextensioninfo](unregisterextensioninfo-action.md)
-   [Unregisterprogidinfo](unregisterprogidinfo-action.md)
-   [Unregistermimeinfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   Registerprogidinfo
-   [Registermimeinfo](registermimeinfo-action.md)

Registerprogidinfo muss z. b. nach [RegisterExtensionInfo](registerextensioninfo-action.md) in der Sequenz Tabelle stehen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                |
|-------|-------------------------------------------|
| \[1\] | Programm Bezeichner des registrierten Programms. |



 

## <a name="remarks"></a>Bemerkungen

Die registerprogidinfo-Aktion registriert alle ProgID-Informationen für Server, die in der [ProgID-Tabelle](progid-table.md) angegeben sind und für die der zugehörige Klassen Server oder Erweiterungs Server für die Installation ausgewählt wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Klassen Tabelle](class-table.md)
</dt> <dt>

[Erweiterungs Tabelle](extension-table.md)
</dt> </dl>

 

 



