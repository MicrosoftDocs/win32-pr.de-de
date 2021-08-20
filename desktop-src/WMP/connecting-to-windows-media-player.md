---
title: Herstellen einer Verbindung mit Windows Media Player
description: Herstellen einer Verbindung mit Windows Media Player
ms.assetid: c6afbd95-bcf8-438a-b854-776c543a5d51
keywords:
- Windows Media Player Plug-Ins, Registrierungseinträge
- Plug-Ins, Registrierungseinträge
- Windows Media Player-Plug-Ins, Herstellen einer Verbindung
- Plug-Ins, Herstellen einer Verbindung
- Digitale Signalverarbeitungs-Plug-Ins, Verbinden
- DSP-Plug-Ins, Herstellen einer Verbindung
- Plug-Ins für die digitale Signalverarbeitung, Registrierungseinträge
- DSP-Plug-Ins, Registrierungseinträge
- Registrierung, DSP-Plug-Ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4d266f1715147d3c7631909e8e23e3e7b1f786337c998d188968a96f6c26b62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997630"
---
# <a name="connecting-to-windows-media-player"></a>Herstellen einer Verbindung mit Windows Media Player

Windows Media Player stellt automatisch eine Verbindung mit DSP-Plug-Ins her, die installiert und ordnungsgemäß registriert wurden. DSP-Plug-Ins müssen [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) aufrufen, um die Registrierungseinträge zu erstellen, die erforderlich sind, damit Windows Media Player das Plug-In erkennen und auf der Registerkarte **Plug-Ins** des Dialogfelds Optionen auflisten kann. Um die von **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin** erstellten Registrierungseinträge zu entfernen, ruft das Plug-In [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin)auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Übersicht über DSP-Plug-In-Entwickler**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




