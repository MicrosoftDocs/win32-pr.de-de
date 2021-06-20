---
title: Erforderliche Schnittstellen (Windows Media Player SDK)
description: Erfahren Sie mehr über die erforderlichen Schnittstellen, Windows Media Player directshow oder Media Foundation.
ms.assetid: 202d5769-edff-46df-bc05-bbb630a8f3f4
keywords:
- Windows Media Player-Plug-Ins,Schnittstellen
- Plug-Ins, Schnittstellen
- Plug-Ins für die digitale Signalverarbeitung, Schnittstellen
- DSP-Plug-Ins, Schnittstellen
- Schnittstellen,DSP-Plug-Ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d27a0c0ed56db5f35c8cde8203fcf99a81a9260
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406093"
---
# <a name="required-interfaces-windows-media-player-sdk"></a>Erforderliche Schnittstellen (Windows Media Player SDK)

Windows Media Player rendert Audio- und Videodaten mithilfe einer der folgenden Pipelines.

-   Directshow
-   Media Foundation

In Microsoft Windows XP und früher verwendet der Player DirectShow. In Windows Vista verwendet der Player manchmal DirectShow und manchmal Media Foundation.

Ein DSP-Plug-In implementiert einige oder alle der folgenden Schnittstellen:

-   **IMediaObject**
-   **IWMPPluginEnable**
-   **VORÜBERSETZUNGTransform**
-   **GEGETService**
-   **Ispecifypropertypages**

Ein Plug-In, das **IMediaObject** und **IWMPPluginEnable** implementiert, kann in der DirectShow-Pipeline ausgeführt werden. Sie kann auch in der Media Foundation Pipeline in einem wrapper ausgeführt werden, der von Media Foundation. Ein Plug-In dieses Typs wird als Microsoft DirectX Media Object (DMO) bezeichnet. Es ist üblich, einen DMO als analog zu einem Filterobjekt in DirectShow zu sehen. Die DMO-Dokumentation befindet sich im Abschnitt DirectShow des Windows SDK.

Ein Plug-In, das **DIEBTRANSFORM** und **DEN -DIENST** implementiert, kann nativ (kein Wrapper erforderlich) in der Media Foundation ausgeführt werden. Ein Plug-In dieses Typs wird als Media Foundation Transform (MFT) bezeichnet. Die MFT-Dokumentation befindet sich im Media Foundation Abschnitt der Windows SDK.

Ein Plug-In, das **IMediaObject,** **IWMPPluginEnable,** **CISTransform** **undGEGETService** implementiert, kann in der DirectShow-Pipeline ausgeführt werden und kann auch nativ in der Media Foundation ausgeführt werden. Dieser Plug-In-Typ, der als *DSP-Plug-In* im dualen Modus bezeichnet wird, kann die Rolle eines DMO- oder MFT-Plug-Ins spielen.

Wenn Windows Media Player ein DSP-Plug-In im dualen Modus in der pipeline Media Foundation verwendet, fragt es zuerst die **BERTRANSFORM-Schnittstelle** ab. Wenn diese Abfrage fehlschlägt, Windows Media Player Abfragen für die **IMediaObject-Schnittstelle.** Wenn die **IMediaObject-Abfrage** erfolgreich ist, wird das Plug-In umschlossen und der Media Foundation hinzugefügt.

Unabhängig von der Pipeline muss jedes DSP-Plug-In, das dem Benutzer das Festlegen von Eigenschaften ermöglicht, **ISpecifyPropertyPages implementieren.**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Übersicht über DSP-Plug-In-Entwickler**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**DSP-Plug-In-Schnittstellen**](dsp-plug-in-interfaces.md)
</dt> <dt>

[**DSP-Plug-In-Paketierung**](dsp-plug-in-packaging.md)
</dt> </dl>

 

 




