---
title: Streampufferformat
description: Streampufferformat
ms.assetid: 4b24c12e-b43f-492e-a000-af4f59d5e16f
keywords:
- Music Instrument Digital Interface (INSTRUMENT DIGITAL INTERFACE), Streampuffer
- INSTRUMENTS (Music Instrument Digital Interface), Streampuffer
- Streampuffer, Format
- STRUKTURENHDR-Struktur
- STRUKTURENEVENT-Struktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 072c2541ab6b731686fc63c59b11b0dfff529ef9cab347d41fbddf13e9b60b04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688500"
---
# <a name="stream-buffer-format"></a>Streampufferformat

Der **lpData-Member** der [**CSVHDR-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-midihdr) zeigt auf einen Streampuffer, und der **dwBufferLength-Member** gibt die tatsächliche Größe dieses Puffers an. Der **dwBytesRecorded-Member** von **GIGABYTEHDR** gibt die Anzahl der Bytes im Puffer an, die tatsächlich von den EREIGNISSEN DES -Attributs verwendet werden. dieser Wert muss kleiner oder gleich dem von **dwBufferLength** angegebenen Wert sein.

Jedes der EREIGNISSE im Streampuffer wird durch eine [**CABEVENT-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-midievent) angegeben, die die Zeit für das Ereignis, einen Streambezeichner, einen Ereigniscode und ggf. Parameter für das Ereignis enthält. Jede dieser **STRUKTURENEVENT-Strukturen** muss an einer Doppelwortgrenze beginnen. Bei Bedarf müssen am Ende der -Struktur Padbytes hinzugefügt werden, um sicherzustellen, dass der nächste an einer Doppelwortgrenze beginnt.

 

 