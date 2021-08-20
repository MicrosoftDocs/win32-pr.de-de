---
title: Verwenden von Inverse Telecine
description: Verwenden von Inverse Telecine
ms.assetid: 7752d1ac-34b1-446a-a69c-29463c9e10f7
keywords:
- Windows Medienformat-SDK, umgekehrtes Telekopieren
- Windows Medienformat-SDK, Telekopieren
- Advanced Systems Format (ASF), umgekehrtes Telekop
- ASF (Advanced Systems Format), umgekehrtes Telekop
- Advanced Systems Format (ASF), telekop
- ASF (Advanced Systems Format), Telekopieren
- umgekehrte Telekope
- Telecine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7885caffea83460d73b1eca26dbfd94eb50d99ac4aa8589113875ffc4358c029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585320"
---
# <a name="to-use-inverse-telecine"></a>Verwenden von Inverse Telecine

Telearbeit ist der Prozess der Konvertierung von Film mit 24 Bildern pro Sekunde in Video mit 60 Feldern (halber Frames) pro Sekunde. Dieser Prozess fügt Bilder aus jedem Filmrahmen in mehrere Videofelder ein.

Wenn Sie ein Video digital codieren, das mithilfe von Telekop aus dem Film erstellt wurde, kann der Komprimierungsprozess Bewegungsartefakte und andere Qualitätsbeeinträchtigungen verursachen. Um die Qualität der digitalen Ausgabe nicht zu beeinträchtigen, unterstützt der Windows Media Video 9-Codec umgekehrte Telekope. Bei Verwendung von inversem Telekop rekonstruiert der Codec die ursprünglichen 24 Filmframes pro Sekunde aus dem Eingabevideo, bevor der Inhalt codiert wird.

Um inverse Telekope verwenden zu können, müssen Sie:

-   Verwenden Sie ein Profil mit einem Videostream, der auf 24 Frames pro Sekunde festgelegt ist.
-   Kennen Sie die Feldkonfiguration des Eingabevideos.

Führen Sie die folgenden Schritte aus, um inverse Telekope für eine Eingabe an den Writer zu verwenden.

1.  Richten Sie den Writer wie gewohnt ein. Weitere Informationen finden Sie unter [Schreiben von ASF-Dateien.](writing-asf-files.md)
2.  Rufen Sie vor dem Schreiben von Beispielen einen Zeiger auf die [**IWMWriterAdvanced2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) ab, indem **Sie IWMWriter::QueryInterface** aufrufen.
3.  Identifizieren Sie den zu rekonstruierten Stream, indem [**Sie IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) für die gewünschte Eingabenummer aufrufen. Übergeben Sie g \_ wszDeinterlaceMode als Einstellung und WM \_ DM \_ DEINTERLACE \_ INVERSETELEEINANDER als Wert.
4.  Rufen Sie **SetInputSetting** erneut auf, um g \_ wszInitialPatternForInverseTelequart festzulegen.
5.  Schreiben Sie die Datei wie gewohnt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Weiterführende Themen**](advanced-topics.md)
</dt> <dt>

[**IWMWriter-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**IWMWriterAdvanced2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)
</dt> </dl>

 

 




