---
description: Proxy Unterstützung für Netzwerk Quellen
ms.assetid: e739746d-2a09-4237-a7c1-0aed4e4516d7
title: Proxy Unterstützung für Netzwerk Quellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97bc1172c072a54f9f76cbcd3a297a972efbde29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349083"
---
# <a name="proxy-support-for-network-sources"></a>Proxy Unterstützung für Netzwerk Quellen

Bei einem Proxy Server handelt es sich um einen zwischengeschalteten Server zwischen Ihrem Intranet und dem Internet, der Anforderungen von der Client Anwendung an den Medienserver weiterleitet und Dateien vom Medienserver abruft.

Media Foundation implizit ein *proxylocatorobjekt* erstellt, wenn eine Client Anwendung versucht, auf eine Quell-URL zuzugreifen. Das proxylocator-Objekt macht die [**IMF netproxylocator**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator) -Schnittstelle verfügbar. Während der Quell Auflösung prüft Media Foundation den an die Quell Auflösungsmethode übergebenen Eigenschaften Speicher.

Wenn der Eigenschaften Speicher die Eigenschaft " [mfnetsource \_ proxylocatorfactory](mfnetsource-proxylocatorfactory-property.md) " enthält, die auf ein von der Anwendung implementiertes proxylocatorfactoryobjekt festgelegt ist, ruft es die [**imfnetproxylocatorfactory::**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) -Methode zum Erstellen eines proxylocators mit benutzerdefinierten Konfigurationseinstellungen auf.

Wenn der Eigenschaften Speicher nicht festgelegt ist, erstellt Media Foundation den proxylocator mit der Standardkonfiguration. Diese Einstellungen lauten wie folgt:

-   Wenn die Benutzer Richtlinie festgelegt ist, verwendet der proxylocator die in der Registrierung angegebenen Einstellungen.

-   Für HTTP verwendet der proxylocator die Browser Proxy Einstellungen.

-   Bei RTSP ist der proxylocator so konfiguriert, dass Proxy Server beim Herstellen einer Verbindung mit dem Medienserver umgangen werden.

Diese Standardkonfiguration kann von der Anwendung geändert werden. Die folgenden Themen enthalten Informationen zu den Konfigurationseinstellungen für einen proxylocator:

-   [Proxy Locator-Konfigurationseinstellungen](proxy-locator-configuration-settings.md)

-   [Konfigurieren des proxylocators](how-to-configure-the-proxy-locator.md)

Media Foundation initialisiert den proxylocator für die Quell-URL, die für den [quellresolver](source-resolver.md)angegeben ist. Der proxylocator erkennt einen Proxy Server, der auf der Grundlage der Konfigurationseinstellungen verwendet werden soll. Wenn der proxylocator versucht, den Proxy Server festzulegen, wird der Erfolg oder das Fehler Ergebnis in der Registrierung aufgezeichnet. Dieser Wert wird beim nächsten Proxy Erkennungsprozess geprüft. Wenn ein bestimmter Proxy Server bekanntermaßen in der Vergangenheit Ausfälle verursacht hat, überspringt der proxylocator ihn.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Attribute und Eigenschaften](attributes-and-properties.md)
</dt> <dt>

[Netzwerk in Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



