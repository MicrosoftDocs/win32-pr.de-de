---
title: VCM-Architektur
description: VCM-Architektur
ms.assetid: cb0b036d-b8b1-4611-965f-08f932dbddb7
keywords:
- Video für Windows (VFW), VCM-Architektur
- VFW (Video für Windows),VCM-Architektur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7676fe7786b8674ddca957a75c33336294b65a9df18d53fe4b9c7f493092b66f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135598"
---
# <a name="vcm-architecture"></a>VCM-Architektur

VCM ist ein Vermittler zwischen einer Anwendung und Komprimierungs- und Dekomprimierungstreibern. Die Komprimierungs- und Dekomprimierungstreiber komprimieren und dekomprimieren einzelne Frames von Daten.

Wenn eine Anwendung VCM aufruft, übersetzt VCM den Aufruf in eine Nachricht. Die Nachricht wird mithilfe der [**ICSendMessage-Funktion**](/windows/desktop/api/Vfw/nf-vfw-icsendmessage) an den entsprechenden Brillen- oder Dekomprimierer gesendet, der die Daten komprimiert oder dekomprimiert. VCM empfängt den Rückgabewert vom Komprimierungs- oder Dekomprimierungstreiber und gibt dann die Steuerung an die Anwendung zurück.

Wenn ein Makro für eine Nachricht definiert ist, wird das Makro auf einen **ICSendMessage-Funktionsaufruf** erweitert, der entsprechende Parameter für diese Nachricht anweist. Wenn ein Makro für eine Nachricht definiert ist, sollte ihre Anwendung es anstelle der Nachricht verwenden. In dieser Übersicht folgen diese Makros Nachrichten in Klammern.

 

 




