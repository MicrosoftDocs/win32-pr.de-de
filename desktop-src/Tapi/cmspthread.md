---
description: Die cmspthread-Klasse implementiert den MSPs-Arbeits Thread.
ms.assetid: 9dc2373a-cdcf-4e60-95fa-56cb68bda15b
title: Cmspthread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a12b71668e81688b5de7f41e188a51b88944d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369013"
---
# <a name="cmspthread"></a>Cmspthread

Die **cmspthread** -Klasse implementiert den MSP-Arbeits Thread. Die Basisklassen verwenden diesen Arbeits Thread für eine Reihe von Zwecken. Ein generischer und schlanker Arbeits Element Mechanismus wird bereitgestellt, damit der abgeleitete MSP diesen Thread für seine eigenen synchronen oder asynchronen Arbeitsaufgaben verwenden kann, was Sie möglicherweise tun. Der Thread pumpt auch Nachrichten und unterstützt die Verarbeitung von APCs (obwohl APCs nicht in den Basisklassen verwendet werden).

Wenn mehrere like-Adressen vorhanden sind (d. h., wenn dieselbe MSP-Implementierung aus derselben DLL mehrmals instanziiert wird), stellt die Thread Klasse die Skalierbarkeit sicher, indem automatisch ein einzelner Thread für alle Adressen verwendet wird. Die Schnittstelle zur Thread Klasse besteht darin, dass die MSP-Implementierung die Thread Klasse als privaten Thread vorstellen kann und die anderen Adressen, die Sie möglicherweise freigeben, nicht wichtig sind.

Definiert in "mspthrd. h".

 

 



