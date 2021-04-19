---
description: Wait-Debugging-Funktionen
ms.assetid: 784ef76e-3c17-45e0-9a0b-656c11c71322
title: Wait-Debugging-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d2f9f8d40e6b9676426254f0b9165b546dec7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345811"
---
# <a name="wait-debugging-functions"></a>Wait-Debugging-Funktionen

Microsoft DirectShow stellt mehrere Funktionen zum Debuggen von unendlichen warte Vorgängen bereit.

In Einzelhandels Builds funktionieren die [**dbgwaitformultipleobjects**](dbgwaitformultipleobjects.md) -und [**dbgwaitforsingleobject**](dbgwaitforsingleobject.md) -Funktionen wie Ihre Windows-API-Entsprechungen, **WaitForMultipleObjects** und **WaitForSingleObject**, mit unendlichen Timeout Intervallen.

In Debugbuilds verwenden diese Funktionen einen globalen Timeout Wert. Wenn das Timeout abgelaufen ist, löst die Funktion eine Assert-Funktion aus. Der folgende Registrierungsschlüssel gibt den Timeout Wert (in Millisekunden) an:

**Timeout für lokalen HKEY- \_ \_ Computer \\ <DebugRoot> \\ <Module Name> \\**

*<DebugRoot>* dabei ist der Registrierungs Pfad, der im Thema [Debug Output Functions](debug-output-functions.md)beschrieben wird.

Wenn der Schlüssel nicht vorhanden ist, ist der Timeout Wert standardmäßig unbegrenzt. Sie können die [**dbgsetwaittimeout**](dbgsetwaittimeout.md) -Funktion verwenden, um den Registrierungs Eintrag zu überschreiben.



| Funktion                                                       | BESCHREIBUNG                                                     |
|----------------------------------------------------------------|-----------------------------------------------------------------|
| [**Dbgsetwaittimeout**](dbgsetwaittimeout.md)                 | Legt den Timeout Wert für das Debuggen fest.                              |
| [**Dbgwaitformultipleobjects**](dbgwaitformultipleobjects.md) | Wartet darauf, dass alle (oder alle) der angegebenen Objekte signalisiert werden. |
| [**Dbgwaitforsingleobject**](dbgwaitforsingleobject.md)       | Wartet darauf, dass ein Objekt signalisiert wird.                         |



 

 

 



