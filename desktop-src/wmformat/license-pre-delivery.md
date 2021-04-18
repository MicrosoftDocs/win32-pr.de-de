---
title: Vorab Bereitstellung von Lizenzen
description: Vorab Bereitstellung von Lizenzen
ms.assetid: 184d9118-5b60-4871-a1e3-75c45153460d
keywords:
- Windows Media-Format-SDK, vorab Bereitstellung von Lizenzen
- Windows Media-Format-SDK, Lizenzen
- Digital Rights Management (DRM), vorab Bereitstellung von Lizenzen
- DRM (Digital Rights Management), vorab Bereitstellung von Lizenzen
- Digital Rights Management (DRM), Lizenzen
- DRM (Digital Rights Management), Lizenzen
- Erweiterte APIs für den DRM-Client, vorab Bereitstellung von Lizenzen
- Erweiterte Client-APIs, vorab Bereitstellung von Lizenzen
- vorab Bereitstellung von Lizenzen
- Lizenzen, vorab Bereitstellung von Lizenzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7691c48233ed986d85c47ae9c99df078d0ed1039
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337667"
---
# <a name="license-pre-delivery"></a>Vorab Bereitstellung von Lizenzen

Die vorab Bereitstellung der Lizenz ist der Prozess, der zum vorzeitigen Abrufen von Lizenzen an einen Client Computer verwendet wird. Ein häufiges Szenario für die Verwendung der vorab Bereitstellung ist, wenn ein Benutzer einen Musikdienst abonniert. Wenn Sie keine Lizenzen bereitstellen, bevor Sie benötigt werden, muss der Benutzer auf den Lizenzerwerb für jeden neuen Song warten.

Da die vorab Bereitstellung nicht als Antwort auf den versuchten Zugriff erfolgt, wird Sie in der Regel nur vom Besitzer des Inhalts ausgeführt. Das heißt, Sie können nur Lizenzen für den von Ihnen kontrollierten Inhalt vorab übermitteln. Der Prozess vor der Übermittlung ist eine Koordination zwischen einer Client Komponente und einem Lizenzserver, der mithilfe der Objekte des Windows Media Digital Rights Management SDK erstellt wurde.

Die vorab Bereitstellung von Lizenzen ähnelt der [nicht automatischen Lizenz Erfassung](non-silent-license-acquisition.md). Führen Sie dieselben Schritte aus, mit dem Unterschied, dass Sie nicht über einen DRM-Header verfügen, der an [**iwmdrmlicenabmanagement:: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md)übergeben werden kann. Die-Methode generiert eine Herausforderung, die nicht inhaltsspezifisch ist, die Sie an Ihren Lizenzserver senden können.

Alternativ können Sie den [Windows Media Rights Manager](/previous-versions//bb676133(v=technet.10)) zum vorab übermitteln von Lizenzen verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erwerben von Lizenzen**](acquiring-licenses.md)
</dt> <dt>

[**Verwenden des Media Foundation-Ereignis Modells**](using-the-media-foundation-model.md)
</dt> </dl>

 

 