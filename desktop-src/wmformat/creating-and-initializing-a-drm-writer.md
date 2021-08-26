---
title: Erstellen und Initialisieren eines DRM-Writers
description: Erstellen und Initialisieren eines DRM-Writers
ms.assetid: ce0508e1-f69f-4e09-8c32-8c9dac48b5ec
keywords:
- Windows Medienformat-SDK, DRM Writer
- Digital Rights Management (DRM), Erstellen von DRM-Writern
- DRM (Verwaltung digitaler Rechte),Erstellen von DRM-Writern
- Digital Rights Management (DRM),Initialisieren von DRM-Writern
- DRM (Verwaltung digitaler Rechte),Initialisieren von DRM-Writern
- Erweiterte DRM-Client-APIs, DRM-Writer
- Erweiterte Client-APIs, DRM-Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c24067e082de38bc396153be918025e2608246e39185c45eaa84bfe0e5c02407
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007050"
---
# <a name="creating-and-initializing-a-drm-writer"></a>Erstellen und Initialisieren eines DRM-Writers

Die folgenden Schritte sind erforderlich, um ein ASF Writer-Objekt zum Importieren verschlüsselter Medienbeispiele in Windows Media DRM zu initialisieren.

1.  Führen Sie die Schritte 1 bis 4 des Importierens von [Lizenz- und Schlüsselmaterial aus.](importing-license-and-key-material.md)
2.  Erstellen und initialisieren Sie ein ASF Writer-Objekt mithilfe des entsprechenden Windows Medien-DRM-Schlüsselmaterials. Weitere Informationen finden Sie unter [Aktivieren der DRM-Unterstützung.](enabling-drm-support.md)
3.  Legen Sie jedes der folgenden Attribute fest, indem [**Sie IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute)aufrufen:
    -   \_DRM-HeaderSignPrivKey
    -   DRM \_ V1LicenseAcqURL
    -   \_DRM-Schlüssel-ID
    -   \_DRM-LizenzAcqURL
4.  Wenn auf dem Computer, auf dem Ihre Software ausgeführt wird, keine lizenzierte Version von Windows Media Rights Manager installiert ist, müssen auch die folgenden vier Attribute festgelegt werden:
    -   DRM \_ LASignatureRootCert
    -   DRM \_ LASignatureCert
    -   DRM \_ LASignatureLicSrvCert
    -   DRM \_ LASignaturePrivKey
    -   Die Anwendung für die erforderlichen Verschlüsselungszertifikate kann durch Ausfüllen des [Windows Media Licensing Agreement (WMLA)](https://www.microsoft.com/licensing/default) online abgeschlossen werden.
5.  Erstellen Sie einen Sitzungsschlüssel, und füllen Sie eine [**WMDRM \_ IMPORT \_ SESSION \_ KEY-Struktur**](wmdrm-import-session-key.md) aus. Der Sitzungsschlüssel wird zum Verschlüsseln eines Inhaltsschlüssels verwendet. Ein Beispiel finden Sie unter [Erstellen eines Sitzungsschlüssels – Beispiel.](create-session-key-example.md)
6.  Erstellen Sie einen Inhaltsschlüssel aus einem zufälligen RC4-Initialisierungsvektor, und füllen Sie eine [**WMDRM \_ IMPORT \_ CONTENT \_ KEY-Struktur**](wmdrm-import-content-key.md) aus. Der Inhaltsschlüssel wird zum Verschlüsseln der Medienbeispiele verwendet. Ein Beispiel finden Sie unter [Erstellen eines Inhaltsschlüssels – Beispiel.](create-content-key-example.md)
7.  Verschlüsseln Sie den Inhaltsschlüssel mit dem Sitzungsschlüssel mithilfe der RC4-Verschlüsselung.
8.  Extrahieren Sie den Schlüssel für die Computerzertifikatsammlung. Ein Beispiel finden Sie unter [Get Machine Certificate Example](get-machine-certificate-example.md).
9.  Verschlüsseln Sie den Sitzungsschlüssel mit dem aus dem Zertifikat extrahierten öffentlichen Schlüssel.
10. Füllen Sie eine [**WMDRM \_ IMPORT \_ \_ INIT-STRUKTURstruktur aus.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmdrm_import_init_struct)
11. Rufen Sie die [**IWMDRMWriter3::SetProtectStreamSamples-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter3-setprotectstreamsamples) auf, um das SDK zu benachrichtigen, dass die im Writer enthaltenen Beispiele bereits geschützt sind und zum Importieren direkt an den Windows Media DRM-Client gesendet werden sollten.
12. Rufen Sie [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)auf.

Die verbleibenden Schritte zum Erstellen einer DRM-geschützten Datei sind im Programmierhandbuch Windows Media Format SDK dokumentiert. Weitere Informationen finden Sie unter [Erstellen von geschützten Dateien.](creating-protected-files.md)

Der nächste Schritt besteht darin, jedes Medienbeispiel zu durchlaufen, zu verschlüsseln und an das Writer-Objekt zu übergeben. Weitere Informationen finden Sie in den [Beispielen zum Verschlüsseln und Importieren von Medien.](encrypting-and-importing-media-samples.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Attribute**](attributes.md)
</dt> <dt>

[**DRM-Import**](drm-import.md)
</dt> </dl>

 

 




