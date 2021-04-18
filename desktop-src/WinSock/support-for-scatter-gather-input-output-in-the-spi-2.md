---
description: Die Routinen "wspsend", "wspsendto", "wsprecv" und "wsprecvfrom" verwenden alle ein Array von Client puffern als Eingabeparameter und können daher für die e/a-Vorgänge vom Typ "Scatter/Gather" (oder "Vector")
ms.assetid: ecd3d2f1-74b1-42f7-8402-3170112e3aca
title: Unterstützung für die Scatter/Gather-Eingabe/-Ausgabe in der SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3f32e016c5c2e9f990c334716d4177d477c50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357493"
---
# <a name="support-for-scattergather-inputoutput-in-the-spi"></a>Unterstützung für die Scatter/Gather-Eingabe/-Ausgabe in der SPI

Die Routinen " [**wspsend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85))", " [**wspsendto**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85))", " [**wsprecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))" und " [**wsprecvfrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) " verwenden alle ein Array von Client puffern als Eingabeparameter und können daher für die e/a-Vorgänge vom Typ "Scatter/Gather" (oder "Vector") Dies kann in Fällen sehr nützlich sein, in denen Teile jeder übermittelten Nachricht zusätzlich zu einem Nachrichtentext aus einer oder mehreren Header Komponenten fester Länge bestehen. Diese Header Komponenten müssen vor dem Senden nicht in einem einzelnen zusammenhängenden Puffer verkettet werden. Beim Empfang können die Header Komponenten auch automatisch in separate Puffer aufgeteilt werden, sodass der Nachrichtentext rein bleibt.

Durch die Verwendung von Listen mit Puffern anstelle eines einzelnen Puffers werden die für Empfangs Vorgänge geltenden Grenzen nicht geändert. Bei Nachrichten orientierten Protokollen wird ein Empfangsvorgang abgeschlossen, wenn eine einzelne Nachricht empfangen wurde, unabhängig davon, wie viele oder wenige der angegebenen Puffer verwendet wurden. Ebenso wird bei streamorientierten Protokollen ein Empfang abgeschlossen, wenn eine nicht angegebene bytemenge über das Netzwerk eingeht, nicht notwendigerweise, wenn alle angegebenen Puffer voll sind.

 

 
