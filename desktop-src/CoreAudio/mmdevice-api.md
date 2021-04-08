---
description: Informationen über die mmdevice-API
ms.assetid: 3a8fd734-0761-4b5b-ba04-677c7c040988
title: Informationen über die mmdevice-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82843bbecf004d0931575d73ec2459c3e72a3cf3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748777"
---
# <a name="about-mmdevice-api"></a>Informationen über die mmdevice-API

Mit der API von Windows Multimedia Device (mmdevice) können audioclients [audioendpunktgeräte](audio-endpoint-devices.md)ermitteln, deren Funktionen ermitteln und Treiber Instanzen für diese Geräte erstellen.

Die Header Datei "mmdeviceapi. h" definiert die Schnittstellen in der mmdevice-API.

Die mmdevice-API besteht aus mehreren Schnittstellen. Der erste ist die [**immdeviceenumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) -Schnittstelle. Für den Zugriff auf die Schnittstellen in der mmdevice-API erhält ein Client einen Verweis auf die **immdeviceenumerator** -Schnittstelle eines Device-Enumerator-Objekts, indem er die [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion aufruft, wie im folgenden Code Fragment gezeigt:


```C++
  const CLSID CLSID_MMDeviceEnumerator = __uuidof(MMDeviceEnumerator);
  const IID IID_IMMDeviceEnumerator = __uuidof(IMMDeviceEnumerator);
  hr = CoCreateInstance(
         CLSID_MMDeviceEnumerator, NULL,
         CLSCTX_ALL, IID_IMMDeviceEnumerator,
         (void**)&pEnumerator);
```



Im vorangehenden Code Fragment sind CLSID \_ mmdeviceenumerator und IID \_ immdeviceenumerator die GUID-Werte, die dem **mmdeviceenumerator** -Klassenobjekt und der [**immdeviceenumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) -Schnittstelle als Attribute angefügt werden. Der [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Befehl übergibt diese Werte als Verweis. Variable `hr` ist vom Typ **HRESULT**, und Variable `pEnumerator` ist ein Zeiger auf die **immdeviceenumerator** -Schnittstelle eines Device-Enumerator-Objekts. **Immdeviceenumerator** stellt Methoden zum Auflisten von audioendpunktgeräten bereit. Weitere Informationen über den **\_ \_ uuidof** -Operator, die **cokreateinstance** -Funktion und die CLSCTX \_ *xxx* -Konstanten finden Sie in der Windows SDK-Dokumentation.

Über die [**immdeviceenumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) -Schnittstelle kann der Client Verweise auf die anderen Schnittstellen in der mmdevice-API abrufen. Die mmdevice-API implementiert die folgenden Schnittstellen.



| Schnittstelle                                          | BESCHREIBUNG                                     |
|----------------------------------------------------|-------------------------------------------------|
| [**Immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice)                     | Stellt ein Audiogerät dar.                     |
| [**Immde vicecollection**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevicecollection) | Stellt eine Auflistung von Audiogeräten dar.       |
| [**Immdeviceenumerator**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) | Stellt Methoden zum Auflisten von Audiogeräten bereit. |
| [**Immendpoint**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immendpoint)                 | Stellt ein audioendpunktgerät dar.            |



 

Außerdem sollten Clients der mmdevice-API, die Benachrichtigungen über Statusänderungen in audioendpunktgeräten erfordern, die folgende Schnittstelle implementieren.



| Schnittstelle                                              | BESCHREIBUNG                                                                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Immnotificationclient**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immnotificationclient) | Stellt Benachrichtigungen bereit, wenn ein audioendpunktgerät hinzugefügt oder entfernt wird, wenn sich der Zustand oder die Eigenschaften eines Geräts ändern oder wenn die Standard Rolle, die einem Gerät zugewiesen ist, geändert wird. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioendpunktgeräte](audio-endpoint-devices.md)
</dt> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 
