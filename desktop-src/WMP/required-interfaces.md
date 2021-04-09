---
title: Erforderliche Schnittstellen (Windows Media Player SDK)
description: Erforderliche Schnittstellen
ms.assetid: 202d5769-edff-46df-bc05-bbb630a8f3f4
keywords:
- Windows Media Player-Plug-ins, Schnittstellen
- Plug-ins, Schnittstellen
- Plug-Ins für die digitale Signalverarbeitung, Schnittstellen
- DSP-Plug-ins, Schnittstellen
- Schnittstellen, DSP-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9c6923af513f2d241955b508f0872f85a4b020
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103858602"
---
# <a name="required-interfaces-windows-media-player-sdk"></a>Erforderliche Schnittstellen (Windows Media Player SDK)

Windows Media Player rendert Audiodaten und Videos mithilfe einer der folgenden Pipelines.

-   DirectShow
-   Media Foundation

In Microsoft Windows XP und früheren Versionen verwendet der Player DirectShow. In Windows Vista verwendet der Player manchmal DirectShow und verwendet manchmal Media Foundation.

Ein DSP-Plug-in implementiert einige oder alle der folgenden Schnittstellen:

-   **Imediaobject**
-   **Iwmppluginenable**
-   **IMF-Transformation**
-   **IMF-Dienst**
-   **ISpecifyPropertyPages**

Ein Plug-in, das **imediaobject** und **iwmppluginenable** implementiert, kann in der DirectShow-Pipeline ausgeführt werden. Sie kann auch in der Media Foundation Pipeline in einem von Media Foundation bereitgestellten Wrapper ausgeführt werden. Ein Plug-in dieses Typs wird als Microsoft DirectX Media Object (DMO) bezeichnet. Es ist üblich, ein DMO als analog zu einem Filter Objekt in DirectShow zu betrachten. Die DMO-Dokumentation befindet sich im Abschnitt DirectShow des Windows SDK.

Ein Plug-in, das **IMF Transform** und **IMF-Service** implementiert, kann nativ (kein Wrapper erforderlich) in der Media Foundation Pipeline ausgeführt werden. Ein Plug-in dieses Typs wird als "Media Foundation Transform (MFT)" bezeichnet. Die MFT-Dokumentation befindet sich im Abschnitt Media Foundation des Windows SDK.

Ein Plug-in, das " **imediaobject**", " **iwmppluginenable**", " **IMF Transform**" und " **IMF GetService** " implementiert, kann in der Pipeline "DirectShow" ausgeführt werden und kann auch nativ in der Media Foundation Pipeline ausgeführt werden. Diese Art von Plug-in, das als *Plug-in für den Dual-Mode-DSP* bezeichnet wird, kann die Rolle eines DMO oder einer MFT wiedergeben.

Wenn Windows Media Player ein bidirektionales DSP-Plug-in in der Media Foundation Pipeline verwendet, fragt es zuerst die **IMF Transform** -Schnittstelle ab. Wenn diese Abfrage fehlschlägt, führt Windows Media Player Abfragen für die **imediaobject** -Schnittstelle aus. Wenn die **imediaobject** -Abfrage erfolgreich ist, wird das Plug-in umschließt und der Media Foundation Pipeline hinzugefügt.

Unabhängig von der Pipeline muss jedes DSP-Plug-in, das es dem Benutzer ermöglicht, Eigenschaften festzulegen, **ISpecifyPropertyPages** implementieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Übersicht über den DSP-Plug-in-Entwickler**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**DSP-Plug-in-Schnittstellen**](dsp-plug-in-interfaces.md)
</dt> <dt>

[**Plug-in-Paket für DSP**](dsp-plug-in-packaging.md)
</dt> </dl>

 

 




