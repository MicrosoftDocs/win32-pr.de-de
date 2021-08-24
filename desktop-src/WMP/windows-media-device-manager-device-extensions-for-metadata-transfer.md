---
title: Windows Media Geräte-Manager-Geräteerweiterungen für die Metadatenübertragung
description: Windows Media Geräte-Manager-Geräteerweiterungen für die Metadatenübertragung
ms.assetid: c1d84225-b5b1-4f9e-8694-a229653e53de
keywords:
- Windows Media Player,Geräteerweiterungen
- Windows Media Player,Erweiterungen
- Windows Media Player,Metadata
- Windows Media Player,beschleunigte Metadatenübertragung
- Windows Media Player,beschleunigte Metadatenübertragung
- Metadaten,Geräteerweiterungen
- Metadaten,Erweiterungen
- Geräteerweiterungen,Metadatenübertragung
- Erweiterungen,Metadatenübertragung
- Beschleunigte Metadatenübertragung
- Metadaten,beschleunigte Übertragung
- Geräteerweiterungen, beschleunigte Metadatenübertragung
- Erweiterungen, beschleunigte Metadatenübertragung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9b37271fc9714bf3665dccf1475da1a5840c429d7df9136a50fe95789f7a02
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571635"
---
# <a name="windows-media-device-manager-device-extensions-for-metadata-transfer"></a>Windows Media Geräte-Manager-Geräteerweiterungen für die Metadatenübertragung

Um die beschleunigte Metadatenübertragung zu aktivieren, müssen Hersteller von Geräten, die MTP nicht unterstützen, folgende Schritte im Quellcode ausführen:

-   Definieren **Sie WMP \_ WMDM DEVICE SUPPORT (WMP-WMDM-GERÄTEUNTERSTÜTZUNG). \_ \_**
-   Schließen Sie wmpdevices.h ein, die als Teil des Windows Media Player SDK installiert wird.

Wmpdevices.h definiert die folgenden Strukturen.



| Struktur                                                                                 | Beschreibung                                                                                                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [WMP \_ WMDM \_ METADATA \_ ROUND \_ TRIP \_ PC2DEVICE](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_pc2device) | Struktur, die von Windows Media Player zum Anfordern von Informationen zur beschleunigten Metadatensynchronisierung von portablen Geräten verwendet wird, die MTP nicht unterstützen. |
| [WMP \_ WMDM \_ METADATA \_ ROUND \_ TRIP \_ DEVICE2PC](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_device2pc) | Struktur, die von Windows Media Player zum Empfangen von Informationen zur beschleunigten Metadatensynchronisierung von portablen Geräten verwendet wird, die MTP nicht unterstützen. |



 

Zum Anfordern von Informationen über geänderte Metadaten vom Gerät ruft Windows Media Player 10 oder höher die Windows Media Geräte-Manager-Methode **IWMDMDevice3::D eviceIoControl auf.** Bei diesem Aufruf folgt der Player den folgenden spezifischen Schritten:

-   Der erste Parameter *dwIoControlCode enthält* die Konstante **IOCTL \_ WMP \_ METADATA ROUND \_ \_ TRIP.** Diese Konstante wird in wmpdevices.h definiert.
-   Der zweite Parameter *lpInBuffer verweist* auf eine **WMP \_ WMDM \_ METADATA ROUND TRIP \_ \_ \_ PC2DEVICE-Struktur.**
-   Der dritte Parameter, *nInBufferSize,* enthält die Größe des Eingabepuffers.
-   Der vierte Parameter, *lpOutBuffer,* verweist auf eine **WMP \_ WMDM \_ METADATA ROUND TRIP \_ \_ \_ DEVICE2PC-Struktur.** Das Gerät muss diese Struktur mit Informationen zu Änderungen füllen.
-   Der fünfte Parameter, *pnOutBufferSize,* empfängt die Größe des Ausgabepuffers.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Geräteerweiterungen für die beschleunigte Metadatenübertragung**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




