---
title: /backward_compat Schalter
description: Der/Backward \_ Kompatibilitäts-Schalter leitet den Mittel l-Compiler zum Deaktivieren einiger erweiterter Features bei der Erstellung von RPC-/com-stubvorzügen.
ms.assetid: eec0ade7-30a0-44e4-92e9-fb03ff657723
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69b558d01b33b99f7d1d9279f729b923ff58df0f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342043"
---
# <a name="backward_compat-switch"></a>/Backward \_ Kompatibilitäts-Schalter

Der/Backward \_ Kompatibilitäts-Schalter leitet den Mittel l-Compiler zum Deaktivieren einiger erweiterter Features bei der Erstellung von RPC-/com-stubvorzügen.

``` syntax
midl /backward_compat { maybenull_sizeis | zeroout_alignmentgap | 
     BSTR_byvalue_escaping | string_defaultvalue | signed_wchar_t }
```

## <a name="switch-options"></a>Optionen wechseln

*maybenull \_ sizeis*<dl> Wendet das Attribut " [ \[ \_ Konsistenz \_ Prüfung \] Deaktivieren](disable-consistence-check.md) " auf eine gesamte Mittell-Kompilierung an.  
</dl>

*NULL ( \_ alignmentgap)*<dl> Deaktiviert das nulren von Lücken im gemarshallten Puffer.  
</dl>

*BSTR byvalue-Escapezeichen \_ \_*<dl> Weist den Mittel l-Compiler an, Escapesequenzen zu berücksichtigen, z \\ . b.-™ oder- \\ ™ in bstrins.  
</dl>

*String \_ DefaultValue*<dl> Erzwingt, dass der mittlerer l-Compiler Zeichen folgen in [**\[ DefaultValue \]**](defaultvalue.md) -Attributen in Variant umwandelt. VT \_ I4 geben Sie ein, bevor Sie den Wert in den richtigen Typ umwandeln.  
</dl>

*signiertes \_ WCHAR \_ t*<dl> Leitet die Mittell so um, dass der WCHAR \_ t-Typ für die Kompatibilität mit Visual Basic als signiert behandelt wird.  
</dl>

## <a name="remarks"></a>Bemerkungen

-   *maybenull \_ sizeis*: siehe \[ Deaktivieren der \_ Konsistenz \_ Prüfung \] .
-   *Nullen von \_ alignmentgap*: Wenn IDLs mit "target nt60" oder höher kompiliert werden, erstellt die Mittel-l stubwerte, die alle Ausrichtungs Lücken zwischen Membern oder einer Struktur im Wire-Puffer Nullen. Der Befehls Zeilenschalter */Backward \_ Kompatibilitäts ZeroOut \_ alignmentgap* leitet "Mittel l" ein, um diese Funktion zu deaktivieren.

    In der folgenden Beispiel Struktur enthält der Wire-Puffer eine Ausrichtungs Lücke von 7 Byte, um den Hyper-Member nach dem char-Member auf 8 auszurichten. Bei Verwendung von "target nt60" oder höher wird diese Lücke von mittlerer l außer 0 gesetzt, es sei denn, es wird der Schalter verwendet.

    IDL-Datei:

    ``` syntax
    typedef struct _structwithgaps{
        char c;
        // 7 byte gap to align the following hyper to 8 
        hyper h;
    } structwithgap;
    ```

    Dieser Switch kann eine geringfügige Leistungsverbesserung mit potenziell erheblichen Erhöhung der Offenlegung von Risiken bereitstellen.

-   *BSTR- \_ byvalue \_*-Escapezeichen: der Interl-Compiler verarbeitet standardmäßig keine Escapesequenzen, wie™ z. b., d \\ \\ . b.™ in Zeichen folgen Konstanten für die OLE-Automatisierung, wenn eine Zeichen folgen Konstante in die Typen VT \_ LPSTR oder VT \_ LPWSTR geändert wird. Mit dieser Option für die Abwärtskompatibilität werden die Escapesequenzen ausgewertet.
-   *String \_ DefaultValue*: erzwingt, dass der mittlerer l-Compiler numerische Zeichen folgen in [**\[ DefaultValue \]**](defaultvalue.md) -Attributen in Variant umwandelt. VT \_ I4 geben Sie ein, bevor Sie den Wert in den richtigen Typ umwandeln. Dies kann in einigen Fällen zu einem Genauigkeits Verlust führen, daher wird diese Switch-Option nicht empfohlen.
-   *signiertes \_ WCHAR \_ t*: leitet die mittlere Zahl so um, dass der WCHAR \_ t-Typ für die Kompatibilität mit Visual Basic als signiert behandelt wird.

 

 




