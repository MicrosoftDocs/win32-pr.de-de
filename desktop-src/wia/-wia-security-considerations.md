---
description: Dieses Dokument enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit der Windows-Abbild Beschaffung (WIA).
ms.assetid: 35455320-7d08-49de-938d-40dc0873917b
title: 'Sicherheitsüberlegungen: Windows-Abbild Beschaffung'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9ab080582492a0c03eab7879624bfb49a370e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372831"
---
# <a name="security-considerations-windows-image-acquisition"></a>Sicherheitsüberlegungen: Windows-Abbild Beschaffung

Dieses Dokument enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit der Windows-Abbild Beschaffung (WIA). Dieses Dokument enthält nicht alles, was Sie über Sicherheitsprobleme wissen müssen, sondern als Ausgangspunkt und Verweis für diesen Technologiebereich.

-   [Verwenden von Anführungszeichen um Pfadnamen](#use-quotation-marks-around-path-names)
-   [Platzieren registrierter Anwendungen an sicheren Orten](#place-registered-applications-in-secure-locations)
-   [Verwenden Sie keine zugrunde liegenden Verzeichnisse oder Registrierungsschlüssel.](#do-not-use-underlying-directories-or-registry-keys)
-   [Verwandte Themen](#related-topics)

## <a name="use-quotation-marks-around-path-names"></a>Verwenden von Anführungszeichen um Pfadnamen

Wenn Sie [**iwiadevmgr:: registereventcallbackprogram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) zum Registrieren einer Anwendung für den Empfang von Geräte Ereignissen verwenden, stellen Sie sicher, dass Sie den Pfad und den Dateinamen der Anwendung in Anführungszeichen einschließen. Dadurch wird vermieden, dass der Pfad falsch interpretiert und eine nicht autorisierte Anwendung ausgeführt wird.

## <a name="place-registered-applications-in-secure-locations"></a>Platzieren registrierter Anwendungen an sicheren Orten

Wenn eine Anwendung für den Empfang eines Geräte Ereignisses registriert ist, kann diese Anwendung von jedem Benutzer ausgeführt werden, der Zugriff auf das Gerät hat. Wenn eine Anwendung z. b. für ein Scan Ereignis registriert ist, wird die Anwendung durch Drücken der Schaltfläche "überprüfen" auf einem Scanner ausgeführt. Wenn die Anwendung mit einer höheren Berechtigung als der Benutzer ausgeführt wird, verursacht dies ein potenzielles Sicherheitsproblem.

## <a name="do-not-use-underlying-directories-or-registry-keys"></a>Verwenden Sie keine zugrunde liegenden Verzeichnisse oder Registrierungsschlüssel.

WIA verwendet intern mehrere Verzeichnisse und Registrierungsschlüssel zum Speichern von Daten oder Informationen. Greifen Sie nicht direkt auf diese Verzeichnisse oder Registrierungsschlüssel zu. Verwenden Sie stattdessen die verfügbar gemachten Schnittstellen Methoden, um Verzeichnisse für abgerufene Bilder anzugeben.

## <a name="related-topics"></a>Verwandte Themen

-   [Microsoft Security](https://www.microsoft.com/security/)
-   [MSDN-Bibliotheks Sicherheit (Startseite)](https://msdn.microsoft.com/security/default.aspx)
-   [Gewusst-wie-Ressourcen für die Sicherheit](https://www.microsoft.com/technet/solutionaccelerators/howto/sechow.mspx)
-   [TechNet-Sicherheitsressourcen](https://technet.microsoft.com/security/default.aspx)
-   [Sicherheitsüberlegungen für Windows XP Embedded-Entwickler](/previous-versions/ms838345(v=msdn.10))
-   [Bewährte Sicherheitsmethoden](../secbp/best-practices-for-the-security-apis.md)

 

 
