---
title: Bereichsattribut
description: Mit dem Attribut \ Range \ können Sie einen Bereich zulässiger Werte für Argumente oder Felder angeben, deren Werte zur Laufzeit festgelegt werden. Bei Verwendung mit einem Pipetyp gibt das-Attribut den zulässigen Bereich für die Anzahl von Elementen in den pipesegmenten an.
ms.assetid: 1609fea5-e82c-4389-b4f4-2cd8d0622cde
keywords:
- Bereichs Attribut-Mittel l
topic_type:
- apiref
api_name:
- range
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e095d420afc433c1f01a63dff51868e57efc50f4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339475"
---
# <a name="range-attribute"></a>Bereichsattribut

Mit dem **\[ Range \]** -Attribut können Sie einen Bereich zulässiger Werte für Argumente oder Felder angeben, deren Werte zur Laufzeit festgelegt werden. Bei Verwendung mit einem Pipetyp gibt das-Attribut den zulässigen Bereich für die Anzahl von Elementen in den pipesegmenten an.

``` syntax
[range(low-val,high-val)] type-specifier declarator
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*niedrig-Val* 
</dt> <dd>

Der niedrigste zulässige Wert, den der-Parameter oder das-Feld enthalten kann.

</dd> <dt>

*High-Val* 
</dt> <dd>

Der höchste zulässige Wert, den der-Parameter oder das-Feld enthalten kann.

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Ein ganzzahliger Typ, der nicht [**Hyper**](hyper.md) oder [**\_ \_ Int64**](--int64.md), ein Typbezeichner für einen ganzzahligen Typ, ein [**Enumeration**](enum.md) -Typ oder ein pipetypname ist.

</dd> <dt>

*Deklarator* 
</dt> <dd>

Ein standardmäßiger C-Deklarator, z. b. ein Bezeichner.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Verwenden Sie das **\[ Range \]** -Attribut, um die Bedeutung von sensiblen Parametern oder Feldern zu ändern, z. b. für die Größe oder Länge, mit konformen oder variierenden Arrays, oder wenn Sie einen Parameter-oder Feldwert auf einen Bereich gültiger Werte überprüfen möchten. Das-Attribut gilt sowohl für Parameter der obersten Ebene als auch für Parameter und Felder auf niedrigerer Ebene. Durch das Hinzufügen des **\[ Range \]** -Attributs zu einem Typ wird das Wire-Format nicht geändert, und die Abwärtskompatibilität wird daher nicht beeinträchtigt.

Das **\[ Range \]** -Attribut kann auch für konforme Daten wie z. b. Puffer oder Arrays mit einem Konformitäts Attribut verwendet werden. Der Effekt besteht darin, alle Konformitäts Größen für die konformen Daten auf den angegebenen Bereich zu beschränken. Wenn es sich bei den überein kompatiblen Daten um ein mehrdimensionales Array handelt, ist jede Array Dimension auf den angegebenen Bereich beschränkt.

Die Verwendung des **\[ Bereichs \]** für konforme Daten erfordert, dass das Kompilierungs Ziel den Wert "nt60" oder höher hat.

Beachten Sie, dass Sie die [**/robust**](-robust.md) -Compileroption verwenden müssen, wenn Sie Ihre IDL-Datei kompilieren, um den Stub-Code zu generieren, der diese Überprüfungen durchführt. Ohne den Schalter **/robust** ignoriert der Mittell-Compiler dieses Attribut.

## <a name="examples"></a>Beispiele

``` syntax
HRESULT Method1(
    [in, range(0,100)] ULONG m,
    [in, range(0,100)] ULONG n,
    [size_is(m,n)] ULONG **pplong);

void InPipe(
    [in, range(0, MAX_CHUNK) LONG_PIPE pipe_date);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[Arrays](/windows/desktop/Rpc/arrays)
</dt> <dt>

[**der erste \_ ist**](first-is.md)
</dt> <dt>

[**Letzter \_ ist**](last-is.md)
</dt> <dt>

[**Länge \_ ist**](length-is.md)
</dt> <dt>

[**Max \_ ist**](max-is.md)
</dt> <dt>

[**/robust**](-robust.md)
</dt> <dt>

[**Größe \_ :**](size-is.md)
</dt> <dt>

[**Switch \_ ist**](switch-is.md)
</dt> </dl>

 

 