---
description: Die folgenden Abschnitte enthalten eine alphabetische Liste der Funktionen, die nach Bereich gruppiert sind. Die Informationen für jede Funktion enthalten eine Liste der gültigen Ansichts Zustände für den Eintrag der Funktion und typische Aufrufe des Zustands von anrufen, wenn die Anforderung beendet ist.
ms.assetid: 555d6af2-b440-4636-b90e-da297a369753
title: TAPI-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38532fa1c0b978e3e59e54b08fbc43152fa0bd64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529213"
---
# <a name="tapi-functions"></a>TAPI-Funktionen

Die folgenden Abschnitte enthalten eine alphabetische Liste der Funktionen, die nach Bereich gruppiert sind. Die Informationen für jede Funktion enthalten eine Liste der gültigen Ansichts Zustände für den Eintrag der Funktion und typische Aufrufe des Zustands von anrufen, wenn die Anforderung beendet ist.

-   [Unterstützte Telefoniefunktionen](assisted-telephony-functions.md)
-   [Callcenter-Funktionen](call-center-functions.md)
-   [Zeilen Gerätefunktionen](line-device-functions.md)
-   [Telefongeräte Funktionen](phone-device-functions.md)

Informationen zu TAPI-Funktionen, die nach Service Level und Task kategorisiert sind, finden Sie unter [TAPI Quick Function Reference](tapi-quick-function-reference.md)

Beachten Sie, dass die Einschränkungen des Dienstanbieters möglicherweise in Bezug auf die tatsächlichen Zustände bestehen, in denen eine Funktion ausgeführt werden kann. Anwendungen müssen den **dwcallfeatures** -Member in der [**linecallstatus**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) -Struktur, den **dwaddressfeatures** -Member in der [**lineaddressstatus**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) -Struktur und den **dwlinefeatures** -Member in der [**linedevstatus**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) -Struktur überprüfen, um zu bestimmen, ob eine Funktion innerhalb des aktuellen Aufruf Zustands zulässig ist oder nicht.

 

 



