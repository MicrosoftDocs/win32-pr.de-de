---
description: Die RegisterClassInfo-Aktion verwaltet die Registrierung von COM-Klasseninformationen beim System. Es wird die Tabelle AppId verwendet.
ms.assetid: f8b60a75-9c0e-41c5-b6af-6a05a26b2d71
title: RegisterClassInfo-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a0983b77c517cb2084b21d6d1500ec9b2a54b45d403c43f65bcc29505e2afe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912890"
---
# <a name="registerclassinfo-action"></a>RegisterClassInfo-Aktion

Die RegisterClassInfo-Aktion verwaltet die Registrierung von COM-Klasseninformationen beim System. Es wird die [AppId-Tabelle verwendet.](appid-table.md)

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die RegisterClassInfo-Aktion muss nach der Aktion [InstallFiles](installfiles-action.md) und der Aktion [UnregisterClassInfo](unregisterclassinfo-action.md) erfolgen.

Die Sequenzierung der Aktionen in der folgenden Gruppe ist eingeschränkt. Wenn eine Teilmenge dieser Aktionen zusammen in einer Sequenztabelle auftritt, müssen sie die gleiche relative Sequenzreihenfolge aufweisen wie gezeigt:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   RegisterClassInfo
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   [RegisterMIMEInfo](registermimeinfo-action.md)

RegisterClassInfo muss beispielsweise nach [UnregisterMIMEInfo](unregistermimeinfo-action.md) in der Sequenztabelle angegeben werden.

## <a name="actiondata-messages"></a>ActionData-Nachrichten



| Feld | Beschreibung der Aktionsdaten                          |
|-------|-----------------------------------------------------|
| \[1\] | GUID-Klassenbezeichner des registrierten COM-Servers. |



 

## <a name="remarks"></a>Hinweise

Wenn das System "Install-on-Demand" für OLE-Server unterstützt, registriert RegisterClassInfo alle COM-Klassen in der [Klassentabelle,](class-table.md) die einem Feature zugeordnet sind, das installiert oder angekündigt werden soll. Andernfalls registriert diese Aktion nur die COM-Klassen, die einem für die Installation ausgewählten Feature zugeordnet sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**OLEAdvtSupport-Eigenschaft**](oleadvtsupport.md)
</dt> </dl>

 

 



