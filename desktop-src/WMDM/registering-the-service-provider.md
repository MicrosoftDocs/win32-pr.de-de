---
title: Registrieren des Dienstanbieters
description: Registrieren des Dienstanbieters
ms.assetid: 556d6519-bc24-446b-a360-e3d83b40d541
keywords:
- Windows Media Device Manager, Registrieren von Dienstanbietern
- Device Manager, Registrieren von Dienstanbietern
- Programmier Handbuch, Registrieren von Dienstanbietern
- Dienstanbieter, Registrieren von Dienstanbietern
- Erstellen von Dienstanbietern, Registrieren von Dienstanbietern
- Registrieren von Dienstanbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1226b724b06990fc1e000a522e3a61672789cf3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036500"
---
# <a name="registering-the-service-provider"></a>Registrieren des Dienstanbieters

Ein Dienstanbieter muss nicht nur als COM-Objekt registriert werden, sondern muss als Plug-in für Windows Media Device Manager registriert werden. Ein Dienstanbieter muss den folgenden Registrierungsschlüssel erstellen, um sich zu registrieren:

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Media Device Manager\Plugins\SP\<             `

In diesem Schlüssel < der *Name Ihres Dienstanbieters* > der Name der dll ist. beispielsweise verwendet der Beispiel Dienstanbieter mshdsp. Der ProgID-Schlüssel sollte über einen Zeichen folgen Wert verfügen, der der CLSID Ihres Dienstanbieters entspricht. Der Beispiel Dienstanbieter hat beispielsweise den Wert "mdserviceproviderhd. mdserviceproviderhd".

Die Implementierung von DllRegisterServer durch den Beispiel Dienstanbieter in mdsp. cpp fügt diesen Registrierungsschlüssel hinzu, wenn Sie die Beispiel-Dienstanbieter-dll registrieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen eines Dienstanbieters**](creating-a-service-provider.md)
</dt> </dl>

 

 




