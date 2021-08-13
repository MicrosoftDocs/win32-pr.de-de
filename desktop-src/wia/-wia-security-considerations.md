---
description: Dieses Dokument enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit Windows Image Acquisition (WIA).
ms.assetid: 35455320-7d08-49de-938d-40dc0873917b
title: 'Sicherheitsüberlegungen: Windows Imageerfassung'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bb8f78e0f45b5b63d5d8deb8ffdd35bc64ee5566ced65ded30ecc51366c0793
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439685"
---
# <a name="security-considerations-windows-image-acquisition"></a>Sicherheitsüberlegungen: Windows Imageerfassung

Dieses Dokument enthält Informationen zu Sicherheitsüberlegungen im Zusammenhang mit Windows Image Acquisition (WIA). Dieses Dokument enthält nicht alles, was Sie über Sicherheitsprobleme wissen müssen. Verwenden Sie es stattdessen als Ausgangspunkt und Referenz für diesen Technologiebereich.

-   [Verwenden von Anführungszeichen um Pfadnamen](#use-quotation-marks-around-path-names)
-   [Platzieren registrierter Anwendungen an sicheren Standorten](#place-registered-applications-in-secure-locations)
-   [Verwenden Sie keine zugrunde liegenden Verzeichnisse oder Registrierungsschlüssel.](#do-not-use-underlying-directories-or-registry-keys)
-   [Verwandte Themen](#related-topics)

## <a name="use-quotation-marks-around-path-names"></a>Verwenden von Anführungszeichen um Pfadnamen

Wenn Sie [**IWiaDevMgr::RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) verwenden, um eine Anwendung zum Empfangen von Geräteereignissen zu registrieren, müssen Sie den Pfad und den Dateinamen der Anwendung mit Anführungszeichen umschließen. Dadurch wird vermieden, dass der Pfad falsch interpretiert wird und eine nicht autorisierte Anwendung ausgeführt wird.

## <a name="place-registered-applications-in-secure-locations"></a>Platzieren registrierter Anwendungen an sicheren Standorten

Wenn eine Anwendung für den Empfang eines Geräteereignisses registriert ist, kann diese Anwendung von jedem Benutzer ausgeführt werden, der Zugriff auf dieses Gerät hat. Wenn beispielsweise eine Anwendung für ein Scanereignis registriert ist, führt das Drücken der Schaltfläche "Scan" auf einem Scanner dazu, dass diese Anwendung ausgeführt wird. Wenn die Anwendung mit einer höheren Berechtigung als der Benutzer ausgeführt wird, führt dies zu einem potenziellen Sicherheitsproblem.

## <a name="do-not-use-underlying-directories-or-registry-keys"></a>Verwenden Sie keine zugrunde liegenden Verzeichnisse oder Registrierungsschlüssel.

WIA verwendet intern mehrere Verzeichnisse und Registrierungsschlüssel, um Daten oder Informationen zu speichern. Greifen Sie nicht direkt auf diese Verzeichnisse oder Registrierungsschlüssel zu. Verwenden Sie stattdessen die verfügbar gemachten Schnittstellenmethoden, um Verzeichnisse für erworbene Bilder anzugeben.

## <a name="related-topics"></a>Verwandte Themen

-   [Microsoft Security](https://www.microsoft.com/security/)
-   [MSDN Library Security Home Page](https://msdn.microsoft.com/security/default.aspx)
-   [Sicherheits-How-to-Resources](https://www.microsoft.com/technet/solutionaccelerators/howto/sechow.mspx)
-   [TechNet-Sicherheitsressourcen](https://technet.microsoft.com/security/default.aspx)
-   [Sicherheitsüberlegungen für Windows XP Embedded-Entwickler](/previous-versions/ms838345(v=msdn.10))
-   [Bewährte Sicherheitsmethoden](../secbp/best-practices-for-the-security-apis.md)

 

 
