---
title: Nutzung von Messungsinhalten
description: Nutzung von Messungsinhalten
ms.assetid: f87b5d95-a497-4356-817f-49ac3819df08
keywords:
- Windows Medien Geräte-Manager, Nutzung von Messungsinhalten
- Geräte-Manager, Nutzung von Verbrauchsinhalten
- Programmierhandbuch,Messung der Inhaltsnutzung
- Desktopanwendungen, Nutzung von Verbrauchsinhalten
- Erstellen Windows Media Geräte-Manager-Anwendungen, Messung der Inhaltsnutzung
- Nutzung von Messungsinhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029bae2bcdd69f9dc58c4a64317f974538c672b1d27597fbdc1915074aff0278
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957200"
---
# <a name="metering-content-usage"></a>Nutzung von Messungsinhalten

Mit Windows Media 10-Technologie können Sie jetzt die Inhaltsnutzung auf einem portablen Gerät gemessen werden. Wenn eine Windows Media 10-Lizenz die Messung zulässt, kann das Gerät die Anzahl der Wiedergaben für Titel speichern und die Nutzung über das Internet an den Lizenzaussteller hochladen. Mit diesem System können Inhaltsanbieter ihre Lizenzgebühren anpassen, indem sie die Nutzung von Inhalten genau messen.

Zur Messung des Inhalts muss die Anwendung über ein Messungszertifikat verfügen, das von einem Lizenzierungsdienst bereitgestellt wird, der auf dem Windows Media Rights Manager 10 SDK basiert. Nur Inhalte, die von diesem Dienst lizenziert wurden, können gemessen werden. Weitere Informationen zur Funktionsweise der Messung und zum Erstellen eines Lizenzmessungsdiensts finden Sie in der [Dokumentation Windows Media Rights Manager SDK](/previous-versions/ms986509(v=msdn.10)) auf MSDN. Sie können das SDK abrufen, indem Sie die erforderlichen Informationen auf der [Seite Windows Medienlizenzierung](https://www.microsoft.com/licensing/default)ausfüllen.

Für eine Anwendung kann eine Messung integriert sein, oder Sie können ein COM-Plug-In für eine vorhandene Anwendung erstellen, z. B. die Windows Media Player, wenn die Anwendung Messungs-Plug-Ins akzeptiert.

Eine Anwendung sollte Benutzer warnen, wenn die Nutzung von Inhalten gemessen wird. Weitere Informationen finden Sie auf den Microsoft-Webseiten, die in den Datenschutzbestimmungen aufgeführt [sind.](privacy-statement.md)

Das Abrufen von Messungsdaten von einem Gerät kann langsam sein. Wenn eine Anwendung die Nutzung misst, sollte sie dies daher häufig tun, um zu verhindern, dass sich große Datenmengen auf dem Gerät ansammeln und die Datenübertragung verlangsamen. Um Datenübertragungen zu verhindern, die zu langsam wären, können Gerätehersteller Teilmengen der verfügbaren Messungsdaten senden. Die Anwendung sollte die von [**IWMDRMDeviceApp::P rocessMeterResponse**](iwmdrmdeviceapp-processmeterresponse.md) abgerufenen Flags überwachen, um festzustellen, ob weitere Messungsdaten auf dem Gerät verbleiben.

Die folgenden Schritte zeigen, wie eine Anwendung die Inhaltsnutzung gemessen werden kann.

1.  Da die Messung nur auf Geräten verfügbar ist, die Windows Media DRM 10 für portable Geräte unterstützen, sollte Ihre Anwendung zu einem bestimmten Zeitpunkt **QueryDeviceStatus** aufrufen, wie unter [Behandeln geschützter Inhalte in der Anwendung](handling-protected-content-in-the-application.md)beschrieben, um sicherzustellen, dass das Gerät gültig und auf dem neuesten Stand ist.
2.  Fordern Sie Messungsinformationen vom Gerät an, indem [**Sie IWMDRMDeviceApp::GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md)aufrufen.
3.  Senden Sie die abgerufenen Messungsdaten an den Messungsdienst unter der URL, die von **GenerateMeterChallenge** abgerufen wurde. Das Format der an den Dienst gesendeten Daten hängt von der Skripterstellung für den jeweiligen Dienst ab. Einige Dienste erfordern beispielsweise die Daten, die als POST-Befehl als Name-Wert-Paar gesendet werden. Der Dienstanbieter sollte Sie über seine speziellen Formatierungsanforderungen informieren.
4.  Rufen Sie eine Antwort vom Messungsdienst ab, und senden Sie sie an das Gerät, indem [**Sie IWMDRMDeviceApp::P rocessMeterResponse**](iwmdrmdeviceapp-processmeterresponse.md)aufrufen. Dadurch setzt das Gerät die Anzahl der Wiedergaben zurück und gibt auch einen Wert zurück, der angibt, ob mehr Messdaten auf dem Gerät vorhanden sind, die durch erneuten Aufruf von **GenerateMeterChallenge** abgerufen werden sollen.

Ausführliche Informationen und Beispielcode für die Messung finden Sie auf der [Windows Media-Website.](/previous-versions//bb614723(v=vs.85))

 

 