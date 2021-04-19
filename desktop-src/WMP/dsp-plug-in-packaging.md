---
title: Plug-in-Paket für DSP
description: Plug-in-Paket für DSP
ms.assetid: 5d40a39b-0fe8-4f77-9465-8e31d1f2708e
keywords:
- Windows Media Player-Plug-ins, Media Foundation Pipeline
- Plug-ins, Media Foundation Pipeline
- Plug-Ins für die digitale Signalverarbeitung, Media Foundation Pipeline
- DSP-Plug-ins, Media Foundation Pipeline
- Media Foundation Pipeline
- Windows Media Player-Plug-ins, DirectShow-Pipeline
- Plug-ins, DirectShow-Pipeline
- Plug-Ins für die digitale Signalverarbeitung, DirectShow-Pipeline
- DSP-Plug-ins, DirectShow-Pipeline
- DirectShow-Pipeline
- Plug-Ins für die digitale Signalverarbeitung, Basic
- DSP-Plug-ins, Basic
- Windows Media Player-Plug-ins, Basic DSP
- Plug-ins, Basic DSP
- grundlegende DSP-Plug-ins
- Windows Media Player-Plug-ins, Dual-Modus-DSP
- Plug-ins, im Dual-Modus-DSP
- Plug-Ins für die digitale Signalverarbeitung, Dual-Mode
- DSP-Plug-ins, Dual-Mode
- Dual-Modus-DSP-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62535abe0d82975bf07fef178ac43cf066c6afbd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339079"
---
# <a name="dsp-plug-in-packaging"></a>Plug-in-Paket für DSP

Windows Media Player rendert Audiodaten und Videos mithilfe einer der folgenden Pipelines.

-   DirectShow
-   Media Foundation

In Microsoft Windows XP und früheren Versionen verwendet der Player DirectShow. In Windows Vista verwendet der Player manchmal DirectShow und verwendet manchmal Media Foundation.

Ein DSP-Plug-in, das in der DirectShow-Pipeline ausgeführt werden soll, wird als *einfaches DSP-Plug-in* bezeichnet. Grundlegende DSP-Plug-ins fungieren als DirectX-Medienobjekt (DMO). Ein einfaches DSP-Plug-in kann nativ in der DirectShow-Pipeline ausgeführt werden und kann auch in der Media Foundation Pipeline innerhalb eines von Media Foundation bereitgestellten Wrappers ausgeführt werden.

Ein DSP-Plug-in, das für die systemeigene (kein Wrapper erforderlich) in den DirectShow-und Media Foundation-Pipelines entwickelt wurde, wird als *Plug-in für das Dual-Modus-DSP* bezeichnet. Ein bidirektionales DSP-Plug-in kann als DMO oder als Media Foundation Transformation (MFT) fungieren.

Ein DSP-Plug-in ist ein COM-Objekt, das als selbst registrierte DLL-Datei verpackt ist. Die Schnittstellen, die das Plug-in implementiert, hängen davon ab, ob das Plug-in als einfaches DSP-Plug-in oder als ein bidirektionales DSP-Plug-in entworfen wurde. Ausführliche Informationen zu den Schnittstellen, die von DSP-Plug-Ins implementiert werden müssen, finden Sie unter [erforderliche Schnittstellen](required-interfaces.md).

Ein DSP-Plug-in, das in der Media Foundation Pipeline (System intern oder umschließt) ausgeführt wird, muss sein Threading Modell als "beides" registrieren. Ausführliche Informationen zu Registrierungs unter Schlüsseln und Einträgen, die DSP-Plug-ins zugeordnet sind, finden Sie unter [Registrieren von DSP-Plug-ins](registering-dsp-plug-ins.md).

Ein DSP-Plug-in, das benutzerdefinierte Schnittstellen implementiert und in der Media Foundation Pipeline (nativ oder umschließt) ausgeführt wird, muss mit einer Proxy-Stub. dll-Datei gekoppelt werden, die die benutzerdefinierten Schnittstellen über Prozess Grenzen hinweg Mars Hallen kann. Weitere Informationen zur Proxy-Stub-Komponente finden Sie unter [Aktualisieren vorhandener DSP-Plug-ins](updating-existing-dsp-plug-ins.md) und [Updates des DSP-Plug-in-Assistenten für Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).

DSP-Plug-in-Objekte dürfen nicht als Singletons erstellt werden. Windows Media Player muss mehrere separate Instanzen eines bestimmten DSP-Plug-ins erstellen können.

DSP-Plug-ins, die im Windows Vista-PMP (geschützter Medien Pfad) ausgeführt werden, müssen signiert sein. Weitere Informationen finden Sie unter [Code Signing for Protected Media Components in Windows Vista](/windows-hardware/test/hlk/).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Übersicht über den DSP-Plug-in-Entwickler**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 