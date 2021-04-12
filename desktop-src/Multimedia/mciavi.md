---
title: MCIAVI
description: MCIAVI
ms.assetid: 68639f35-bc20-457d-b937-760af8323dce
keywords:
- MCI-Geräte, MCIAVI-Treiber
- MCI-Befehle, MCIAVI-Treiber
- MCIAVI-Treiber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be2e69cf2b0fd9ee71650c56b0d7d9efb50a46e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471469"
---
# <a name="mciavi"></a>MCIAVI

Eine AVI-Datei kann mehr als zwei Streams enthalten – z. b. eine Videosequenz, einen englischen Sound Sound und einen französischen Sound. Die Anwendung kann einen Stream unabhängig von den anderen Datenströmen in der Datei verwenden.

Der **Digitalvideo** -Gerätetyp steuert Videodateien. Eine Liste der von Digital-Video-Geräten erkannten MCI-Befehle finden Sie unter [Digital-Video Command Set](digital-video-command-set.md).

Der MCIAVI-Treiber gibt Videosequenzen und andere Datenströme unter der Kontrolle über MCI-Befehle wieder. Datenströme können Bilder, Audiodaten und Paletten enthalten. Die Bilddaten können aus Bildern mit Farbpaletten oder echten Farbinformationen bestehen.

Audiodaten werden mit dem Video innerhalb von einem Drittel einer Sekunde synchronisiert. Wenn keine Audiohardware verfügbar ist, gibt der Treiber jedoch nur den Videostream aus. Der MCIAVI-Treiber kann bei Bedarf Video Frames ablegen, um einen Stream ohne audiounterbrechung wiederzugeben.

Die Anwendung kann die mciwnd-Fenster Klassen Dienste anstelle der MCI-Befehlsschnittstelle verwenden, um einen beliebigen MCI-Treiber zu steuern. Diese Fenster Klasse behandelt viele der Details der Verwaltung des Fensters, das das MCI-Gerät unterstützt, und vereinfacht die zum Senden der MCI-Befehle erforderliche Programmierung. Die Anwendung kann die mciwnd-Bibliotheksdienste direkt verwenden, um das MCI-Gerät zu steuern. Alternativ kann mciwnd eine Symbolleiste, eine Scrollleiste und Menüs anzeigen, mit denen der Benutzer das Gerät steuern kann. Weitere Informationen zur mciwnd-Fenster Klasse finden Sie unter [mciwnd Window Class](mciwnd-window-class.md).

 

 




