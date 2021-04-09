---
title: So legen Sie Eingabeeinstellungen fest
description: So legen Sie Eingabeeinstellungen fest
ms.assetid: 288801a7-793f-43bd-9c5a-f9e1bd86ecc3
keywords:
- Advanced Systems Format (ASF), Eingabeeinstellungen
- ASF (Advanced Systems Format), Eingabeeinstellungen
- Profile, Eingabeeinstellungen
- Codecs, Eingabeeinstellungen
- Streams, Eingabeeinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e7b2db64a7346cc8b9d46c48f0add79dafcac95
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948443"
---
# <a name="to-set-input-settings"></a>So legen Sie Eingabeeinstellungen fest

Die grundlegenden Eigenschaften von Eingabemedien und Streamingmedien werden durch die [**WM- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur definiert. Bei Eingabe Formaten werden die Medientyp Informationen von der Anwendung festgelegt. Bei streamformaten werden die Medientyp Informationen in dem Profil festgelegt, das Sie dem Writer zuweisen. Einige Eigenschaften sind vom Medientyp unabhängig und müssen für eine Eingabe festgelegt werden, bevor der Schreibvorgang beginnt. Bei diesen Eigenschaften handelt es sich um Codec-und Writer-Funktionen, die vom Streamtyp unabhängig sind. Sie müssen festgelegt werden, nachdem das Profil im Writer zugewiesen wurde, aber bevor das Schreiben beginnt.

Für das Festlegen einer Eingabe Einstellung ist ein aufrufsbefehl von [**IWMWriterAdvanced2:: * tinputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)erforderlich. Sie können auch den aktuellen Wert einer Einstellung mit einem Aufrufen von [**IWMWriterAdvanced2:: getinputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting)überprüfen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden von Profilen mit dem Writer**](to-use-profiles-with-the-writer.md)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> <dt>

[**Schreiben von bildstreams**](writing-image-streams.md)
</dt> </dl>

 

 




