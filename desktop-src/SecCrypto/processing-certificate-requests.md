---
description: Erläutert, wie Zertifikat Dienste Zertifikat Anforderungen verarbeiten.
ms.assetid: 40641167-12de-4008-80e4-2fb758146421
title: Verarbeiten von Zertifikat Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70a25d9ca633247c3995677825dc011b2b38d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104561427"
---
# <a name="processing-certificate-requests"></a>Verarbeiten von Zertifikat Anforderungen

Die Zertifikat Dienste führen die folgenden Schritte aus, wenn eine [*Zertifikat Anforderung*](../secgloss/c-gly.md)verarbeitet wird:

1.  Anforderungs Empfang.

    Die [*Zertifikat Anforderung*](../secgloss/c-gly.md) wird vom Client an eine Vermittler Anwendung gesendet, die Sie in eine PKCS \# 10-Format Anforderung formatiert und an die Server-Engine übermittelt.

2.  Genehmigung anfordern.

    Die Server-Engine Ruft das- [Richtlinien Modul](policy-modules.md)auf, das Anforderungs Eigenschaften abfragt, entscheidet, ob die Anforderung autorisiert ist oder nicht, und legt optionale Zertifikat Eigenschaften fest.

3.  Zertifikats Bildung.

    Wenn die Anforderung genehmigt ist, übernimmt die Server-Engine die Anforderung und alle Eigenschaften, die vom Richtlinien Modul angefordert werden, und erstellt ein umfassendes Zertifikat.

4.  Zertifikat Veröffentlichung.

    Die Server-Engine speichert das abgeschlossene Zertifikat in der Datenbank der Zertifikat Dienste und benachrichtigt die Vermittler Anwendung über den Anforderungs Status. Wenn das Beendigungs [Modul](exit-modules.md) dies angefordert hat, wird es vom Servermodul über ein Zertifikat Ausstellungs Ereignis benachrichtigt. Dadurch kann das Beendigungs Modul weitere Vorgänge ausführen, wie z. b. das Veröffentlichen des Zertifikats in einem externen zertifikatrepository (z. b. einem Verzeichnisdienst). Zwischenzeitlich erhält der Vermittler das veröffentlichte Zertifikat von den Zertifikat Diensten und übergibt es an den Client.

In der folgenden Abbildung wird gezeigt, wie eine [*Zertifikat Anforderung*](../secgloss/c-gly.md) von Zertifikat Diensten verarbeitet wird.

![Verarbeiten einer Zertifikat Anforderung](images/certflow.png)

 

 
