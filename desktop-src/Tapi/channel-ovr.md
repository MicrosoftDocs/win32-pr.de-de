---
description: Jede Zeile verfügt über einen oder mehrere Kanäle. Die Dienstanbieter behandeln normalerweise, wie Kanäle als Adressen für eine Anwendung verfügbar gemacht werden, und der Endbenutzer oder Server benötigt keine speziellen Kenntnisse von Kanälen.
ms.assetid: 8c7d38e0-1863-461f-9225-7a0b419532a3
title: Channel (telefonieapi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b793a23c945cad79c9e2401ab6944302e908fd73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527236"
---
# <a name="channel-telephony-api"></a>Channel (telefonieapi)

Jede Zeile verfügt über einen oder mehrere Kanäle. Die Dienstanbieter behandeln normalerweise, wie Kanäle als Adressen für eine Anwendung verfügbar gemacht werden, und der Endbenutzer oder Server benötigt keine speziellen Kenntnisse von Kanälen.

Kanäle sind identisch und somit austauschbar. In den Töpfen (Plain Old Telefon Service) ist genau ein Kanal in einer Zeile vorhanden, und der Kanal wird ausschließlich für Voice verwendet. Mit ISDN können mindestens drei (und bis zu 30 oder mehr) Kanäle gleichzeitig in einer Zeile vorhanden sein.

Jeder Kanal kann über eine eigene Adresse verfügen. Dies bedeutet, dass eine Zeile über so viele Adressen verfügen kann, wie Sie über Kanäle verfügt. Die genaue Beziehung zwischen Kanälen und Adressen, die für eine Anwendung verfügbar gemacht werden, hängt von der Implementierung eines Dienstanbieters ab.

Einige Dienstanbieter unterstützen die Zuweisung von mehr als einer Adresse zu einem einzelnen Kanal. In den Pots-Zeilen werden mehrere Adressen durch verschiedene Systeme ermöglicht, wie z. b. eine direkte, innere Wahl (was) oder ein charakteristisches Klingeln, bei dem es sich um zusätzliche kostenpflichtige Dienste handelt, die das Telefonunternehmen bereitstellt.

Viele große Unternehmen verwenden für eingehende Aufrufe. Vor dem Herstellen eines Aufrufs wird die Nummer der zielweiterung an die PBX signalisiert. Dies bewirkt, dass die Erweiterung anstelle des Telefons des Operators klingelt. Ein Beispiel für ein besonderes Klingeln bei einem privaten Zuhause wäre, wenn die übergeordneten Elemente eine Adresse, die anderen untergeordneten Elemente und einen faxcomputer als dritte verwendet haben. Da nur eine einzige Zeile das Haus mit dem Telefon Netzwerk verbindet, werden alle Telefone beim Erscheinen eines Aufrufs Klingeln, das Ring Muster unterscheidet sich jedoch je nach der Anzahl, die von der aufrufenden Partei gewählt wurde. Bei einem markanten Klingeln wissen die Menschen, für wen der eingehende Anruf vorgesehen ist, und der faxcomputer antwortet seine Anrufe, indem er seine eigene Klingel Art erkennt.

In ISDN haben die verschiedenen B-Kanäle möglicherweise keine separaten Adressen. Da sich diese B-Kanäle möglicherweise auf derselben Adresse befinden, ist Sie der Dienstanbieter (und nicht die Anwendung oder eine Person, die die Zahl gewählt hat), die diesen Kanälen Aufrufe zuweist.

 

 



