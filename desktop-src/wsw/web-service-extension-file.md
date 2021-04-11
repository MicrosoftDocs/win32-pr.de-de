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
# <a name="web-service-extension-file"></a><span data-ttu-id="b0921-106">Webdienst-Erweiterungs Datei</span><span class="sxs-lookup"><span data-stu-id="b0921-106">Web Service Extension File</span></span>

<span data-ttu-id="b0921-107">In diesem Abschnitt wird die Webdienst-Erweiterungs Datei beschrieben.</span><span class="sxs-lookup"><span data-stu-id="b0921-107">This section outlines Web Service extension file.</span></span>


<span data-ttu-id="b0921-108">Die WSX-Datei (WCF-Dienst Erweiterung) ist unsere Erweiterungs Datei, damit die Anwendung das lokale Verhalten bearbeiten kann, das sich nicht auf die Datendarstellung von Wire auswirkt.</span><span class="sxs-lookup"><span data-stu-id="b0921-108">WSX file (WCF service extension) is our extension file to allow application to manipulate local behaviors that do not affect wire data representation.</span></span> <span data-ttu-id="b0921-109">Es sollte erweiterbar sein, dass wir in Zukunft neue Features hinzufügen können, ohne die Interoperabilität zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="b0921-109">It should be extensible that we can add new features in the future without breaking interoperability.</span></span>

<span data-ttu-id="b0921-110">Die Gesamtstruktur von WSX imitiert die Struktur von XSD-oder WSDL-Dateien, bei der es sich um eine XML-Datei handelt, die dieselbe Struktur wie die Haupt Eingabedatei beibehält.</span><span class="sxs-lookup"><span data-stu-id="b0921-110">The overall structure of WSX would mimic the structure of XSD or WSDL file, which is a XML file that maintains the same structure as the main input file.</span></span> <span data-ttu-id="b0921-111">Zusätzliche Attribute für dasselbe benannte Token in der Hauptdatei geben die Attribute an, die die Anwendung über das Standardverhalten steuern möchte.</span><span class="sxs-lookup"><span data-stu-id="b0921-111">Extra attributes on the same named token in main file would specify the attributes that application wants to control over the default behavior.</span></span>

<span data-ttu-id="b0921-112">In der M3-Aktion ist es unter Umständen nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="b0921-112">We might not do anything here in M3.</span></span> <span data-ttu-id="b0921-113">In v1 kann ich sehen, dass die folgenden Attribute unterstützt werden:</span><span class="sxs-lookup"><span data-stu-id="b0921-113">In V1, I can see we support the following attributes:</span></span>

<span data-ttu-id="b0921-114">Verwendungs Angabe für das count-Argument/Parameter-Feld.</span><span class="sxs-lookup"><span data-stu-id="b0921-114">Usage Specifying count argument/parameter field.</span></span>

<span data-ttu-id="b0921-115">Dies ist ein Element Attribut, das nur für den Arraytyp anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="b0921-115">This is an element attribute but applicable to array type only.</span></span> <span data-ttu-id="b0921-116">Das iszähltof-Attribut gibt das Array Element an.</span><span class="sxs-lookup"><span data-stu-id="b0921-116">IsCountOf attribute specifies the array element.</span></span> <span data-ttu-id="b0921-117">Das count-Feld/der-Parameter wird bei der Übertragung nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b0921-117">The count field/parameter does not appear on wire.</span></span>

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

<span data-ttu-id="b0921-118">Angeben von Lese-/schreibrückruf</span><span class="sxs-lookup"><span data-stu-id="b0921-118">Specifying read/write callback for custom type</span></span>

<span data-ttu-id="b0921-119">Diese Attribute erzwingen, dass wsutil.exe [**den \_ Benutzer \_ definierten WS-Typ**](/windows/desktop/api/WebServices/ne-webservices-ws_type) für den angegebenen Typ generiert.</span><span class="sxs-lookup"><span data-stu-id="b0921-119">These attributes force wsutil.exe to generate [**WS\_CUSTOM\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_type) for specified type.</span></span> <span data-ttu-id="b0921-120">das benutzerdefinierte \_ lesecallback-Attribut gibt die [**Lese Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback) Routine an, und der benutzerdefinierte \_ beschreibende Rückruf gibt die [**Schreib Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback) Routine an.</span><span class="sxs-lookup"><span data-stu-id="b0921-120">custom\_readcallback attribute specifies the [**read callback**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback) routine, and custom\_writecallback specifies the [**write callback**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback) routine.</span></span>

``` syntax
<xs:schema xmlns:tns="http://Example.org" elementFormDefault="qualified" 
targetNamespace="http://Example.org" xmlns:xs="http://www.w3.org/2001/XMLSchema">
 <element name="mytype" custom_readcallback="myreadcallback" custom_writecallback="mywritecallback"> 
 </element>
</xs:schema>
```

<span data-ttu-id="b0921-121">Wir können über eine passende WSX-Datei verfügen, um das lokale Verhalten zu beschreiben:</span><span class="sxs-lookup"><span data-stu-id="b0921-121">We can have a matching WSX file to describe its local behavior:</span></span>

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

<span data-ttu-id="b0921-122">WsUtil.exe generiert den folgenden Prototyp für die Struktur:</span><span class="sxs-lookup"><span data-stu-id="b0921-122">WsUtil.exe generates the following prototype for the structure:</span></span>

``` syntax
typedef struct FooInParam
{
  ULONG MyLocalArrayCount;
  int * MyArray;
};
```

 

 




