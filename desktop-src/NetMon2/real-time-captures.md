---
description: Monitore empfangen erfasste Netzwerk Frames im Echtzeitmodus. Die Frames werden von einem Netzwerk Paketanbieter (NPP) mithilfe der-Schnittstelle "untc-com-Schnittstelle" erfasst und an den Monitor in einem der Monitore mit zwei Ausführungsthreads übermittelt.
ms.assetid: 50aa9da2-3a8a-4514-9b1b-9c8364d074d0
title: Real-Time Erfassungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24bdf5bc451173a98d1c4428674d308f8b3b8d79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869032"
---
# <a name="real-time-captures"></a>Real-Time Erfassungen

Monitore empfangen erfasste Netzwerk Frames im Echtzeitmodus. Die Frames werden von einem [*Netzwerk Paketanbieter*](n.md) (NPP) mithilfe der-Schnittstelle des Anbieters " [untc](irtc.md) -com" aufgezeichnet und an den Monitor in einem der zwei Ausführungsthreads des Monitors übermittelt.

Monitore können die Anzahl der zu verarbeitenden Rahmen beschränken, indem Sie einen [*Erfassungs Filter*](c.md) an den NPP übergeben, der die Frames bereitstellt. In der Regel ist ein bestimmter Monitor auf bestimmte Arten von Datenverkehr, z. b. http, RIPX oder SMB, ausgelegt. Im Unterschied zu Experten, die anspruchsvolle Parser verwenden, um die zu analysierenden Informationen auszuwählen, muss ein Monitor jeden Frame auf die für die Erkennung vorgesehenen Bedingungen untersuchen. Der Grund für diese Frame-für-Frame-Methode ist die Leistung. Ein Monitor muss seine Rahmen schnell genug verarbeiten, damit er nicht hinter den Treiber fällt, der die Frames an den NPP liefert. Andernfalls gehen Daten verloren.

 

 



