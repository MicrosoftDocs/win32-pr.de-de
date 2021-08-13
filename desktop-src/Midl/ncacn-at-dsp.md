---
title: ncacn_at_dsp-Attribut
description: Das Schlüsselwort ncacn \_ at \_ dsp identifiziert AppleTalk DSP als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte nicht in neuen Anwendungen verwendet werden.
ms.assetid: 3165e4f6-8869-4eff-af65-53e85f78a949
keywords:
- ncacn_at_dsp-Attribut MIDL
topic_type:
- apiref
api_name:
- ncacn_at_dsp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb021f9212f1034f0b3c235ad77d9ad270325af914887252494316f9ae1c41b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118642771"
---
# <a name="ncacn_at_dsp-attribute"></a>ncacn \_ am \_ dsp-Attribut

Das **Schlüsselwort ncacn \_ at \_ dsp** identifiziert AppleTalk DSP als Protokollfamilie für den Endpunkt. Diese Protokollfamilie ist veraltet und sollte nicht in neuen Anwendungen verwendet werden.

``` syntax
endpoint("ncacn_at_dsp:[port-name]")
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Portname* 
</dt> <dd>

Gibt eine Zeichenfolge mit einer Länge von bis zu 22 Byte an.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die Syntax der AppleTalk DSP-Portzeichenfolge wird wie alle Portzeichenfolgen von der Transportimplementierungen definiert und ist unabhängig von der IDL-Spezifikation. Der MIDL-Compiler führt eine eingeschränkte Syntaxüberprüfung durch, garantiert jedoch nicht, dass die Endpunktspezifikation korrekt ist. Einige Fehlerklassen werden möglicherweise zur Laufzeit und nicht zur Kompilierzeit gemeldet.

## <a name="examples"></a>Beispiele

``` syntax
[
    uuid(12345678-4000-2006-0000-20000000001a), 
    version(1.1), 
    endpoint("ncacn_at_dsp:[my_services_endpoint]") 
] 
interface iface
{
    // Interface definition statements.
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Endpunkt**](endpoint.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**Zeichenfolgenbindung**](/windows/desktop/Rpc/string-binding)
</dt> </dl>

 

 