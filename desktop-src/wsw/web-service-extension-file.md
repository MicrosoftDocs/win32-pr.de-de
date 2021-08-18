---
title: Webdiensterweiterungsdatei
description: In diesem Abschnitt wird die Webdiensterweiterungsdatei beschrieben.
ms.assetid: 856d4ff5-2292-4d87-ae7c-19b100fd1cb3
keywords:
- Webdiensterweiterungsdatei-Webdienste für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1b11e8e871399e1a499a6cfbb68a8e66b152d8f07f4fa5f2cda6585678af8e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707230"
---
# <a name="web-service-extension-file"></a>Webdiensterweiterungsdatei

In diesem Abschnitt wird die Webdiensterweiterungsdatei beschrieben.


Die WSX-Datei (WCF-Diensterweiterung) ist unsere Erweiterungsdatei, die es der Anwendung ermöglicht, lokale Verhaltensweisen zu bearbeiten, die sich nicht auf die Darstellung von Wire Data auswirken. Es sollte erweiterbar sein, dass wir in Zukunft neue Features hinzufügen können, ohne die Interoperabilität zu brechen.

Die Gesamtstruktur von WSX würde die Struktur der XSD- oder WSDL-Datei imitieren, bei der es sich um eine XML-Datei handelt, die dieselbe Struktur wie die Haupteingabedatei verwaltet. Zusätzliche Attribute für das gleiche benannte Token in der Hauptdatei geben die Attribute an, die die Anwendung über das Standardverhalten steuern möchte.

In M3 werden wir möglicherweise nichts unternehmen. In V1 sehen wir, dass die folgenden Attribute unterstützt werden:

Verwendung Gibt das Count-Argument/Parameterfeld an.

Dies ist ein Elementattribut, gilt aber nur für den Arraytyp. Das IsCountOf-Attribut gibt das Arrayelement an. Das Count-Feld bzw. der Parameter wird nicht im Netzwerk angezeigt.

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="FooInParam">
  <complexType> 
   <!-- MyArray field is presented in WSDL file as an element -->
    <element name="MyArrayCount" IsCountOf="MyArray"></element>
   </complexType>
  </element>
 </xs:schema>
```

Angeben des Lese-/Schreibrückrufs für den benutzerdefinierten Typ

Diese Attribute erzwingen, wsutil.exe [**WS \_ CUSTOM TYPE für \_ den**](/windows/desktop/api/WebServices/ne-webservices-ws_type) angegebenen Typ zu generieren. \_Benutzerdefiniertes Readcallback-Attribut gibt die [**Read-Rückrufroutine**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback) an, und custom \_ writecallback gibt die [**Rückrufroutine für das Schreiben**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback) an.

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="mytype" custom_readcallback="myreadcallback" custom_writecallback="mywritecallback"> 
 </element>
</xs:schema>
```

Wir können über eine entsprechende WSX-Datei verfügen, um das lokale Verhalten zu beschreiben:

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">

 <element name="FooInParam" DataValidationRoutine="MyArrayValidation">
  <complexType> 
   <element name="MyLocalArrayCount" IsCountOf="MyArray"></element> 
  </complexType>
 </element>
</xs:schema>
```

WsUtil.exe generiert den folgenden Prototyp für die -Struktur:

``` syntax
typedef struct FooInParam
{
  ULONG MyLocalArrayCount;
  int * MyArray;
};
```

 

 




