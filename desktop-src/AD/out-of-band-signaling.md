---
title: Out-of-Band-Signalisierung
description: Bei der Zusammenarbeit von Anwendungen, die gemeinsame Daten mit dem Verzeichnis gemeinsam nutzen, kann die Out-of-Band-Signalisierung verwendet werden
ms.assetid: 82960273-5cda-44d2-bc17-d604f34f5a9b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bc630bfdf3a2700ab187cd24bbfc5a52def1103
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036351"
---
# <a name="out-of-band-signaling"></a>Out-of-Band-Signalisierung

Bei der Zusammenarbeit von Anwendungen, die gemeinsame Daten mit dem Verzeichnis gemeinsam nutzen, kann die Out-of-Band-Signalisierung verwendet werden Einfach ausgedrückt: die kooperierenden Anwendungen verwenden einen Mechanismus, der von der Verzeichnisreplikation getrennt ist, um einander über Änderungen in den gemeinsam genutzten allgemeinen Daten zu informieren. Die Out-of-Band-Signalisierung ist am effektivsten, wenn Sie in Kombination mit einem Versionsmechanismus verwendet wird – dies ermöglicht dem Partner, die Änderungen zu erkennen, um Remote Partner zu benachrichtigen, auf welche Version der freigegebenen Daten gewartet werden

Wenn Sie zum RPC-Beispiel zurückkehren, das im Abschnitt "Versions Schiefe" des [Replikations Verhaltens in Active Directory Domain Services](replication-behavior-in-active-directory-domain-services.md)angegeben ist, könnte der RPC-Server einen Rückruf an verbundene Clients durchführen, um Sie über den Umstieg auf einen neuen Server zu informieren: "Ich werde das verschieben. Bitte stellen Sie sich vor, die Replikation bringt Ihnen die neue Adresse in Kürze, damit der Client den Übergangszeitraum verarbeiten kann.

Anwendungen, für die identische Richtlinien erforderlich sind, um miteinander zu kommunizieren, können Out-of-Band-Signalisierung verwenden, um sicherzustellen, dass eine neue Richtlinie erst verwendet wird, wenn Sie von allen beteiligten Parteien empfangen wurde. Wenn beispielsweise die IPSec-Richtlinie (Internet Protocol Security, Internet Protokoll Sicherheit) zwischen zwei Computern geändert wird, kann ein Agent auf dem Quellcomputer einen Agent auf dem Zielcomputer kontaktieren, um die Anwendung der geänderten Richtlinie zu aushandeln, wobei der Quellcomputer die Anwendung verzögert, bis der Zielcomputer ebenfalls die neue Richtlinie empfangen hat.

 

 




