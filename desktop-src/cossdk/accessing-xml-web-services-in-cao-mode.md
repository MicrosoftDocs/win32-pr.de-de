---
description: Wenn der XML-Webdienst, auf den Sie zugreifen möchten, durch Bereitstellen einer COM+-Anwendung erstellt wurde, können Sie im Client aktivierten Objekt Modus (Cao) darauf zugreifen, wodurch die Lauf Zeit Generierung eines Proxys vermieden und die Leistung mithilfe dauerhafter Verbindungen gesteigert wird.
ms.assetid: 471de0fa-3429-45f8-abe2-aff0cf6fb350
title: Zugreifen auf XML-Webdienste im Modus "Cao"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50f1e15c18a925ba88f1b9c7c8267bfb2ef12292
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341131"
---
# <a name="accessing-xml-web-services-in-cao-mode"></a>Zugreifen auf XML-Webdienste im Modus "Cao"

Wenn der XML-Webdienst, auf den Sie zugreifen möchten, durch Bereitstellen einer COM+-Anwendung erstellt wurde, können Sie im Client aktivierten Objekt Modus (Cao) darauf zugreifen, wodurch die Lauf Zeit Generierung eines Proxys vermieden und die Leistung mithilfe dauerhafter Verbindungen gesteigert wird. Um auf einen XML-Webdienst im Modus "Cao" zuzugreifen, [exportieren](exporting-a-soap-enabled-application.md) Sie zuerst die entsprechende SOAP-aktivierte Anwendung vom Server im Proxy Modus, und [importieren](importing-a-soap-enabled-application.md) Sie die Anwendung dann in den Client, von dem aus Sie als XML-Webdienst auf die Anwendung zugreifen möchten. Die Komponenten der Anwendung können dann auf dem Client genauso wie die Komponenten lokaler Anwendungen instanziiert werden – z. b. **GetObject** und [**cokreatinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

## <a name="user-interface"></a>Benutzeroberfläche

Nicht anwendbar.

## <a name="visual-basic"></a>Visual Basic

Das folgende Visual Basic Code Fragment veranschaulicht die Verwendung einer Komponente einer COM+-Anwendung, die als XML-Webdienst im Modus "Cao" verfügbar gemacht wurde.


```VB
Set Obj = GetObject("progID")
output = Obj.Method(input)
```



## <a name="cc"></a>C/C++

Das folgende Code Fragment veranschaulicht die Verwendung einer Komponente einer COM+-Anwendung, die als XML-Webdienst im Modus "Cao" verfügbar gemacht wurde.


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

[Übersicht über den COM+ SOAP-Dienst](com--soap-service-overview.md)
</dt> <dt>

[Erstellen von XML-Webdiensten](creating-xml-web-services.md)
</dt> <dt>

[Sichern von XML-Webdiensten](securing-xml-web-services.md)
</dt> </dl>

 

 
