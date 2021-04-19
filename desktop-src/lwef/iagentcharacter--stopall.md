---
title: Iagentcharacter stopAll
description: Iagentcharacter stopAll
ms.assetid: cb0ce220-7b35-45c0-b587-30939d26740f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbe745f0611d184fefd729c04e50635bc4006e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342290"
---
# <a name="iagentcharacterstopall"></a>Iagentcharacter:: stopAll

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

``` syntax
HRESULT StopAll();
   long lType,  // request type
```

Beendet alle Animationen (Anforderungen) und entfernt Sie aus der Animations Warteschlange des Zeichens.

<dl> <dt>

<span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*ltype*
</dt> <dd>

Ein Bitfeld, das die Typen von Anforderungen angibt, die beendet (und aus der Warteschlange des Zeichens entfernt) werden sollen, bestehend aus folgendem:



|                                                                                   |                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| konstanter **Ganzzahl ohne Vorzeichen long** - **\_ stopptyp \_ alle = 0xFFFFFFFF;**<br/>              | Beendet alle Animations Anforderungen, einschließlich der nicht in die Warteschlange eingereihten [**Vorbereitungs**](iagentcharacter--prepare.md) Anforderungen. |
| **Ganzzahl ohne Vorzeichen long** - **\_ stopptyp \_ Play = 0x00000001;**<br/>             | Beendet alle Wiedergabe Anforderungen.                                                                                 |
| **Ganzzahl ohne Vorzeichen long** - **\_ stopptyp \_ Move = 0x00000002;**<br/>             | Beendet alle [](https://www.bing.com/search?q=**Move**) Verschiebungs Anforderungen.                                               |
| konstanter **Ganzzahl ohne Vorzeichen long** - **\_ stopptyp \_ sprechen = 0x00000004;**<br/>            | Beendet alle [**sprach**](iagentcharacter--speak.md) Anforderungen.                                              |
| konstanter **Ganzzahl ohne Vorzeichen long** - **\_ stopptyp \_ Prepare = 0x00000008;**<br/>          | Beendet alle [**Vorbereitungs**](iagentcharacter--prepare.md) Anforderungen in der Warteschlange.                                   |
| konstanter **Ganzzahl ohne Vorzeichen long** - **\_ stopptyp \_ nonqueuedprepare = 0x00000010;**<br/> | Beendet alle [**Vorbereitungs**](iagentcharacter--prepare.md) Anforderungen, die nicht in der Warteschlange stehen.                               |
| konstanter **Ganzzahl ohne Vorzeichen long** - **\_ stopptyp ist \_ sichtbar = 0x00000020;**<br/>          | Beendet alle Anforderungen zum [**Ausblenden**](iagentcharacter--hide.md) oder [**anzeigen**](iagentcharacter--show.md) .       |



 

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**Iagentcharacter:: Beendigung**](iagentcharacter--stop.md)


 

 





