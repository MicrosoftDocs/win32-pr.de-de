---
title: Behandeln geschützter Inhalte
description: Behandeln geschützter Inhalte
ms.assetid: f218d69e-ac80-43ba-be31-af3abf2b8de9
keywords:
- Windows Media Device Manager, Zertifikate
- Device Manager, Zertifikate
- Desktop Anwendungen, Zertifikate
- Dienstanbieter, Zertifikate
- Programmier Handbuch, Zertifikate
- certificates
- Windows Media Device Manager, Anbieter für sichere Inhalte (Secure Content Provider, SCP)
- Device Manager, sicherer Inhaltsanbieter (Secure Content Provider, SCP)
- Desktop Anwendungen, Secure Content Provider (SCP)
- Dienstanbieter, Anbieter für sichere Inhalte (Secure Content Provider, SCP)
- Programmier Handbuch, Anbieter für sichere Inhalte (Secure Content Provider, SCP)
- Secure Content Provider (SCP)
- SCP (sicherer Inhaltsanbieter)
- Windows Media Device Manager, DRM-geschützter Inhalt
- Device Manager, DRM-geschützter Inhalt
- Programmier Handbuch, DRM-geschützter Inhalt
- Desktop Anwendungen, DRM-geschützter Inhalt
- Dienstanbieter, DRM-geschützter Inhalt
- DRM-geschützter Inhalt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd0fb6ab155d08ed19eb84988709695f9ed63fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388168"
---
# <a name="handling-protected-content"></a>Behandeln geschützter Inhalte

Wenn Sie eine Anwendung oder einen Dienstanbieter entwickeln, die von Windows Media Digital Rights Management (DRM) geschützte Inhalte nutzen, müssen Sie über ein Schlüssel-/zertifikatpaar verfügen, das von Microsoft ausgegeben wird. Informationen dazu, wo Sie dieses Zertifikat erhalten, finden Sie unter [Tools für die Entwicklung](tools-for-development.md). Wenn Sie nicht beabsichtigen, geschützte Inhalte zu verarbeiten, können Sie den Dummy-Schlüssel und das Zertifikat, das mit diesem SDK bereitgestellt wird, in einer Datei namens Key. c verwenden.

Für alle Dateien, die durch DRM-Technologie geschützt sind, muss für Windows Media Device Manager ein sicherer Inhaltsanbieter (Secure Content Provider, SCP) für dieses Dateiformat vorhanden sein. Microsoft stellt ein SCP-Modul für WMA-und WMV-Dateien bereit. Wenn Ihre Anwendung oder Ihr Dienstanbieter von DRM geschützten Inhalten in einem anderen Format verarbeitet, müssen Sie Ihr eigenes SCP-Modul bereitstellen. Ein SCP-Modul ist ein COM-Objekt, das alle [Schnittstellen für sichere Inhaltsanbieter](interfaces-for-secure-content-providers.md)implementiert.

Eine Anwendung kann DRM-geschützte Inhalte an Geräte senden, die entweder auf Windows Media DRM 10 für tragbare Geräte oder auf einem tragbaren Geräte-DRM (PDDRM) erstellt wurden. Sie können jedoch nur einen Dienstanbieter für Geräte erstellen, die auf PDDRM erstellt wurden. Es ist nicht möglich, einen Dienstanbieter für Geräte zu erstellen, die mit Windows Media DRM 10 für tragbare Geräte erstellt wurden. Diese letzteren Geräte können nur den von Microsoft bereitgestellten MTP-Dienstanbieter verwenden.

Geräte, die auf PDDRM basieren, können nur Lizenzen für erworbene Inhalte unterstützen. Lizenzen mit Zeitablauf Bedingungen werden nur von Geräten unterstützt, die auf Windows Media DRM 10 für tragbare Geräte basieren und spezielle Anforderungen erfüllen, wie z. b. eine sichere Uhr und eine individuelle Individualisierung. Windows Media DRM 10 for Portable Devices SDK enthält Details zu den Geräteanforderungen zur Unterstützung der Technologie der Version 10.

Vor dem Senden von DRM-Inhalten an das Gerät muss eine Anwendung verschiedene Dinge überprüfen:

-   Das Gerät unterstützt DRM-Technologie.
-   Welche Version der DRM-Technologie unterstützt wird (Version 10 oder früher).
-   Wenn das Gerät auf Version 10 basiert, sind alle Komponenten auf dem neuesten Stand (z. b. die sichere Uhr und alle individuellen Anforderungen).

Alle Methodenaufrufe zum Beantworten dieser Fragen werden vom Client durchgeführt und von Windows Media Device Manager und der Komponente für den sicheren Inhaltsanbieter verarbeitet. der Dienstanbieter verarbeitet diese Aufrufe nicht.

Wenn das Gerät Windows Media DRM 10 für tragbare Geräte nicht unterstützt, kann es möglicherweise trotzdem geschützte Inhalte nutzen (abhängig von der Inhalts Lizenz und dem Geräte Entwurf), aber alle an ihn gesendeten Inhalte verfügen über eine vereinfachte Nutzungslizenz mit eingeschränkten Rechten (z. b. kein Zeitablauf).

-   Beispiele, die zeigen, wie eine Anwendung überprüft, ob ein Gerät geschützte Inhalte verarbeiten kann und ob die zugehörigen DRM-Komponenten aktualisiert werden müssen, finden Sie unter [behandeln geschützter Inhalte in der Anwendung](handling-protected-content-in-the-application.md).
-   Weitere Informationen zum Aufbau eines Dienstanbieters, der geschützte Inhalte verarbeiten kann, finden Sie unter [verarbeiten geschützter Inhalte im Dienstanbieter](handling-protected-content-in-the-service-provider.md).

> [!Note]  
> Beim Verarbeiten von DRM-geschützten Dateien mit einem angefügten Debugger tritt bei vielen Windows  Media Device Manager-Methoden zum Übertragen von Dateien oder beim Anfordern von Berechtigungen ein Fehler auf. Daher müssen Sie zum Debuggen des Codes Alternative Methoden verwenden, z. b. die Protokollierung von Ausgaben in eine Windows Form oder eine Protokolldatei. Weitere Informationen zu Protokollierungs Optionen finden Sie unter [Aktivieren der Protokollierung](enabling-logging.md). Wenn Sie einen Debugger für geschützte Inhalte ausführen, gibt eine Methode einen der im DRM-Abschnitt [Fehlercodes](error-codes.md)oder möglicherweise unbekannten Fehlercodes aufgelisteten Fehlercodes zurück. Wenn Sie beim Ausführen eines Debuggers auf geschützten Inhalten oder Methoden rätselhafte **HRESULT** -Werte erhalten, könnte der DRM-Schutz die Ursache sein.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 




