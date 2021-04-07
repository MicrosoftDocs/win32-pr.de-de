---
title: Mittel l-Bindungs Handles
description: Bindungs Handles sind Datenobjekte, die die Bindung zwischen Client und Server darstellen.
ms.assetid: 178f4838-3deb-43d4-804f-ad6404b377bd
keywords:
- Datentypen-Mittel l, Bindungs Handles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e59faea2137cb037cab1e5969e53fff2c146ad31
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038822"
---
# <a name="midl-binding-handles"></a>Mittel l-Bindungs Handles

Bindungs Handles sind Datenobjekte, die die Bindung zwischen Client und Server darstellen.

"Mittel l" unterstützt das Basistyp [**handle \_ t**](handle-t.md). Handles dieses Typs werden als "primitive Handles" bezeichnet.

Mit dem **\[ handle \]** -Attribut können Sie eigene handle-Typen definieren. Auf diese Weise definierte Handles werden als "benutzerdefinierte" oder "angepasste" oder "generische" Handles bezeichnet.

Sie können auch ein Handle definieren, das Zustandsinformationen mithilfe des **\[** [**Kontext \_ handle**](context-handle.md) - **\]** Attributs verwaltet. Auf diese Weise definierte Handles werden als "Kontext"-Handles bezeichnet.

Wenn keine Zustandsinformationen erforderlich sind und Sie nicht auswählen, die RPC-Laufzeitbibliotheken zum Verwalten des Handles aufzurufen, können Sie anfordern, dass die Laufzeitbibliotheken eine automatische Bindung bereitstellen. Dies erfolgt mithilfe des automatischen ACF-Schlüssel Worts **\[** [**\_**](auto-handle.md) **\]** .

Sie können eine globale Variable als Bindungs Handle angeben, indem Sie das implizite ACF-Schlüsselwort **\[** [**\_ handle**](implicit-handle.md)verwenden **\]** . Mit dem **\[ expliziten \_ handle \]** -Schlüsselwort wird festgelegt, dass jede Remote Funktion über ein explizit angegebenes Handle verfügt.

Weitere Informationen finden Sie unter [Bindung und Handles](/windows/desktop/Rpc/binding-and-handles).

 

 