---
title: Codes in FACILITY_ITF
description: Codes in FACILITY \_ ITF
ms.assetid: 1f9f7b2c-a4e4-41c0-9ba5-b8bbf722e077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba2a16d051c352c353376865265c0451014f6110fbcde326914c3cc244a36223
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793790"
---
# <a name="codes-in-facility_itf"></a>Codes in FACILITY \_ ITF

**HRESULT-Werte** mit Einrichtungen wie FACILITY NULL und FACILITY RPC haben universelle Bedeutung, da sie an einer einzelnen Quelle \_ \_ definiert sind: Microsoft. **HRESULT-Werte** in FACILITY ITF werden jedoch durch die Funktion oder Schnittstellenmethode bestimmt, \_ von der sie zurückgegeben werden. Dies bedeutet, dass der gleiche 32-Bit-Wert in FACILITY ITF, der von zwei verschiedenen Schnittstellenmethoden zurückgegeben wird, \_ möglicherweise unterschiedliche Bedeutungen hat.

**HRESULT-Ergebnisse** in FACILITY ITF können in verschiedenen Schnittstellen unterschiedliche Bedeutungen haben, da HRESULT-S auf eine effiziente Datentypgröße von \_ 32 Bits beibehalten werden.  Leider sind 32 Bits nicht groß genug für die Entwicklung eines Fehlercodezuordnungssystems, das in Konflikt stehende Codes vermeidet, die von verschiedenen Programmierern zu unterschiedlichen Zeiten an verschiedenen Stellen zugeordnet werden (im Gegensatz zur Behandlung von Schnittstellenbezeichnern und CLSIDs). Daher ist das 32-Bit-HRESULT so strukturiert, dass Microsoft mehrere universelle Fehlercodes definieren kann, während es anderen Programmierern ermöglicht wird, neue Fehlercodes ohne Konfliktangst zu definieren.  Die Statuscodekonvention lautet wie folgt:

-   Statuscodes in anderen Einrichtungen als FACILITY \_ ITF können nur von Microsoft definiert werden.
-   Statuscodes in facility FACILITY ITF werden ausschließlich vom Entwickler der Schnittstelle oder Funktion definiert, \_ die den Statuscode zurückgibt. Um in Konflikt stehende Fehlercodes zu vermeiden, ist jeder, der die Schnittstelle definiert, für die Koordination und Veröffentlichung der FACILITY ITF-Statuscodes verantwortlich, die \_ dieser Schnittstelle zugeordnet sind.

Alle COM-definierten FACILITY ITF-Codes verfügen über einen Codewert im Bereich \_ 0x0000-0x01FF. Es ist zwar gesetzlich, Codes in FACILITY ITF zu verwenden, es wird jedoch empfohlen, nur Codewerte im Bereich \_ 0x0200-0xFFFF zu verwenden. Diese Empfehlung wird als Mittel zur Reduzierung von Verwechslungen mit COM-definierten Fehlern gemacht.

Es wird auch empfohlen, dass Entwickler neue Funktionen und Schnittstellen definieren, um Fehlercodes gemäß der Definition durch COM und in anderen Einrichtungen als FACILITY \_ ITF zurück zu geben. Insbesondere Schnittstellen, die in Zukunft per RPC remote entfernt werden können, sollten die FACILITY \_ RPC-Codes als legal definieren. E UNEXPECTED ist ein bestimmter Fehlercode, der von den meisten Entwicklern \_ allgemein als "legal" bezeichnet werden soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehlerbehandlung in COM](error-handling-in-com.md)
</dt> </dl>

 

 




