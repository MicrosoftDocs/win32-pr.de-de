---
description: Die RegisterMIMEInfo-Aktion registriert MIME-bezogene Registrierungsinformationen beim System.
ms.assetid: 2ba88b5f-bd8a-4572-af82-9c0b91b9b6d9
title: RegisterMIMEInfo-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369f35eab4e6d4228167bfbeda48cf21249ea6a63297f5a9e893b84dcc4ed5bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041740"
---
# <a name="registermimeinfo-action"></a>RegisterMIMEInfo-Aktion

Die RegisterMIMEInfo-Aktion registriert MIME-bezogene Registrierungsinformationen beim System.

## <a name="sequence-restrictions"></a>Sequenzeinschränkungen

Die RegisterMIMEInfo-Aktion muss nach der [InstallFiles-Aktion,](installfiles-action.md) der [UnregisterMIMEInfo-Aktion,](unregistermimeinfo-action.md) der [RegisterClassInfo-Aktion](registerclassinfo-action.md) und der [RegisterExtensionInfo-Aktion](registerextensioninfo-action.md) durchgeführt werden.

Die Sequenzierung der Aktionen in der folgenden Gruppe ist eingeschränkt. Wenn eine Teilmenge dieser Aktionen zusammen in einer Sequenztabelle auftritt, müssen sie dieselbe relative Sequenzreihenfolge wie gezeigt haben:

-   [UnregisterClassInfo](unregisterclassinfo-action.md)
-   [UnregisterExtensionInfo](unregisterextensioninfo-action.md)
-   [UnregisterProgIdInfo](unregisterprogidinfo-action.md)
-   [UnregisterMIMEInfo](unregistermimeinfo-action.md)
-   [RegisterClassInfo](registerclassinfo-action.md)
-   [RegisterExtensionInfo](registerextensioninfo-action.md)
-   [RegisterProgIdInfo](registerprogidinfo-action.md)
-   RegisterMIMEInfo

Beispielsweise muss RegisterMIMEInfo nach [UnregisterMIMEInfo](unregistermimeinfo-action.md) in der Sequenztabelle kommen.

## <a name="actiondata-messages"></a>ActionData-Meldungen



| Feld | Beschreibung der Aktionsdaten                   |
|-------|----------------------------------------------|
| \[1\] | Bezeichner des registrierten MIME-Inhaltstyps.  |
| \[2\] | Erweiterung, die dem MIME-Inhaltstyp zugeordnet ist. |



 

## <a name="remarks"></a>Hinweise

Die Aktion RegisterMIMEInfo registriert alle MIME-Informationen für Server aus der [MIME-Tabelle,](mime-table.md) für die der entsprechende Klassenserver oder Erweiterungsserver für die Installation ausgewählt wurde.

 

 



