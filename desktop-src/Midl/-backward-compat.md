---
title: /backward_compat Switch
description: Der \_ /backward-Kompatibilitätsschalter weist den MIDL-Compiler an, einige erweiterte Features beim Generieren von RPC/COM-Stubs zu deaktivieren.
ms.assetid: eec0ade7-30a0-44e4-92e9-fb03ff657723
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd412bdabe4255a9a4538503b29ddf5681265ce5e16c81d3d5fc2484eb6c9675
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086390"
---
# <a name="backward_compat-switch"></a>\_/backward compat Switch

Der \_ /backward-Kompatibilitätsschalter weist den MIDL-Compiler an, einige erweiterte Features beim Generieren von RPC/COM-Stubs zu deaktivieren.

``` syntax
midl /backward_compat { maybenull_sizeis | zeroout_alignmentgap | 
     BSTR_byvalue_escaping | string_defaultvalue | signed_wchar_t }
```

## <a name="switch-options"></a>Optionen wechseln

*maybenull \_ sizeis*<dl> Wendet das [ \[ Disable \_ Consistency \_ Check-Attribut \] ](disable-consistence-check.md) auf eine gesamte MIDL-Kompilierung an.  
</dl>

*\_Zeroout-Ausrichtungslücke*<dl> Deaktiviert das Aufstellen von Lücken im gemarshallten Puffer.  
</dl>

*\_ \_ BSTR-Byvalue-Kapselung*<dl> Weist den MIDL-Compiler an, Escapesequenzen wie â€ \\ nâ€™ oder â€ â \\ tâ€™ in BSTRs zu achten.  
</dl>

*string \_ defaultvalue*<dl> Erzwingt, dass der MIDL-Compiler Zeichenfolgen in [**\[ \] defaultvalue-Attributen**](defaultvalue.md) in VARIANT einreiht. VT \_ I4-Typ, bevor der Wert in den richtigen Typ umgewandelt wird.  
</dl>

*\_signed wchar \_ t*<dl> Weist MIDL an, den wchar t-Typ aus Gründen der Kompatibilität mit Visual Basic als signiert zu \_ behandeln.  
</dl>

## <a name="remarks"></a>Hinweise

-   *maybenull \_ sizeis:* Siehe \[ Deaktivieren der \_ \_ \] Konsistenzprüfung.
-   *zeroout \_ alignmentgap*: Wenn IDLs mit â€"target NT60 oder höher kompiliert werden, erstellt MIDL Stubs, die keine Ausrichtungslücken zwischen Membern oder einer Struktur im Kabelpuffer ausschließen. Der Befehlszeilenschalter */backward \_ compat zeroout \_ alignmentgap* weist MIDL an, dieses Feature zu deaktivieren.

    In der folgenden Beispielstruktur enthält der Kabelpuffer eine Ausrichtungslücke von 7 Byte, um den Hypermember nach dem char-Member auf 8 auszurichten. Mit dem Ziel NT60 oder höher schließt MIDL diese Lücke auf null, es sei denn, der Schalter wird verwendet.

    IDL-Datei:

    ``` syntax
    typedef struct _structwithgaps{
        char c;
        // 7 byte gap to align the following hyper to 8 
        hyper h;
    } structwithgap;
    ```

    Dieser Wechsel kann zu einer geringfügigen Leistungsverbesserung mit potenziell erheblich erhöhten Offenlegungsrisiken führen.

-   *BSTR \_ \_ byvalue-Escapezeichen:* Standardmäßig verarbeitet der MIDL-Compiler keine Escapesequenzen wie â€ \\ nâ €™ oder â€ â \\ €™ in Zeichenfolgenkonstanten für OLE Automation, wenn eine Zeichenfolgenkonstante in die Typen VT \_ LPSTR oder VT \_ LPWSTR konvertiert wird. Mit dieser Option für die Abwärtskompatibilität werden die Escapesequenzen ausgewertet.
-   *string \_ defaultvalue: Erzwingt,* dass der MIDL-Compiler numerische Zeichenfolgen in [**\[ \] defaultvalue-Attributen**](defaultvalue.md) in VARIANT umgewandelt. VT \_ I4-Typ, bevor der Wert in den richtigen Typ umgewandelt wird. Dies kann in einigen Fällen zu einem Genauigkeitsverlust führen, daher wird diese Option nicht empfohlen.
-   *signed \_ wchar \_ t:* Weist MIDL an, den wchar t-Typ aus Gründen der Kompatibilität mit Visual Basic als signiert zu \_ behandeln.

 

 




