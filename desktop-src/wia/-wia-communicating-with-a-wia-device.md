---
description: Wenn ein Thread aktiv mit einem WIA-Gerät (Windows Image Acquisition) kommuniziert (z.B. Übertragen von Daten oder Schreiben von Geräteeigenschaften), wia &\# 0034;sperrt&\# 0034; das Gerät.
ms.assetid: 59533937-284a-4732-a73b-d2e0b5a9a370
title: Kommunizieren mit einem WIA-Gerät in mehreren Threads oder Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6f54cc8fe9a3b60d684ff9a62def2c0cf8862576034b16f58d3dd369d2b8be0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118209264"
---
# <a name="communicating-with-a-wia-device-in-multiple-threads-or-applications"></a>Kommunizieren mit einem WIA-Gerät in mehreren Threads oder Anwendungen

Wenn ein Thread aktiv mit einem WIA-Gerät (Windows Image Acquisition) kommuniziert (z. B. Daten übertragen oder Geräteeigenschaften schreiben), "sperrt" WIA das Gerät. Wenn ein Gerät gesperrt ist, können keine anderen Threads oder Prozesse aktiv mit diesem Gerät kommunizieren.

WIA verhindert nicht, dass mehrere Threads oder Prozesse Verbindungen mit einem einzelnen Gerät aufrechterhalten. Das heißt, ein Gerät wird nur während der eigentlichen Kommunikation gesperrt, und für zwei oder mehr Anwendungen kann gleichzeitig ein einzelnes Gerät ausgewählt werden.

WIA erstellt jedes Mal eine separate Elementstruktur, wenn jeder Thread oder jede Anwendung [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) oder [**IWiaDevMgr2::CreateDevice aufruft,**](-wia-iwiadevmgr2-createdevice.md) um eine Instanz dieses Geräts zu erstellen. WIA verwaltet separate Zustandsinformationen für jede Elementstruktur. Wenn ein Thread beispielsweise zwei Instanzen eines bestimmten Scanners erstellt, kann er unterschiedliche Scanauflösungen für die beiden Instanzen festlegen. Wenn [**IWiaDataTransfer::idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) für eine bestimmte Instanz aufgerufen wird, lädt WIA die eigenschaften, die dieser Instanz zugeordnet sind, auf das Gerät, bevor die eigentliche Überprüfung durchgeführt wird. Dies wirkt sich nicht auf den Zustand der anderen Instanz des Geräts aus.

Wenn für einen Thread derzeit ein Gerät gesperrt ist (er kommuniziert aktiv mit diesem Gerät), und ein anderer Thread versucht, eine Methode aufzurufen, die aktiv mit dem Gerät kommuniziert, gibt die Methode einen WIA \_ ERROR \_ BUSY-Fehler zurück.

In der Regel dauert das Lesen und Schreiben von Geräteeigenschaften so wenig Zeit, dass diese Vorgänge selten einen Konflikt verursachen. Die Übertragung von Daten dauert jedoch in der Regel länger und führt daher eher zu Konflikten beim Gerätezugriff. Es ist eine solide Programmierung, um lange Gerätevorgänge (Datenübertragungen) gleichzeitig in separaten Threads innerhalb einer Anwendung zu vermeiden.

Eine Anwendung sollte nie davon ausgehen, dass sie die einzige Anwendung ist, die beim Starten mit einem WIA-Gerät kommuniziert.

 

 



