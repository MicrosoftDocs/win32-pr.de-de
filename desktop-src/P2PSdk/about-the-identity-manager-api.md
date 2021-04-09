---
description: Die Peer Identity Manager-API ermöglicht es Ihnen, Peer Identitäten in einer Peer Anwendung zu erstellen, aufzulisten und zu bearbeiten.
ms.assetid: c1b2a587-71c7-4623-a318-4624dad7feba
title: Informationen zu Identity Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfe66e21bf6c131006ed98c7f5f211c316464ebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865175"
---
# <a name="about-identity-manager"></a>Informationen zu Identity Manager

Die Peer Identity Manager-API ermöglicht es Ihnen, Peer Identitäten in einer Peer Anwendung zu erstellen, aufzulisten und zu bearbeiten. Sie können die mit dieser API erstellten Peer Identitäten als Eingabe für die Peer Gruppierung und die PNRP-Namespace Anbieter-APIs (Peer Name Resolution Protocol) verwenden.

## <a name="peer-identity-manager-best-practices"></a>Bewährte Methoden für Peer Identity Manager

Jeder Benutzer sollte über einige Peer Identitäten verfügen, die für die Peer Aktivitäten verwendet werden können. Beispielsweise kann ein Benutzer über zwei Peer Identitäten für Arbeit und Freizeit verfügen.

Eine gut entworfene Peer Anwendung ermöglicht es Benutzern, eine zu verwendende Peer Identität auszuwählen. Ein Benutzer kann eine neue Peer Identität erstellen, wenn keine der vorhandenen Peer Identitäten für die Verwendung mit einer Anwendung geeignet ist.

Eine gut entworfene Peer Anwendung steuert außerdem die Anzahl der von ihr erstellten Identitäten. Wenn eine Anwendung eine temporäre Peer Identität erstellt, muss die Anwendung die Peer Identität löschen, wenn die Identität nicht benötigt wird. Wenn eine Anwendung diese Wartung nicht durchführt, kann der Peer Identity Manager möglicherweise keine Peer Identitäten erstellen, bis einige Peer Identitäten entfernt wurden.

 

 



