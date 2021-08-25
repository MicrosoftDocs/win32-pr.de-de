---
title: Zugreifen auf eine alternative Registrierungsansicht
description: Eine 32-Bit-Anwendung, die unter WOW64 ausgeführt wird, greift standardmäßig auf die 32-Bit-Registrierungsansicht zu, und eine 64-Bit-Anwendung greift auf die 64-Bit-Registrierungsansicht zu.
ms.assetid: 2c5fd3de-998c-44ab-863e-8e0e90d56e5d
keywords:
- 64-Bit-64-Bit-Windows Programmierung
- WOW64 64-Bit-Windows Programmierung, Registrierungsansichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1642de971a2342ab26114803689b8de21dd66194618a8db23f97170bc8da576a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859080"
---
# <a name="accessing-an-alternate-registry-view"></a>Zugreifen auf eine alternative Registrierungsansicht

Eine 32-Bit-Anwendung, die unter WOW64 ausgeführt wird, greift standardmäßig auf die 32-Bit-Registrierungsansicht zu, und eine 64-Bit-Anwendung greift auf die 64-Bit-Registrierungsansicht zu. Die folgenden Flags ermöglichen 32-Bit-Anwendungen den Zugriff auf umgeleitete Schlüssel in der 64-Bit-Registrierungsansicht und 64-Bit-Anwendungen für den Zugriff auf umgeleitete Schlüssel in der 32-Bit-Registrierungsansicht. Diese Flags haben keine Auswirkungen auf freigegebene Registrierungsschlüssel. Weitere Informationen finden Sie unter [Registrierungsschlüssel, die von WOW64 betroffen sind.](shared-registry-keys.md)



| Flagname         | Wert  | BESCHREIBUNG                                                                                                                                                                                                                                       |
|-------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| KEY \_ WOW64 \_ 64KEY | 0x0100 | Greifen Sie über eine 32-Bit- oder 64-Bit-Anwendung auf einen 64-Bit-Schlüssel zu.                                                                                                                                                                                   |
| KEY \_ WOW64 \_ 32KEY | 0x0200 | Greifen Sie über eine 32-Bit- oder 64-Bit-Anwendung auf einen 32-Bit-Schlüssel zu.<br/>**Windows 10 auf ARM:** Dies bezieht sich auf die 32-Bit-ARM-Registrierungsansicht für 32-Bit-ARM-Prozesse und die 32-Bit-x86-Registrierungsansicht für 32-Bit-x86- und 64-Bit-ARM64-Prozesse. |



 

Diese Flags können im *samDesired-Parameter* der folgenden Registrierungsfunktionen angegeben werden:

-   [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [**RegDeleteKeyEx**](/windows/desktop/api/winreg/nf-winreg-regdeletekeyexa)
-   [**RegOpenKeyEx**](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)

Entweder KEY \_ WOW64 \_ 32KEY oder KEY \_ WOW64 \_ 64KEY kann angegeben werden. Wenn beide Flags angegeben werden, schlägt die Funktion mit ERROR \_ INVALID \_ PARAMETER fehl.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Wenn beide Flags angegeben werden, ist das Verhalten der Funktion nicht definiert.

Die [**RegDeleteKey-Funktion**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya) kann nicht für den Zugriff auf eine alternative Registrierungsansicht verwendet werden.

Im Folgenden finden Sie bewährte Methoden für den Zugriff auf die Registrierung aus einer Anwendung:

-   Nachdem die Anwendung mithilfe eines der Flags auf eine alternative Registrierungsansicht zugegriffen hat, müssen alle nachfolgenden Vorgänge (Erstellen, Löschen oder Öffnen) für untergeordnete Registrierungsschlüssel explizit das gleiche Flag verwenden. Andernfalls kann es zu unerwartetem Verhalten führen.
-   Um alle Schlüssel in beiden Ansichten genau aufzählen zu können, führen Sie die Enumeration in zwei Durchläufen aus. Der erste Durchgang sollte ein Handle verwenden, das mit einem der Flags geöffnet wurde, und der andere Durchgang sollte ein Handle verwenden, das mit dem anderen Flag geöffnet wurde.

> [!Note]  
> Die **Schlüssel Wow6432Node** und **WowAA32Node** sind reserviert. Aus Kompatibilitäts- und Kompatibilitätsanforderungen sollten Anwendungen diese Schlüssel nicht direkt verwenden.

 

Informationen zum Zugriff auf die alternative Registrierungsansicht über WMI finden Sie unter Anfordern von [WMI-Daten auf einer 64-Bit-Plattform.](/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrierungsumleitung](registry-redirector.md)
</dt> <dt>

[Registrierungslektion](registry-reflection.md)
</dt> </dl>

 

