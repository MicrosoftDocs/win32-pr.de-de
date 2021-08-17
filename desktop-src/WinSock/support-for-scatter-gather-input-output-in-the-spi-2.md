---
description: Die Routinen WSPSend, WSPSendTo, WSPRecv und WSPRecvFrom nehmen alle ein Array von Clientpuffern als Eingabeparameter an und können daher für Punkt-/Gather-E/A-E/A(oder vektorierte) E/A verwendet werden.
ms.assetid: ecd3d2f1-74b1-42f7-8402-3170112e3aca
title: Unterstützung für Scatter/Gather-Eingabe/-Ausgabe in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b136898c1163ab298d8a177238f11239262b04306662b3f11b75bfb847f335d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739997"
---
# <a name="support-for-scattergather-inputoutput-in-the-spi"></a>Unterstützung für Scatter/Gather-Eingabe/-Ausgabe in der SPI

Die [**Routinen WSPSend,**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) [**WSPSendTo,**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))und [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) nehmen alle ein Array von Clientpuffern als Eingabeparameter an und können daher für Punkt-/Gather-E/A-E/A(oder vektorierte) E/A verwendet werden. Dies kann in Fällen sehr nützlich sein, in denen Teile jeder übertragenen Nachricht zusätzlich zu einem Nachrichtentext aus einer oder mehreren Headerkomponenten fester Länge bestehen. Solche Headerkomponenten müssen vor dem Senden nicht zu einem einzelnen zusammenhängenden Puffer verkettet werden. Ebenso können die Headerkomponenten beim Empfang automatisch in separate Puffer aufgeteilt werden, damit der Nachrichtentext rein ist.

Die Verwendung von Pufferlisten anstelle eines einzelnen Puffers ändert nicht die Grenzen, die für Empfangsvorgänge gelten. Bei nachrichtenorientierten Protokollen wird ein Empfangsvorgang immer dann abgeschlossen, wenn eine einzelne Nachricht empfangen wurde, unabhängig davon, wie viele oder wenige der angegebenen Puffer verwendet wurden. Ebenso bei streamorientierten Protokollen wird ein Empfang abgeschlossen, wenn eine nicht angegebene Anzahl von Bytes über das Netzwerk eintrifft, nicht notwendigerweise, wenn alle bereitgestellten Puffer voll sind.

 

 
