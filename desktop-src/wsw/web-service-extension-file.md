---
title: Webdienst-Erweiterungs Datei
description: In diesem Abschnitt wird die Webdienst-Erweiterungs Datei beschrieben.
ms.assetid: 856d4ff5-2292-4d87-ae7c-19b100fd1cb3
keywords:
- Webdienst-Erweiterungs Datei-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0802e31895aa5dd5051c94746e774033a1ebe677
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104316814"
---
# <a name="web-service-extension-file"></a>Webdienst-Erweiterungs Datei

In diesem Abschnitt wird die Webdienst-Erweiterungs Datei beschrieben.


Die WSX-Datei (WCF-Dienst Erweiterung) ist unsere Erweiterungs Datei, damit die Anwendung das lokale Verhalten bearbeiten kann, das sich nicht auf die Datendarstellung von Wire auswirkt. Es sollte erweiterbar sein, dass wir in Zukunft neue Features hinzufügen können, ohne die Interoperabilität zu unterbrechen.

Die Gesamtstruktur von WSX imitiert die Struktur von XSD-oder WSDL-Dateien, bei der es sich um eine XML-Datei handelt, die dieselbe Struktur wie die Haupt Eingabedatei beibehält. Zusätzliche Attribute für dasselbe benannte Token in der Hauptdatei geben die Attribute an, die die Anwendung über das Standardverhalten steuern möchte.

In der M3-Aktion ist es unter Umständen nicht möglich. In v1 kann ich sehen, dass die folgenden Attribute unterstützt werden:

Verwendungs Angabe für das count-Argument/Parameter-Feld.

Dies ist ein Element Attribut, das nur für den Arraytyp anwendbar ist. Das iszähltof-Attribut gibt das Array Element an. Das count-Feld/der-Parameter wird bei der Übertragung nicht angezeigt.

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

Angeben von Lese-/schreibrückruf

Diese Attribute erzwingen, dass wsutil.exe [**den \_ Benutzer \_ definierten WS-Typ**](/windows/desktop/api/WebServices/ne-webservices-ws_type) für den angegebenen Typ generiert. das benutzerdefinierte \_ lesecallback-Attribut gibt die [**Lese Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback) Routine an, und der benutzerdefinierte \_ beschreibende Rückruf gibt die [**Schreib Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback) Routine an.

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="mytype" custom_readcallback="myreadcallback" custom_writecallback="mywritecallback"> 
 </element>
</xs:schema>
```

Wir können über eine passende WSX-Datei verfügen, um das lokale Verhalten zu beschreiben:

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

WsUtil.exe generiert den folgenden Prototyp für die Struktur:

``` syntax
typedef struct FooInParam
{
  ULONG MyLocalArrayCount;
  int * MyArray;
};
```

 

 




