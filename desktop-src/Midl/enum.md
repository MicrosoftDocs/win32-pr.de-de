---
title: Aufzählungs Attribut
description: Die Schlüsselwort-Enumeration identifiziert einen enumerierten Typ.
ms.assetid: 1aaa3c36-17f7-42ff-8f4c-66133fcf4a1a
keywords:
- Aufzählungs Attribut-Mittell
topic_type:
- apiref
api_name:
- enum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 681244c9d852c25d8e63ad389b03f16e6db8148c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312221"
---
# <a name="enum-attribute"></a>Aufzählungs Attribut

Die Schlüssel **Wort** -Enumeration identifiziert einen enumerierten Typ.

``` syntax
enum [tag ] 
{ 
    identifier [=integer-value ] 
    [ , ... ] 
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*Tag* 
</dt> <dd>

Gibt ein optionales Tag für den enumerierten Typ an.

</dd> <dt>

*identifier* 
</dt> <dd>

Gibt die jeweilige Enumeration an.

</dd> <dt>

*ganzzahliger Wert* 
</dt> <dd>

Gibt einen Konstanten ganzzahligen Wert an.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

 Enumerationstypen können als Typspezifizierer in [**typedef**](typedef.md) -Deklarationen, allgemeinen Deklarationen und Funktions Deklaratoren (entweder als Funktions Rückgabetyp oder als Parametertyp Spezifizierer) angezeigt werden. Informationen zu dem Kontext, in dem typspezifier angezeigt wird, finden Sie unter [Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md).

Im Standardmodus des compl-Compilers können Enumeratoren ganzzahlige Werte zugewiesen werden. (Diese Funktion ist nicht verfügbar, wenn Sie mit dem [**/OSF**](-osf.md) -Schalter kompilieren.) Wie bei C-Language-Enumeratoren müssen Enumeratornamen eindeutig sein, aber die Enumeratorwerte müssen nicht gleich sein.

Wenn Zuweisungs Operatoren nicht bereitgestellt werden, werden Bezeichner von links nach rechts aufeinander folgende ganzzahlige Werte zugeordnet, beginnend mit 0 (null). Wenn Zuweisungs Operatoren bereitgestellt werden, beginnen zugewiesene Werte mit dem zuletzt zugewiesenen Wert.

Die maximale Anzahl von Bezeichner beträgt 65.535.

Objekte vom Typ " **Enumeration** " sind [**int**](int.md) -Typen, und ihre Größe ist System abhängig. Standardmäßig werden Objekte von Enumerationstypen als 16-Bit- **Objekte vom Typ** [**Ganzzahl ohne Vorzeichen**](unsigned.md) [**Short**](short.md) behandelt, wenn Sie über ein Netzwerk übertragen werden. Werte außerhalb des Bereichs 0 bis 32.767 bewirken, dass der RPC X-Enumerationswert für die Lauf Zeit Ausnahme außerhalb \_ \_ des gültigen Bereichs liegt \_ \_ \_ \_ . Um Objekte als 32-Bit-Entitäten zu übertragen, wenden Sie das **\[** [**v1- \_ Enumeration**](v1-enum.md) - **\]** Attribut auf die **Enumeration** -typedef an.

## <a name="examples"></a>Beispiele

``` syntax
typedef enum {Monday=2, Tuesday, Wednesday, Thursday, Friday} workdays; 
 
typedef enum {Clemens=21, Palmer=22, Ryan=34} pitchers;
```

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**INT**](int.md)
</dt> <dt>

[**short**](short.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**Ganzzahl ohne Vorzeichen**](unsigned.md)
</dt> <dt>

[**v1-Aufzählung \_**](v1-enum.md)
</dt> </dl>

 

 




