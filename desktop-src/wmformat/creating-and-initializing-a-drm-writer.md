---
title: Erstellen und Initialisieren eines DRM-Writers
description: Erstellen und Initialisieren eines DRM-Writers
ms.assetid: ce0508e1-f69f-4e09-8c32-8c9dac48b5ec
keywords:
- Windows Media-Format-SDK, DRM-Writer
- Digital Rights Management (DRM), Erstellen von DRM-Writern
- DRM (Digital Rights Management), Erstellen von DRM-Writern
- Digital Rights Management (DRM), Initialisieren von DRM-Writern
- DRM (Digital Rights Management), Initialisieren von DRM-Writern
- Erweiterte APIs für den DRM-Client, DRM-Writer
- Erweiterte Client-APIs, DRM-Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ed40b7f9dd9c486b1ef22e5042261c5ce03d2f7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "106337268"
---
# <a name="creating-and-initializing-a-drm-writer"></a>Erstellen und Initialisieren eines DRM-Writers

Die folgenden Schritte sind erforderlich, um ein ASF Writer-Objekt zum Importieren verschlüsselter Medien Beispiele in Windows Media DRM zu initialisieren.

1.  Führen Sie die Schritte 1 bis 4 zum [Importieren von Lizenz-und Schlüssel Material](importing-license-and-key-material.md)aus.
2.  Erstellen und initialisieren Sie ein ASF-Writer-Objekt mit dem entsprechenden Windows Media DRM-Schlüsselmaterial. Weitere Informationen finden Sie [unter Aktivieren der DRM-Unterstützung](enabling-drm-support.md).
3.  Legen Sie jedes der folgenden Attribute fest, indem Sie [**iwmdrmwriter:: setdrmattribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)aufrufen:
    -   DRM \_ headersignprivkey
    -   DRM- \_ V1LicenseAcqURL
    -   DRM- \_ Schlüssel-ID
    -   DRM- \_ Lizenz-AcqURL
4.  Wenn auf dem Computer, auf dem die Software ausgeführt wird, keine lizenzierte Version von Windows Media Rights Manager installiert ist, müssen auch die folgenden vier Attribute festgelegt werden:
    -   DRM \_ lasignaturerootcert
    -   DRM- \_ lasignaturecert
    -   DRM \_ lasignaturelicsrvcert
    -   DRM- \_ lasignatureprivkey
    -   Die Anwendung für die erforderlichen Verschlüsselungs Zertifikate kann durch Ausfüllen des [Windows Media Licensing Agreement (wmla)](https://www.microsoft.com/licensing/default) Online abgeschlossen werden.
5.  Erstellen Sie einen Sitzungsschlüssel, und füllen Sie eine [**WMDRM- \_ \_ \_ Schlüssel**](wmdrm-import-session-key.md) Struktur zum Importieren der Sitzung aus. Der Sitzungsschlüssel wird zum Verschlüsseln eines Inhalts Schlüssels verwendet. Ein Beispiel finden Sie unter [Beispiel für das Erstellen eines Sitzungsschlüssels](create-session-key-example.md).
6.  Erstellen Sie einen Inhalts Schlüssel aus einem zufälligen RC4-Initialisierungs Vektor, und füllen Sie eine [**WMDRM- \_ \_ \_ Schlüssel**](wmdrm-import-content-key.md) Struktur zum Importieren von Inhalten aus. Der Inhalts Schlüssel wird zum Verschlüsseln der Medien Beispiele verwendet. Ein Beispiel finden Sie unter [Create Content Key example](create-content-key-example.md).
7.  Verschlüsseln Sie den Inhalts Schlüssel mit dem Sitzungsschlüssel, indem Sie die RC4-Verschlüsselung verwenden.
8.  Extrahieren Sie den Schlüssel für die Computer Zertifikat Sammlung. Ein Beispiel finden Sie unter [Get Machine Certificate example](get-machine-certificate-example.md).
9.  Verschlüsseln Sie den Sitzungsschlüssel mit dem aus dem Zertifikat extrahierten öffentlichen Schlüssel.
10. Füllen Sie eine [**WMDRM- \_ Import \_ Init \_ struct**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct) -Struktur aus.
11. Aufrufen der [**IWMDRMWriter3:: setprotectstreamsamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples) -Methode, um das SDK zu benachrichtigen, dass die im Writer kommenden Beispiele bereits geschützt sind und für den Import direkt an den Windows Media DRM-Client gesendet werden sollen.
12. Nennen Sie [**iwmwriter:: BeginWrite**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).

Die verbleibenden Schritte zum Erstellen einer DRM-geschützten Datei werden im Windows Media Format SDK-Programmier Handbuch dokumentiert. Weitere Informationen finden Sie unter [Erstellen geschützter Dateien](creating-protected-files.md).

Der nächste Schritt besteht darin, die einzelnen Medien Beispiele zu durchlaufen, zu verschlüsseln und an das Writer-Objekt zu übergeben. Weitere Informationen finden Sie unter [verschlüsseln und Importieren von Medien Beispielen](encrypting-and-importing-media-samples.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Attribute**](attributes.md)
</dt> <dt>

[**DRM-Import**](drm-import.md)
</dt> </dl>

 

 




