---
title: Schreiben Streams in eine Datei
description: Schreiben Streams in eine Datei
ms.assetid: a3766f8c-aaa6-4fc5-a306-54aee71018f1
keywords:
- AVIFileCreateStream-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baaedd4103d2141ecaccde78462b2290cf5d5d37813b224c20101eacbe580d70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891760"
---
# <a name="writing-streams-to-a-file"></a>Schreiben Streams in eine Datei

Sie können auch eine Datei mit Datenströmen erstellen, indem Sie einen neuen Datenstrom in eine Datei schreiben.

Sie können einen neuen Stream in einer neuen oder vorhandenen Datei erstellen, indem Sie die [**FUNKTION AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream) verwenden. Diese Funktion definiert einen neuen Stream gemäß den in einer [**AVISTREAMINFO-Struktur**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) beschriebenen Merkmalen, erstellt eine Streamschnittstelle für den neuen Stream, erhöht die Verweisanzahl des Streams und gibt die Adresse des Streamschnittstellenzeigers zurück.

Bevor Sie den Inhalt des Streams schreiben, müssen Sie das Streamformat angeben. Sie können das Streamformat mithilfe der [**FUNKTION AVIStreamSetFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat) festlegen. Wenn Sie das Format eines Videostreams festlegen, müssen Sie diese Funktion mit einer [**BITMAPINFO-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) mit den entsprechenden Informationen angeben. Wenn Sie das Format eines Audiostreams festlegen, müssen Sie eine [**WAVEFORMAT-**](/windows/win32/api/mmreg/ns-mmreg-waveformat) oder [**WAVEFORMATEX-Struktur**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) mit den entsprechenden Informationen zur Verfügung stellen. Die Informationen, die Sie der Funktion für andere Streamtypen zur Verfügung stellen müssen, hängen vom Streamtyp und dem Streamhandler ab.

Sie können den Multimediainhalt in einen Stream schreiben, indem Sie die [**FUNKTION AVIStreamWrite**](/windows/desktop/api/Vfw/nf-vfw-avistreamwrite) verwenden. Diese Funktion kopiert Rohdaten aus einem von der Anwendung bereitgestellten Puffer in den angegebenen Stream. Der standardmäßige AVI-Dateihandler fügt Informationen an das Ende eines Streams an. Der WAVE-Standardhandler kann Waveform-Audiodaten innerhalb eines Streams sowie am Ende eines Streams schreiben.

Mithilfe der [**Funktionen AVIFileWriteData**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) und [**AVIStreamWriteData**](/windows/desktop/api/Vfw/nf-vfw-avistreamwritedata) können Sie ergänzende Informationen über die Datei oder den Stream schreiben, die nicht in der [**FUNKTION AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream) oder [**AVIStreamSetFormat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat) enthalten sind. Sie können Daten aufzeichnen, die für die gesamte Datei gelten, z. B. Copyrightinformationen und Änderungsverlauf, indem Sie **AVIFileWriteData verwenden.** Sie können streamspezifische Informationen wie Komprimierungs- und Dekomprimierungseinstellungen mithilfe von **AVIStreamWriteData aufzeichnen.** Die ergänzenden Informationen werden in separaten Blocken in der Datei gespeichert.

Sie können den Stream schließen, nachdem Sie das Schreiben in den neuen Stream abgeschlossen haben, indem Sie die [**AVIStreamRelease-Funktion**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) verwenden. Diese Funktion clears buffers used in recording the stream data, and it completes and closes any incomplete data chunks in the file.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Streamoperationen](stream-operations.md)
</dt> </dl>

 

 