---
title: Zugreifen auf eine Alternative Registrierungs Ansicht
description: Eine 32-Bit-Anwendung, die unter WOW64 ausgeführt wird, greift standardmäßig auf die 32-Bit-Registrierungsansicht zu, und eine 64-Bit-Anwendung greift auf die 64-Bit-Registrierungsansicht zu.
ms.assetid: 2c5fd3de-998c-44ab-863e-8e0e90d56e5d
keywords:
- Registrierungs Sichten 64-Bit-Windows-Programmierung
- WOW64 64-Bit-Windows-Programmierung, Registrierungs Sichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3bca57367394e1b2fffc6486065e93c966f224
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "106355088"
---
# <a name="accessing-an-alternate-registry-view"></a>Zugreifen auf eine Alternative Registrierungs Ansicht

Eine 32-Bit-Anwendung, die unter WOW64 ausgeführt wird, greift standardmäßig auf die 32-Bit-Registrierungsansicht zu, und eine 64-Bit-Anwendung greift auf die 64-Bit-Registrierungsansicht zu. Die folgenden Flags ermöglichen 32-Bit-Anwendungen den Zugriff auf umgeleitete Schlüssel in der 64-Bit-Registrierungs Ansicht und 64-Bit-Anwendungen für den Zugriff auf umgeleitete Schlüssel in der 32-Bit-Registrierungs Ansicht. Diese Flags haben keine Auswirkung auf freigegebene Registrierungsschlüssel. Weitere Informationen finden Sie unter [Registrierungsschlüssel, die von WOW64 betroffen sind](shared-registry-keys.md).



| Flagname         | Wert  | BESCHREIBUNG                                                                                                                                                                                                                                       |
|-------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Key \_ WOW64 \_ 64key | 0x0100 | Greifen Sie entweder über eine 32-Bit-oder 64-Bit-Anwendung auf einen 64-Bit-Schlüssel zu.                                                                                                                                                                                   |
| Key \_ WOW64 \_ 32key | 0x0200 | Greifen Sie entweder über eine 32-Bit-oder 64-Bit-Anwendung auf einen 32-Bit-Schlüssel zu.<br/>**Windows 10 auf ARM:** Dies bezieht sich auf die 32-Bit-ARM-Registrierungs Sicht für 32-Bit-ARM-Prozesse und die 32-Bit-x86-Registrierungs Ansicht für 32-Bit-x86-und 64-Bit ARM64-Prozesse. |



 

Diese Flags können im Parameter *samgewünschter* Parameter der folgenden Registrierungsfunktionen angegeben werden:

-   [**Regkreatekeyex**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [**Regdeletekeyex**](/windows/desktop/api/winreg/nf-winreg-regdeletekeyexa)
-   [**Fehler bei RegOpenKeyEx**](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)

Entweder Key \_ WOW64 \_ 32key oder Key \_ WOW64 \_ 64key kann angegeben werden. Wenn beide Flags angegeben sind, schlägt die Funktion mit einem \_ ungültigen \_ Parameter fehl.

**Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Wenn beide Flags angegeben sind, ist das Verhalten der Funktion nicht definiert.

Die [**regdeletekey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya) -Funktion kann nicht für den Zugriff auf eine Alternative Registrierungs Ansicht verwendet werden.

Im folgenden finden Sie bewährte Methoden für den Zugriff auf die Registrierung von einer Anwendung aus:

-   Nachdem die Anwendung mit einem der Flags auf eine Alternative Registrierungs Ansicht zugegriffen hat, müssen alle nachfolgenden Vorgänge (erstellen, löschen oder öffnen) für untergeordnete Registrierungsschlüssel explizit dasselbe Flag verwenden. Andernfalls kann es zu unerwartetem Verhalten kommen.
-   Um alle Schlüssel in beiden Ansichten genau aufzuzählen, führen Sie die Enumeration in zwei Durchläufen aus. Der erste Durchlauf sollte ein Handle verwenden, das mit einem der-Flags geöffnet wurde, und der andere Durchlauf sollte ein Handle verwenden, das mit dem anderen Flag geöffnet wurde.

> [!Note]  
> Die Schlüssel **Wow6432Node** und **WowAA32Node** sind reserviert. Aus Kompatibilitätsgründen sollten Anwendungen diese Schlüssel nicht direkt verwenden.

 

Weitere Informationen zum Zugreifen auf die Alternative Registrierungs Ansicht über WMI finden Sie unter [anfordern von WMI-Daten auf einer 64-Bit-Plattform](/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrierungs Redirector](registry-redirector.md)
</dt> <dt>

[Registrierungs Reflektion](registry-reflection.md)
</dt> </dl>

 

