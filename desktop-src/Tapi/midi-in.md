---
description: Die Klasse "MIDI/in" besteht aus den für die Eingabe verwendeten MIDI-Sequencern. Sie greifen auf diese Geräte mithilfe der Funktionen von MIDI zu, die im Platform Software Development Kit (SDK) beschrieben werden.
ms.assetid: 8997a391-bf61-4ec9-8ffc-fe3e6b92d63a
title: MIDI/in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1d8119990af37cb030211b7dcc3a75d5261411f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749537"
---
# <a name="midiin"></a>MIDI/in

Die Klasse "MIDI/in" besteht aus den für die Eingabe verwendeten MIDI-Sequencern. Sie greifen auf diese Geräte mithilfe der Funktionen von MIDI zu, die im Platform Software Development Kit (SDK) beschrieben werden.

Die Funktionen [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) und [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) füllen eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur aus, indem Sie das Element **dwstringformat** auf den Binär Wert StringFormat festlegen \_ und diesen zusätzlichen Member anhängen:

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

Der Member " **enviceid** " ist der Bezeichner eines geschlossenen MIDI-Geräts. Sie verwenden diesen Bezeichner in einem aufzurufenden Befehl der [**midiinopen**](/windows/win32/api/mmeapi/nf-mmeapi-midiinopen) -Funktion zum Öffnen des Geräts für die Eingabe. Sie können das resultierende Geräte Handle verwenden, um die Daten von MIDI von der Zeile oder dem Telefongerät aufzuzeichnen.

Weitere Informationen zu den Funktionen von MIDI finden Sie unter [**Multimedia Functions**](../multimedia/multimedia-functions.md).

 

 
