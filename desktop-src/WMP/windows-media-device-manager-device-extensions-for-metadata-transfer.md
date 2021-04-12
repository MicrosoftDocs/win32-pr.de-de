---
title: Windows Media Device Manager-Geräte Erweiterungen für die metadatenübertragung
description: Windows Media Device Manager-Geräte Erweiterungen für die metadatenübertragung
ms.assetid: c1d84225-b5b1-4f9e-8694-a229653e53de
keywords:
- Windows Media Player, Geräte Erweiterungen
- Windows-Media Player, Erweiterungen
- Windows-Media Player, Metadaten
- Windows Media Player, beschleunigte metadatenübertragung
- Windows Media Player, beschleunigte metadatenübertragung
- Metadaten, Geräte Erweiterungen
- Metadaten, Erweiterungen
- Geräte Erweiterungen, metadatenübertragung
- Erweiterungen, metadatenübertragung
- beschleunigte metadatenübertragung
- Metadaten, beschleunigte Übertragung
- Geräte Erweiterungen, beschleunigte metadatenübertragung
- Erweiterungen, beschleunigte metadatenübertragung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d85ff7026e3395338fdf048c54b8ff7401c9ee7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471437"
---
# <a name="windows-media-device-manager-device-extensions-for-metadata-transfer"></a>Windows Media Device Manager-Geräte Erweiterungen für die metadatenübertragung

Zum Aktivieren der beschleunigten metadatenübertragung müssen Hersteller von Geräten, die MTP nicht unterstützen, im Quellcode folgende Aktionen ausführen:

-   Definieren der **WMP- \_ WMDM- \_ Geräte \_ Unterstützung**.
-   Fügen Sie wmpdevices. h ein, das als Teil des Windows Media Player SDK installiert wird.

Wmpdevices. h definiert die folgenden Strukturen.



| Struktur                                                                                 | BESCHREIBUNG                                                                                                                                       |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [WMP \_ WMDM \_ - \_ \_ metadatenroundtrip \_ PC2DEVICE](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_pc2device) | Struktur, die von Windows-Media Player verwendet wird, um beschleunigte Metadaten-Synchronisierungs Informationen von tragbaren Geräten anzufordern, die MTP nicht unterstützen. |
| [WMP \_ WMDM \_ - \_ \_ metadatenroundtrip \_ DEVICE2PC](/previous-versions/windows/desktop/api/wmpdevices/ns-wmpdevices-wmp_wmdm_metadata_round_trip_device2pc) | Struktur, die von Windows Media Player verwendet wird, um beschleunigte Metadaten-Synchronisierungs Informationen von tragbaren Geräten zu empfangen, die MTP nicht unterstützen. |



 

Um Informationen von dem Gerät über geänderte Metadaten anzufordern, ruft Windows Media Player 10 oder höher die Windows Media Device Manager-Methode **IWMDMDevice3::D eviceiocontrol** auf. Wenn Sie diesen Befehl ausführen, befolgt der Player bestimmte Schritte wie folgt:

-   Der erste Parameter, *dwIoControlCode*, enthält die Konstante **IOCTL \_ WMP \_ Metadata \_ \_ Roundtrip**. Diese Konstante ist in wmpdevices. h definiert.
-   Der zweite Parameter, *lpinbuffer*, verweist auf eine **WMP- \_ WMDM- \_ \_ metadatenroundtrip \_ \_ PC2DEVICE** -Struktur.
-   Der dritte Parameter *nInBufferSize* enthält die Größe des Eingabe Puffers.
-   Der vierte Parameter, *lpoutbuffer*, verweist auf eine **WMP- \_ WMDM- \_ \_ metadatenroundtrip \_ \_ DEVICE2PC** -Struktur. Das Gerät muss diese Struktur mit Informationen zu Änderungen ausfüllen.
-   Der fünfte Parameter, *pnoutbuffersize*, empfängt die Größe des Ausgabepuffers.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Geräte Erweiterungen für die beschleunigte metadatenübertragung**](device-extensions-for-accelerated-metadata-transfer.md)
</dt> </dl>

 

 




