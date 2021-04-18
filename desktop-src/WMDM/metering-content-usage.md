---
title: Verwendung von Messungs Inhalten
description: Verwendung von Messungs Inhalten
ms.assetid: f87b5d95-a497-4356-817f-49ac3819df08
keywords:
- Windows Media Device Manager, Verwendung von Messungs Inhalten
- Device Manager, Verwendung von Messungs Inhalten
- Programmier Handbuch, Verwendung von Messungs Inhalten
- Desktop Anwendungen, Verwendung von Messungs Inhalten
- Erstellen von Windows Media Device Manager-Anwendungen, Verwendung von Messungs Inhalten
- Verwendung von Messungs Inhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 649eee810e7bbdbc2ea93a32c6368ec345fa7364
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "106337881"
---
# <a name="metering-content-usage"></a>Verwendung von Messungs Inhalten

Mit der Windows Media 10-Technologie können Sie nun die Inhalts Verwendung auf einem tragbaren Gerät messen. Wenn eine Windows Media 10-Lizenz eine Messung zulässt, kann das Gerät die Wiedergabe Anzahl für Lieder speichern und die Nutzung über das Internet wieder in den Lizenz Aussteller hochladen. Mit diesem System können Inhaltsanbieter Ihre Lizenzgebühren anpassen, indem Sie die Inhalts Verwendung genau messen.

Zum Messen von Inhalten muss die Anwendung über ein Messungs Zertifikat verfügen, das von einem Lizenzierungs Dienst bereitgestellt wird, der auf dem Windows Media Rights Manager 10 SDK erstellt wurde. Nur Inhalt, der durch denselben Dienst lizenziert ist, kann gemessen werden. Weitere Informationen zur Funktionsweise der Messung und zum Erstellen eines Lizenz Messungs Dienstanbieter finden Sie in der [Dokumentation zum Windows Media Rights Manager SDK](/previous-versions/ms986509(v=msdn.10)) auf MSDN. Das SDK kann abgerufen werden, indem Sie die erforderlichen Informationen auf der [Seite Windows Media-Lizenzierung](https://www.microsoft.com/licensing/default)ausfüllen.

In einer Anwendung kann eine Messung erstellt werden, oder Sie können ein com-Plug-in für eine vorhandene Anwendung erstellen, z. b. die Windows-Media Player, wenn die Anwendung Messungs-Plug-ins akzeptiert.

Eine Anwendung sollte Benutzer warnen, wenn die Nutzung von Inhalten gemessen wird. Weitere Informationen finden Sie in den Microsoft-Webseiten, die in der [Datenschutzerklärung](privacy-statement.md)aufgeführt sind.

Das Abrufen von Messungs Daten von einem Gerät kann langsam sein. Wenn eine Anwendungs Verbrauchseinheiten verwendet werden, sollten Sie dies häufig tun, um zu verhindern, dass sich große Datenmengen auf dem Gerät anhäufen und die Datenübertragung verlangsamt. Um Datenübertragungen zu vermeiden, die zu langsam sind, können Gerätehersteller Teilmengen verfügbarer Messungs Daten senden. Die Anwendung sollte die von [**iwmdrmdeviceapp abgerufenen Flags überwachen::P rocessmeterresponse**](iwmdrmdeviceapp-processmeterresponse.md) , um festzustellen, ob weitere Messungs Daten auf dem Gerät verbleiben.

Die folgenden Schritte zeigen, wie eine Anwendung die Inhalts Verwendung messen kann.

1.  Da die Messung nur auf Geräten verfügbar ist, die Windows Media DRM 10 für tragbare Geräte unterstützen, sollte Ihre Anwendung zu einem bestimmten Zeitpunkt **querydevicestatus** abrufen, wie in [behandeln geschützter Inhalte in der Anwendung](handling-protected-content-in-the-application.md)beschrieben, um sicherzustellen, dass das Gerät gültig und auf dem neuesten Stand ist.
2.  Anfordern von Messungs Informationen vom Gerät durch Aufrufen von [**iwmdrmdeviceapp:: generatemeterchallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).
3.  Senden Sie die abgerufenen Messungs Daten an den Messungs Dienst unter der URL, die von **generatemeterchallenge** abgerufen wurde. Das Format der Daten, die an den Dienst gesendet werden, hängt von der Skripterstellung für den jeweiligen Dienst ab. Beispielsweise erfordern einige Dienste möglicherweise, dass die Daten als Post-Befehl als Name/Wert-Paar gesendet werden. Der Dienstanbieter sollte Ihnen Ihre speziellen Formatierungs Anforderungen mitteilen.
4.  Rufen Sie eine Antwort vom Messungs Dienst ab, und senden Sie Sie durch Aufrufen von [**iwmdrmdeviceapp::P rocessmeterresponse**](iwmdrmdeviceapp-processmeterresponse.md)an das Gerät. Dies bewirkt, dass das Gerät die Wiedergabe Anzahl zurücksetzt und außerdem einen Wert zurückgibt, der angibt, ob auf dem Gerät, das durch Aufrufen von **generatemeterchallenge** abgerufen werden soll, mehr Messungs Daten vorhanden sind.

Ausführliche Informationen und Beispielcode für die Messung finden Sie auf der [Windows Media](/previous-versions//bb614723(v=vs.85))-Website.

 

 