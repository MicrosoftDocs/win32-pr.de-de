---
description: Wiedergabelistenbeispiel
ms.assetid: ffe663ce-3e9a-4dfc-8904-6f055332c119
title: Wiedergabelistenbeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5cad2ef96c76512947a5b74e7eac54e3ad5787218e625f30fea5b8e5164177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239127"
---
# <a name="playlist-sample"></a>Wiedergabelistenbeispiel

Zeigt, wie sie Microsoft Media Foundation, um eine Sequenz von Audiodateien in einer Wiedergabeliste wieder zu spielen. Im Beispiel wird die [Sequencerquelle verwendet,](sequencer-source.md) um die Wiedergabeliste zu erstellen und zu verwalten.

> [!Note]  
> Dieses Beispiel ist nicht mehr im SDK enthalten.

 

## <a name="apis-demonstrated"></a>Gezeigte APIs

In diesem Beispiel werden die folgenden Media Foundation veranschaulicht:

-   [**TOPOLOGYMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
-   [**VERERBUNGMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
-   [**VERALTENQuencerSource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)

## <a name="usage"></a>Verbrauch

Im Playlist-Beispiel wird eine Windows erstellt.

-   Wählen Sie zum Erstellen einer neuen Wiedergabeliste **im** Menü Datei die Option Zur **Wiedergabeliste hinzufügen** aus. Wählen Sie **im Dialogfeld Datei** öffnen mindestens eine Audiodatei aus. Die Dateien werden der Wiedergabeliste hinzugefügt.
-   Klicken Sie auf Wiedergabe, um die Sequenz **wieder zu spielen.**
-   Klicken Sie auf Anhalten, um das aktuelle **Segment anzuhalten.**
-   Klicken Sie auf Beenden, um das aktuelle **Segment zu beenden.**
-   Doppelklicken Sie auf das Element in der Wiedergabeliste, um zu einer Datei zu springen.
-   Um eine Datei aus der Wiedergabeliste zu löschen, wählen Sie das Element in der Wiedergabeliste aus. Wählen Sie dann im Menü Datei die Option **Aus Wiedergabeliste** **entfernen** aus.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist an den folgenden Speicherorten verfügbar.



| Standort                                                     | Pfad/URL                                                   |
|--------------------------------------------------------------|------------------------------------------------------------|
| [Windows SDK](https://www.microsoft.com/download/details.aspx?id=8279) | *SDK-Stamm* \\ Beispiele \\ für \\ multimediale Medienfoundation \\ Playlist |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[BasicPlayback-Beispiel](/previous-versions//bb970475(v=vs.85))
</dt> <dt>

[Media Foundation-SDK-Beispiele](media-foundation-sdk-samples.md)
</dt> <dt>

[Sequencerquelle](sequencer-source.md)
</dt> </dl>

 

 
