---
description: VMR-Unterstützung für DirectX-Videobeschleunigung
ms.assetid: 4bb5612d-3841-4920-a5ef-39ce357a6d1c
title: VMR-Unterstützung für DirectX-Videobeschleunigung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9f1998f5e55d7aa4d191ac2a312995db69d9e248349034e119ded8e99774c43
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119696730"
---
# <a name="vmr-support-for-directx-video-acceleration"></a>VMR-Unterstützung für DirectX-Videobeschleunigung

DirectX-Videobeschleunigung ist eine Anwendungsprogrammierschnittstelle (Application Programming Interface, API) und eine entsprechende Gerätetreiberschnittstelle (Device Driver Interface, DDI) für die Hardwarebeschleunigung der Verarbeitung digitaler Videodecodierung mit Unterstützung von Alphablending für Zwecke wie die Unterstützung von DVD-Unteraufnahmen. DirectX VA ist im Windows DDK dokumentiert. Die [**IAMVideoAccelerator-Schnittstelle,**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) die den Benutzermoduszugriff auf DirectX VA-Funktionen auf einem Hardwaregerät ermöglicht, ist in diesem SDK dokumentiert.

Der VMR unterstützt [**IAMVideoAccelerator,**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator)und seine Implementierung ist mit dem alten Overlay-Mixer mit Ausnahme eines wichtigen Unterschieds identisch. Die Overlay-Mixer garantiert, dass die Ausgabe in einer Überlagerungsoberfläche gerendert wird, während der VMR die Ausgabe zur weiteren Verarbeitung senden kann, z. B. einen 3D-Vorgang, oder die Ausgabe an eine Offscreenoberfläche senden kann, die dann auf die primäre Oberfläche aufgeblittet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur DirectX-Videobeschleunigung](about-directx-video-acceleration.md)
</dt> </dl>

 

 



