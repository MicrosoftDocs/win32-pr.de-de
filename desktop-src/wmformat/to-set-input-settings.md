---
title: So legen Sie die Einstellungen
description: So legen Sie die Einstellungen
ms.assetid: 288801a7-793f-43bd-9c5a-f9e1bd86ecc3
keywords:
- Advanced Systems Format (ASF), Eingabeeinstellungen
- ASF (Advanced Systems Format), Eingabeeinstellungen
- Profile,Eingabeeinstellungen
- Codecs,Eingabeeinstellungen
- Streams, Eingabeeinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5df5b10ea6bd15ad083b26a61af037527f00576eaa6b7e1fa795ea1591417ac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447020"
---
# <a name="to-set-input-settings"></a>So legen Sie die Einstellungen

Die grundlegenden Eigenschaften von Eingabe- und Streammedien werden durch die [**WM \_ MEDIA \_ TYPE-Struktur**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) definiert. Für Eingabeformate werden die Medientypinformationen von Ihrer Anwendung festgelegt. Bei Streamformaten werden die Medientypinformationen in dem Profil festgelegt, das Sie dem Writer zuweisen. Einige Eigenschaften sind unabhängig vom Medientyp und müssen für eine Eingabe festgelegt werden, bevor mit dem Schreiben begonnen wird. Diese Eigenschaften sind Codec- und Writerfeatures, die unabhängig vom Streamtyp sind und festgelegt werden müssen, nachdem das Profil im Writer zugewiesen wurde, aber bevor mit dem Schreiben begonnen wird.

Zum Festlegen einer Eingabeeinstellung ist ein Aufruf von [**IWMWriterAdvanced2::SetInputSetting erforderlich.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) Sie können den aktuellen Wert einer Einstellung auch mit einem Aufruf von [**IWMWriterAdvanced2::GetInputSetting überprüfen.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden von Profilen mit dem Writer**](to-use-profiles-with-the-writer.md)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> <dt>

[**Schreiben von Streams**](writing-image-streams.md)
</dt> </dl>

 

 




