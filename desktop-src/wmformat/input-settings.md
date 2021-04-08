---
title: Eingabeeinstellungen
description: Eingabeeinstellungen
ms.assetid: 23adbb64-5733-4198-8f2b-d02052ddb848
keywords:
- Windows Media-Format-SDK, globale Konstanten
- Advanced Systems Format (ASF), globale Konstanten
- ASF (Advanced Systems Format), globale Konstanten
- Globale Konstanten, Liste der
- Windows Media-Format-SDK, Konstanten
- Advanced Systems Format (ASF), Konstanten
- ASF (Advanced Systems Format), Konstanten
- Konstanten, Liste der
- Windows Media-Format-SDK, Eingabeeinstellungen
- Advanced Systems Format (ASF), Eingabeeinstellungen
- ASF (Advanced Systems Format), Eingabeeinstellungen
- Eingabeeinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70ef0db6a3d9371bd1c8e9a20157f5f0ac73b3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038523"
---
# <a name="input-settings"></a>Eingabeeinstellungen

Die folgenden globalen Konstanten werden verwendet, um Eingabeeinstellungen für den Writer zu identifizieren.



| Globale Konstante                        | WMT \_ attr- \_ DataType                                                                                                                       | Beschreibung von *pValue*                                                                                                                                                                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszdeinterlacemode                  | **WMT \_ Geben Sie \_ DWORD** auf einen der Werte in der Mode-Tabelle im Thema [zu deinterlace-Video](to-deinterlace-video.md)ein.            | Gibt bei Festlegung den Typ von Zeilen Sprung Inhalt der Eingabe an. Weitere Informationen finden [Sie unter dem deinterlace-Video](to-deinterlace-video.md).                                                                                                                            |
| g \_ wszfixedframerate                   | **WMT- \_ Typ \_ bool**                                                                                                                       | Wenn der Wert auf true festgelegt ist, wird der Codec angewiesen, während der Codierung keine Frames abzulegen. Dies führt dazu, dass die [*Framerate*](wmformat-glossary.md) des Ausgabevideo Datenstroms konstant ist. Die Framerate des Eingabestreams muss nicht konstant sein. |
| g \_ wszinitialpatternforinvertartelecine | **WMT \_ Geben Sie \_ DWORD** auf einen der Werte in der ursprünglichen Muster Tabelle im Thema [zu deinterlace-Video](to-deinterlace-video.md)ein. | Wenn der Deinterlacing-Modus auf WM \_ DM \_ Deinterlacing \_ inversetelecine festgelegt ist, kann dieser so festgelegt werden, dass er das Muster der [*telecine*](wmformat-glossary.md) -Eingabe angibt. Weitere Informationen finden [Sie unter dem deinterlace-Video](to-deinterlace-video.md).        |
| g \_ wszinterlacedcoding                 | **WMT- \_ Typ \_ bool**                                                                                                                       | Wenn der Wert auf true festgelegt ist, wird angegeben, dass der Codec den Stream als Zeilen Sprung-Inhalt codieren soll. Weitere Informationen finden [Sie unter So verwenden Sie](to-use-interlaced-video.md)ein Zeilen Sprung Video.                                                                                       |
| g \_ wszjpgcompressionquality           | **WMT- \_ Typ \_ DWORD**                                                                                                                      | Gibt die JPEG-Qualitätsstufe (von 1 bis 100) an, die für die Eingabe verwendet werden soll.                                                                                                                                                                                               |
| g \_ wszwatermarkclsid                   | **WMT- \_ Typ- \_ GUID**                                                                                                                       | Der Wert wird auf die Wasserzeichen-GUID festgelegt.                                                                                                                                                                                                                                 |
| g \_ wszwatermarkconfig                  | **WMT \_ - \_ Typzeichenfolge**                                                                                                                     | Der Wert wird auf die Wasserzeichen Konfiguration festgelegt. Dieser Wert variiert je nach dem Wasserzeichen DMO. Weitere Informationen finden Sie in der Dokumentation des Wasserzeichen Systems.                                                                                   |



 

> [!Note]  
> Die für einen Stream konfigurierten Eingabeeinstellungen werden in der geschriebenen Datei nicht beibehalten. Wenn Sie möchten, dass Ihr benutzerdefinierter Reader Zugriff auf diese Codierungs Parameter hat, müssen Sie benutzerdefinierte Attribute erstellen, um Sie im Dateiheader zu speichern.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMWriterAdvanced2:: getinputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting)
</dt> <dt>

[**IWMWriterAdvanced2:: abputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)
</dt> </dl>

 

 




