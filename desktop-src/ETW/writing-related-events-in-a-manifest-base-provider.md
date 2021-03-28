---
description: Verwenden Sie die EventWrite-Funktion, wenn mehrere Komponenten Ihre Ereignisse in einem End-to-End-Ablauf Verfolgungs Szenario miteinander verknüpfen möchten.
ms.assetid: 715e3161-d85a-45c0-84df-c6c360b266a1
title: Schreiben verwandter Ereignisse in einem Manifest-basierten Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb9508996503f53c738d62fac32905919a8c73ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527281"
---
# <a name="writing-related-events-in-a-manifest-based-provider"></a>Schreiben verwandter Ereignisse in einem Manifest-basierten Anbieter

Verwenden Sie die [**EventWrite**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) -Funktion, wenn mehrere Komponenten Ihre Ereignisse in einem End-to-End-Ablauf Verfolgungs Szenario miteinander verknüpfen möchten. Die Komponenten A, B und C arbeiten z. b. für eine verwandte Aktivität und möchten alle Ereignisse verknüpfen, die mit dieser Aktivität verknüpft sind.

Etw verwendet den lokalen Thread Speicher, um den Aktivitäts Bezeichner der vorherigen Komponente für die nächste Komponente verfügbar zu machen. Die Komponente ruft den Bezeichner der vorherigen Komponente aus dem lokalen Speicher ab und legt den zugehörigen Aktivitäts Bezeichner darauf fest. Der Consumer kann dann den zugehörigen Aktivitäts Bezeichner verwenden, um die Kette der Ereignisse von einer Komponente zum nächsten zu durchlaufen.

 

 



