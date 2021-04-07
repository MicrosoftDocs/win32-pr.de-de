---
title: context_handle-Attribut
description: Das \ Context \_ handle \-Attribut identifiziert ein Bindungs handle, das Kontext-oder Zustandsinformationen auf dem Server zwischen Remote Prozedur aufrufen verwaltet.
ms.assetid: ab1aee44-4add-4816-a7ef-38bbf7b38918
keywords:
- context_handle Attribut-Mittel l
topic_type:
- apiref
api_name:
- context_handle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d71c47554454118d584110ec43211a302e12cd77
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724960"
---
# <a name="context_handle-attribute"></a>Kontext \_ handle-Attribut

Das **\[ Kontext \_ handle \]** -Attribut identifiziert ein Bindungs handle, das Kontext-oder Zustandsinformationen auf dem Server zwischen Remote Prozedur aufrufen verwaltet.

``` syntax
typedef [context_handle [ , type-attribute-list ] ] type-specifier declarator-list;

[context_handle [, function-attr-list ] ] type-specifier [ptr-decl] function-name(
    [ [parameter-attribute-list] ] type-specifier [declarator], ...);

[ [ function-attr-list ] ] type-specifier [ ptr-decl ] function-name(
    [context_handle [ , parameter-attribute-list ] ] type-specifier [declarator], ...);

[ void __RPC_USER context-handle-type_rundown (
  context-handle-type); ]
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Type-Attribute-List* 
</dt> <dd>

Gibt ein oder mehrere Attribute an, die auf den Typ angewendet werden.

</dd> <dt>

*Typspezifizierer* 
</dt> <dd>

Gibt einen Zeigertyp oder einen Typbezeichner an. Eine optionale Speicher Spezifikation kann dem *Typspezifizierer* vorangestellt werden.

</dd> <dt>

*Deklarator und Deklarator-List* 
</dt> <dd>

Gibt Standard-C-Deklaratoren an, z. b. Bezeichner, Zeiger Deklaratoren und Array Deklaratoren. Der Deklarator für ein Kontext Handle muss mindestens einen zeigerdeklarator enthalten. Weitere Informationen finden Sie unter [Array-und Sized-Pointer Attribute](array-and-sized-pointer-attributes.md), [**Arrays**](arrays-1.md)und [Arrays und Zeiger](/windows/desktop/Rpc/arrays-and-pointers). Die *declarator-List* besteht aus einem oder mehreren Deklaratoren, die durch Kommas getrennt sind. Der Parameter-Name-Bezeichner im funktionsdedeclarator ist optional.

</dd> <dt>

*Function-attr-List* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die für die Funktion gelten. Gültige Funktions Attribute sind **\[** [**Callback**](callback.md) **\]** , **\[** [**local**](local.md), **\]** das Zeiger Attribut **\[** [**ref**](ref.md) **\]** , **\[** [**Unique**](unique.md) **\]** oder **\[** [**ptr**](ptr.md) **\]** und die Zeichenfolge der Verwendungs Attribute **\[** [**Zeichenfolge**](string.md) **\]** , **\[** [**ignorieren**](ignore.md) **\]** und **\[ Kontext \_ handle \]**.

</dd> <dt>

*PTR-decl* 
</dt> <dd>

Gibt 0 (null) oder mehr Zeiger Deklaratoren an. Ein zeigerdeklarator ist derselbe wie der in C verwendete zeigerdeklarator. Sie wird aus dem Kenn **\*** Zeichner, den Modifizierern, z. b. **weit**, und dem Qualifizierer " [**Konstanten**](const.md)" erstellt.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Remote Prozedur an.

</dd> <dt>

*Parameter-Attribute-List* 
</dt> <dd>

Gibt 0 (null) oder mehr direktionale Attribute, Feld Attribute, Verwendungs Attribute und Zeiger Attribute an, die für den angegebenen Parametertyp geeignet sind. Trennen Sie mehrere Attribute durch Kommas.

</dd> <dt>

*Context-Handle-type* 
</dt> <dd>

Gibt den Bezeichner an, der den in einer [**typedef**](typedef.md) -Deklaration definierten Kontext Handle-Typ angibt, der das **\[ Kontext \_ handle \]** -Attribut annimmt. Die Rundown-Routine ist optional.

**Windows Server 2003 und Windows XP:** Eine einzelne Schnittstelle kann sowohl serialisierte als auch nicht serialisierte Kontext Handles aufnehmen, sodass eine Methode in einer Schnittstelle ausschließlich auf ein Kontext Handle (serialisiert) zugreifen kann, während andere Methoden auf dieses Kontext Handle im freigegebenen Modus zugreifen (nicht serialisiert). Diese Zugriffs Funktionen sind mit Lese-/schreibsperrungs-Mechanismen vergleichbar. Methoden, die ein serialisiertes Kontext Handle verwenden, sind exklusive Benutzer (Writer), während Methoden, die ein nicht serialisiertes Kontext Handle verwenden, freigegebene Benutzer (Reader) sind. Methoden, die den Zustand eines Kontext Handles zerstören oder ändern, müssen serialisiert werden. Methoden, die den Zustand eines Kontext Handles nicht ändern, wie z. b. die Methoden, die einfach aus einem Kontext Handle lesen, können nicht serialisiert werden. Beachten Sie, dass Erstellungs Methoden implizit serialisiert werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **\[ Kontext \_ handle \]** -Attribut kann als Attribut vom Typ "IDL [**typedef**](typedef.md) ", als Funktions Rückgabetyp Attribut oder als Parameter Attribut angezeigt werden. Wenn Sie das **\[ Kontext \_ handle \]** -Attribut auf eine Typdefinition anwenden, müssen Sie auch eine Kontext-Rundown-Routine bereitstellen. Ausführliche Informationen finden Sie in der ausführungsausführungsroutine des [Server Kontexts](/windows/desktop/Rpc/server-context-run-down-routine)

Wenn Sie den Mittelwert Compiler im Standardmodus ([**/MS \_ ext**](-ms-ext.md)) verwenden, kann es sich bei einem Kontext Handle um jeden vom Benutzer ausgewählten Zeigertyp handeln, sofern er die Anforderungen für die hier beschriebenen Kontext Handles erfüllt. Die Daten, die einem solchen Kontext behandlertyp zugeordnet sind, werden nicht im Netzwerk übertragen und sollten nur von der Serveranwendung bearbeitet werden. DCE-IDL-Compiler beschränken Kontext Handles auf Zeiger vom Typ " [**void**](void.md) " **\*** . Diese Funktion ist daher nicht verfügbar, wenn Sie den [**/OSF**](-osf.md) -Schalter für den Mittelwert Compiler verwenden.

Wie bei anderen handle-Typen ist das Kontext Handle für die Client Anwendung nicht transparent, und alle damit verknüpften Daten werden nicht übertragen. Auf dem Server dient das Kontext Handle als Handle für den aktiven Kontext, und auf alle Daten, die dem Kontext behandlertyp zugeordnet sind, kann zugegriffen werden.

Zum Erstellen eines Kontext Handles übergibt der Client an den Server einen **\[** [**out**](out-idl.md)- **\]** , **\[** [**ref**](ref.md) - **\]** Zeiger auf ein Kontext handle. (Das Kontext Handle selbst kann einen **null** -Wert oder einen nicht-**null** -Wert haben – solange sein Wert mit seinen Zeiger Attributen konsistent ist. Wenn z. b. auf den Kontext behandlertyp das **\[** [**ref**](ref.md) - **\]** Attribut angewendet wird, kann er keinen **null** -Wert aufweisen.) Ein weiteres Bindungs Handle muss bereitgestellt werden, um die Bindung zu erreichen, bis das Kontext Handle erstellt wird. Wenn kein explizites handle angegeben ist, wird eine implizite Bindung verwendet. Wenn kein **\[** [**implizites \_ handle**](implicit-handle.md) - **\]** Attribut vorhanden ist, wird ein automatisches Handle verwendet.

Mit der Remote Prozedur auf dem Server wird ein aktives Kontext Handle erstellt. Der Client muss dieses Kontext Handle als in- **\[** [](in.md) **\]** oder **\[ in**- **out \]** -Parameter in nachfolgenden Aufrufen verwenden. Ein **\[ in \]**-only-Kontext Handle kann als Bindungs Handle verwendet werden, daher muss es einen Wert aufweisen, der nicht **null** ist. Ein **\[ in \]**-only-Kontext Handle reflektiert keine Zustandsänderungen auf dem Server.

Auf dem Server kann die aufgerufene Prozedur das Kontext Handle nach Bedarf interpretieren. Beispielsweise kann die aufgerufene Prozedur Heap Speicher zuordnen und das Kontext Handle als Zeiger auf diesen Speicher verwenden.

Zum Schließen eines Kontext Handles übergibt der Client das Kontext Handle als in- **\[** [](in.md) **\]** , **\[** [**out**](out-idl.md) - **\]** Argument. Der Server muss ein **null** -Kontext Handle zurückgeben, wenn er nicht mehr den Kontext im Auftrag des Aufrufers beibehält. Wenn das Kontext Handle z. b. eine geöffnete Datei darstellt und der-Befehl die Datei schließt, muss der Server das Kontext Handle auf **null** festlegen und an den Client zurückgeben. Ein **null** -Wert ist als Bindungs Handle bei nachfolgenden Aufrufen ungültig.

Ein Kontext Handle ist nur für einen Server gültig. Wenn eine Funktion über zwei handle-Parameter verfügt und das Kontext Handle nicht **null** ist, müssen die Bindungs Handles auf denselben Adressraum verweisen.

Wenn eine Funktion über ein **\[** [**in**](in.md) - **\]** oder ein **\[ in**-, **out \]** -Kontext Handle verfügt, kann Ihr Kontext Handle als Bindungs Handle verwendet werden. In diesem Fall wird die implizite Bindung nicht verwendet, und das **\[** [**implizite \_ handle**](implicit-handle.md) - **\]** oder **\[** [**Auto \_ handle**](auto-handle.md) - **\]** Attribut wird ignoriert.

Für Kontext Handles gelten die folgenden Einschränkungen:

-   Kontext Handles können keine Array Elemente, Strukturmember oder Union-Member sein. Sie können nur Parameter sein.
-   Kontext Handles können nicht über die über **\[** [**Tragung \_ als**](transmit-as.md) **\]** oder das **\[** [**\_ As**](represent-as.md) - **\]** Attribut verfügen.
-   Parameter, die Zeiger auf **\[** [**out**](out-idl.md) - **\]** Kontext Handles sind, müssen **\[** [**ref**](ref.md) - **\]** Zeiger sein.
-   Ein **\[** [**im**](in.md) **\]** Kontext Handle kann als Bindungs Handle verwendet werden und darf nicht **null** sein.
-   Ein **\[ in**-, [**out**](out-idl.md) -Kontext Handle kann bei Eingabe **null** sein, aber nur, wenn die Prozedur einen anderen expliziten handle-Parameter aufweist. Wenn keine anderen expliziten nicht-**null** -Kontext handle-Parameter vorhanden sind, darf der **\[ in**-, **out \]** -Kontext Handle nicht **null** sein.
-   Ein Kontext Handle kann nicht für Rückrufe verwendet werden.

## <a name="examples"></a>Beispiele

``` syntax
typedef [context_handle] void * PCONTEXT_HANDLE_TYPE; 
short RemoteFunc1([out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
short RemoteFunc2([in, out] PCONTEXT_HANDLE_TYPE * pCxHandle); 
void __RPC_USER PCONTEXT_HANDLE_TYPE_rundown (PCONTEXT_HANDLE_TYPE);
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Mikro**](arrays-1.md)
</dt> <dt>

[**Automatisches \_ handle**](auto-handle.md)
</dt> <dt>

[**Rückruf**](callback.md)
</dt> <dt>

[Client Kontext Zurücksetzung](/windows/desktop/Rpc/client-context-reset)
</dt> <dt>

[**const**](const.md)
</dt> <dt>

[Kontext Handles](/windows/desktop/Rpc/context-handles)
</dt> <dt>

[**bewältigen**](handle.md)
</dt> <dt>

[Bindung und Handles](/windows/desktop/Rpc/binding-and-handles)
</dt> <dt>

[**lassen**](ignore.md)
</dt> <dt>

[**implizites \_ handle**](implicit-handle.md)
</dt> <dt>

[**in**](in.md)
</dt> <dt>

[**nah**](local.md)
</dt> <dt>

[Multithread-Clients und Kontext Handles](/windows/desktop/Rpc/multithreaded-clients-and-context-handles)
</dt> <dt>

[**/MS \_ ext**](-ms-ext.md)
</dt> <dt>

[**vorgenommen**](out-idl.md)
</dt> <dt>

[**ptr**](ptr.md)
</dt> <dt>

[**ref**](ref.md)
</dt> <dt>

[**Darstellung \_ als**](represent-as.md)
</dt> <dt>

[**Rpcssdestroyclientcontext**](/windows/desktop/api/rpcndr/nf-rpcndr-rpcssdestroyclientcontext)
</dt> <dt>

[Server Kontext-Lauf-ab-Routine](/windows/desktop/Rpc/server-context-run-down-routine)
</dt> <dt>

[**Zeichenfolge**](string.md)
</dt> <dt>

[**übertragen \_ als**](transmit-as.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**gem**](unique.md)
</dt> <dt>

[**void**](void.md)
</dt> </dl>

 

 