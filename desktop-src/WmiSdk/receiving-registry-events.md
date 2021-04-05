---
description: Der System Registrierungs Anbieter versucht, für jedes auftretende Ereignis eine Benachrichtigung zu senden.
ms.assetid: 51ef0ccb-02d5-4dac-9c71-a7f4e25a0d00
ms.tgt_platform: multiple
title: Empfangen von Registrierungs Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f0da8c039f83e3d4eb1f51d6b6707d0edd6b3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042005"
---
# <a name="receiving-registry-events"></a>Empfangen von Registrierungs Ereignissen

Der System Registrierungs Anbieter versucht, für jedes auftretende Ereignis eine Benachrichtigung zu senden. Der System Registrierungs Anbieter garantiert jedoch nicht, dass der Consumer ein oder alle Ereignisse empfängt. Die Ausnahme besteht darin, dass der System Registrierungs Anbieter sicherstellt, dass ein Consumer eine Benachrichtigung für jede Ereignis Registrierung erhält.

Nehmen wir beispielsweise an, ein Consumer registriert sich für zwei Struktur Änderungs Ereignisse, die eine Benachrichtigung für [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) -Instanzen anfordern. Jede Registrierung hat denselben Hive-Wert (Unterstruktur), aber einen anderen RootPath-Wert. Wenn sich die Schlüssel in beiden Pfaden mehrmals ändern, stellt der System Registrierungs Anbieter sicher, dass der Consumer eine Benachrichtigung für jeden Pfad erhält. Abhängig von der Antwortzeit der Registrierung und des System Registrierungs Anbieters erhält der Consumer möglicherweise so viele Benachrichtigungen wie Ereignisse.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrierung für System Registrierungs Ereignisse](registering-for-system-registry-events.md)
</dt> </dl>

 

 
