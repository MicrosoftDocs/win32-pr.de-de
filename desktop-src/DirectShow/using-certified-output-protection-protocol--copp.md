---
description: Verwenden des Certified Output Protection-Protokolls (COPP)
ms.assetid: 23eebe93-416b-48c8-a05f-019e38b9a660
title: Verwenden des Certified Output Protection-Protokolls (COPP)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76460e335985c2aab7f9047b55d2df05aace0269
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357879"
---
# <a name="using-certified-output-protection-protocol-copp"></a>Verwenden des Certified Output Protection-Protokolls (COPP)

Mit dem Certified Output Protection Protocol (COPP) kann eine Anwendung einen Videodaten Strom beim Durchlaufen vom Grafikadapter zum Anzeigegerät schützen. Eine Anwendung kann COPP verwenden, um zu ermitteln, welche Art von physischem Connector mit dem Anzeigegerät verbunden ist und welche Arten von Ausgabe Schutz verfügbar sind. Schutzmechanismen umfassen Folgendes:

-   High-Bandwidth digitaler Content Protection (HDCP)
-   Copy Generation Management System – Analog (CGMS-A)
-   Der Schutz von analogen Kopien (ACP)

Wenn der Grafikadapter einen dieser Mechanismen unterstützt, kann die Anwendung COPP zum Festlegen der Schutz Ebene verwenden.

COPP definiert ein Protokoll, das verwendet wird, um einen sicheren Kommunikationskanal mit dem Grafiktreiber einzurichten. Er verwendet Message Authentication Codes (Macs), um die Integrität der von der Anwendung und dem Anzeigetreiber übergebenen COPP-Befehle zu überprüfen. Die Anwendung verwendet COPP durch Aufrufen von Methoden in der [**iamcertifiedoutputprotection**](/windows/desktop/api/Strmif/nn-strmif-iamcertifiedoutputprotection) -Schnittstelle des DirectShow-Video Mischungs-rendererfilters (VMR-7 oder VMR-9).

COPP definiert keine Informationen zu den Richtlinien für digitale Rechte, die möglicherweise für digitale Medieninhalte gelten. Außerdem implementiert COPP selbst keine Ausgabe Schutzsysteme. Das COPP-Protokoll bietet lediglich eine Möglichkeit zum Festlegen und Abfragen von Schutz Ebenen auf dem Grafikadapter mithilfe der Schutzsysteme, die vom Adapter bereitgestellt werden.

In diesem Abschnitt wird davon ausgegangen, dass Sie mit den folgenden Technologien vertraut sind:

-   DirectShow
-   SDK für Windows Media-Format
-   XML
-   Kryptografie mit öffentlichem Schlüssel und symmetrische Kryptografie

Die Codebeispiele in diesem Abschnitt verwenden die CryptoAPI von Microsoft, um kryptografische Vorgänge auszuführen. Dieser Abschnitt enthält die folgenden Themen:

-   [Übersicht über COPP](overview-of-copp.md)
-   [Abrufen der Zertifikat Kette des Treibers](obtaining-the-drivers-certificate-chain.md)
-   [Überprüfen der Zertifikat Kette](validating-the-certificate-chain.md)
-   [Zertifikat Sperr Listen](certificate-revocation-lists.md)
-   [Importieren des öffentlichen Schlüssels des Treibers](importing-the-drivers-public-key.md)
-   [Initiieren einer COPP-Sitzung](initiating-a-copp-session.md)
-   [Senden von COPP-Status Anforderungen](sending-copp-status-requests.md)
-   [Senden von COPP-Befehlen](sending-copp-commands.md)
-   [Testen, ob ein Grafiktreiber COPP unterstützt](testing-whether-a-graphics-driver-supports-copp.md)
-   [COPP-Abfrage Verweis](copp-query-reference.md)
-   [COPP-Befehlsreferenz](copp-command-reference.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Video Mischungs Renderers](using-the-video-mixing-renderer.md)
</dt> </dl>

 

 



