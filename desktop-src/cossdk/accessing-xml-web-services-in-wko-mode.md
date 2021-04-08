---
description: Sie können auf jeden beliebigen XML-Webdienst zugreifen und ihn verwenden, auch wenn dieser XML-Webdienst nicht mit com+ oder sogar Microsoft Windows erstellt wurde, solange der XML-Webdienst eine WSDL-Beschreibung seiner Syntax veröffentlicht.
ms.assetid: 5b21ff0c-f3a5-464b-b927-a7872ac54fe2
title: Zugreifen auf XML-Webdienste im WKO-Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e726f430c47b3202932796455e1cf997e370a022
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748193"
---
# <a name="accessing-xml-web-services-in-wko-mode"></a>Zugreifen auf XML-Webdienste im WKO-Modus

Sie können auf jeden beliebigen XML-Webdienst zugreifen und ihn verwenden, auch wenn dieser XML-Webdienst nicht mit com+ oder sogar Microsoft Windows erstellt wurde, solange der XML-Webdienst eine WSDL-Beschreibung seiner Syntax veröffentlicht. Erstellen Sie einfach eine Instanz der Komponente, indem Sie den SOAP: WSDL = URL-Moniker verwenden, wobei URL die URL der WSDL-Beschreibung des XML-Webdiensts ist, auf den Sie zugreifen möchten. Dies ist der WKO-Modus (well-known Object) für den Zugriff auf XML-Webdienste.

Die Methoden des-Objekts können ohne besondere Überlegungen aufgerufen werden. Der Zugriff auf den XML-Webdienst erfolgt über eine SOAP-Abfrage, und die Antwort wird transparent interpretiert.

## <a name="component-services-administrative-tool"></a>Verwaltungs Tool für Komponenten Dienste

Nicht anwendbar.

## <a name="visual-basic"></a>Visual Basic

Das folgende Microsoft Visual Basic-Code Fragment veranschaulicht die Verwendung eines XML-Webdiensts im WKO-Modus.


```VB
Set Obj = GetObject("soap:wsdl=https://servername/vroot/progID.soap?WSDL")
output = Obj.Method(input)
```



In diesem Code Fragment, das die Verwendung einer Komponente einer COM+-Anwendung veranschaulicht, die als XML-Webdienst verfügbar gemacht wurde, ist Servername der voll qualifizierte Domänen Name des Servers, der den XML-Webdienst anbietet. vroot ist das virtuelle IIS-Stammverzeichnis, von dem der XML-Webdienst verfügbar gemacht wird. und ProgID ist die ProgID der Komponente, die Sie verwenden möchten.

## <a name="cc"></a>C/C++

Das folgende Code Fragment veranschaulicht die Verwendung eines XML-Webdiensts im WKO-Modus.


```C++
HRESULT hr = CoGetObject(
     L"soap:wsdl=https://servername/vroot/progID.soap?WSDL",
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr); 
```



In diesem Code Fragment, das die Verwendung einer Komponente einer COM+-Anwendung veranschaulicht, die als XML-Webdienst verfügbar gemacht wurde, ist Servername der voll qualifizierte Domänen Name des Servers, der den XML-Webdienst anbietet. vroot ist das virtuelle IIS-Stammverzeichnis, von dem der XML-Webdienst verfügbar gemacht wird. und ProgID ist die ProgID der Komponente, die Sie verwenden möchten.

## <a name="remarks"></a>Bemerkungen

Beim ersten Zugriff auf einen XML-Webdienst im WKO-Modus generiert com+ einen Proxy Client und kompiliert ihn im Hintergrund. Diese Lauf Zeit Generierung und der Mangel an permanenten Verbindungen im WKO-Modus führen im Vergleich zum Modus "Cao" zu einer erheblich geringeren Leistung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf XML-Webdienste im Modus "Cao"](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[Übersicht über den COM+ SOAP-Dienst](com--soap-service-overview.md)
</dt> <dt>

[Erstellen von XML-Webdiensten](creating-xml-web-services.md)
</dt> <dt>

[Sichern von XML-Webdiensten](securing-xml-web-services.md)
</dt> </dl>

 

 



