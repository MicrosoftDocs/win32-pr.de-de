---
title: Updates des DSP-Plug-in-Assistenten für Windows Media Player 11
description: Updates des DSP-Plug-in-Assistenten für Windows Media Player 11
ms.assetid: 975c18d5-06d7-4db2-a558-bc6557963425
keywords:
- Windows Media Player-Plug-ins, Plug-in-Assistent
- Plug-ins, Plug-in-Assistent
- Plug-Ins für die digitale Signalverarbeitung, Plug-in-Assistent
- DSP-Plug-ins, Plug-in-Assistent
- Plug-in-Assistent
- Visual Studio, DSP-Plug-in-Assistent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8efe798a3c324f9ecfac0a5b6021db4ea5abdf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389879"
---
# <a name="updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11"></a>Updates des DSP-Plug-in-Assistenten für Windows Media Player 11

Das Windows Media Player 11 SDK führt die folgenden Änderungen am DSP-Plug-in-Assistenten ein:

-   Plug-Ins registrieren das Threading Modell als "both". Dadurch kann das Plug-in in der Media Foundation Pipeline unter Windows Vista ausgeführt werden. Weitere Informationen finden Sie in der Datei *ProjectName*. rgs.

    -   Audiodsp-Plug-ins haben Unterstützung für die folgenden zwei zusätzlichen Formate:

    <!-- -->

    -   "Wave \_ Format \_ IEEE \_ float"
    -   Das Wave- \_ Format ist \_ erweiterbar mit dem unter Format "ksdataformat"- \_ Untertyp \_ IEEE \_ float.

    Weitere Informationen finden Sie in der Datei *ProjectName*. cpp.

    1.  Video DSP-Plug-ins haben Unterstützung für das Videoformat NV12.
    2.  Plug-ins führen zusätzliche Aufrufe an [iwmpmediapluginregistrar:: wmpregisterplayerplugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) und [iwmpmediapluginregistrar:: wmpunregisterplayerplugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) durch einen neuen Plug-in-Typ aus: WMP \_ PlugInType \_ DSP \_ oudefproc. Weitere Informationen finden Sie in der Projektdatei *projectnamedll*. cpp.
    3.  Ein zusätzliches Projekt in jeder Projekt Mappe erstellt eine Proxy-/Stub-DLL für die benutzerdefinierte Schnittstelle der Eigenschaften Seiteneinstellungen. Weitere Informationen finden Sie Unterprojekt *Name* .
    4.  Aufrufe von veralteten Methoden wurden geändert, um die neuesten Versionen zu verwenden.
    5.  Der Assistent kann ein Dual-Mode-Plug-in generieren, das sowohl als DMO als auch durch Implementieren von **imediaobject** und als MFT durch Implementieren von **imftransform** funktioniert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DSP-Plug-in-Assistent**](dsp-plug-in-wizard.md)
</dt> </dl>

 

 




