---
title: Abschluss Benachrichtigungen
description: Der RAS-Verbindungs-Manager setzt Status Benachrichtigungen fort, bis der Verbindungsvorgang abgeschlossen ist.
ms.assetid: 2c3b0d03-1cb7-4fa4-a7fa-bcfe623b791f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b949eb7dcc0f09d05d2fb272f4f3d36da40fac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037003"
---
# <a name="completion-notifications"></a>Abschluss Benachrichtigungen

Der RAS-Verbindungs-Manager setzt Status Benachrichtigungen fort, bis der Verbindungsvorgang abgeschlossen ist. Dies tritt in den folgenden Situationen auf:

-   Der Handler empfängt eine mit rascs \_ verbundene oder mit rascs \_ getrennte Benachrichtigung. Die RAS-Client Anwendung kann beendet werden, ohne dass eine bestehende Verbindung unterbrochen wird.
-   Ein Fehler tritt auf. Der Handler empfängt eine Benachrichtigung, die den Fehler und den Verbindungsstatus angibt, als der Fehler aufgetreten ist. Die RAS-Client Anwendung kann beendet werden.

Die RAS-Client Anwendung sollte nicht annehmen, dass der Verbindungsvorgang nach dem Aufrufen von [**rashangup**](/windows/desktop/api/Ras/nf-ras-rashangupa)beendet wurde. Vor dem beenden sollte eine der oben genannten Bedingungen gewartet werden.

 

 




