---
title: Attribut codieren
description: Das Attribut "\ Encode \ ACF" gibt an, dass für eine Prozedur oder einen Datentyp eine Serialisierungsunterstützung erforderlich ist.
ms.assetid: 2661021d-8a26-4216-935b-ca40b6f8b9ec
keywords:
- Codieren von Attributen in der Mitte
topic_type:
- apiref
api_name:
- encode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c2a35c6d6910229a9e14026f6727db5c3176050
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948621"
---
# <a name="encode-attribute"></a>Attribut codieren

Das **\[ COF \] -Attribut codieren** gibt an, dass für eine Prozedur oder einen Datentyp eine Serialisierungsunterstützung erforderlich ist.

``` syntax
[ 
    encode 
    [ , interface-attribute-list] 
] 
interface interface-name
{
    interface-definition
}

[ encode [ , op-attribute-list] ] proc-name

typedef [encode [ , type-attribute-list] ] type-name
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Interface-Attribute-List* 
</dt> <dd>

Gibt andere Attribute an, die auf die gesamte Schnittstelle angewendet werden.

</dd> <dt>

*Schnittstellen Name* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> <dt>

*Schnittstellen Definition* 
</dt> <dd>

Gibt IDL-Anweisungen an, die die Definition der-Schnittstelle bilden.

</dd> <dt>

*OP-Attribute-List* 
</dt> <dd>

Gibt andere operative Attribute an, die für die Prozedur (z **\[** . b. [**Decodierung**](decode.md)) gelten **\]** .

</dd> <dt>

*proc-Name* 
</dt> <dd>

Gibt den Namen der Prozedur an.

</dd> <dt>

*Type-Attribute-List* 
</dt> <dd>

Gibt andere Attribute an, die auf den Typ angewendet werden, z **\[** . b. [**decodieren**](decode.md) **\]** und **\[** [**zuordnen**](allocate.md) **\]** .

</dd> <dt>

*Typname* 
</dt> <dd>

Gibt einen Typ an, der in der IDL-Datei definiert ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **\[ Codieren \]** -Attribut bewirkt, dass der mittlerer l-Compiler Code generiert, der von einer Anwendung zum Serialisieren von Daten in einen Puffer verwendet werden kann. Das **\[** [**decodieren**](decode.md) - **\]** Attribut generiert den Code zum Zurücksetzen von Daten aus einem Puffer.

Verwenden Sie die Attribute **\[ Codieren \]** und **\[** [**decodieren**](decode.md) **\]** in einer ACF, um Serialisierungscode für Prozeduren oder Typen zu generieren, die in der IDL-Datei einer Schnittstelle definiert sind. Bei Verwendung als Schnittstellen Attribut gilt die **\[ Codierung \]** für alle Typen und Prozeduren, die in der IDL-Datei definiert sind. Wenn die **\[ Codierung \]** als Betriebs Attribut verwendet wird, gilt sie nur für die angegebene Prozedur. Wenn die **\[ Codierung \]** als Type-Attribut verwendet wird, gilt sie nur für den angegebenen Typ.

Wenn das Attribut **\[ Codieren \]** oder **\[** [**decodieren**](decode.md) **\]** auf eine Prozedur angewendet wird, generiert der mittlerer l-Compiler einen serialisierungsstub in ähnlicher Weise, wie remotestubs für Remote Routinen generiert werden. Eine Prozedur kann entweder eine Remote-oder eine Serialisierungsprozedur sein, aber nicht beides. Der Prototyp der generierten Routine wird an den Stub gesendet. H-Datei, während der Stub selbst in die Stub- \_ c. c-Datei übergeht.

Der-compilercompiler generiert zwei Funktionen für jeden Typ, auf den das **\[ Codieren \]** -Attribut angewendet wird, und eine zusätzliche Funktion für jeden Typ, auf den das Attribut " **\[** [**Decodierung**](decode.md) " **\]** angewendet wird. Für einen benutzerdefinierten Typ mit dem Namen "MyType" generiert der Compiler z. b. Code für die Funktionen "MyType \_ encode", "MyType \_ Decode" und "MyType \_ alignsize". Für diese Funktionen schreibt der Compiler Prototypen in den Stub. H und Quellcode zu Stub \_ C.C.

Weitere Informationen zu serialisierungshandles und zum Codieren oder Decodieren von Daten finden Sie unter [Serialisierung Services](/windows/desktop/Rpc/serialization-services).

## <a name="examples"></a>Beispiele

``` syntax
/* 
    ACF file example; 
    Assumes MyType1, MyType2, MyType3, MyProc1, MyProc2, MyProc3 defined 
    in IDL file  
    MyType1, MyType2, MyProc1, MyProc2 have encode and decode 
    serialization support 
    MyType3 and MyProc3 have encode serialization support only 
*/ 
[ 
    encode, 
    implicit_handle(handle_t bh) 
]    
interface regress 
{ 
    typedef [ decode ] MyType1; 
    typedef [ encode, decode ] MyType2; 
    [ decode ] MyProcc1(); 
    [ encode ] MyProc2(); 
}
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[**Decodieren**](decode.md)
</dt> </dl>

 

 