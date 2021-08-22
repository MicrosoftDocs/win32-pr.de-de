---
description: Der Systemregistrierungsanbieter versucht, eine Benachrichtigung für jedes auftretende Ereignis zu senden.
ms.assetid: 51ef0ccb-02d5-4dac-9c71-a7f4e25a0d00
ms.tgt_platform: multiple
title: Empfangen von Registrierungsereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d6f3c8f39be30beeb64e7c8d8ff7f1bacfba8a47b7f4bd0c70e7cf638bf726e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817456"
---
# <a name="receiving-registry-events"></a>Empfangen von Registrierungsereignissen

Der Systemregistrierungsanbieter versucht, eine Benachrichtigung für jedes auftretende Ereignis zu senden. Der Systemregistrierungsanbieter garantiert jedoch nicht, dass der Consumer beliebige oder alle Ereignisse empfängt. Die Ausnahme besteht darin, dass der Systemregistrierungsanbieter sicherstellt, dass ein Consumer eine Benachrichtigung für jede Ereignisregistrierung erhält.

Angenommen, ein Consumer registriert sich für zwei Strukturänderungsereignisse und fordert eine Benachrichtigung für [**RegistryTreeChangeEvent-Instanzen**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) an. Jede Registrierung hat den gleichen Hive-Wert (Unterstruktur), aber einen anderen RootPath-Wert. Wenn schlüssel in beiden Pfaden mehrmals geändert werden, garantiert der Systemregistrierungsanbieter, dass der Consumer eine Benachrichtigung für jeden Pfad erhält. Abhängig von der Antwortzeit der Registrierung und des Systemregistrierungsanbieters erhält der Consumer möglicherweise so viele Benachrichtigungen, wie Ereignisse aufgetreten sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrieren für Systemregistrierungsereignisse](registering-for-system-registry-events.md)
</dt> </dl>

 

 
