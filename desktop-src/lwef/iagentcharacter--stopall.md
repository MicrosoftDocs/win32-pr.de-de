---
title: IAgentCharacter StopAll
description: IAgentCharacter StopAll
ms.assetid: cb0ce220-7b35-45c0-b587-30939d26740f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ff1811e7b7ee323ef57e21dbeea4e6ea9d33dc8bc735327ec9ba5afc2ce299b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609779"
---
# <a name="iagentcharacterstopall"></a>IAgentCharacter::StopAll

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

``` syntax
HRESULT StopAll();
   long lType,  // request type
```

Beendet alle Animationen (Anforderungen) und entfernt sie aus der Animationswarteschlange des Zeichens.

<dl> <dt>

<span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*
</dt> <dd>

Ein Bitfeld, das die Typen der anzuhaltenden (und aus der Warteschlange des Zeichens zu entfernenden) Anforderungen angibt, bestehend aus folgendem Code:



| Wert                                                                                  |  Beschreibung                                                                                                        |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| **const unsigned long** **STOP TYPE ALL = \_ \_ 0xFFFFFFFF;**<br/>              | Beendet alle Animationsanforderungen, einschließlich nicht in die Warteschlange [**gestellter**](iagentcharacter--prepare.md) Vorbereitungsanforderungen. |
| **const unsigned long** **STOP TYPE PLAY = \_ \_ 0x00000001;**<br/>             | Beendet alle Wiedergabeanforderungen.                                                                                 |
| **const unsigned long** **STOP TYPE MOVE = \_ \_ 0x00000002;**<br/>             | Beendet alle [**Move-Anforderungen.**](https://www.bing.com/search?q=**Move**)                                               |
| **const unsigned long** **STOP TYPE SPEAK = \_ \_ 0x00000004;**<br/>            | Beendet alle [**Speak-Anforderungen.**](iagentcharacter--speak.md)                                              |
| **const unsigned long** **STOP TYPE PREPARE = \_ \_ 0x00000008;**<br/>          | Beendet alle in der [**Warteschlange warteschlangenbereiten**](iagentcharacter--prepare.md) Anforderungen.                                   |
| **const unsigned long** **STOP TYPE \_ \_ NONQUEUEDPREPARE = 0x00000010;**<br/> | Beendet alle Vorbereitungsanforderungen, die sich nicht in der [**Warteschlange**](iagentcharacter--prepare.md) befinden.                               |
| **const unsigned long** **STOP TYPE VISIBLE = \_ \_ 0x00000020;**<br/>          | Beendet alle [**Hide-**](iagentcharacter--hide.md) [**oder Show-Anforderungen.**](iagentcharacter--show.md)       |



 

</dd> </dl>

## <a name="see-also"></a>Weitere Informationen

[**IAgentCharacter::Stop**](iagentcharacter--stop.md)


 

 





