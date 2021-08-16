---
title: DSP-Plug-In-Paketierung
description: DSP-Plug-In-Paketierung
ms.assetid: 5d40a39b-0fe8-4f77-9465-8e31d1f2708e
keywords:
- Windows Media Player-Plug-Ins, Media Foundation Pipeline
- Plug-Ins, Media Foundation Pipeline
- Digitale Signalverarbeitungs-Plug-Ins, Media Foundation Pipeline
- DSP-Plug-Ins, Media Foundation Pipeline
- Media Foundation Pipeline
- Windows Media Player-Plug-Ins, DirectShow-Pipeline
- Plug-Ins, DirectShow-Pipeline
- Digitale Signalverarbeitungs-Plug-Ins, DirectShow-Pipeline
- DSP-Plug-Ins, DirectShow-Pipeline
- DirectShow-Pipeline
- Digitale Signalverarbeitungs-Plug-Ins, Basic
- DSP-Plug-Ins, Basic
- Windows Media Player-Plug-Ins, DSP basic
- Plug-Ins, DSP basic
- Grundlegende DSP-Plug-Ins
- Windows Media Player-Plug-Ins, Dualmodus-DSP
- Plug-Ins, Dualmodus-DSP
- Digitale Signalverarbeitungs-Plug-Ins, Dualmodus
- DSP-Plug-Ins, Dualmodus
- Dualmodus-DSP-Plug-Ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2bd87e1729b4d8759f3b9f1d7d4d7993660512d49c34ea9bf9aa34802b69cd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749505"
---
# <a name="dsp-plug-in-packaging"></a>DSP-Plug-In-Paketierung

Windows Media Player rendert Audio- und Videodaten mithilfe einer der folgenden Pipelines.

-   Directshow
-   Media Foundation

In Microsoft Windows XP und früher verwendet der Player DirectShow. In Windows Vista verwendet der Player manchmal DirectShow und manchmal Media Foundation.

Ein DSP-Plug-In, das für die Ausführung in der DirectShow-Pipeline entwickelt wurde, wird als *einfaches DSP-Plug-In* bezeichnet. Ein einfaches DSP-Plug-In fungiert als DirectX-Medienobjekt (DMO). Ein einfaches DSP-Plug-In kann nativ in der DirectShow-Pipeline und auch in der Media Foundation Pipeline innerhalb eines Wrappers ausgeführt werden, der von Media Foundation bereitgestellt wird.

Ein DSP-Plug-In, das sowohl in directShow- als auch in Media Foundation Pipelines nativ ausgeführt werden kann (kein Wrapper erforderlich), wird als *Dualmodus-DSP-Plug-In* bezeichnet. Ein Dualmodus-DSP-Plug-In kann als DMO oder als Media Foundation Transform (MFT) fungieren.

Ein DSP-Plug-In ist ein COM-Objekt, das als selbst registrierende .dll-Datei gepackt ist. Welche Schnittstellen das Plug-In implementiert, hängt davon ab, ob das Plug-In als einfaches DSP-Plug-In oder als Dual-Mode-DSP-Plug-In entworfen wurde. Ausführliche Informationen zu den Schnittstellen, die DSP-Plug-Ins implementieren müssen, finden Sie unter [Erforderliche Schnittstellen.](required-interfaces.md)

Ein DSP-Plug-In, das in der Media Foundation Pipeline ausgeführt wird (entweder nativ oder umschlossen), muss sein Threadingmodell als "Beide" registrieren. Ausführliche Informationen zu Registrierungsunterschlüsseln und Einträgen, die DSP-Plug-Ins zugeordnet sind, finden Sie unter [Registrieren von DSP-Plug-Ins.](registering-dsp-plug-ins.md)

Ein DSP-Plug-In, das benutzerdefinierte Schnittstellen implementiert und in der Media Foundation Pipeline ausgeführt wird (entweder nativ oder umschlossen), muss mit einem Proxystub .dll Datei gekoppelt werden, mit der die benutzerdefinierten Schnittstellen über Prozessgrenzen hinweg gemarshallt werden können. Informationen zur Proxystubkomponente finden Sie unter [Aktualisieren vorhandener DSP-Plug-Ins](updating-existing-dsp-plug-ins.md) und [Updates für den DSP-Plug-In-Assistenten für Windows Media Player 11.](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md)

DSP-Plug-In-Objekte dürfen nicht als Singletons erstellt werden. Windows Media Player müssen mehrere separate Instanzen eines bestimmten DSP-Plug-Ins erstellen können.

DSP-Plug-Ins, die in Windows Vista Protected Media Path (PMP) ausgeführt werden, müssen signiert sein. Weitere Informationen finden Sie unter [Codesignieren von Geschützten Medienkomponenten in Windows Vista.](/windows-hardware/test/hlk/)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Übersicht über DSP-Plug-In-Entwickler**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 