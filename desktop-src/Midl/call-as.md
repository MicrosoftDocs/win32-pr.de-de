---
title: Aufruf als Attribut
description: Mit dem \-Aufruf \_ als \-Attribut können Sie eine Funktion zuordnen, die nicht remote zu einer Remote Funktion aufgerufen werden kann.
ms.assetid: 4078f37a-9bd7-4316-b228-afbffc4caeab
keywords:
- Call_as Attribut-Mittel l
topic_type:
- apiref
api_name:
- call_as
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 519ceabc2714e65bcb87651b74518228245afb5f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106337629"
---
# <a name="call_as-attribute"></a>\_als Attribut aufzurufen

Der **\[ Aufruf \_ als \]** -Attribut ermöglicht es Ihnen, eine Funktion zuzuordnen, die nicht remote zu einer Remote Funktion aufgerufen werden kann.

``` syntax
[call_as (local-proc), [ , operation-attribute-list ] ] operation-name ;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*local-proc* 
</dt> <dd>

Gibt eine Vorgangs definierte Routine an.

</dd> <dt>

*Operation-Attribut-List* 
</dt> <dd>

Gibt ein oder mehrere Attribute an, die für den Vorgang gelten. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Vorgangs Name* 
</dt> <dd>

Gibt den benannten Vorgang an, der der Anwendung angezeigt wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Möglichkeit, eine Funktion zuzuordnen, die nicht Remote an eine Remote Funktion aufgerufen werden kann, ist besonders hilfreich bei Schnittstellen, die über zahlreiche Parametertypen verfügen, die nicht über das Netzwerk übertragen werden können. Anstatt viele **\[** [**\_**](represent-as.md) **\]** Darstellungs-und-über **\[** [**Tragung \_ als**](transmit-as.md) -Typen zu verwenden **\]** , können Sie alle Konvertierungen mithilfe von **\[ \_ Callas \]** -Routinen kombinieren. Sie geben die beiden **\[ Aufrufe \_ als \]** Routinen (Client seitig und serverseitig) an, um die Routine zwischen den Anwendungs aufrufen und den Remote aufrufen zu binden.

Der " **\[ \_ Callas \]** "-Attribut kann für Objekt Schnittstellen verwendet werden. In diesem Fall kann die Schnittstellen Definition sowohl für lokale Aufrufe als auch für Remote Aufrufe verwendet werden, da **\[ Aufruf \_ als \]** eine Schnittstelle zulässt, auf die nicht remote zugegriffen werden kann, um einer Remote Schnittstelle transparent zugeordnet zu werden. Der " **\[ \_ Callas \]** "-Attribut kann nicht im [**/OSF**](-osf.md) -Modus verwendet werden.

Nehmen wir beispielsweise an, dass für die Routine **F1** in Object Interface **iface** zahlreiche Konvertierungen zwischen den Benutzer aufrufen und den tatsächlich übertragenen Inhalt erforderlich sind. In den folgenden Beispielen werden die IDL-und ACF-Dateien für die Schnittstelle **iface** beschrieben:

In der IDL-Datei für Interface **iface**:

``` syntax
[local] HRESULT f1 ( <users parameter list> ) 
[call_as( f1 )] long Remf1( <remote parameter list> );
```

In der ACF für Schnittstelle **iface**:

``` syntax
[call_as( f1 )] Remf1();
```

Dies bewirkt, dass die generierte Header Datei die-Schnittstelle mithilfe der Definition von **F1** definiert, aber auch stusb für **Remf1** bereitstellt.

Der mittlerer l-Compiler generiert die folgende Vtable in der Header Datei für die Schnittstelle **iface**:

``` syntax
struct IFace_vtable
{ 
    HRESULT ( * f1) ( <users parameter list> ); 
    /* Other vtable functions. */
};
```

Der Client seitige Proxy verfügt dann über einen typischen, von der Mitte generierten Proxy für **Remf1**, während der serverseitige Stub für **Remf1** mit dem typischen, von der Mittel l generierten Stub identisch ist:

``` syntax
HRESULT IFace_Remf1_Stub ( <parameter list> ) 
{ 
    // Other function code.

    /* instead of IFace_f1 */
    invoke IFace_f1_Stub ( <remote parameter list> ); 

    // Other function code.
}
```

Anschließend müssen die beiden **\[ Aufrufe \_ als \]** Bindungs Routinen (Clientseite und serverseitig) manuell codiert werden:

``` syntax
HRESULT f1_Proxy ( <users parameter list> ) 
{ 
    // Other function code.

    Remf1_Proxy ( <remote parameter list> ); 

    // Other function code.
} 
 
long IFace_f1_Stub ( <remote parameter list> ) 
{ 
    // Other function code.

    IFace_f1 ( <users parameter list> ); 

    // Other function code.
    }
```

Bei Objekt Schnittstellen sind dies die Prototypen für die Bindungs Routinen.

Client seitig:

``` syntax
<local_return_type>  <interface>_<local_routine>_proxy( 
    <local_parameter_list> );
```

Für serverseitig:

``` syntax
<remote_return_type>  <interface>_<local_routine>_stub(
    <remote_parameter_list> );
```

Bei nicht-Objekt Schnittstellen sind dies die Prototypen für die Bindungs Routinen.

Client seitig:

``` syntax
<local_return_type>  <local_routine> ( <local_parameter_list> );
```

Für serverseitig:

``` syntax
<local_return_type>  <interface>_v<maj>_<min>_<local_routine> ( 
    <remote_parameter_list> );
```

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**Darstellung \_ als**](represent-as.md)
</dt> <dt>

[**übertragen \_ als**](transmit-as.md)
</dt> </dl>

 

 




