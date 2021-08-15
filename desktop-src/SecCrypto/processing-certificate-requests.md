---
description: Erläutert, wie Zertifikatanforderungen von Zertifikatdiensten verarbeitet werden.
ms.assetid: 40641167-12de-4008-80e4-2fb758146421
title: Verarbeiten von Zertifikatanforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be2c8e8acacbb001803cf3ce8d7e1263e920673eb912a04105ec8bb2772953a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117977404"
---
# <a name="processing-certificate-requests"></a>Verarbeiten von Zertifikatanforderungen

Zertifikatdienste führen die folgenden Schritte aus, wenn eine [*Zertifikatanforderung verarbeitet wird:*](../secgloss/c-gly.md)

1.  Empfang anfordern.

    Die [*Zertifikatanforderung*](../secgloss/c-gly.md) wird vom Client an eine zwischengeschaltete Anwendung gesendet, die sie in eine PKCS 10-Formatanforderung formatiert und an die \# Server-Engine übermittelt.

2.  Anfordern der Genehmigung.

    Die Server-Engine ruft das [Richtlinienmodul auf,](policy-modules.md)das Anforderungseigenschaften abfragt, entscheidet, ob die Anforderung autorisiert ist, und legt optionale Zertifikateigenschaften fest.

3.  Zertifikatsbildung.

    Wenn die Anforderung genehmigt wird, nimmt die Server-Engine die Anforderung und alle vom Richtlinienmodul angeforderten Eigenschaften an und erstellt ein vollständiges Zertifikat.

4.  Zertifikatveröffentlichung.

    Die Server-Engine speichert das abgeschlossene Zertifikat in der Zertifikatdienste-Datenbank und benachrichtigt die Zwischenanwendung über den Anforderungsstatus. Wenn das [Exitmodul dies](exit-modules.md) angefordert hat, benachrichtigt die Server-Engine es über ein Zertifikatausstellungsereignis. Dadurch kann das Exitmodul weitere Vorgänge ausführen, z. B. das Veröffentlichen des Zertifikats in einem externen Zertifikatrepository (z. B. einem Verzeichnisdienst). In der Zwischenzeit ruft der Vermittler das veröffentlichte Zertifikat von den Zertifikatdiensten ab und übergibt es an den Client.

Die folgende Abbildung zeigt, wie [*eine Zertifikatanforderung*](../secgloss/c-gly.md) von Den Zertifikatdiensten verarbeitet wird.

![Verarbeiten einer Zertifikatanforderung](images/certflow.png)

 

 
