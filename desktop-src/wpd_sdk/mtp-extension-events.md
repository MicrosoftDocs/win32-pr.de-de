---
description: MTP-Erweiterungs Ereignisse
ms.assetid: c04554cd-d68d-455e-afa3-29d4186dad65
title: MTP-Erweiterungs Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10389df9105615befa9ba0f32824615977cc3cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373359"
---
# <a name="mtp-extension-events"></a>MTP-Erweiterungs Ereignisse

Ereignisse benachrichtigen eine Anwendung, dass Änderungen am oder mit einem Gerät aufgetreten sind. Beispielsweise kann eine Anwendung registrieren, um Benachrichtigungen zu erhalten, dass ein Gerät entfernt wurde.

## <a name="vendor-extended-event-codes"></a>Vom Hersteller erweiterte Ereignis Codes

Wenn ein Gerätehersteller ein vom Hersteller erweitertes Ereignis unterstützt, kombiniert der Treiber den Ereignis Code des Anbieters (UInt16) mit den höchsten 16 Bits der GUID für die **\_ \_ \_ \_ Erweiterte \_ Ereignisse des WPD-Ereignis-MTP-Anbieters** .

Wenn beispielsweise der erweiterte Code des Anbieters 0xc001 ist, würde die resultierende GUID wie im folgenden Beispiel gezeigt lauten:


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="vendor-extended-event-parameters"></a>Vom Hersteller erweiterte Ereignis Parameter

Die Parameter für ein vom Hersteller erweitertes Ereignis werden von der Ereignis-ID-GUID des **WPD- \_ Ereignis \_ Parameters \_ \_** und der **WPD- \_ Eigenschaft \_ MTP \_ Ext- \_ Ereignis \_** Parameter gemeldet, eine Auflistung von **propvarianten**. Diese **propvarianten** entsprechen den Ereignis Parametern. Wenn keine Parameter vorhanden sind, ist diese Auflistung leer.


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützen von MTP-Erweiterungen](supporting-mtp-extensions.md)
</dt> </dl>

 

 



