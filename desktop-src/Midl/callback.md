---
title: Rückruf Attribut
description: Das Attribut \ Callback \ deklariert eine statische Rückruffunktion, die auf der Clientseite der verteilten Anwendung vorhanden ist. Rückruf Funktionen bieten dem Server die Möglichkeit, Code auf dem Client auszuführen.
ms.assetid: c78947ae-614c-4f33-9ab7-1231e5031f80
keywords:
- Rückruf Attribut-Mittel l
topic_type:
- apiref
api_name:
- callback
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379aa3cbef4df872f8b133017b1b06a6c73e8181
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390253"
---
# <a name="callback-attribute"></a>Rückruf Attribut

Das **\[ Callback \]** -Attribut deklariert eine statische Rückruffunktion, die auf der Clientseite der verteilten Anwendung vorhanden ist. Rückruf Funktionen bieten dem Server die Möglichkeit, Code auf dem Client auszuführen.

``` syntax
[callback [ , function-attr-list] ] type-specifier [ptr-declarator] function-name(
        [ [attribute-list] ] type-specifier [declarator]
        , ...);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Function-attr-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten. Gültige Funktions Attribute sind **\[** [**local**](local.md), **\]** das Zeiger Attribut **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** und die Verwendungs Attribute **\[** [**Zeichenfolge**](string.md) **\]** , **\[** [**ignorieren**](ignore.md) **\]** und **\[** [**Kontext \_ handle**](context-handle.md) **\]** . Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt einen [ \_ Basistyp](midl-base-types.md), eine [**Struktur**](struct.md), eine [**Union**](union.md), einen [**Enumeration**](enum.md) -Typ oder einen Typbezeichner an. Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.

</dd> <dt>

*PTR-Deklarator* 
</dt> <dd>

Gibt 0 (null) oder mehr Zeiger Deklaratoren an. Ein zeigerdeklarator ist derselbe wie der in C verwendete zeigerdeklarator. Sie wird aus dem Kenn \* Zeichner, den Modifizierern, z. b. **weit**, und dem Qualifizierer " [**Konstanten**](const.md)" erstellt.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Remote Prozedur an.

</dd> <dt>

*Attribut-List* 
</dt> <dd>

Gibt 0 (null) oder mehr direktionale Attribute, Feld Attribute, Verwendungs Attribute und Zeiger Attribute an, die für den angegebenen Parametertyp geeignet sind. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Deklarator* 
</dt> <dd>

Gibt einen Standard-C-Deklarator an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren. Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers). Der Parameter-Name-Bezeichner ist optional.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **\[ Rückruf \]** Funktion ist hilfreich, wenn der Server Informationen vom Client abrufen muss. , Wenn Server Anwendungen unter Windows 3 unterstützt werden. *x*, der Server kann eine Remote Prozedur auf Windows 3 abrufen. *x* -Server, um die benötigten Informationen zu erhalten. Die Rückruffunktion erreicht denselben Zweck und ermöglicht dem Server, Informationen im Kontext des ursprünglichen Aufrufs abzufragen.

Rückrufe sind Sonderfälle von Remote aufrufen, die als Teil eines einzelnen Threads ausgeführt werden. Ein Rückruf wird im Kontext eines Remote Aufrufs ausgegeben. Alle Remote Prozeduren, die als Teil derselben Schnittstelle wie die statische Rückruffunktion definiert sind, können die Rückruffunktion aufzurufen.

Beachten Sie, dass die Verwendung von \[ Callback bei der \] Multithreadprogrammierung nicht empfohlen wird. Als Single Thread-Programmierfunktion ist Sie nicht für die Unterstützung der Sicherheitsanforderungen, die eine Multithreadumgebung bereitstellt, bereit.

Die **rpccancelthread** -Funktion kann nicht zum Abbrechen eines Aufrufs verwendet werden, der möglicherweise einen statischen Rückruf versendet. Wenn ein bestimmter Remote Prozedur Aufrufs nie zu einem Rückruf führt, kann er abgebrochen werden. Andernfalls kann ein-Rückruf nur abgebrochen werden, wenn sichergestellt werden kann, dass kein Rückruf für ihn ausgegeben wurde.

Nur die Verbindungs orientierten und lokalen Protokoll Sequenzen unterstützen das Rückruf Attribut. Die Größe der \[ out \] -Daten für Rückrufe über die lokale Protokoll Sequenz ist auf 150 Bytes beschränkt. Wenn eine RPC-Schnittstelle eine verbindungslose (Datagram) Protokoll Sequenz verwendet, schlagen Aufrufe von Prozeduren mit dem Rückruf Attribut fehl.

Handles können nicht als Parameter in Rückruf Funktionen verwendet werden. Da Rückrufe immer im Kontext eines-Aufrufes ausgeführt werden, wird das Bindungs handle, das vom Client für den Aufruf des Servers verwendet wird, auch als Bindungs Handle vom Server zum Client verwendet.

Rückrufe können in beliebiger Tiefe verschachtelt werden.

## <a name="examples"></a>Beispiele

``` syntax
[callback] HRESULT DisplayString([in, string] char * p1);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Mikro**](arrays-1.md)
</dt> <dt>

[Mittel l-Basis Typen](midl-base-types.md)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[**Kontext \_ handle**](context-handle.md)
</dt> <dt>

[**Enumeration**](enum.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**lassen**](ignore.md)
</dt> <dt>

[**nah**](local.md)
</dt> <dt>

[**/osf**](-osf.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**Zeichenfolge**](string.md)
</dt> <dt>

[**struct**](struct.md)
</dt> <dt>

[**Union**](union.md)
</dt> <dt>

[**gem**](unique.md)
</dt> <dt>

[**Rpccancelthread**](/windows/desktop/api/rpcdce/nf-rpcdce-rpccancelthread)
</dt> </dl>

 

 