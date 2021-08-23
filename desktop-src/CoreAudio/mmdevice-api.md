---
description: Informationen zur MMDevice-API
ms.assetid: 3a8fd734-0761-4b5b-ba04-677c7c040988
title: Informationen zur MMDevice-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23e2f33c6969e00006c12b0bc6dc1ba37b70c5ff38ea2846633d5eb61da03b19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077544"
---
# <a name="about-mmdevice-api"></a>Informationen zur MMDevice-API

Mit der MMDevice-API (Windows Multimedia Device) können Audioclients [Audioendpunktgeräte](audio-endpoint-devices.md)ermitteln, ihre Funktionen bestimmen und Treiberinstanzen für diese Geräte erstellen.

Die Headerdatei Mmdeviceapi.h definiert die Schnittstellen in der MMDevice-API.

Die MMDevice-API besteht aus mehreren Schnittstellen. Die erste davon ist die [**IMMDeviceEnumerator-Schnittstelle.**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) Um auf die Schnittstellen in der MMDevice-API zuzugreifen, ruft ein Client einen Verweis auf die **IMMDeviceEnumerator-Schnittstelle** eines Geräteenumeratorobjekts ab, indem er die [**CoCreateInstance-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufruft, wie im folgenden Codefragment gezeigt:


```C++
  const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
  const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
  hr = CoCreateInstance(
         CLSID_MMDeviceEnumerator, NULL,
         CLSCTX_ALL, IID_IMMDeviceEnumerator,
         (void**)&pEnumerator);
```



Im vorangehenden Codefragment sind CLSID \_ MMDeviceEnumerator und IID \_ IMMDeviceEnumerator die GUID-Werte, die als Attribute an das **MMDeviceEnumerator-Klassenobjekt** und an die [**IMMDeviceEnumerator-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) angefügt werden. Der [**CoCreateInstance-Aufruf**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) übergibt diese Werte als Verweis. Variable `hr` ist vom Typ **HRESULT,** und variable `pEnumerator` ist ein Zeiger auf die **IMMDeviceEnumerator-Schnittstelle** eines Geräteenumeratorobjekts. **IMMDeviceEnumerator** stellt Methoden zum Auflisten von Audioendpunktgeräten bereit. Informationen zum **\_ \_ uuidof-Operator,** zur **CoCreateInstance-Funktion** und zu den CLSCTX \_ *Xxx-Konstanten* finden Sie in der Dokumentation zum Windows SDK.

Über die [**IMMDeviceEnumerator-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) kann der Client Verweise auf die anderen Schnittstellen in der MMDevice-API abrufen. Die MMDevice-API implementiert die folgenden Schnittstellen.



| Schnittstelle                                          | BESCHREIBUNG                                     |
|----------------------------------------------------|-------------------------------------------------|
| [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                     | Stellt ein Audiogerät dar.                     |
| [**IMMDeviceCollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) | Stellt eine Auflistung von Audiogeräten dar.       |
| [**IMMDeviceEnumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) | Stellt Methoden zum Aufzählen von Audiogeräten bereit. |
| [**IMMEndpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                 | Stellt ein Audioendpunktgerät dar.            |



 

Darüber hinaus sollten Clients der MMDevice-API, die eine Benachrichtigung über Statusänderungen auf Audioendpunktgeräten erfordern, die folgende Schnittstelle implementieren.



| Schnittstelle                                              | BESCHREIBUNG                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMMNotificationClient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | Stellt Benachrichtigungen bereit, wenn ein Audioendpunktgerät hinzugefügt oder entfernt wird, wenn sich der Zustand oder die Eigenschaften eines Geräts ändern oder wenn sich die Standardrolle ändert, die einem Gerät zugewiesen ist. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioendpunktgeräte](audio-endpoint-devices.md)
</dt> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 
