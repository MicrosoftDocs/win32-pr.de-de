---
description: Wenn ein Thread aktiv mit einem Windows-Abbild Erfassungsgerät (WIA) kommuniziert (z. b. das Übertragen von Daten oder das Schreiben von Geräteeigenschaften), sperrt WIA &\# 0034; sperrt&\# 0034; das Gerät.
ms.assetid: 59533937-284a-4732-a73b-d2e0b5a9a370
title: Kommunizieren mit einem WIA-Gerät in mehreren Threads oder Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7a4b518093c3a0fc09534d67e22e5349d44d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216055"
---
# <a name="communicating-with-a-wia-device-in-multiple-threads-or-applications"></a>Kommunizieren mit einem WIA-Gerät in mehreren Threads oder Anwendungen

Wenn ein Thread aktiv mit einem WIA-Gerät (Windows Image Acquisition) kommuniziert (z. b. das Übertragen von Daten oder das Schreiben von Geräteeigenschaften), wird das Gerät durch einen "Sperren" gesperrt. Wenn ein Gerät gesperrt ist, können keine anderen Threads oder Prozesse aktiv mit dem Gerät kommunizieren.

WIA lässt nicht zu, dass mehrere Threads oder Prozesse Verbindungen mit einem einzelnen Gerät aufrechterhalten. Das heißt, dass ein Gerät nur während der eigentlichen Kommunikation gesperrt ist und zwei oder mehr Anwendungen gleichzeitig ein einzelnes Gerät auswählen können.

WIA erstellt immer dann eine separate Elementstruktur, wenn ein Thread oder eine Anwendung [**iwiadevmgr:: foratedevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) oder [**IWiaDevMgr2:: foratedevice**](-wia-iwiadevmgr2-createdevice.md) aufruft, um eine Instanz dieses Geräts zu erstellen. WIA verwaltet separate Zustandsinformationen für jede Elementstruktur. Wenn ein Thread z. b. zwei Instanzen eines bestimmten Scanners erstellt, kann er verschiedene Scanauflösungen für die beiden Instanzen festlegen. Wenn [**iwiadatatransfer:: idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) für eine bestimmte Instanz aufgerufen wird, lädt WIA die Eigenschaften, die dieser Instanz zugeordnet sind, dem Gerät, bevor die tatsächliche Überprüfung erfolgt. Dies wirkt sich nicht auf den Status der anderen Instanz des Geräts aus.

Wenn für einen Thread zurzeit ein Gerät gesperrt ist (es wird aktiv mit diesem Gerät kommuniziert) und ein anderer Thread versucht, eine Methode aufzurufen, die aktiv mit dem Gerät kommuniziert, gibt die Methode einen Fehler aufgrund eines WIA- \_ Fehlers zurück \_ .

Das Lesen und Schreiben von Geräteeigenschaften dauert in der Regel so wenig Zeit, dass diese Vorgänge selten zu Konflikten führen. Das Übertragen von Daten dauert jedoch in der Regel länger und ist daher wahrscheinlicher, dass Geräte Zugriffs Konflikte entstehen. Es handelt sich um eine solide Programmierung, um langwierige Geräte Vorgänge (Datenübertragungen) gleichzeitig in separaten Threads innerhalb einer Anwendung zu vermeiden.

Eine Anwendung sollte niemals davon ausgehen, dass es sich um die einzige Anwendung handelt, die beim Start mit einem WIA-Gerät kommuniziert.

 

 



