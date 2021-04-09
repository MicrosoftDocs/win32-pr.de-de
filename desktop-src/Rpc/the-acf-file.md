---
title: Die ACF-Datei
description: Mithilfe der ACF-Datei können Sie die RPC-Schnittstelle Ihrer Client-und/oder Server Anwendungen anpassen, ohne dass sich dies auf die Netzwerk Merkmale der Schnittstelle auswirkt.
ms.assetid: 7d3fef5c-b645-4e10-b08d-b339025718b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e803201004cd73a4be507aaba2affd20f1ea3d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949070"
---
# <a name="the-acf-file"></a>Die ACF-Datei

Mithilfe der ACF-Datei können Sie die RPC-Schnittstelle Ihrer Client-und/oder Server Anwendungen anpassen, ohne dass sich dies auf die Netzwerk Merkmale der Schnittstelle auswirkt. Wenn Ihre Client Anwendung z. b. eine komplexe Datenstruktur enthält, die nur auf dem lokalen Computer Bedeutung hat, können Sie in der ACF-Datei angeben, wie die Daten in dieser Struktur in einem Computer unabhängigen Formular für Remote Prozedur Aufrufe dargestellt werden können.

Dieses Tutorial veranschaulicht eine weitere Verwendung der ACF-Datei – gibt den Typ des Bindungs Handles an, das die Verbindung zwischen Client und Server darstellt. Mit dem **\[** [**impliziten \_ handle**](/windows/desktop/Midl/implicit-handle) - **\]** Attribut im ACF-Header kann die Client Anwendung einen Server für den Remote Prozedur aufzurufen auswählen. Der ACF definiert das Handle, das vom [**Typhandle \_ t**](/windows/desktop/Midl/handle-t) (ein primitiver primitiver Datentyp) sein soll. Der mittlerer l-Compiler fügt den von der ACF angegebenen Bindungs Handle-Namen, Hello \_ ifhandle, in die von ihm generierte Header Datei ein. Beachten Sie, dass diese bestimmte ACF-Datei einen leeren Text enthält.

``` syntax
//file: hello.acf
[
    implicit_handle (handle_t hello_IfHandle)
] 
interface hello
{
}
```

Der mittlerer l-Compiler verfügt über die Option [**/App \_ config**](/windows/desktop/Midl/-app-config), mit der Sie bestimmte ACF-Attribute (z. b. **implizites \_ handle**) in die IDL-Datei einschließen können, anstatt eine separate ACF-Datei zu erstellen. Verwenden Sie diese Option, wenn für Ihre Anwendung keine sehr spezielle Konfiguration erforderlich ist und die strikte OSF-Kompatibilität kein Problem ist.

 

 