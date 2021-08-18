---
description: Gerätemeldungen sind Systemmeldungen, die Anwendungen und andere Features von Geräteänderungsereignissen benachrichtigen.
ms.assetid: 4d1ace87-2d02-4ba4-9bcc-da86cf3481db
title: Gerätemeldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a26666ab0f7675da02e70d53ffd8aec5040a0482a0a2cdc71279fcaeca8ca92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053509"
---
# <a name="device-messages"></a>Gerätemeldungen

Gerätemeldungen sind Systemmeldungen, die Anwendungen und andere Features von Geräteänderungsereignissen benachrichtigen. Diese Ereignisse treten immer dann auf, wenn das System eine Änderung der Systemhardware erkennt, z. B. wenn der Benutzer einen Laptop andockt und abdockt oder ein Gerät wie eine PCMCIA-Karte ein- oder entfernt. Geräteereignisse können auftreten, während das System ausgeführt wird oder wenn das System den Betrieb nach dem vorübergehenden Aussetzen wieder aufgenommen hat.

Um sicherzustellen, dass Anwendungen keine Daten verlieren, wenn Geräte nicht mehr verfügbar sind, überwacht das System die Hardwarekonfiguration und sendet Gerätenachrichten an die Anwendungen, um sie über die Änderungen zu benachrichtigen und ihnen die Möglichkeit zu geben, sich auf die Änderungen vorzubereiten, bevor sie auftreten.

Für jedes Geräteereignis sendet das System eine [**WM \_ DEVICECHANGE-Nachricht**](wm-devicechange.md) an alle Anwendungen. In dieser Meldung identifiziert der *wParam-Parameter* den Geräteereignistyp, und der [](device-event-types.md) *lParam-Parameter* ist ein Zeiger auf ereignisspezifische Daten.

 

 



