---
title: typedef-Attribut
description: Das IDL-typedef-Schlüsselwort lässt typedef-Deklarationen zu, die den Deklarationen der C-Programmiersprache typedef sehr ähneln.
ms.assetid: 995a233e-0d07-4051-9f00-d1dc0b563f8f
keywords:
- typedef-Attribut-Mittel l
topic_type:
- apiref
api_name:
- typedef
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecfce98e5a83f8d2a5e2499a5ceceba755e68f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725144"
---
# <a name="typedef-attribute"></a>typedef-Attribut

Das IDL- **typedef** -Schlüsselwort lässt **typedef** -Deklarationen zu, die den Deklarationen der C-Programmiersprache **typedef** sehr ähneln.

``` syntax
/* IDL file typedef syntax */
typedef [[ [ idl-type-attribute-list ] ]] type-specifier declarator-list;

/* ACF typedef syntax */
typedef [ acf-type-attribute-list ] typename;
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*IDL-Type-Attribute-List* 
</dt> <dd>

Gibt ein oder mehrere Attribute an, die auf den Typ angewendet werden. Gültige Typattribute in einer IDL-Datei sind **\[** [**handle**](handle.md) **\]** , **\[** [**\_ Switchtyp**](switch-type.md) **\]** , über **\[** [**Tragung \_ als**](transmit-as.md) **\]** ; Zeiger Attribut Verweis **\[** [](ref.md) **\]** , **\[** [**eindeutig**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** und das **\[** [**Kontext \_ handle**](context-handle.md) **\]** , die **\[** [**Zeichenfolge**](string.md) **\]** und **\[** [](ignore.md) **\]** die Syntax der Verwendungs Attribute. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt einen [Basistyp](midl-base-types.md), eine [**Struktur**](struct.md), eine [**Union**](union.md), einen [**Enumeration**](enum.md) -Typ oder einen Typbezeichner an. Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden. Das [**Schlüssel**](const.md) Wort "Schlüsselwort" kann dem *Typspezifizierer* vorangestellt werden.

</dd> <dt>

*Deklarator-List* 
</dt> <dd>

Gibt standardmäßige Mittelwert Deklaratoren an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren. Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers). Die *declarator-List* besteht aus einem oder mehreren Deklaratoren, die durch Kommas getrennt sind.

</dd> <dt>

*ACF-Type-Attribute-List* 
</dt> <dd>

Gibt ein oder mehrere Attribute an, die auf den Typ angewendet werden. Zu den gültigen Typattributen in einer ACF gehören **\[** [**zuordnen**](allocate.md) **\]** , **\[** [**Codieren**](encode.md) **\]** und **\[** [**decodieren**](decode.md) **\]** .

</dd> <dt>

*typeName* 
</dt> <dd>

Gibt einen Typ an, der in der IDL-Datei definiert ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die IDL- **typedef** -Deklaration wird erweitert, um es Ihnen zu ermöglichen, den definierten Typen Typattribute zuzuordnen. Gültige Typattribute sind **\[** [**handle**](handle.md) **\]** , **\[** [**\_ Switchtyp**](switch-type.md) **\]** , über **\[** [**Tragung \_ als**](transmit-as.md) **\]** ; Zeiger Attribut Verweis **\[** [](ref.md) **\]** , **\[** [**eindeutig**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** ; und die Verwendungs Attribute **\[** [**Kontext \_ handle**](context-handle.md) **\]** , **\[** [**String**](string.md) **\]** und **\[** [**Ignore**](ignore.md) **\]** .

Das **typedef** -Schlüsselwort in einer ACF wendet Attribute auf Typen an, die in der entsprechenden IDL-Datei definiert sind. Beispielsweise können Sie mit dem Attribut " [**zuordnen**](allocate.md) " die Speicher Belegung und die Aufhebung der Zuordnung sowohl von der Anwendung als auch vom Stub anpassen.

Die ACF- **typedef** -Anweisung wird als Teil des ACF-Texts angezeigt. Beachten Sie, dass die ACF- **typedef** -Syntax von der IDL- **typedef** -Syntax und der Syntax der C-Programmiersprache **typedef** abweicht. In der ACF können keine neuen Typen eingeführt werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[**Mikro**](arrays-1.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**Kontext \_ handle**](context-handle.md)
</dt> <dt>

[**Decodieren**](decode.md)
</dt> <dt>

[**Codieren**](encode.md)
</dt> <dt>

[**Enumeration**](enum.md)
</dt> <dt>

[**bewältigen**](handle.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**lassen**](ignore.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Zeichenfolge**](string.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**\_Switchtyp**](switch-type.md)
</dt> <dt>

[**übertragen \_ als**](transmit-as.md)
</dt> <dt>

[**Union**](union.md)
</dt> <dt>

[**gem**](unique.md)
</dt> </dl>

 

 