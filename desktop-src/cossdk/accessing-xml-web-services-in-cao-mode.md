---
description: Wenn der XML-Webdienst, auf den Sie zugreifen möchten, durch Verfügbarmachen einer COM+-Anwendung erstellt wurde, sollten Sie den Zugriff auf diesen im CAO-Modus (Client-Activated Object) in Betracht ziehen, der die Laufzeitgenerierung eines Proxys vermeidet und die Leistung mithilfe persistenter Verbindungen erhöht.
ms.assetid: 471de0fa-3429-45f8-abe2-aff0cf6fb350
title: Zugreifen auf XML-Webdienste im CAO-Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e3f8dc1fa3c037d03d8b69cf45737c7211d92f7d38e733a97b9be109a2243a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549458"
---
# <a name="accessing-xml-web-services-in-cao-mode"></a>Zugreifen auf XML-Webdienste im CAO-Modus

Wenn der XML-Webdienst, auf den Sie zugreifen möchten, durch Verfügbarmachen einer COM+-Anwendung erstellt wurde, sollten Sie den Zugriff auf diesen im CAO-Modus (Client-Activated Object) in Betracht ziehen, der die Laufzeitgenerierung eines Proxys vermeidet und die Leistung mithilfe persistenter Verbindungen erhöht. Um auf einen XML-Webdienst im CAO-Modus zuzugreifen, [exportieren](exporting-a-soap-enabled-application.md) Sie zunächst die entsprechende SOAP-fähige Anwendung von Ihrem Server im Proxymodus, und [importieren](importing-a-soap-enabled-application.md) Sie dann die Anwendung in den Client, von dem aus Sie als XML-Webdienst auf die Anwendung zugreifen möchten. Die Komponenten der Anwendung können dann wie die Komponenten lokaler Anwendungen auf dem Client instanziiert werden, z. B. mit **GetObject** und [**CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)

## <a name="user-interface"></a>Benutzeroberfläche

Nicht anwendbar.

## <a name="visual-basic"></a>Visual Basic

Das folgende Visual Basic Codefragment veranschaulicht die Verwendung einer Komponente einer COM+-Anwendung, die als XML-Webdienst im CAO-Modus verfügbar gemacht wurde.


```VB
Set Obj = GetObject("progID")
output = Obj.Method(input)
```



## <a name="cc"></a>C/C++

Das folgende Codefragment veranschaulicht die Verwendung einer Komponente einer COM+-Anwendung, die als XML-Webdienst im CAO-Modus verfügbar gemacht wurde.


```C++
HRESULT hr = CoCreateInstance(
     CLSID_CObject,  // CLSID of the server component
     NULL,
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf XML-Webdienste im WKO-Modus](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[Übersicht über den COM+-SOAP-Dienst](com--soap-service-overview.md)
</dt> <dt>

[Erstellen von XML-Webdiensten](creating-xml-web-services.md)
</dt> <dt>

[Sichern von XML-Webdiensten](securing-xml-web-services.md)
</dt> </dl>

 

 
