---
title: Rückrufattribut
description: Das Attribut \callback\ deklariert eine statische Rückruffunktion, die auf der Clientseite der verteilten Anwendung vorhanden ist. Rückruffunktionen bieten dem Server die Möglichkeit, Code auf dem Client auszuführen.
ms.assetid: c78947ae-614c-4f33-9ab7-1231e5031f80
keywords:
- Rückrufattribut MIDL
topic_type:
- apiref
api_name:
- callback
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e77eb93a78553ccbc95b1671dc215012eeccc56b0bff8ea23e47f68aaf51e10b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807336"
---
# <a name="callback-attribute"></a>Rückrufattribut

Das **\[ \] Rückrufattribut** deklariert eine statische Rückruffunktion, die auf der Clientseite der verteilten Anwendung vorhanden ist. Rückruffunktionen bieten dem Server die Möglichkeit, Code auf dem Client auszuführen.

``` syntax
[callback [ , function-attr-list] ] type-specifier [ptr-declarator] function-name(
        [ [attribute-list] ] type-specifier [declarator]
        , ...);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*function-attr-list* 
</dt> <dd>

Gibt null oder mehr Attribute an, die für die Funktion gelten. Gültige Funktionsattribute sind **\[** [**lokal;**](local.md) **\]** das Zeigerattribut **\[** [**ref**](ref.md), **\]** **\[** [**eindeutig**](unique.md)oder **\]** **\[** [**ptr;**](ptr.md)und die **\]** Verwendungsattribute **\[** [**Zeichenfolge**](string.md), **\]** **\[** [**ignorieren**](ignore.md)und **\]** **\[** [**\_ Kontexthandle**](context-handle.md) **\]** . Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt einen [ \_ Basistyp,](midl-base-types.md) [**eine Struktur,**](struct.md) [**einen Union-,**](union.md) [**Enumerations-**](enum.md) oder Typbezeichner an. Eine optionale Speicherspezifikation kann dem *Typspezifizierer* vorangestellt werden.

</dd> <dt>

*ptr-declarator* 
</dt> <dd>

Gibt null oder mehr Zeigerdeklaratoren an. Ein Zeigerdeklarator entspricht dem in C verwendeten Zeigerdeklarator. sie wird aus dem \* Bezeichner, Modifizierern wie **far** und dem Qualifizierer [**const**](const.md)erstellt.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Remoteprozedur an.

</dd> <dt>

*Attributliste* 
</dt> <dd>

Gibt null oder mehr direktionale Attribute, Feldattribute, Verwendungsattribute und Zeigerattribute an, die für den angegebenen Parametertyp geeignet sind. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Deklarator* 
</dt> <dd>

Gibt einen C-Standarddeklarator an, z. B. Bezeichner, Zeigerdeklaratoren und Arraydeklaratoren. Weitere Informationen finden Sie unter [Array- und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger.](/windows/desktop/Rpc/arrays-and-pointers) Der Parameternamenbezeichner ist optional.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **\[ Rückruffunktion \]** ist nützlich, wenn der Server Informationen vom Client abrufen muss. Wenn Serveranwendungen auf Windows 3 unterstützt wurden. *x*, könnte der Server eine Remoteprozedur auf der Windows 3 aufrufen. *x* Server, um die erforderlichen Informationen abzurufen. Die Rückruffunktion erfüllt denselben Zweck und ermöglicht es dem Server, den Client im Kontext des ursprünglichen Aufrufs nach Informationen abzufragen.

Rückrufe sind Sonderfälle von Remoteaufrufen, die als Teil eines einzelnen Threads ausgeführt werden. Ein Rückruf wird im Kontext eines Remoteaufrufs ausgegeben. Jede Remoteprozedur, die als Teil derselben Schnittstelle wie die statische Rückruffunktion definiert ist, kann die Rückruffunktion aufrufen.

Es ist wichtig zu beachten, dass die Verwendung des Rückrufs bei der \[ \] Multithreadprogrammierung nicht empfohlen wird. Als Singlethread-Programmierfunktion ist sie nicht für die Unterstützung der Sicherheitsanforderungen einer Multithreadumgebung ausgestattet.

Die **RpcCancelThread-Funktion** kann nicht verwendet werden, um einen Aufruf abzubrechen, der einen statischen Rückruf senden kann. Wenn ein bestimmter Remoteprozeduraufruf nie zu einem Rückruf führt, kann er abgebrochen werden. Andernfalls kann ein Aufruf nur abgebrochen werden, wenn sichergestellt werden kann, dass kein Rückruf für ihn ausgegeben wurde.

Nur die verbindungsorientierten und lokalen Protokollsequenzen unterstützen das Rückrufattribut. Die Größe der \[ \] ausgehenden Daten für Rückrufe über die lokale Protokollsequenz ist auf 150 Bytes beschränkt. Wenn eine RPC-Schnittstelle eine verbindungslose Protokollsequenz (Datagramm) verwendet, schlagen Aufrufe von Prozeduren mit dem Rückrufattribut fehl.

Handles können nicht als Parameter in Rückruffunktionen verwendet werden. Da Rückrufe immer im Kontext eines Aufrufs ausgeführt werden, wird das Bindungshandle, das vom Client zum Aufrufen des Servers verwendet wird, auch als Bindungshandle vom Server an den Client verwendet.

Rückrufe können in beliebige Tiefe geschachtelt werden.

## <a name="examples"></a>Beispiele

``` syntax
[callback] HRESULT DisplayString([in, string] char * p1);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Arrays**](arrays-1.md)
</dt> <dt>

[MIDL-Basistypen](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**\_Kontexthandle**](context-handle.md)
</dt> <dt>

[**Enum**](enum.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**Ignorieren**](ignore.md)
</dt> <dt>

[**lokal**](local.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Ptr**](ptr.md)
</dt> <dt>

[**Schnur**](string.md)
</dt> <dt>

[**Struktur**](struct.md)
</dt> <dt>

[**Union**](union.md)
</dt> <dt>

[**Einzigartige**](unique.md)
</dt> <dt>

[**RpcCancelThread**](/windows/desktop/api/rpcdce/nf-rpcdce-rpccancelthread)
</dt> </dl>

 

 