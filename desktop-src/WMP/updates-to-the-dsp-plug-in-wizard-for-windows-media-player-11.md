---
title: Updates des DSP-Plug-In-Assistenten für Windows Media Player 11
description: Updates des DSP-Plug-In-Assistenten für Windows Media Player 11
ms.assetid: 975c18d5-06d7-4db2-a558-bc6557963425
keywords:
- Windows Media Player Plug-Ins, Plug-In-Assistent
- Plug-Ins, Plug-In-Assistent
- Plug-Ins für die digitale Signalverarbeitung, Plug-In-Assistent
- DSP-Plug-Ins, Plug-In-Assistent
- Plug-In-Assistent
- Visual Studio,DSP-Plug-In-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2fb6ffaa9384f46e4630b16310a599de8508d953aabd4a5cdf277e91c130641
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762170"
---
# <a name="updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11"></a>Updates des DSP-Plug-In-Assistenten für Windows Media Player 11

Das Windows Media Player 11 SDK führt die folgenden Änderungen am DSP-Plug-In-Assistenten ein:

-   Plug-Ins registrieren das Threadingmodell als "Beide". Dadurch kann das Plug-In in der Media Foundation unter Windows Vista ausgeführt werden. Weitere Informationen finden *Sie in der* RGS-Projektnamendatei.

    -   Audio-DSP-Plug-Ins unterstützen die folgenden beiden zusätzlichen Formate:

    <!-- -->

    -   \_WAVE-FORMAT \_ IEEE \_ FLOAT
    -   WAVE \_ FORMAT \_ EXTENSIBLE mit dem Unterformat KSDATAFORMAT \_ SUBTYPE IEEE \_ \_ FLOAT.

    Weitere Informationen finden *Sie in der* CPP-Projektnamendatei.

    1.  Video-DSP-Plug-Ins unterstützen das NV12-Videoformat.
    2.  Plug-Ins führen zusätzliche Aufrufe an [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) und [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) mit einem neuen Plug-In-Typ aus: WMP \_ PLUGINTYPE \_ DSP \_ OUTOFPROC. Weitere Informationen finden Sie in der CPP-Datei *projectnamedll* des Projekts.
    3.  Ein zusätzliches Projekt in jeder Projektmappe erstellt eine Proxy-/Stub-DLL für die benutzerdefinierte Schnittstelle für Eigenschaftenseiteneinstellungen. Siehe *ProjektnamePS-Projekt.*
    4.  Aufrufe veralteter Methoden wurden geändert, um die neuesten Versionen zu verwenden.
    5.  Der Assistent kann ein Dual-Mode-Plug-In generieren, das sowohl als DMO fungiert, indem **IMediaObject** und als MFT implementiert werden, indem **EINETRANSFORM implementiert wird.**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DSP-Plug-In-Assistent**](dsp-plug-in-wizard.md)
</dt> </dl>

 

 




