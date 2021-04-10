---
description: VMR-Unterstützung für die DirectX-Video Beschleunigung
ms.assetid: 4bb5612d-3841-4920-a5ef-39ce357a6d1c
title: VMR-Unterstützung für die DirectX-Video Beschleunigung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ed2e9f4907fdc653ccea6b6244c744073a9d157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753809"
---
# <a name="vmr-support-for-directx-video-acceleration"></a>VMR-Unterstützung für die DirectX-Video Beschleunigung

Die DirectX-Video Beschleunigung ist eine Anwendungsprogrammierschnittstelle (Application Programming Interface, API) und eine entsprechende Gerätetreiber Schnittstelle (DDI) für die Hardwarebeschleunigung der Verarbeitung digitaler Video Decodierung mit Unterstützung von Alpha Blending für solche Zwecke wie die Unterstützung von DVD-Unterbildern. DirectX VA ist im Windows-DDK dokumentiert. Die [**iamvideoaccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator) -Schnittstelle, die den Benutzermodus-Zugriff auf die DirectX-VA-Funktionalität auf einem Hardware Gerät bietet, ist in diesem SDK dokumentiert.

VMR unterstützt [**iamvideoaccelerator**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoaccelerator), und die Implementierung ist mit dem alten Überlagerungs-Mixer identisch, mit Ausnahme eines wichtigen Unterschieds. Der Überlagerungs Mixer garantierte, dass die Ausgabe in eine Überlagerungs Oberfläche gerendert wird, während der VMR die Ausgabe zur weiteren Verarbeitung senden kann, z. b. ein 3D-Vorgang, oder die Ausgabe an eine Offscreen-Oberfläche senden kann, die dann auf die primäre Oberfläche geblittet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur DirectX-Video Beschleunigung](about-directx-video-acceleration.md)
</dt> </dl>

 

 



