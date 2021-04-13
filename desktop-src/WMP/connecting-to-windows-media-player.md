---
title: Herstellen einer Verbindung mit Windows Media Player
description: Herstellen einer Verbindung mit Windows Media Player
ms.assetid: c6afbd95-bcf8-438a-b854-776c543a5d51
keywords:
- Windows Media Player-Plug-ins, Registrierungseinträge
- Plug-ins, Registrierungseinträge
- Windows Media Player-Plug-ins, verbinden
- Plug-ins, verbinden
- Plug-Ins für die digitale Signalverarbeitung, verbinden
- DSP-Plug-ins, verbinden
- Plug-Ins für die digitale Signalverarbeitung, Registrierungseinträge
- DSP-Plug-ins, Registrierungseinträge
- Registrierung, DSP-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fa0851e271631e2c37bf716c427b5af34ade14
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389839"
---
# <a name="connecting-to-windows-media-player"></a><span data-ttu-id="0cb96-112">Herstellen einer Verbindung mit Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="0cb96-112">Connecting to Windows Media Player</span></span>

<span data-ttu-id="0cb96-113">Windows Media Player stellt automatisch eine Verbindung mit DSP-Plug-ins her, die installiert und ordnungsgemäß registriert wurden.</span><span class="sxs-lookup"><span data-stu-id="0cb96-113">Windows Media Player automatically connects to DSP plug-ins that have been installed and properly registered.</span></span> <span data-ttu-id="0cb96-114">DSP-Plug-Ins müssen [iwmpmediapluginregistrar:: wmpregisterplayerplugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) aufrufen, um die Registrierungseinträge zu erstellen, die erforderlich sind, damit Windows Media Player das Plug-in erkennen und auf der Registerkarte **Plug-ins** im Dialogfeld Optionen auflisten kann.</span><span class="sxs-lookup"><span data-stu-id="0cb96-114">DSP plug-ins must call [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) to create the registry entries necessary to allow Windows Media Player to recognize the plug-in and to list it on the **Plug-ins** tab of the Options dialog box.</span></span> <span data-ttu-id="0cb96-115">Zum Entfernen der Registrierungseinträge, die von **iwmpmediapluginregistrators:: wmpregisterplayerplugin** erstellt wurden, ruft das Plug-in [iwmpmediapluginregistrar:: wmpunregisterplayerplugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin)auf.</span><span class="sxs-lookup"><span data-stu-id="0cb96-115">To remove the registry entries created by **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin**, the plug-in calls [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cb96-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0cb96-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cb96-117">**Übersicht über den DSP-Plug-in-Entwickler**</span><span class="sxs-lookup"><span data-stu-id="0cb96-117">**DSP Plug-in Developer Overview**</span></span>](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




