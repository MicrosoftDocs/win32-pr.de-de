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
# <a name="accessing-xml-web-services-in-cao-mode"></a><span data-ttu-id="0dfb9-103">Zugreifen auf XML-Webdienste im Modus "Cao"</span><span class="sxs-lookup"><span data-stu-id="0dfb9-103">Accessing XML Web Services in CAO Mode</span></span>

<span data-ttu-id="0dfb9-104">Wenn der XML-Webdienst, auf den Sie zugreifen möchten, durch Bereitstellen einer COM+-Anwendung erstellt wurde, können Sie im Client aktivierten Objekt Modus (Cao) darauf zugreifen, wodurch die Lauf Zeit Generierung eines Proxys vermieden und die Leistung mithilfe dauerhafter Verbindungen gesteigert wird.</span><span class="sxs-lookup"><span data-stu-id="0dfb9-104">If the XML web service you want to access was created by exposing a COM+ application, consider accessing it in client-activated object (CAO) mode, which avoids the run-time generation of a proxy and increases performance by using persistent connections.</span></span> <span data-ttu-id="0dfb9-105">Um auf einen XML-Webdienst im Modus "Cao" zuzugreifen, [exportieren](exporting-a-soap-enabled-application.md) Sie zuerst die entsprechende SOAP-aktivierte Anwendung vom Server im Proxy Modus, und [importieren](importing-a-soap-enabled-application.md) Sie die Anwendung dann in den Client, von dem aus Sie als XML-Webdienst auf die Anwendung zugreifen möchten.</span><span class="sxs-lookup"><span data-stu-id="0dfb9-105">To access an XML web service in CAO mode, first [export](exporting-a-soap-enabled-application.md) the corresponding SOAP-enabled application from your server in proxy mode and then [import](importing-a-soap-enabled-application.md) the application into the client from which you want to access the application as an XML web service.</span></span> <span data-ttu-id="0dfb9-106">Die Komponenten der Anwendung können dann auf dem Client genauso wie die Komponenten lokaler Anwendungen instanziiert werden – z. b. **GetObject** und [**cokreatinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="0dfb9-106">The application's components can then be instantiated on the client just like the components of local applications—for example, using **GetObject** and [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

## <a name="user-interface"></a><span data-ttu-id="0dfb9-107">Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="0dfb9-107">User Interface</span></span>

<span data-ttu-id="0dfb9-108">Nicht anwendbar.</span><span class="sxs-lookup"><span data-stu-id="0dfb9-108">Does not apply.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="0dfb9-109">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="0dfb9-109">Visual Basic</span></span>

<span data-ttu-id="0dfb9-110">Das folgende Visual Basic Code Fragment veranschaulicht die Verwendung einer Komponente einer COM+-Anwendung, die als XML-Webdienst im Modus "Cao" verfügbar gemacht wurde.</span><span class="sxs-lookup"><span data-stu-id="0dfb9-110">The following Visual Basic code fragment illustrates the use of a component of a COM+ application that has been exposed as an XML web service in CAO mode.</span></span>


```VB
Set Obj = GetObject("progID")
output = Obj.Method(input)
```



## <a name="cc"></a><span data-ttu-id="0dfb9-111">C/C++</span><span class="sxs-lookup"><span data-stu-id="0dfb9-111">C/C++</span></span>

<span data-ttu-id="0dfb9-112">Das folgende Code Fragment veranschaulicht die Verwendung einer Komponente einer COM+-Anwendung, die als XML-Webdienst im Modus "Cao" verfügbar gemacht wurde.</span><span class="sxs-lookup"><span data-stu-id="0dfb9-112">The following code fragment illustrates the use of a component of a COM+ application that has been exposed as an XML web service in CAO mode.</span></span>


```C++
HRESULT hr = CoCreateInstance(
     CLSID_CObject,  // CLSID of the server component
     NULL,
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr);
```



## <a name="related-topics"></a><span data-ttu-id="0dfb9-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0dfb9-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0dfb9-114">Zugreifen auf XML-Webdienste im WKO-Modus</span><span class="sxs-lookup"><span data-stu-id="0dfb9-114">Accessing XML Web Services in WKO Mode</span></span>](accessing-xml-web-services-in-wko-mode.md)
</dt> <dt>

[<span data-ttu-id="0dfb9-115">Übersicht über den COM+ SOAP-Dienst</span><span class="sxs-lookup"><span data-stu-id="0dfb9-115">COM+ SOAP Service Overview</span></span>](com--soap-service-overview.md)
</dt> <dt>

[<span data-ttu-id="0dfb9-116">Erstellen von XML-Webdiensten</span><span class="sxs-lookup"><span data-stu-id="0dfb9-116">Creating XML Web Services</span></span>](creating-xml-web-services.md)
</dt> <dt>

[<span data-ttu-id="0dfb9-117">Sichern von XML-Webdiensten</span><span class="sxs-lookup"><span data-stu-id="0dfb9-117">Securing XML Web Services</span></span>](securing-xml-web-services.md)
</dt> </dl>

 

 
