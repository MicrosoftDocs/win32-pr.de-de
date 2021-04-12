---
title: Iagentnotifysink activateinputstate
description: Iagentnotifysink activateinputstate
ms.assetid: 2476e475-d80c-47e9-bb60-e0fca41becc9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5821f5943bb87f9c19a66125028604fa5d116a7e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207103"
---
# <a name="iagentnotifysinkactivateinputstate"></a>Iagentnotifysink:: activateinputstate

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT ActivateInputState(
   long dwCharID,   // character ID
   long bActivated  // input activation flag
);                          
```

Benachrichtigt eine Client Anwendung, dass sich der aktive Eingabe Zustand eines Zeichens geändert hat.

-   Kein Rückgabewert.

<dl> <dt>

<span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwcharid*
</dt> <dd>

Der Bezeichner des Zeichens, dessen Eingabe Aktivierungszustand geändert wurde.

</dd> <dt>

<span id="bActivated"></span><span id="bactivated"></span><span id="BACTIVATED"></span>*bactivated*
</dt> <dd>

Aktives Eingabe-Flag. Dieser boolesche Wert ist **true** , wenn das Zeichen, auf das von *dwcharid* verwiesen wird, aktiv wurde. und **false** , wenn das Zeichen seinen Eingang in den aktiven Zustand verliert.

</dd> </dl>

 

 




