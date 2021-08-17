---
description: Sie können auf einen beliebigen XML-Webdienst zugreifen und diesen verwenden, auch wenn dieser XML-Webdienst nicht mit COM+ oder sogar Microsoft Windows erstellt wurde, solange der XML-Webdienst eine WSDL-Beschreibung seiner Syntax veröffentlicht.
ms.assetid: 5b21ff0c-f3a5-464b-b927-a7872ac54fe2
title: Zugreifen auf XML-Webdienste im WKO-Modus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f412a1ec6493e713d2635136b2c4e82063cde56c30358653e476f300ffd2ae4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129402"
---
# <a name="accessing-xml-web-services-in-wko-mode"></a>Zugreifen auf XML-Webdienste im WKO-Modus

Sie können auf einen beliebigen XML-Webdienst zugreifen und diesen verwenden, auch wenn dieser XML-Webdienst nicht mit COM+ oder sogar Microsoft Windows erstellt wurde, solange der XML-Webdienst eine WSDL-Beschreibung seiner Syntax veröffentlicht. Erstellen Sie einfach eine Instanz der Komponente mithilfe des Monikers soap:wsdl=URL, wobei URL die URL der WSDL-Beschreibung des XML-Webdiensts ist, auf den Sie zugreifen möchten. Dies ist der bekannte Objektmodus (WKO) für den Zugriff auf XML-Webdienste.

Die Methoden des Objekts können ohne besondere Überlegungen aufgerufen werden. Der Zugriff auf den XML-Webdienst erfolgt über eine SOAP-Abfrage, und die Antwort wird transparent interpretiert.

## <a name="component-services-administrative-tool"></a>Verwaltungstool für Komponentendienste

Nicht anwendbar.

## <a name="visual-basic"></a>Visual Basic

Das folgende Microsoft Visual Basic-Codefragment veranschaulicht die Verwendung eines XML-Webdiensts im WKO-Modus.


```VB
Set Obj = GetObject("soap:wsdl=https://servername/vroot/progID.soap?WSDL")
output = Obj.Method(input)
```



In diesem Codefragment, das die Verwendung einer Komponente einer COM+-Anwendung veranschaulicht, die als XML-Webdienst verfügbar gemacht wurde, ist servername der vollqualifizierte Domänenname des Servers, der den XML-Webdienst an anbieten. vroot ist das virtuelle IIS-Stammverzeichnis, aus dem der XML-Webdienst verfügbar gemacht wird. und progID ist die ProgID der Komponente, die Sie verwenden möchten.

## <a name="cc"></a>C/C++

Das folgende Codefragment veranschaulicht die Verwendung eines XML-Webdiensts im WKO-Modus.


```C++
HRESULT hr = CoGetObject(
     L"soap:wsdl=https://servername/vroot/progID.soap?WSDL",
     pBindOptions,
     IID_IUnknown,
     (void**)&pIUnknown);
if (FAILED(hr)) throw(hr); 
```



In diesem Codefragment, das die Verwendung einer Komponente einer COM+-Anwendung veranschaulicht, die als XML-Webdienst verfügbar gemacht wurde, ist servername der vollqualifizierte Domänenname des Servers, der den XML-Webdienst an anbieten. vroot ist das virtuelle IIS-Stammverzeichnis, aus dem der XML-Webdienst verfügbar gemacht wird. und progID ist die ProgID der Komponente, die Sie verwenden möchten.

## <a name="remarks"></a>Hinweise

Wenn zum ersten Mal im WKO-Modus auf einen XML-Webdienst zugegriffen wird, generiert COM+ einen Proxyclient und kompiliert ihn im Hintergrund. Diese Laufzeitgenerierung und das Fehlen persistenter Verbindungen im WKO-Modus führen im Vergleich zum CAO-Modus zu einer erheblichen Leistungsverkleinerung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Zugreifen auf XML-Webdienste im CAO-Modus](accessing-xml-web-services-in-cao-mode.md)
</dt> <dt>

[ÜBERSICHT ÜBER DEN COM+-SOAP-Dienst](com--soap-service-overview.md)
</dt> <dt>

[Erstellen von XML-Webdiensten](creating-xml-web-services.md)
</dt> <dt>

[Sichern von XML-Webdiensten](securing-xml-web-services.md)
</dt> </dl>

 

 



