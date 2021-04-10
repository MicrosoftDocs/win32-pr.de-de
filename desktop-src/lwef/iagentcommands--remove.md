---
title: Iagentcommands entfernen
description: Iagentcommands entfernen
ms.assetid: 1f41aa2d-e50b-48a8-87fc-fda4730b035a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0c3321de3d06b5e2ebea873a4bace91482d8c5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104208947"
---
# <a name="iagentcommandsremove"></a>Iagentcommands:: Remove

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT Remove(
   long dwID  // Command ID
);
```

Entfernt den angegebenen [**Befehl**](/windows/desktop/lwef/the-command-object) aus einer [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="dwID"></span><span id="dwid"></span><span id="DWID"></span>*dwID*
</dt> <dd>

Die ID eines [**Befehls**](/windows/desktop/lwef/the-command-object) , der aus der [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung entfernt werden soll.

</dd> </dl>

Wenn Sie einen [**Befehl**](/windows/desktop/lwef/the-command-object) aus [**einer Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung entfernen, wird dieser auch aus dem Popupmenü und dem **Fenster "Sprachbefehle** " entfernt, wenn die Anwendung aktiv ist.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Insert**](iagentcommands--insert.md), [**iagentcommands:: RemoveAll**](iagentcommands--removeall.md)


 

 