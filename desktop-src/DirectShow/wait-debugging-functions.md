---
description: Wartedebuggingfunktionen
ms.assetid: 784ef76e-3c17-45e0-9a0b-656c11c71322
title: Wartedebuggingfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f8f1de3d19ce7408625a5ab42f230d23ce401728e9fa7cf060edae62e19fcfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049200"
---
# <a name="wait-debugging-functions"></a>Wartedebuggingfunktionen

Microsoft DirectShow bietet mehrere Funktionen zum Debuggen unendlicher Wartefunktionen.

In Einzelhandels-Builds funktionieren die [**Funktionen DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) und [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) wie ihre Windows-API-Entsprechungen **WaitForMultipleObjects** und **WaitForSingleObject** mit unendlichen Time out-Intervallen.

In Debugbuilds verwenden diese Funktionen einen globalen Time out-Wert. Wenn das Time out abläuft, löst die Funktion eine Assert-Funktion aus. Der folgende Registrierungsschlüssel gibt den Time out-Wert in Millisekunden an:

**HKEY \_ LOCAL \_ MACHINE \\ <DebugRoot> \\ <Module Name> \\ TIMEOUT**

Dabei *<DebugRoot>* ist der Registrierungspfad, der im Thema [Debugausgabefunktionen beschrieben wird.](debug-output-functions.md)

Wenn der Schlüssel nicht vorhanden ist, wird der Time out-Wert standardmäßig auf INFINITE festgelegt. Sie können die [**DbgSetWaitTimeout-Funktion**](dbgsetwaittimeout.md) verwenden, um den Registrierungseintrag zu überschreiben.



| Funktion                                                       | BESCHREIBUNG                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------|
| [**DbgSetWaitTimeout**](dbgsetwaittimeout.md)                 | Legt den Time out-Wert für das Debuggen fest.                              |
| [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) | Wartet, bis ein (oder alle) der angegebenen Objekte signalisiert wird. |
| [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md)       | Wartet, bis ein Objekt signalisiert wird.                         |



 

 

 



