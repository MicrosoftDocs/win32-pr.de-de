---
title: VCM-Architektur
description: VCM-Architektur
ms.assetid: cb0b036d-b8b1-4611-965f-08f932dbddb7
keywords:
- Video für Windows (Vfw), VCM-Architektur
- VFW (Video für Windows), VCM-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89b672c86053086f63127aae586517fac4906326
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310568"
---
# <a name="vcm-architecture"></a>VCM-Architektur

VCM ist ein Vermittler zwischen einer Anwendung und Komprimierungs-und Komprimierungs Treibern. Die Komprimierungs-und die Komprimierungs Treiber komprimieren und decokomprimieren einzelne Datenrahmen.

Wenn eine Anwendung VCM aufruft, übersetzt VCM den-Rückruf in eine-Nachricht. Die Nachricht wird mithilfe der [**icsendmessage**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) -Funktion an den entsprechenden Kompressor oder Dekompressor gesendet, der die Daten komprimiert oder dekomprimiert. VCM empfängt den Rückgabewert des Komprimierungs-oder Entkomprimierungs Treibers und gibt dann die Steuerung an die Anwendung zurück.

Wenn für eine Nachricht ein Makro definiert ist, wird das Makro zu einem **icsendmessage** -Funktions aufrufswert erweitert, der entsprechende Parameter für diese Nachricht bereitstellt. Wenn für eine Nachricht ein Makro definiert ist, sollte Sie von Ihrer Anwendung anstelle der Nachricht verwendet werden. In dieser Übersicht folgen diese Makros Nachrichten in Klammern.

 

 




