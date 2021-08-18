---
title: Eingabe Einstellungen
description: Eingabe Einstellungen
ms.assetid: 23adbb64-5733-4198-8f2b-d02052ddb848
keywords:
- Windows Medienformat-SDK, globale Konstanten
- Advanced Systems Format (ASF), globale Konstanten
- ASF (Advanced Systems Format), globale Konstanten
- globale Konstanten, Liste der
- Windows Medienformat-SDK, Konstanten
- Advanced Systems Format (ASF), Konstanten
- ASF (Advanced Systems Format), Konstanten
- Konstanten, Liste der
- Windows Medienformat-SDK, Eingabeeinstellungen
- Advanced Systems Format (ASF), Eingabeeinstellungen
- ASF (Advanced Systems Format), Eingabeeinstellungen
- Eingabeeinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ad72a8a5cc70dc28dcaa7be1e24b721e0b3f644e7694ea5c00d87ba2418846a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701805"
---
# <a name="input-settings"></a>Eingabe Einstellungen

Die folgenden globalen Konstanten werden verwendet, um Eingabeeinstellungen für den Writer zu identifizieren.



| Globale Konstante                        | WMT \_ \_ ATTR-DATENTYP                                                                                                                       | Beschreibung von *pValue*                                                                                                                                                                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| g \_ wszDeinterlaceMode                  | **WMT \_ TYPE \_ DWORD** wird auf einen der Werte in der Modetabelle im Thema [To Deinterlace Video](to-deinterlace-video.md)festgelegt.            | Gibt bei Festlegung den Typ des Interlacinginhalts der Eingabe an. Weitere Informationen finden Sie unter [Deinterlace Video](to-deinterlace-video.md).                                                                                                                            |
| g \_ wszFixedFrameRate                   | **\_WMT-TYP \_ BOOL**                                                                                                                       | Wenn diese Einstellung auf TRUE festgelegt ist, weist den Codec an, während der Codierung keine Frames zu löschen. Dies führt dazu, dass die [*Bildfrequenz*](wmformat-glossary.md) des Ausgabevideostreams konstant ist. Die Bildfrequenz des Eingabestreams muss nicht konstant sein. |
| g \_ wszInitialPatternForInverseTelequart | **WMT \_ TYPE \_ DWORD** wird auf einen der Werte in der anfänglichen Mustertabelle im Thema [To Deinterlace Video](to-deinterlace-video.md)festgelegt. | Wenn der Deinterlacemodus auf WM \_ DM \_ DEINTERLACE \_ INVERSETELECHIN festgelegt ist, kann dies festgelegt werden, um das Muster der [*Telekopeingabe*](wmformat-glossary.md) anzugeben. Weitere Informationen finden Sie unter [Deinterlace Video](to-deinterlace-video.md).        |
| g \_ wszInterlacedCoding                 | **\_WMT-TYP \_ BOOL**                                                                                                                       | Gibt bei Festlegung auf True an, dass der Codec den Stream als Interlacinginhalt codieren soll. Weitere Informationen finden Sie unter [To Use Interlaced Video](to-use-interlaced-video.md).                                                                                       |
| g \_ wszJPEGCompressionQuality           | **\_WMT-TYP \_ DWORD**                                                                                                                      | Gibt den JPEG-Qualitätsgrad (von 1 bis 100) an, der für die Eingabe verwendet werden soll.                                                                                                                                                                                               |
| g \_ wszWatermarkCLSID                   | **\_ \_ WMT-TYP-GUID**                                                                                                                       | Der Wert wird auf die Wasserzeichen-GUID festgelegt.                                                                                                                                                                                                                                 |
| g \_ wszWatermarkConfig                  | **\_ \_ WMT-TYPZEICHENFOLGE**                                                                                                                     | Der Wert wird auf die Wasserzeichenkonfiguration festgelegt. Dieser Wert variiert abhängig von der Wasserzeichen-DMO. Weitere Informationen finden Sie in der Dokumentation des Wasserzeichensystems.                                                                                   |



 

> [!Note]  
> Die für einen Stream konfigurierten Eingabeeinstellungen werden nicht in der geschriebenen Datei beibehalten. Wenn Ihr benutzerdefinierter Reader Zugriff auf diese Codierungsparameter haben soll, müssen Sie benutzerdefinierte Attribute erstellen, um sie im Dateiheader zu speichern.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMWriterAdvanced2::GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting)
</dt> <dt>

[**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)
</dt> </dl>

 

 




