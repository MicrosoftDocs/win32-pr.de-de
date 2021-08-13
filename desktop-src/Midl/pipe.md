---
title: pipe-Attribut
description: Der Pipetypkonstruktor ermöglicht die Übertragung eines open-ended-Datenstroms von typierten Daten über einen Remoteprozeduraufruf.
ms.assetid: 85b76a55-8df2-4417-9a39-3e3bf49651fc
keywords:
- Pipeattribut MIDL
topic_type:
- apiref
api_name:
- pipe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b8c407bef0a9e610d21e7221eb9a06560f33300f4f1f388fa699ca9dfb18531
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641953"
---
# <a name="pipe-attribute"></a>pipe-Attribut

Der  Pipetypkonstruktor ermöglicht die Übertragung eines open-ended-Datenstroms von typierten Daten über einen Remoteprozeduraufruf.

``` syntax
typedef pipe element-type pipe-declarator;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Elementtyp* 
</dt> <dd>

Definiert die Größe eines einzelnen Elements im Übertragungspuffer. Der *Elementtyp kann* ein [Basistyp,](midl-base-types.md)ein vordefinierter Typ, eine \_ Struktur, eine [**32b-enum**](v1-enum.md)oder ein Typbezeichner sein. [](struct.md) Für Elementtypen gelten *mehrere \_ Einschränkungen,* wie unten in den Anmerkungen beschrieben.

</dd> <dt>

*Pipedeklarator* 
</dt> <dd>

Gibt einen oder mehrere Bezeichner oder Zeiger auf Bezeichner an. Trennen Sie mehrere Deklaratoren durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Sie können den **Pipetypkonstruktor** verwenden, um Daten in beide Richtungen zu übertragen. Ein **\[** [**In-Pipe-Parameter**](in.md) ermöglicht es dem Server, den Datenstrom während eines Remoteprozeduraufrufs vom **\]** Client zu pullen. Mit **\[** [**einem out**](out-idl.md) **\]** pipe-Parameter kann der Server den Datenstrom zurück an den Client übertragen. Sie geben die clientseitigen Routinen zum Pushen und Pullen des Datenstroms sowie zum Zuordnen eines globalen Puffers für die Daten an. Die Client- und Serverstubroutinen marshallen und entmarshalieren Daten und übergeben einen Verweis auf den Puffer zurück an die Anwendung.

Die folgenden Einschränkungen gelten für Pipes:

-   Ein Pipeelement darf kein Zeiger, ein konformes oder variierendes Array, ein Handle oder ein Kontexthand handle sein oder enthalten. Außerdem kann ein Pipeelement in der Microsoft-Implementierung von Pipes keine [**Union,**](union.md) [**eine 16b-enum**](enum.md)oder [**\_ \_ eine int3264**](--int3264.md)sein oder enthalten.
-   Sie können die Übertragung nicht **\[** [**\_ als**](transmit-as.md) **\]** , darstellen **\[** [**\_ als**](represent-as.md) **\]** , **\[** [**Wire \_ Marshal**](wire-marshal.md)oder Benutzer-Marshallingattribute **\]** **\[** [**\_**](user-marshal.md) **\]** auf einen Pipetyp oder auf den Elementtyp anwenden.
-   Ein Pipetyp darf kein Member einer Struktur oder Union, das Ziel eines Zeigers oder der Basistyp eines Arrays sein.
-   Ein Als Pipetyp deklarierter Datentyp kann nur als Parameter eines Remoteaufrufs verwendet werden.
-   Sie können einen Pipeparameter in beide Richtungen als Wert oder als Verweis **\[** [](ref.md) **\]** (Verweiszeiger) übergeben. Sie können das **\[** [**ptr-Attribut jedoch nicht**](ptr.md) **\]** auf eine Pipe anwenden, die als Verweis übergeben wird. Sie können keinen Pipeparameter mit einem **\[** [**eindeutigen oder**](unique.md) vollständigen Zeiger **\]** angeben, unabhängig von der Richtung.
-   Pipes können nicht in **\[** [**Objektschnittstellen verwendet**](object.md) **\]** werden.
-   Sie können das **\[** [**idempotente Attribut nicht auf**](idempotent.md) eine **\]** Routine anwenden, die über einen Pipeparameter verfügt.
-   Sie können die Serialisierungsattribute nicht verwenden, nicht mit Pipes **\[** [](encode.md) **\]** codieren und **\[** [**decodieren.**](decode.md) **\]**
-   Automatische Handles können nicht standardmäßig oder mit dem AutoHandles-Attribut mit Pipes verwendet **\[** [**\_**](auto-handle.md) **\]** werden.

> [!Note]  
> Der MIDL-Compiler unterstützt pipes nur im [**/Oif-Modus.**](-oi.md)

 

Weitere Informationen zum Implementieren von Routinen mit Pipeparametern finden Sie unter [Pipes](/windows/desktop/Rpc/pipes) im RPC-Programmiererhandbuch und in der Referenz.

## <a name="examples"></a>Beispiele

``` syntax
typedef pipe unsigned char UCHAR_PIPE1, UCHAR_PIPE2;
 
//SIMPLE_STRUCT defined elsewhere
typedef pipe SIMPLE_STRUCT SIMPLE_STRUCT_PIPE;
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Automatisches \_ Handle**](auto-handle.md)
</dt> <dt>

[MIDL-Basistypen](midl-base-types.md)
</dt> <dt>

[**Decodieren**](decode.md)
</dt> <dt>

[**Codieren**](encode.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[**In**](in.md)
</dt> <dt>

[**Objekt (object)**](object.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**darstellen \_ als**](represent-as.md)
</dt> <dt>

[**Struktur**](struct.md)
</dt> <dt>

[**übertragen \_ als**](transmit-as.md)
</dt> <dt>

[**Einzigartige**](unique.md)
</dt> <dt>

[**\_Benutzer-Marshalling**](user-marshal.md)
</dt> <dt>

[**Wire \_ Marshal**](wire-marshal.md)
</dt> </dl>

 

 