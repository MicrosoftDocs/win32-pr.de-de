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
ms.openlocfilehash: 6d4a7a6bc8da314cc5cb891846e46289396fefb6be60d92ddd38f17ab1aff0ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119783429"
---
# <a name="mciavi"></a>MCIAVI

Eine AVI-Datei kann mehr als zwei Streams enthalten, z. B. eine Videosequenz, einen englischen Und einen französischen Ausschnitt. Ihre Anwendung kann einen Stream unabhängig von den anderen Streams in der Datei verwenden.

Der **Gerätetyp digitalvideo** steuert Videodateien. Eine Liste der MCI-Befehle, die von Digital-Video-Geräten erkannt werden, finden Sie unter [Digital-Video-Befehlssatz.](digital-video-command-set.md)

Der MCIAVI-Treiber gibt Videosequenzen und andere Datenströme unter der Kontrolle von MCI-Befehlen wieder. Datenströme können Bilder, Audio und Paletten enthalten. Die Bilddaten können aus Bildern mit Farbpaletten oder Informationen zu richtigen Farben bestehen.

Audiodaten werden mit dem Video innerhalb einer Sekunde synchronisiert. Wenn keine Audiohardware verfügbar ist, gibt der Treiber jedoch nur den Videostream wieder. Der MCIAVI-Treiber kann bei Bedarf Videoframes löschen, um einen Stream ohne Audiounterbrechung wiederzuspielen.

Ihre Anwendung kann die Klassendienste des MCIWnd-Fensters anstelle der MCI-Befehlsschnittstelle verwenden, um einen beliebigen MCI-Treiber zu steuern. Diese Fensterklasse verarbeitet viele Details der Verwaltung des Fensters, das das MCI-Gerät unterstützt, und vereinfacht die Programmierung, die zum Senden der MCI-Befehle erforderlich ist. Ihre Anwendung kann die MCIWnd-Bibliotheksdienste direkt verwenden, um das MCI-Gerät zu steuern, oder MCIWnd kann eine Symbolleiste, eine Scrollleiste und Menüs anzeigen lassen, mit denen der Benutzer das Gerät steuern kann. Weitere Informationen zur MCIWnd-Fensterklasse finden Sie unter [MCIWnd-Fensterklasse.](mciwnd-window-class.md)

 

 




