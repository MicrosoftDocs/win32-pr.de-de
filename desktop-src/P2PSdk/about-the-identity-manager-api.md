---
description: Mit der Peer Identity Manager-API können Sie Peeridentitäten in einer Peeranwendung erstellen, aufzählen und bearbeiten.
ms.assetid: c1b2a587-71c7-4623-a318-4624dad7feba
title: Informationen zu Identity Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d062f7324bb949c657b7687b533058cb9e74d3102eea1e484284453d3ff7f25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119579920"
---
# <a name="about-identity-manager"></a>Informationen zu Identity Manager

Mit der Peer Identity Manager-API können Sie Peeridentitäten in einer Peeranwendung erstellen, aufzählen und bearbeiten. Sie können die mit dieser API erstellten Peeridentitäten als Eingabe für die Namespaceanbieter-APIs Peer Grouping and Peer Name Resolution Protocol (PNRP) verwenden.

## <a name="peer-identity-manager-best-practices"></a>Bewährte Methoden für Peer Identity Manager

Jeder Benutzer sollte über einige Peeridentitäten verfügen, die er für die Peeraktivitäten verwenden kann. Beispielsweise kann ein Benutzer über zwei Peeridentitäten für Arbeit und Arbeit verfügen.

Mit einer gut entworfenen Peeranwendung kann ein Benutzer eine Peeridentität auswählen, die verwendet werden soll. Ein Benutzer kann eine neue Peeridentität erstellen, wenn keine der vorhandenen Peeridentitäten für die Verwendung mit einer Anwendung geeignet ist.

Eine gut entworfene Peeranwendung steuert auch die Anzahl von Identitäten, die sie erstellt. Wenn eine Anwendung eine temporäre Peeridentität erstellt, muss die Anwendung die Peeridentität löschen, wenn die Identität nicht benötigt wird. Wenn eine Anwendung diese Wartung nicht übernimmt, kann der Peeridentitäts-Manager möglicherweise erst Peeridentitäten erstellen, wenn einige Peeridentitäten entfernt wurden.

 

 



