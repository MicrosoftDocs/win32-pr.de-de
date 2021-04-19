---
description: Mit der RegisterExtensionInfo-Aktion wird die Registrierung von Erweiterungs bezogenen Informationen im System verwaltet.
ms.assetid: 3c243ca3-9fa7-41ec-968e-7954d7d45432
title: RegisterExtensionInfo-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0310344b6579ef65faac41238bb607ce98411b52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348597"
---
# <a name="registerextensioninfo-action"></a>RegisterExtensionInfo-Aktion

Mit der RegisterExtensionInfo-Aktion wird die Registrierung von Erweiterungs bezogenen Informationen im System verwaltet.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die Aktion RegisterExtensionInfo muss nach der Aktion [InstallFiles](installfiles-action.md) und der [unregisterextensioninfo](unregisterextensioninfo-action.md) -Aktion erfolgen.

Die Sequenzierung der Aktionen in der folgenden Gruppe ist eingeschränkt. Wenn eine Teilmenge dieser Aktionen in einer Sequenz Tabelle enthalten ist, müssen Sie dieselbe relative Reihenfolge Reihenfolge aufweisen wie in der folgenden Abbildung:

-   [Unregisterclassinfo](unregisterclassinfo-action.md)
-   [Unregisterextensioninfo](unregisterextensioninfo-action.md)
-   [Unregisterprogidinfo](unregisterprogidinfo-action.md)
-   [Unregistermimeinfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   RegisterExtensionInfo
-   [Registerprogidinfo](registerprogidinfo-action.md)
-   [Registermimeinfo](registermimeinfo-action.md)

So muss z. b. RegisterExtensionInfo in der Sequenz Tabelle auf [unregistermimeinfo](unregistermimeinfo-action.md) folgen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten |
|-------|----------------------------|
| \[1\] | Registrierte Erweiterung.      |



 

## <a name="remarks"></a>Bemerkungen

Wenn das System die Installation bei Bedarf für Erweiterungs Server unterstützt, registriert RegisterExtensionInfo alle Erweiterungs Server in der [Erweiterungs Tabelle](extension-table.md) , die den Funktionen zugeordnet ist, die für die Installation oder Ankündigung festgelegt sind. Andernfalls werden durch diese Aktion nur Erweiterungs Server registriert, die den Funktionen von zugewiesen sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Shelladvtsupport (Eigenschaft)**](shelladvtsupport.md)
</dt> </dl>

 

 



