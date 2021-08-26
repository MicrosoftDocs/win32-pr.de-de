---
description: Die UnregisterExtensionInfo-Aktion verwaltet das Entfernen von Erweiterungsinformationen aus der Systemregistrierung.
ms.assetid: 62bb9d17-c221-4bd2-bd7f-9930e28bb946
title: UnregisterExtensionInfo-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e8dae707bc4dd517402d8a85fb64402637a815f8249d4677f18818c855ba4e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810230"
---
# <a name="unregisterextensioninfo-action"></a>UnregisterExtensionInfo-Aktion

Die UnregisterExtensionInfo-Aktion verwaltet das Entfernen von Erweiterungsinformationen aus der Systemregistrierung.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die UnregisterExtensionInfo-Aktion muss nach der [InstallInitialize-Aktion](installinitialize-action.md) und vor der [Aktion RegisterExtensionInfo](registerextensioninfo-action.md) angezeigt werden.

[RemoveRegistryValues](removeregistryvalues-action.md) muss vor UnregisterExtensionInfo in der Sequenz kommen.

Die Sequenzierung der Aktionen in der folgenden Gruppe ist eingeschränkt. Wenn eine Teilmenge dieser Aktionen zusammen in einer Sequenztabelle auftritt, müssen sie dieselbe relative Sequenzreihenfolge wie gezeigt haben:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   UnregisterExtensionInfo
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

UnregisterExtensionInfo muss beispielsweise vor [UnregisterProgIdInfo](unregisterprogidinfo-action.md) in der Sequenztabelle liegen.

## <a name="actiondata-messages"></a>ActionData-Meldungen



| Feld | Beschreibung der Aktionsdaten |
|-------|----------------------------|
| \[1\] | Erweiterung entfernt.         |



 

## <a name="remarks"></a>Hinweise

Wenn das System die bedarfsbasierte Installation von Erweiterungsservern nicht unterstützt, entfernt UnregisterExtensionInfo alle Erweiterungsserver in der Erweiterungstabelle, die entweder einem deinstallierten Feature oder einem Feature zugeordnet sind, das wie aus der Registrierung angekündigt installiert wurde. [](extension-table.md) Andernfalls entfernt diese Aktion die Erweiterungsserver, die einem Feature zugeordnet sind, das aus der Registrierung entfernt werden soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ShellAdvtSupport-Eigenschaft**](shelladvtsupport.md)
</dt> </dl>

 

 



