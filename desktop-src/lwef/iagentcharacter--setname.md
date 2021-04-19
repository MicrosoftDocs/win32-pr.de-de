---
title: Iagentcharacter SetName
description: Iagentcharacter SetName
ms.assetid: 4944f910-60e9-446b-82e9-2794f445789a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec058e338adfa8c998bf26a1223ae71f0c7de3d4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341269"
---
# <a name="iagentcharactersetname"></a>Iagentcharacter:: SetName

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetName(
   BSTR bszName   // character name
);
```

Legt den Namen des Zeichens fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszname*
</dt> <dd>

Ein BSTR, das den Namen des Zeichens festlegt. Der Standardname eines Zeichens wird bei der Kompilierung mit dem Microsoft-Agent-Zeichen-Editor definiert. Sie können es mit **iagentcharacter:: SetName**; ändern. Dadurch wird jedoch der Zeichen Name für alle aktuellen Clients des Zeichens geändert. Diese Eigenschaft ist nicht persistent (wird permanent gespeichert). Der Name des Zeichens wird auf den Standardnamen zurückgesetzt, wenn das Zeichen zuerst von einem Client geladen wird.

Der Name des Zeichens kann auch von seiner Sprach-ID abhängen. Zeichen können mit unterschiedlichen Namen für verschiedene Sprachen kompiliert werden.

Der Server verwendet die namens Einstellung des Zeichens in Teilen der Benutzeroberfläche des Microsoft-Agents, z. b. den Titel des sprach Befehls Fensters, wenn das Zeichen ein Eingabe-aktiv ist, und im Popup Menü der Microsoft-agenttaskleiste.

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter:: GetName**](iagentcharacter--getname.md)


 

 




