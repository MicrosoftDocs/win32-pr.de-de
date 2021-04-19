---
title: Verwenden von Inverse Telecine
description: Verwenden von Inverse Telecine
ms.assetid: 7752d1ac-34b1-446a-a69c-29463c9e10f7
keywords:
- SDK für Windows Media-Format, Inverse Telecine
- Windows Media-Format-SDK, telecine
- Advanced Systems Format (ASF), Inverse Telecine
- ASF (Advanced Systems Format), Inverse Telecine
- Advanced Systems Format (ASF), telecine
- ASF (Advanced Systems Format), telecine
- Inverse Telecine
- Telecine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17d4f4e3ae34c2a9efcaa4fe8e5ce7256474404
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "106341510"
---
# <a name="to-use-inverse-telecine"></a>Verwenden von Inverse Telecine

Telecine ist der Prozess der Umstellung von Film, der über 24 Frames pro Sekunde verfügt, in Video, das 60 Felder (halbframes) pro Sekunde enthält. Bei diesem Prozess werden Bilder aus jedem Filmframe in mehreren Video Feldern abgelegt.

Wenn Sie ein Video, das aus einem Film mithilfe von telecine erstellt wurde, Digital codieren, kann der Komprimierungs Vorgang Bewegungsartefakte und andere Beeinträchtigungen der Qualität verursachen. Um zu vermeiden, dass die Qualität der digitalen Ausgabe beeinträchtigt wird, unterstützt der Windows Media Video 9-Codec Inverse Telecine. Wenn Sie Inverse Telecine verwenden, rekonstruiert der Codec die ursprünglichen 24 Filmframes pro Sekunde aus dem Eingabe Video, bevor der Inhalt codiert wird.

Um Inverse Telecine verwenden zu können, müssen Sie folgende Schritte ausführen:

-   Verwenden Sie ein Profil mit einem Videostream, der auf 24 Frames pro Sekunde festgelegt ist.
-   Informieren Sie sich über die Feld Konfiguration des Eingangs Videos.

Führen Sie die folgenden Schritte aus, um Inverse Telecine für eine Eingabe für den Writer zu verwenden.

1.  Richten Sie den Writer wie gewohnt ein. Weitere Informationen finden Sie unter [Schreiben von ASF-Dateien](writing-asf-files.md).
2.  Bevor Sie mit dem Schreiben von Beispielen beginnen, erhalten Sie einen Zeiger auf die [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) -Schnittstelle, indem Sie **iwmwriter:: QueryInterface** aufrufen.
3.  Identifizieren Sie den zu rekonstruierenden Stream, indem Sie für die gewünschte Eingabe Nummer [**IWMWriterAdvanced2:: * tinputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) aufrufen. Übergeben Sie g \_ wszdeinterlacemode als Einstellung und WM \_ DM \_ deinterlace \_ invertartelecine als Wert.
4.  **Setinputsetting** wird erneut aufgerufen, um g \_ wszinitialpatternforinversetelecine festzulegen.
5.  Schreiben Sie die Datei wie gewohnt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erweiterte Themen**](advanced-topics.md)
</dt> <dt>

[**Iwmwriter-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**IWMWriterAdvanced2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)
</dt> </dl>

 

 




