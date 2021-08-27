---
description: Wartedebuggingfunktionen
ms.assetid: 784ef76e-3c17-45e0-9a0b-656c11c71322
title: Wartedebuggingfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f2aabec60a14ff36d74298a21d31c91b4bc6d94
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884029"
---
# <a name="wait-debugging-functions"></a>Wartedebuggingfunktionen

Microsoft DirectShow bietet mehrere Funktionen zum Debuggen unendlicher Wartefunktionen.

In Einzelhandels-Builds funktionieren die [**Funktionen DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) und [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md) wie ihre Windows-API-Entsprechungen **WaitForMultipleObjects** und **WaitForSingleObject** mit unendlichen Time out-Intervallen.

In Debugbuilds verwenden diese Funktionen einen globalen Time out-Wert. Wenn das Time out abläuft, löst die Funktion eine Assert-Funktion aus. Der folgende Registrierungsschlüssel gibt den Time out-Wert in Millisekunden an:

**HKEY \_ LOCAL \_ MACHINE \\ &lt; DebugRoot &gt; \\ <Module Name> \\ TIMEOUT**

Wobei *&lt; DebugRoot &gt; der* Registrierungspfad ist, der im Thema [Debugausgabefunktionen beschrieben wird.](debug-output-functions.md)

Wenn der Schlüssel nicht vorhanden ist, wird der Time out-Wert standardmäßig auf INFINITE festgelegt. Sie können die [**DbgSetWaitTimeout-Funktion**](dbgsetwaittimeout.md) verwenden, um den Registrierungseintrag zu überschreiben.



| Funktion                                                       | Beschreibung                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------|
| [**DbgSetWaitTimeout**](dbgsetwaittimeout.md)                 | Legt den Time out-Wert für das Debuggen fest.                              |
| [**DbgWaitForMultipleObjects**](dbgwaitformultipleobjects.md) | Wartet, bis ein (oder alle) der angegebenen Objekte signalisiert wird. |
| [**DbgWaitForSingleObject**](dbgwaitforsingleobject.md)       | Wartet, bis ein Objekt signalisiert wird.                         |



 

 

 



