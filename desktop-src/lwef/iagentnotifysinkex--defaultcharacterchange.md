---
title: Iagentnotifysinkex defaultcharacters-Änderung
description: Iagentnotifysinkex defaultcharacters-Änderung
ms.assetid: 13acb502-e247-433f-abf3-2d78a2d6a4a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ec212887d17d1aa59d942ece79b3e6928900ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339001"
---
# <a name="iagentnotifysinkexdefaultcharacterchange"></a>Iagentnotifysinkex::D efaultcharacters-Änderung

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT DefaultCharacterChange(
   BSTR bszGUID  // character identifier
);
```

Benachrichtigt eine Client Anwendung, wenn sich das Standard Zeichen ändert.

-   Kein Rückgabewert.

<dl> <dt>

<span id="bszGUID"></span><span id="bszguid"></span><span id="BSZGUID"></span>*bszguid*
</dt> <dd>

Der eindeutige Bezeichner für das Zeichen.

</dd> </dl>

Wenn der Benutzer das als Standard Zeichen des Benutzers zugewiesene Zeichen ändert, sendet der Server dieses Ereignis an Clients, die das Standard Zeichen geladen haben. Das Ereignis gibt den eindeutigen Bezeichner (GUID) des Zeichens zurück, der mit geschweiften Klammern und Bindestrichen formatiert ist, die definiert wird, wenn das Zeichen mit dem Microsoft-Agent-Zeichen-Editor erstellt wird

Wenn das neue Zeichen angezeigt wird, wird die gleiche Größe wie jede bereits geladene Instanz des Zeichens oder das vorherige Standard Zeichen (in dieser Reihenfolge) angenommen.

## <a name="see-also"></a>Weitere Informationen

[**Iagent:: Load**](iagent--load.md)


 

 




