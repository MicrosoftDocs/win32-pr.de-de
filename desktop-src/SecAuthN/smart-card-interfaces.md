---
description: Eine smartcardschnittstelle besteht aus einem vordefinierten Satz von Diensten, die auf einer Smartcard verfügbar sind, den Protokollen, die zum Aufrufen der Dienste erforderlich sind, und Annahmen über den Kontext der Dienste.
ms.assetid: 4f9c13da-8fe3-43e7-875f-04850495edf3
title: Smartcardschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5f11f619e69cafa484e209c3346357aa5a031d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758389"
---
# <a name="smart-card-interfaces"></a>Smartcardschnittstellen

Eine [*smartcardschnittstelle*](../secgloss/s-gly.md) besteht aus einem vordefinierten Satz von Diensten, die auf einer *Smartcard* verfügbar sind, den Protokollen, die zum Aufrufen der Dienste erforderlich sind, und Annahmen über den Kontext der Dienste.

In Bezug auf Smartcards ähnelt der Begriff "Interface" der Art und Weise, wie er in com verwendet wird, was wiederum dem Konzept des ISO 7816/5-Anwendungs Bezeichners ähnlich ist, jedoch mit einem anderen Bereich.

Jede Smartcard-Schnittstelle wird durch eine GUID identifiziert. Beispielsweise kann eine Schnittstelle definiert werden, die dem Inhaber Biorhythmus Informationen bereitstellt. Wenn dieser Dienst von einer bestimmten Smartcard unterstützt wird, kann dieser Anspruch darauf beanspruchen, diese Schnittstellen-GUID zu unterstützen. Mithilfe der Schnittstellen-GUIDs kann eine Anwendung nach einem bestimmten Satz von Schnittstellen suchen, um eine beliebige Karte zu suchen, die diese Gruppe unterstützt, um eine Aufgabe abzuschließen.

Obwohl eine Schnittstelle über eine GUID verfügt, kann Sie auf unterschiedlichen Karten anders implementiert werden. Die oben erwähnte Biorhythm-Schnittstelle kann z. b. über mehrere verschiedene Implementierungen verfügen, aber auf alle wird mit derselben GUID verwiesen. Durch die verschiedenen Implementierungen wird die Interaktion zwischen der Anwendung und der Smartcard nicht geändert. die Interaktion zwischen dem [*Dienstanbieter*](../secgloss/c-gly.md) und den Smartcards kann jedoch abhängig von der Implementierung der Schnittstelle abweichen.

Der Satz von Schnittstellen, die von einer Smartcard unterstützt werden, wird während der Einführung in die Smartcard definiert (Weitere Informationen finden [Sie unter Einführung in Smartcards](introducing-smart-cards-to-the-system.md)

 

 
