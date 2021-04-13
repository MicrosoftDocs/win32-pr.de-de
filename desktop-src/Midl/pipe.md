---
title: Pipe-Attribut
description: Der pipetypkonstruktor ermöglicht das übertragen eines geöffneten Datenstroms von typisierten Daten über einen Remote Prozedur Aufrufe.
ms.assetid: 85b76a55-8df2-4417-9a39-3e3bf49651fc
keywords:
- Pipe-Attribut-Mittel l
topic_type:
- apiref
api_name:
- pipe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0aaab8d399c99e02b5393ee9f5258da53aea491
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314762"
---
# <a name="pipe-attribute"></a>Pipe-Attribut

Der  pipetypkonstruktor ermöglicht das übertragen eines geöffneten Datenstroms von typisierten Daten über einen Remote Prozedur Aufrufe.

``` syntax
typedef pipe element-type pipe-declarator;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Elementtyp* 
</dt> <dd>

Definiert die Größe eines einzelnen Elements im Übertragungs Puffer. Der *Elementtyp* kann ein [Basistyp](midl-base-types.md), ein vordefinierter \_ Typ, eine [**Struktur**](struct.md), eine [**32B-Enumeration**](v1-enum.md)oder ein Typbezeichner sein. Einige Einschränkungen gelten für *Element \_ Typen*, wie in den Hinweisen weiter unten beschrieben.

</dd> <dt>

*Pipe-declarator* 
</dt> <dd>

Gibt einen oder mehrere Bezeichner oder Zeiger auf Bezeichner an. Trennen Sie mehrere Deklaratoren durch Kommas.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Sie **können den** pipetypkonstruktor verwenden, um Daten in beide Richtungen zu übertragen. Ein **\[** [**in**](in.md) **\]** Pipe-Parameter ermöglicht dem Server das Abrufen des Datenstroms vom Client während eines Remote Prozedur Aufrufes. Ein **\[** [**out**](out-idl.md) - **\]** Pipe-Parameter ermöglicht es dem Server, den Datenstrom an den Client zurückzusenden. Sie stellen die Client seitigen Routinen bereit, um den Datenstream per Push und Pull abzurufen und einen globalen Puffer für die Daten zuzuordnen. Die Client-und Serverstub-Routinen Mars Hallen und entsperren Daten und übergeben einen Verweis auf den Puffer zurück an die Anwendung.

Für Pipes gelten die folgenden Einschränkungen:

-   Ein Pipe-Element darf weder einen Zeiger, ein konformes-Array noch ein unterschiedliches Array, ein Handle oder ein Kontext Handle enthalten. Außerdem kann ein Pipe-Element in der Microsoft-Implementierung von Pipes weder eine [**Union**](union.md), eine [**16B-Enumeration**](enum.md)noch eine [**\_ \_ int3264**](--int3264.md)enthalten.
-   Die Attribute "über **\[** [**Tragung \_ als**](transmit-as.md)", " **\]** **\[** [**darstellen \_ als**](represent-as.md)" **\]** , " **\[** [**Wire \_ Marshal**](wire-marshal.md)" oder " **\]** **\[** [**User \_ Marshal**](user-marshal.md) " können nicht **\]** auf einen Pipetyp oder auf den *Elementtyp* angewendet werden.
-   Ein Pipetyp kann kein Member einer Struktur oder Union, des Ziels eines Zeigers oder des Basistyps eines Arrays sein.
-   Ein als Pipetyp deklarierter Datentyp kann nur als Parameter eines Remote Aufrufes verwendet werden.
-   Sie können einen Pipe-Parameter in beide Richtungen als Wert oder als Verweis übergeben **\[** [**(Verweis**](ref.md) **\]** Zeiger). Allerdings können Sie das **\[** [**ptr**](ptr.md) - **\]** Attribut nicht auf eine Pipe anwenden, die als Verweis übergeben wird. Es ist nicht möglich, einen Pipe-Parameter mit einem **\[** [**eindeutigen**](unique.md) **\]** oder einem vollständigen Zeiger anzugeben, unabhängig von der Richtung.
-   Pipes können nicht in **\[** [**Objekt**](object.md) **\]** Schnittstellen verwendet werden.
-   Sie können das **\[** [**idempotente**](idempotent.md) - **\]** Attribut nicht auf eine Routine anwenden, die über einen Pipe-Parameter verfügt.
-   Sie können die Serialisierungsattribute nicht verwenden, **\[** [**Codieren**](encode.md) **\]** und **\[** mit Pipes [**decodieren**](decode.md) **\]** .
-   Sie können automatische Handles weder standardmäßig noch mit dem **\[** [**Auto \_ handle**](auto-handle.md) - **\]** Attribut mit Pipes verwenden.

> [!Note]  
> Der mittlerer l-Compiler unterstützt Pipes nur im [**/OIF**](-oi.md) -Modus.

 

Weitere Informationen zum Implementieren von Routinen mit Pipe-Parametern finden Sie unter [Pipes](/windows/desktop/Rpc/pipes) im RPC-Programmier Handbuch und in der Referenz.

## <a name="examples"></a>Beispiele

``` syntax
typedef pipe unsigned char UCHAR_PIPE1, UCHAR_PIPE2;
 
//SIMPLE_STRUCT defined elsewhere
typedef pipe SIMPLE_STRUCT SIMPLE_STRUCT_PIPE;
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Automatisches \_ handle**](auto-handle.md)
</dt> <dt>

[Mittel l-Basis Typen](midl-base-types.md)
</dt> <dt>

[**Decodieren**](decode.md)
</dt> <dt>

[**Codieren**](encode.md)
</dt> <dt>

[**Enumeration**](enum.md)
</dt> <dt>

[**idempotent**](idempotent.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**Objekt (object)**](object.md)
</dt> <dt>

[**vorgenommen**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Darstellung \_ als**](represent-as.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**übertragen \_ als**](transmit-as.md)
</dt> <dt>

[**gem**](unique.md)
</dt> <dt>

[**Benutzer \_ Mars Hall**](user-marshal.md)
</dt> <dt>

[**Wire \_ Marshal**](wire-marshal.md)
</dt> </dl>

 

 