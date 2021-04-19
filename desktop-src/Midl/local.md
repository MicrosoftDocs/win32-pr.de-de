---
title: Lokales Attribut
description: Das Attribut \ local \ gibt für den Mittelwert Compiler an, dass eine Schnittstelle oder Funktion nicht Remote ist.
ms.assetid: 17ad3d87-4ca4-4e9b-91bc-280c03830f54
keywords:
- lokales Attribut, Mittel l
topic_type:
- apiref
api_name:
- local
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40b1842bf637d3b7fcaab7a0c13319def1d1663
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106337824"
---
# <a name="local-attribute"></a>Lokales Attribut

Das **\[ lokale \]** Attribut gibt für den mittlerer l-Compiler an, dass eine Schnittstelle oder Funktion nicht Remote ist.

``` syntax
[ 
    local 
    [, interface-attribute-list] 
] 
interface interface-name
{
}

[ 
    object, 
    uuid(string-uuid), 
    local [, interface-attribute-list] 
]
interface interface-name
{
}

[ local [, function-attribute-list] ] function-declarator ;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Interface-Attribute-List* 
</dt> <dd>

Gibt andere Attribute an, die auf die gesamte Schnittstelle angewendet werden. Die Attribute **\[** [**EndPoint**](endpoint.md) **\]** , **\[** [**Version**](version.md) **\]** und **\[** [**Zeiger \_ Standard**](pointer-default.md) **\]** sind optional. Wenn Sie mit dem [**/App \_ config**](-app-config.md) -Schalter kompilieren, **\[** kann auch ein [**implizites \_ handle**](implicit-handle.md) **\]** oder ein **\[** [**Automatisches \_ handle**](auto-handle.md) **\]** vorhanden sein. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Schnittstellen Name* 
</dt> <dd>

Gibt den Namen an, mit dem Softwarekomponenten die Schnittstelle definieren können.

</dd> <dt>

*Zeichenfolge-UUID* 
</dt> <dd>

Gibt eine UUID-Zeichenfolge an, die vom Hilfsprogramm uuidgen generiert wird. Wenn Sie nicht den Mittel-Compilerschalter [**/OSF**](-osf.md)verwenden, können Sie die UUID-Zeichenfolge in Anführungszeichen einschließen.

</dd> <dt>

*Function-Attribute-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten. Gültige Funktions Attribute sind **\[** [**Callback**](callback.md), **\]** das Zeiger Attribut **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** und die Verwendungs Attribute **\[** [**Zeichenfolge**](string.md) **\]** , **\[** [**ignorieren**](ignore.md) **\]** und **\[** [**Kontext \_ handle**](context-handle.md) **\]** . Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Function-declarator* 
</dt> <dd>

Gibt den Typspezifizierer, den Funktionsnamen und die Parameterliste für die Funktion an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **\[ lokale \]** Attribut kann auf einzelne Funktionen oder auf die gesamte Schnittstelle angewendet werden.

Wenn das **\[ lokale \]** Attribut im Schnittstellen Header verwendet wird, können Sie den Mittel l-Compiler als Header Generator verwenden. Der Compiler generiert keine stubweise für Funktionen und stellt nicht sicher, dass der Header übertragen werden kann.

Für eine RPC-Schnittstelle kann das **\[ lokale \]** Attribut nicht gleichzeitig mit dem **\[** [**UUID**](uuid.md) -Attribut verwendet werden **\]** . Im Schnittstellen Header muss entweder **\[ UUID \]** oder **\[ local \]** vorhanden sein, und der von Ihnen gewählte muss genau einmal erfolgen.

Für eine COM-Schnittstelle (identifiziert durch das **\[** [**Objekt**](object.md) **\]** Schnittstellen Attribut) kann die Schnittstellen Attribut Liste das **\[ lokale \]** Attribut enthalten, auch wenn das **\[** [**UUID**](uuid.md) - **\]** Attribut vorhanden ist.

Wenn Sie in einer einzelnen Funktion verwendet wird, kennzeichnet das **\[ lokale \]** Attribut eine lokale Prozedur, für die keine stut generiert werden. Die Verwendung des **\[ lokalen \]** as a function-Attributs ist eine Microsoft-Erweiterung für DCE IDL. Daher ist dieses Attribut nicht verfügbar, wenn Sie mithilfe des [**/OSF**](-osf.md) -Schalters für mittlere Kompilierung kompilieren.

Beachten Sie, dass eine Schnittstelle ohne Attribute in eine Basis-IDL-Datei importiert werden kann. Allerdings darf die-Schnittstelle nur Datentypen ohne Prozeduren enthalten. Wenn auch eine Prozedur in der Schnittstelle enthalten ist, muss ein lokales Attribut oder ein uuid-Attribut angegeben werden.

## <a name="examples"></a>Beispiele

``` syntax
/* IDL file #1 */ 
[
    local
] 
interface local_procs 
{ 
    void MyLocalProc(void);
} 
 
/* IDL file #2 */ 
[
    object, 
    uuid(12345678-1234-1234-123456789ABC), 
    local
] 
interface local_object_procs : IUnknown
{ 
    void MyLocalObjectProc(void);
} 
 
/* IDL file #3 */ 
[
    uuid(87654321-1234-1234-123456789ABC)
] 
interface mixed_procs 
{ 
    [local] void MyLocalProc(void); 
    HRESULT MyRemoteProc([in] short sParam); 
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**/APP- \_ Konfiguration**](-app-config.md)
</dt> <dt>

[**Automatisches \_ handle**](auto-handle.md)
</dt> <dt>

[**Rückruf**](callback.md)
</dt> <dt>

[**Kontext \_ handle**](context-handle.md)
</dt> <dt>

[**Dreher**](endpoint.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**lassen**](ignore.md)
</dt> <dt>

[**implizites \_ handle**](implicit-handle.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**Objekt (object)**](object.md)
</dt> <dt>

[**Zeiger \_ Standard**](pointer-default.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Zeichenfolge**](string.md)
</dt> <dt>

[**gem**](unique.md)
</dt> <dt>

[**UUID**](uuid.md)
</dt> <dt>

[**version**](version.md)
</dt> </dl>

 

 




