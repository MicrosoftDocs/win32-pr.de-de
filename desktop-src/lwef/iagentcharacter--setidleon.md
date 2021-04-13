---
title: Iagentcharacter-/tidleon
description: Iagentcharacter-/tidleon
ms.assetid: 397d223a-0970-4535-ad46-2923df6b9975
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98db30c9c440ed0564b98977d33e15e390cf57d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388805"
---
# <a name="iagentcharactersetidleon"></a>Iagentcharacter::/tidleon

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT SetIdleOn(
   long bOn  // idle processing flag
);
```

Legt die automatische Leerlauf Verarbeitung für ein Zeichen fest.

-   Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.

<dl> <dt>

<span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Böller*
</dt> <dd>

Flag für Leerlauf Verarbeitung. Wenn dieser Parameter **true** ist, spielt der Microsoft-Agent automatisch **idck** State-Animationen.

</dd> </dl>

Der Server legt automatisch einen Timeout Wert fest, nachdem die letzte Animation für ein Zeichen wiedergegeben wurde. Wenn das Intervall des Zeit Gebers abgelaufen ist, beginnt der Server mit den **idck** Zuständen für ein Zeichen, wobei die zugehörigen **idlinger** -Animationen in regelmäßigen Abständen abgespielt werden. Wenn Sie die **idlinger** -Zustands Animationen selbst verwalten möchten, legen Sie die-Eigenschaft auf " **false**" fest. Diese Eigenschaft gilt nur für die Verwendung des Zeichens durch die Client Anwendung. Diese Einstellung wirkt sich nicht auf andere Clients des Zeichens oder andere Zeichen ihrer Client Anwendung aus.

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter:: getidleon**](iagentcharacter--getidleon.md)


 

 




