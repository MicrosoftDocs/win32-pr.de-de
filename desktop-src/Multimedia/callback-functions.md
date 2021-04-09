---
title: Rückruffunktionen
description: Rückruffunktionen
ms.assetid: d96e93e5-ebc9-4ad4-aaec-dcc4197a3fc5
keywords:
- installierbare Treiber, Rückruf Funktionen
- installierbare Treiber, drivercallback-Funktion
- installierbare Treiber, Ereignisse
- Drivercallback-Funktion
- DRV_OPEN Meldung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e23f933567d125dd07f81047ea8868c12f41ac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858234"
---
# <a name="callback-functions"></a>Rückruffunktionen

Installierbare Treiber können die Anwendung, das Fenster oder den Task, der die angegebene Instanz zu Ereignissen geöffnet hat, mithilfe der [drivercallback](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback) -Funktion benachrichtigen. Diese Funktion ermöglicht dem Treiber das Zurückgeben von Informationen an eine Anwendung oder dll, während eine Anforderung weiterhin verarbeitet wird.

Wenn ein Treiber Rückruf Funktionen unterstützt, muss die Anwendung oder dll, die die Instanz öffnet, einen Wert bereitstellen, der entweder die Adresse einer Rückruffunktion, ein Fenster Handle oder ein Task Handle ist. Dieser Wert und ein Flag, das den Typ des Werts identifiziert, werden in der Regel in einer Struktur übergeben, auf die der zweite Parameter der von [**drv \_ geöffneten**](drv-open.md) Nachricht zeigt.

 

 