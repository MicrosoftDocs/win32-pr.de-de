---
title: Rückruffunktionen
description: Rückruffunktionen
ms.assetid: d96e93e5-ebc9-4ad4-aaec-dcc4197a3fc5
keywords:
- Installierbare Treiber, Rückruffunktionen
- Installierbare Treiber, DriverCallback-Funktion
- Installierbare Treiber, Ereignisse
- DriverCallback-Funktion
- DRV_OPEN Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fabb833b0aa3adef444f8242d540eb48dcbe381ebc5c7f62c6dedc0d5e9160e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786200"
---
# <a name="callback-functions"></a>Rückruffunktionen

Installierbare Treiber können die Anwendung, das Fenster oder den Task benachrichtigen, die bzw. der die angegebene Instanz über Ereignisse geöffnet hat, indem sie die [DriverCallback-Funktion](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback) verwenden. Diese Funktion gibt dem Treiber die Möglichkeit, Informationen an eine Anwendung oder DLL zurückzugeben, während eine Anforderung weiterhin verarbeitet wird.

Wenn ein Treiber Rückruffunktionen unterstützt, muss die Anwendung oder DLL, die die Instanz öffnet, einen Wert bereitstellen. Dies ist entweder die Adresse einer Rückruffunktion, ein Fensterhandle oder ein Aufgabenhandle. Dieser Wert und ein Flag, das den Typ des Werts identifiziert, werden in der Regel in einer Struktur übergeben, auf die der zweite Parameter der [**DRV \_ OPEN-Nachricht**](drv-open.md) zeigt.

 

 