---
title: Energie Verwaltung (TPM-Basisdienste)
description: Die TSB empfängt Energie Verwaltungs Ereignisse.
ms.assetid: 21f76bea-a313-46b7-99b3-422f17376a5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e21f2c6a2292b7d49fae3b15691703fa34667a
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2019
ms.locfileid: "106339037"
---
# <a name="power-management-tpm-base-services"></a>Energie Verwaltung (TPM-Basisdienste)

Die TSB empfängt Energie Verwaltungs Ereignisse. Wenn ein Hinweis darauf eingeht, dass das TPM oder andere Teile der Plattform in einen Energiezustand eintreten werden, in dem die Ausführung unterbrochen wird oder der TPM-Status verloren geht, prüft die TSB, ob der aktuell ausgeführte Befehl wahrscheinlich abgeschlossen ist, bevor das System ausfällt. Im allgemeinen ermöglicht die TSB die Fertigstellung von Befehlen für kurze und mittlere Dauer, bricht jedoch Befehle mit langer Ausführungsdauer ab. Nachdem der Befehl zurückgegeben wurde, sendet der TSB keine neuen Befehle an das TPM und bereitet sich selbst auf den Ruhezustand vor. Wenn die Stromversorgung wieder hergestellt wird, gibt die TSB das Ergebnis des Befehls an den Aufrufer zurück und fährt dann mit der Verarbeitung ausstehender TSB-Befehle fort. Der TSB-Energie Verwaltungs Code wird asynchron ausgeführt, sodass Energie Verwaltungsanforderungen verarbeitet werden können, auch wenn das TPM einen langen Befehl verarbeitet.

Wenn ein Computer in den Standbymodus wechselt, einschließlich S3 (Standby) und S4 (Ruhezustand), wird das TPM ausgeschaltet. Daher gehen alle nicht persistenten TPM-Zustände verloren. Vor der Eingabe dieser Zustände wird erwartet, dass sich die Anwendungssoftware auf den Verlust flüchtiger TPM-Zustände vorbereitet. Wenn das System aus dem Ruhezustand zurückkehrt, wird die TSB mit dem TPM synchronisiert, sodass der TSB-Status mit dem TPM-Status konsistent ist. Möglicherweise müssen von der Anwendungssoftware nicht unterbrochene Befehle neu ausgestellt werden.

 

 




