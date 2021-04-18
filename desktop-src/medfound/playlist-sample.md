---
description: Wiedergabelisten Beispiel
ms.assetid: ffe663ce-3e9a-4dfc-8904-6f055332c119
title: Wiedergabelisten Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f83d05762385d0de43a5d7f2bcd73cda2c6e2d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343382"
---
# <a name="playlist-sample"></a>Wiedergabelisten Beispiel

Zeigt, wie Sie mit Microsoft Media Foundation eine Sequenz von Audiodateien in einer Wiedergabeliste abspielen können. Im Beispiel wird die [Sequencer-Quelle](sequencer-source.md) verwendet, um die Wiedergabeliste zu erstellen und zu verwalten.

> [!Note]  
> Dieses Beispiel ist nicht mehr im SDK enthalten.

 

## <a name="apis-demonstrated"></a>Gezeigte APIs

In diesem Beispiel werden die folgenden Media Foundation Schnittstellen veranschaulicht:

-   [**Imfmediasourcetopologyprovider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider)
-   [**Imfmediasession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
-   [**IMF sequencersource**](/windows/desktop/api/mfidl/nn-mfidl-imfsequencersource)

## <a name="usage"></a>Verbrauch

Das Wiedergabelisten Beispiel erstellt eine Windows-Anwendung.

-   Um eine neue Wiedergabeliste zu erstellen, wählen Sie im Menü **Datei** die Option **zu Wiedergabeliste hinzufügen** aus. Wählen Sie im Dialogfeld **Datei öffnen** mindestens eine Audiodatei aus. Die Dateien werden der Wiedergabeliste hinzugefügt.
-   Um die Sequenz wiederzugeben, **Klicken Sie auf wieder** geben.
-   Um das aktuelle Segment anzuhalten **, klicken Sie auf Anhalten**.
-   Um das aktuelle Segment anzuhalten, klicken Sie auf " **Abbrechen**".
-   Um zu einer Datei zu springen, doppelklicken Sie auf das Element in der Wiedergabeliste.
-   Wenn Sie eine Datei aus der Wiedergabeliste löschen möchten, wählen Sie das Element in der Wiedergabeliste aus. Wählen Sie dann im Menü **Datei** die Option **aus Wiedergabeliste entfernen** aus.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist in den folgenden Speicherorten verfügbar.



| Standort                                                     | Pfad/URL                                                   |
|--------------------------------------------------------------|------------------------------------------------------------|
| [Windows SDK](https://www.microsoft.com/download/details.aspx?id=8279) | *SDK-Stamm* \\ Beispiele \\ \\ multimediaremediafoundations \\ Wiedergabeliste |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Basicplayback-Beispiel](/previous-versions//bb970475(v=vs.85))
</dt> <dt>

[Media Foundation-SDK-Beispiele](media-foundation-sdk-samples.md)
</dt> <dt>

[Sequencer-Quelle](sequencer-source.md)
</dt> </dl>

 

 
