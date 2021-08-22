---
description: Die RegisterExtensionInfo-Aktion verwaltet die Registrierung von Erweiterungsinformationen beim System.
ms.assetid: 3c243ca3-9fa7-41ec-968e-7954d7d45432
title: RegisterExtensionInfo-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0541fc512c2300b0cb37f4a23305a3d312a4e60208890507fb7c6112e00c94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519380"
---
# <a name="registerextensioninfo-action"></a>RegisterExtensionInfo-Aktion

Die RegisterExtensionInfo-Aktion verwaltet die Registrierung von Erweiterungsinformationen beim System.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die RegisterExtensionInfo-Aktion muss nach der [InstallFiles-Aktion](installfiles-action.md) und der [UnregisterExtensionInfo-Aktion](unregisterextensioninfo-action.md) erfolgen.

Die Sequenzierung der Aktionen in der folgenden Gruppe ist eingeschränkt. Wenn eine Teilmenge dieser Aktionen zusammen in einer Sequenztabelle auftritt, müssen sie die gleiche relative Sequenzreihenfolge aufweisen wie gezeigt:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   RegisterExtensionInfo
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

RegisterExtensionInfo muss beispielsweise nach [UnregisterMIMEInfo](unregistermimeinfo-action.md) in der Sequenztabelle enthalten sein.

## <a name="actiondata-messages"></a>ActionData-Nachrichten



| Feld | Beschreibung der Aktionsdaten |
|-------|----------------------------|
| \[1\] | Registrierte Erweiterung.      |



 

## <a name="remarks"></a>Hinweise

Wenn das System installation-on-demand für Erweiterungsserver unterstützt, registriert RegisterExtensionInfo alle Erweiterungsserver in der [Erweiterungstabelle,](extension-table.md) die features zugeordnet sind, die für die Installation oder Ankündigung festgelegt wurden. Andernfalls registriert diese Aktion nur Erweiterungsserver, die features zugeordnet sind, die auf installation festgelegt sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ShellAdvtSupport-Eigenschaft**](shelladvtsupport.md)
</dt> </dl>

 

 



