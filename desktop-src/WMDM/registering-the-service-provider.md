---
title: Registrieren des Dienstanbieters
description: Registrieren des Dienstanbieters
ms.assetid: 556d6519-bc24-446b-a360-e3d83b40d541
keywords:
- Windows Medien Geräte-Manager,Registrieren von Dienstanbietern
- Geräte-Manager,Registrieren von Dienstanbietern
- Programmierhandbuch,Registrieren von Dienstanbietern
- Dienstanbieter,Registrieren von Dienstanbietern
- Erstellen von Dienstanbietern,Registrieren von Dienstanbietern
- Registrieren von Dienstanbietern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f480fff04d34cf671bdc37e3bcded92c73f20d31d2fb67e4d6e41593a724d392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584285"
---
# <a name="registering-the-service-provider"></a>Registrieren des Dienstanbieters

Ein Dienstanbieter muss nicht nur als COM-Objekt registriert werden, sondern auch als Plug-In für Windows Media Geräte-Manager. Für die Registrierung muss ein Dienstanbieter den folgenden Registrierungsschlüssel erstellen:

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Media Device Manager\Plugins\SP\<             `

Geben Sie in < *Dienstanbieternamen* an, > der Name Ihrer DLL ist. Beispielsweise verwendet der Beispieldienstanbieter MsHDSP. Der ProgID-Schlüssel sollte über einen Zeichenfolgenwert verfügen, der der CLSID Ihres Dienstanbieters entspricht. Der Beispieldienstanbieter hat beispielsweise den Wert "MDServiceProviderHD.MDServiceProviderHD".

Die Implementierung von DLLRegisterServer durch den Beispieldienstanbieter in Mdsp.cpp fügt diesen Registrierungsschlüssel hinzu, wenn Sie die Beispiel-Dienstanbieter-DLL registrieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen eines Dienstanbieters**](creating-a-service-provider.md)
</dt> </dl>

 

 




