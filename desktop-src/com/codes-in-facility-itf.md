---
title: Codes in FACILITY_ITF
description: Codes in der \_ Einrichtung der Einrichtung
ms.assetid: 1f9f7b2c-a4e4-41c0-9ba5-b8bbf722e077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc4375b5956502dbaee97057d347aff1da77e3a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947551"
---
# <a name="codes-in-facility_itf"></a>Codes in der \_ Einrichtung der Einrichtung

**HRESULT** s mit Einrichtungen wie z. b. dem Werk \_ null und dem Werk- \_ RPC haben universelle Bedeutung, da Sie an einer einzigen Quelle definiert sind: Microsoft. **HRESULT** s in der Anlage " \_ ITF" werden jedoch durch die Funktion oder Schnittstellen Methode bestimmt, von der Sie zurückgegeben werden. Dies bedeutet, dass derselbe 32-Bit-Wert in Einrichtung, der \_ von zwei verschiedenen Schnittstellen Methoden zurückgegeben wurde, möglicherweise eine andere Bedeutung hat.

Der Grund für **HRESULT** s in der Einrichtung \_ von "ITF" kann in verschiedenen Schnittstellen unterschiedliche Bedeutungen haben, da **HRESULT** s in einer effizienten Datentyp Größe von 32 Bits aufbewahrt werden. Leider ist 32 Bits nicht groß genug für die Entwicklung eines Fehlercode-Zuordnungs Systems, das in Konflikt stehende Codes vermeidet, die von verschiedenen Programmierern zu unterschiedlichen Zeiten an unterschiedlichen Stellen zugeordnet werden (im Gegensatz zur Handhabung von Schnittstellen bezeichmern und CLSIDs). Demzufolge ist das 32-Bit- **HRESULT** so strukturiert, dass Microsoft mehrere universelle Fehlercodes definieren und anderen Programmierern das Definieren neuer Fehlercodes ohne Angst vor Konflikten ermöglicht. Die Statuscode Konvention lautet wie folgt:

-   Status Codes in anderen Einrichtungen als Einrichtung- \_ ITF können nur von Microsoft definiert werden.
-   Statuscodes in der Einrichtung der Einrichtung \_ werden ausschließlich vom Entwickler der-Schnittstelle oder der-Funktion definiert, die den Statuscode zurückgibt. Um widersprüchliche Fehlercodes zu vermeiden, ist der Benutzer, der die Schnittstelle definiert, verantwortlich für die Koordination und Veröffentlichung der \_ mit dieser Schnittstelle verknüpften Statuscodes der Einrichtung.

Alle com-definierten Einrichtung- \_ Codes der Einrichtung haben einen Codewert im Bereich von 0x0000-0x01ff. Es ist zwar zulässig, beliebige Codes in der Einrichtung von "" zu verwenden \_ , es wird jedoch empfohlen, dass nur Codewerte im Bereich von 0x0200-0xFFFF verwendet werden. Diese Empfehlung dient als Mittel zum Reduzieren von Verwirrung durch com-definierte Fehler.

Außerdem wird empfohlen, dass Entwickler neue Funktionen und Schnittstellen definieren, um Fehlercodes gemäß der Definition durch com und in anderen Einrichtungen als in der Einrichtung von "Einrichtung" zurückzugeben \_ . Insbesondere sollten Schnittstellen, die die Möglichkeit haben, in Zukunft Remote über RPC zu sein, die Standort- \_ RPC-Codes als legal definieren. E \_ unerwartet ist ein bestimmter Fehlercode, der von den meisten Entwicklern universell legal gemacht werden soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Fehlerbehandlung in com](error-handling-in-com.md)
</dt> </dl>

 

 




