---
description: Die Aktion RegisterProgIdInfo verwaltet die Registrierung von OLE ProgId-Informationen beim System.
ms.assetid: f6fd4d0d-d2dc-4953-9402-314c7932746b
title: RegisterProgIdInfo-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84cebf5ddb3bf8b9c98ebea0364b685016d343afa283b937400360f31bbcebd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912830"
---
# <a name="registerprogidinfo-action"></a>RegisterProgIdInfo-Aktion

Die Aktion RegisterProgIdInfo verwaltet die Registrierung von OLE ProgId-Informationen beim System.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die RegisterProgIdInfo-Aktion muss nach der [InstallFiles-Aktion,](installfiles-action.md) der [UnregisterProgIdInfo-Aktion,](unregisterprogidinfo-action.md) der [RegisterClassInfo-Aktion](registerclassinfo-action.md) und der [RegisterExtensionInfo-Aktion](registerextensioninfo-action.md) angezeigt werden.

Die Sequenzierung der Aktionen in der folgenden Gruppe ist eingeschränkt. Wenn eine Teilmenge dieser Aktionen zusammen in einer Sequenztabelle auftritt, müssen sie dieselbe relative Sequenzreihenfolge wie gezeigt haben:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   RegisterProgIdInfo
-   [RegisterMIMEInfo](registermimeinfo-action.md)

RegisterProgIdInfo muss z. B. hinter [RegisterExtensionInfo](registerextensioninfo-action.md) in der Sequenztabelle liegen.

## <a name="actiondata-messages"></a>ActionData-Meldungen



| Feld | Beschreibung der Aktionsdaten                |
|-------|-------------------------------------------|
| \[1\] | Programmbezeichner des registrierten Programms. |



 

## <a name="remarks"></a>Hinweise

Die Aktion RegisterProgIdInfo registriert alle ProgId-Informationen für Server, die in der [ProgId-Tabelle](progid-table.md) angegeben sind und für die der entsprechende Klassenserver oder Erweiterungsserver für die Installation ausgewählt wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Klassentabelle](class-table.md)
</dt> <dt>

[Erweiterungstabelle](extension-table.md)
</dt> </dl>

 

 



