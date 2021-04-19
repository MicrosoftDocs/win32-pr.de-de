---
description: Mit der unregisterextensioninfo-Aktion wird das Entfernen von Erweiterungs bezogenen Informationen aus der Systemregistrierung verwaltet.
ms.assetid: 62bb9d17-c221-4bd2-bd7f-9930e28bb946
title: Unregisterextensioninfo-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85d069a686c5f0e517a0cc9556634895216dd8cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352791"
---
# <a name="unregisterextensioninfo-action"></a>Unregisterextensioninfo-Aktion

Mit der unregisterextensioninfo-Aktion wird das Entfernen von Erweiterungs bezogenen Informationen aus der Systemregistrierung verwaltet.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die unregisterextensioninfo-Aktion muss nach der [InstallInitialize](installinitialize-action.md) -Aktion und vor der [RegisterExtensionInfo](registerextensioninfo-action.md) -Aktion erfolgen.

[Removeregistryvalues](removeregistryvalues-action.md) muss in der Sequenz vor ' unregisterextensioninfo ' stehen.

Die Sequenzierung der Aktionen in der folgenden Gruppe ist eingeschränkt. Wenn eine Teilmenge dieser Aktionen in einer Sequenz Tabelle enthalten ist, müssen Sie dieselbe relative Reihenfolge Reihenfolge aufweisen wie in der folgenden Abbildung:

-   [Unregisterclassinfo](unregisterclassinfo-action.md)
-   Unregisterextensioninfo
-   [Unregisterprogidinfo](unregisterprogidinfo-action.md)
-   [Unregistermimeinfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [Registerprogidinfo](registerprogidinfo-action.md)
-   [Registermimeinfo](registermimeinfo-action.md)

Unregisterextensioninfo muss z. b. vor [unregisterprogidinfo](unregisterprogidinfo-action.md) in der Sequenz Tabelle stehen.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten |
|-------|----------------------------|
| \[1\] | Erweiterung entfernt.         |



 

## <a name="remarks"></a>Bemerkungen

Wenn das System die Bedarfs gesteuerte Installation von Erweiterungs Servern nicht unterstützt, entfernt unregisterextensioninfo alle Erweiterungs Server in der [Erweiterungs Tabelle](extension-table.md) , die entweder einer nicht installierten Funktion oder einem von der Registrierung installierten Feature zugeordnet sind. Andernfalls entfernt diese Aktion die Erweiterungs Server, die einer Funktion zugeordnet sind, die aus der Registrierung entfernt werden soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Shelladvtsupport (Eigenschaft)**](shelladvtsupport.md)
</dt> </dl>

 

 



