---
title: Behandeln geschützter Inhalte im Dienstanbieter
description: Behandeln geschützter Inhalte im Dienstanbieter
ms.assetid: 5c18c8ec-d579-41df-8c25-c143fb9cdbef
keywords:
- Windows Media Device Manager, Zertifikate
- Device Manager, Zertifikate
- Programmier Handbuch, Zertifikate
- Dienstanbieter, Zertifikate
- Erstellen von Dienstanbietern, Zertifikaten
- certificates
- Windows Media Device Manager, DRM-geschützter Inhalt
- Device Manager, DRM-geschützter Inhalt
- Programmier Handbuch, DRM-geschützter Inhalt
- Dienstanbieter, DRM-geschützter Inhalt
- Erstellen von Dienstanbietern, DRM-geschütztem Inhalt
- DRM-geschützter Inhalt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d10cf9078cf9aaf631b65de968f01491a97781
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337977"
---
# <a name="handling-protected-content-in-the-service-provider"></a>Behandeln geschützter Inhalte im Dienstanbieter

Sie können einen Dienstanbieter erstellen, der DRM-geschützten Inhalt an ein auf portable Geräte-DRM (PDDRM) aufgebautes Gerät senden kann. Sie können jedoch keinen Dienstanbieter erstellen, der von DRM-geschützten Inhalten an Geräte senden kann, die auf Windows Media DRM 10 für tragbare Geräte erstellt wurden. Diese Geräte verwenden MTP, und Sie können keinen eigenen MTP-Dienstanbieter erstellen.

Der einzige zusätzliche Schritt, den ein Dienstanbieter zum Senden von DRM-Material an ein PDDRM-Gerät ausführen muss, besteht darin, ein von Microsoft ausgestelltes Zertifikat/Schlüssel-Paar zu erhalten. Informationen dazu, wo Sie dieses Zertifikat/welchen Schlüssel erhalten, finden Sie unter [Tools für die Entwicklung](tools-for-development.md) . Die Lizenzen, die für diese Geräte ausgestellt werden, sind vereinfachte Lizenzen, die nur die einfache Wiedergabe erworbener Inhalte unterstützen. Es werden keine Zeitablauf Lizenzen unterstützt. Diese Lizenz wird vom Anbieter für sichere Inhalte (von Microsoft für WMA/WMV-Dateien bereitgestellt) erstellt und im Header der Datei gespeichert, die an den Dienstanbieter gesendet wird. Sie müssen keine speziellen Schritte für geschützte Dateien ausführen.

Nachdem die geschützte Datei gesendet wurde, ruft der Windows Media-Device Manager den Dienstanbieter auf, um eine spezielle Lizenz Speicherdatei vom Gerät anzufordern. Windows Media Device Manager fügt dieser Datei eine Kopie der neuen Lizenz hinzu und sendet Sie an den Dienstanbieter zurück, um Sie zurück an das Gerät zu senden. Auch wenn der Dienstanbieter diese Datei nicht finden oder zurückgeben kann, sollte das Gerät weiterhin in der Lage sein, die geschützte Datei mit der Lizenz Kopie im Dateiheader wiederzugeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen eines Dienstanbieters**](creating-a-service-provider.md)
</dt> <dt>

[**Behandeln geschützter Inhalte**](handling-protected-content.md)
</dt> </dl>

 

 




