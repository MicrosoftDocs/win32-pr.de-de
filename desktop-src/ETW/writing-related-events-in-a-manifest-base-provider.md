---
description: Verwenden Sie die EventWriteTransfer-Funktion, wenn mehrere Komponenten ihre Ereignisse in einem End-to-End-Ablaufverfolgungsszenario in Beziehung setzen möchten.
ms.assetid: 715e3161-d85a-45c0-84df-c6c360b266a1
title: Schreiben verwandter Ereignisse in einem manifestbasierten Anbieter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7f6d09e7e95617b662c3530497b199925921ef9abfd4f3825a5ac799886f95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015208"
---
# <a name="writing-related-events-in-a-manifest-based-provider"></a>Schreiben verwandter Ereignisse in einem manifestbasierten Anbieter

Verwenden Sie die [**EventWriteTransfer-Funktion,**](/windows/desktop/api/Evntprov/nf-evntprov-eventwritetransfer) wenn mehrere Komponenten ihre Ereignisse in einem End-to-End-Ablaufverfolgungsszenario in Beziehung setzen möchten. Beispielsweise führen die Komponenten A, B und C Arbeiten an einer verwandten Aktivität aus und möchten alle Ereignisse im Zusammenhang mit dieser Aktivität verknüpfen.

ETW verwendet lokalen Threadspeicher, um den Aktivitätsbezeichner der vorherigen Komponente für die nächste Komponente verfügbar zu machen. Die Komponente ruft den Bezeichner der vorherigen Komponente aus dem lokalen Speicher ab und legt den zugehörigen Aktivitätsbezeichner darauf fest. Der Consumer kann dann den zugehörigen Aktivitätsbezeichner verwenden, um die Kette der Ereignisse von einer Komponente zur nächsten zu durchgehen.

 

 



