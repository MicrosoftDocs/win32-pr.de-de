---
description: Eine Smartcardschnittstelle besteht aus einem vordefinierten Satz von Diensten, die in einer Smartcard verfügbar sind, den Protokollen, die zum Aufrufen der Dienste erforderlich sind, und allen Annahmen in Bezug auf den Kontext der Dienste.
ms.assetid: 4f9c13da-8fe3-43e7-875f-04850495edf3
title: Smartcardschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db3fb5369f36f76e8bf5909afad94959ff70541d9026762234d65ae181b0172
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917769"
---
# <a name="smart-card-interfaces"></a>Smartcardschnittstellen

Eine [*Smartcardschnittstelle*](../secgloss/s-gly.md) besteht aus einem vordefinierten Satz von Diensten, die in einer *Smartcard* verfügbar sind, den Protokollen, die zum Aufrufen der Dienste erforderlich sind, und allen Annahmen in Bezug auf den Kontext der Dienste.

In Bezug auf Smartcards ähnelt der Begriff "Schnittstelle" der Verwendung in COM, was wiederum dem Konzept des ISO 7816/5-Anwendungsbezeichners ähnelt, aber einen anderen Bereich aufwendet.

Jede Smartcardschnittstelle wird durch eine GUID identifiziert. Beispielsweise kann eine Schnittstelle definiert werden, die Biorhythmusinformationen für ihren Besitzer bereitstellt. Wenn eine bestimmte Smartcard diesen Dienst unterstützt, kann sie beanspruchen, diese Schnittstellen-GUID zu unterstützen. Mithilfe der Schnittstellen-GUIDs kann eine Anwendung nach einem bestimmten Satz von Schnittstellen suchen und eine beliebige Karte suchen, die diese Gruppe unterstützt, um eine Aufgabe abzuschließen.

Obwohl eine Schnittstelle über eine GUID verfügt, kann sie auf verschiedenen Karten unterschiedlich implementiert werden. Beispielsweise kann die oben erwähnte Biorhythmusschnittstelle mehrere verschiedene Implementierungen aufweisen, auf die jedoch mit derselben GUID verwiesen wird. Die verschiedenen Implementierungen würden die Interaktion zwischen der Anwendung und der Smartcard nicht ändern. Die Interaktion zwischen dem [*Dienstanbieter*](../secgloss/c-gly.md) und den Smartcards kann sich jedoch je nach Implementierung der Schnittstelle unterscheiden.

Der Satz von Schnittstellen, die von einer Smartcard unterstützt werden, wird während der Einführung in Smartcards definiert (siehe [Einführung von Smartcards in das System](introducing-smart-cards-to-the-system.md)).

 

 
