---
title: error_status_t-Attribut
description: Das \_ t-Schlüsselwort für den Fehlerstatus \_ legt einen Typ für ein Objekt fest, das Kommunikationsstatus- oder Fehlerstatusinformationen enthält.
ms.assetid: 7eff0d20-c058-4f16-a3db-0b4c82303135
keywords:
- error_status_t-Attribut MIDL
topic_type:
- apiref
api_name:
- error_status_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02e404992e8fca98eba41f5ea85571160582827816a945d7ab8db505b28ba0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119067270"
---
# <a name="error_status_t-attribute"></a>Error \_ Status t attribute \_ (Fehlerstatus-t-Attribut)

Das t-Schlüsselwort für **den \_ Fehlerstatus \_** legt einen Typ für ein Objekt fest, das Kommunikationsstatus- oder Fehlerstatusinformationen enthält.

``` syntax
[ [ , ACF-function-attributes ] ] error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] error_status_t parameter-name
    , ...);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*ACF-funktionsattribute* 
</dt> <dd>

Gibt 0 (null) oder mehr ACF-Funktionsattribute an, z. B. **\[** [**\_ comm-Status,**](comm-status.md) **\]** **\[** [**\_ Fehlerstatus**](fault-status.md) **\]** oder **\[** [**Nocode.**](nocode.md) **\]** Funktionsattribute werden in eckige Klammern eingeschlossen. Null oder mehr Attribute können auf eine Funktion angewendet werden. Trennen Sie mehrere Funktionsattribute durch Kommas.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Funktion an, wie in der IDL-Datei definiert.

</dd> <dt>

*ACF-parameter-attributes* 
</dt> <dd>

Gibt Attribute an, die auf einen Parameter angewendet werden. Beachten Sie, dass null, ein oder mehrere Attribute auf den Parameter angewendet werden können. Trennen Sie mehrere Parameterattribute durch Kommas. Parameterattribute werden in eckige Klammern eingeschlossen. IDL-Parameterattribute, z. B. richtungsale Attribute, sind in ACF nicht zulässig.

</dd> <dt>

*Parametername* 
</dt> <dd>

Gibt den Parameter für die Funktion an, wie in der IDL-Datei definiert. Jeder Parameter für die Funktion muss in derselben Sequenz angegeben werden, wobei der gleiche Name wie in der IDL-Datei definiert wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der **\_ Fehlerstatus \_ t-Typ** wird als Teil der Ausnahmebehandlungsarchitektur in IDL verwendet. Dieser Typ wird einem [**nicht signierten**](unsigned.md) [**langen**](long.md)zugeordnet. Anwendungen, die Fehlersituationen abfangen, verfügen über einen **\[** [**out-Parameter**](out-idl.md) **\]** oder einen Rückgabetyp einer Prozedur, die als **\_ Fehlerstatus \_ t** angegeben ist, und qualifizieren den **\_ Fehlerstatus \_ t** mit dem **\[** [**Comm-Status \_**](comm-status.md) oder den **\]** **\[** [**\_ Fehlerstatusattributen**](fault-status.md) **\]** in der ACF. Wenn der Parameter oder Rückgabetyp nicht mit den Attributen **\[ comm \_ status \]** oder **\[ fault \_ status \]** qualifiziert wurde, funktioniert der Parameter so, als wäre er ein long-Attribut ohne Vorzeichen.

Ab Version 2.0 generiert der MIDL-Compiler Stubs, die die richtige Fehlerbehandlungsarchitektur enthalten. Frühere Versionen des MIDL-Compilers behandelten jedoch einen Parameter oder Rückgabetyp des **\_ Fehlerstatus \_ t** so, als ob die Attribute **\[** [**comm \_ status**](comm-status.md) **\]** und fault **\[** [**\_ status**](fault-status.md) **\]** angewendet wurden, auch wenn sie dies nicht waren. Mit MIDL 2.0 oder höher müssen Sie die Attribute **\[ comm \_ status \]** und **\[ fault \_ status \]** explizit auf den Parameter oder die Prozedur im ACF anwenden.

Der **\_ Fehlerstatus \_ t** type ist einer der vordefinierten Typen der Schnittstellendefinitionssprache. Vordefinierte Typen können als Typspezifizierer in typedef-Deklarationen, in allgemeinen Deklarationen und in Funktionsdeklaratoren (entweder als Funktionsrückgabetyp oder als Parametertypspezifizierer) angezeigt werden. [](typedef.md)

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_comm-Status**](comm-status.md)
</dt> <dt>

[**\_Fehlerstatus**](fault-status.md)
</dt> <dt>

[IDL-Datei (Interface Definition)](interface-definition-idl-file.md)
</dt> <dt>

[**long**](long.md)
</dt> <dt>

[**out**](out-idl.md)
</dt> <dt>

[**Typedef**](typedef.md)
</dt> <dt>

[**Unsigned**](unsigned.md)
</dt> </dl>

 

 




