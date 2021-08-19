---
title: Die ACF-Datei
description: Mit der ACF-Datei können Sie die RPC-Schnittstelle Ihrer Client- und/oder Serveranwendungen anpassen, ohne die Netzwerkmerkmale der Schnittstelle zu beeinträchtigen.
ms.assetid: 7d3fef5c-b645-4e10-b08d-b339025718b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d234b30c25870dd7a21cb790cc4839236ab69093291285b64c870cf7c05cb11f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080840"
---
# <a name="the-acf-file"></a>Die ACF-Datei

Mit der ACF-Datei können Sie die RPC-Schnittstelle Ihrer Client- und/oder Serveranwendungen anpassen, ohne die Netzwerkmerkmale der Schnittstelle zu beeinträchtigen. Wenn Ihre Clientanwendung beispielsweise eine komplexe Datenstruktur enthält, die nur auf dem lokalen Computer eine Bedeutung hat, können Sie in der ACF-Datei angeben, wie die Daten in dieser Struktur in computerunabhängiger Form für Remoteprozeduraufrufe dargestellt werden können.

In diesem Tutorial wird eine weitere Verwendung der ACF-Datei veranschaulicht, indem der Typ des Bindungshandle angegeben wird, das die Verbindung zwischen Client und Server darstellt. Mit dem **\[** [**impliziten \_ Handleattribut**](/windows/desktop/Midl/implicit-handle) **\]** im ACF-Header kann die Clientanwendung einen Server für den Remoteprozeduraufruf auswählen. Der ACF definiert das Handle als [**Typhandle \_ t**](/windows/desktop/Midl/handle-t) (ein primitiver MIDL-Datentyp). Der MIDL-Compiler legt den Bindungshandlenamen, den der ACF angegeben hat, hello \_ IfHandle in die generierte Headerdatei ein. Beachten Sie, dass diese bestimmte ACF-Datei einen leeren Text enthält.

``` syntax
//file: hello.acf
[
    implicit_handle (handle_t hello_IfHandle)
] 
interface hello
{
}
```

Der MIDL-Compiler verfügt über die Option [**/app \_ config,**](/windows/desktop/Midl/-app-config)mit der Sie bestimmte ACF-Attribute, z. B. **implizites \_ Handle,** in die IDL-Datei einschließen können, anstatt eine separate ACF-Datei zu erstellen. Erwägen Sie die Verwendung dieser Option, wenn Ihre Anwendung nicht viel besondere Konfiguration erfordert und wenn die strikte OSF-Kompatibilität kein Problem darstellt.

 

 