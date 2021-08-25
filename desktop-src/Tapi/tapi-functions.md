---
description: Die folgenden Abschnitte enthalten eine alphabetische Liste der Funktionen gruppiert nach Bereich. Die Informationen für jede Funktion enthalten eine Liste der gültigen Aufrufzustände beim Eintrag der Funktion und typische Aufrufzustandsübergänge, wenn die Anforderung abgeschlossen ist.
ms.assetid: 555d6af2-b440-4636-b90e-da297a369753
title: TAPI-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27ec2383f826efe5620ea44d3a643e46a90b08c7820548733238290bff26512
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872910"
---
# <a name="tapi-functions"></a>TAPI-Funktionen

Die folgenden Abschnitte enthalten eine alphabetische Liste der Funktionen gruppiert nach Bereich. Die Informationen für jede Funktion enthalten eine Liste der gültigen Aufrufzustände beim Eintrag der Funktion und typische Aufrufzustandsübergänge, wenn die Anforderung abgeschlossen ist.

-   [Unterstützte Telefoniefunktionen](assisted-telephony-functions.md)
-   [Callcenterfunktionen](call-center-functions.md)
-   [Line Device Functions](line-device-functions.md)
-   [Telefon Gerätefunktionen](phone-device-functions.md)

Informationen zu TAPI-Funktionen, die nach Dienstebene und Aufgabe kategorisiert sind, finden Sie unter [TAPI Quick Function Reference (TAPI-Schnellfunktionsreferenz).](tapi-quick-function-reference.md)

Beachten Sie, dass Dienstanbietereinschränkungen hinsichtlich der tatsächlichen Zustände bestehen können, in denen eine Funktion ausgeführt werden kann. Anwendungen müssen den **dwCallFeatures-Member** in der [**LINECALLSTATUS-Struktur,**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) den **dwAddressFeatures-Member** in der [**LINEADDRESSSTATUS-Struktur**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) und den **dwLineFeatures-Member** in der [**LINEDEVSTATUS-Struktur**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) überprüfen, um zu bestimmen, ob eine Funktion im aktuellen Aufrufzustand zulässig ist.

 

 



