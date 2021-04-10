---
description: Die Geräteklasse "MIDI/Out" besteht aus den für die Ausgabe verwendeten MIDI-Sequencern. Sie greifen auf diese Geräte mithilfe der Funktionen von MIDI zu, die im Platform Software Development Kit (SDK) beschrieben werden.
ms.assetid: 398119ec-2d08-4c37-a993-a9b5ce52bcc8
title: "\"MIDI/Out\""
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6ae6a3daba8fa0520fca666e6c43a8b3db86c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214369"
---
# <a name="midiout"></a>"MIDI/Out"

Die Geräteklasse "MIDI/Out" besteht aus den für die Ausgabe verwendeten MIDI-Sequencern. Sie greifen auf diese Geräte mithilfe der Funktionen von MIDI zu, die im Platform Software Development Kit (SDK) beschrieben werden.

Die Funktionen [**lineGetID**](/windows/desktop/api/Tapi/nf-tapi-linegetid) und [**phonegetid**](/windows/desktop/api/Tapi/nf-tapi-phonegetid) füllen eine [**varstring**](/windows/desktop/api/Tapi/ns-tapi-varstring) -Struktur aus, indem Sie das Element **dwstringformat** auf den Binär Wert StringFormat festlegen \_ und diesen zusätzlichen Member anhängen:

``` syntax
DWORD DeviceId;  // identifier of MIDI device
```

Der Member " **enviceid** " ist der Bezeichner eines geschlossenen MIDI-Geräts. Sie verwenden diesen Bezeichner in einem Aufrufe der [**midioutopen**](/windows/win32/api/mmeapi/nf-mmeapi-midioutopen) -Funktion, um das Gerät für die Ausgabe zu öffnen. Sie können das resultierende Geräte Handle verwenden, um die Daten von MIDI an der Zeile oder dem Telefongerät wiederzugeben.

Weitere Informationen zu den Funktionen von MIDI finden Sie unter [**Multimedia Functions**](../multimedia/multimedia-functions.md).

 

 
