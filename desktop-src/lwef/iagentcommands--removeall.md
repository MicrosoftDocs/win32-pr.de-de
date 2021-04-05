---
title: Iagentcommands RemoveAll
description: Iagentcommands RemoveAll
ms.assetid: fab43363-6325-4566-b7bb-599591f67321
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8bd374b7c5767c416d2c3bb2281e651ba71acd8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727040"
---
# <a name="iagentcommandsremoveall"></a>Iagentcommands:: RemoveAll

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT Remove();
```

Entfernt alle [**Befehle**](/windows/desktop/lwef/the-command-object) aus einer [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

Wenn Sie alle [**Befehle**](/windows/desktop/lwef/the-command-object) aus einer [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung entfernen, werden diese auch aus dem Popupmenü und dem **Fenster "Sprachbefehle** " entfernt, wenn die Anwendung aktiv ist. **RemoveAll** entfernt keine Server-oder andere Client Einträge.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcommands:: Add**](iagentcommands--add.md), [**iagentcommands:: Insert**](iagentcommands--insert.md), [**iagentcommands:: Remove**](iagentcommands--remove.md)


 

 