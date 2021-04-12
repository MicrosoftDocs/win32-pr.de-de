---
title: NoCode-Attribut
description: Das Attribut \ NoCode \ wird in ACF-Headern oder mit einzelnen Funktionen verwendet, um die Generierung von Client-Stub-Code zu verhindern.
ms.assetid: d3b6e4c8-103c-4ea2-8748-11d844fdda97
keywords:
- NoCode-Attribut (Mittelwert)
topic_type:
- apiref
api_name:
- nocode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64f5138dc1794e9b2714e5f64762c1af17b47fb2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312210"
---
# <a name="nocode-attribute"></a>NoCode-Attribut

Das **\[ NoCode \]** -Attribut wird in ACF-Headern oder mit einzelnen Funktionen verwendet, um die Generierung von Client-Stub-Code zu verhindern.

``` syntax
[ 
    nocode 
    [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typename; ] 
  [ [ nocode [ , ACF-function-attributes ] ] function-name (
        [ ACF-parameter-attributes ] parameter-name ;
        ...);
  ]
    ...
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*ACF-Interface-Attribute* 
</dt> <dd>

Gibt eine Liste mit einem oder mehreren Attributen an, die auf die gesamte Schnittstelle angewendet werden. Gültige Attribute sind entweder **\[** [**Automatisches \_ handle**](auto-handle.md) **\]** oder **\[** [**implizites \_ handle**](implicit-handle.md) **\]** und entweder **\[** [**Code**](code.md) **\]** oder **\[ NoCode \]**. Wenn zwei oder mehr Schnittstellen Attribute vorhanden sind, müssen diese durch Kommas getrennt werden.

</dd> <dt>

*Schnittstellen Name* 
</dt> <dd>

Gibt den Namen der Schnittstelle an. Im DCE-Kompatibilitätsmodus muss der Schnittstellen Name mit dem Namen der Schnittstelle, die in der IDL-Datei angegeben ist, identisch sein. Wenn Sie den-Compilerschalter [**/ACF**](-acf.md)verwenden, können sich der Schnittstellen Name in der ACF und der Schnittstellen Name in der IDL-Datei unterscheiden.

</dd> <dt>

*Dateiname-List* 
</dt> <dd>

Gibt eine durch Kommas getrennte Liste mit einem oder mehreren C-sprach Header Dateinamen an. Der vollständige Dateiname, einschließlich der Erweiterung, muss angegeben werden.

</dd> <dt>

*Type-Attribute-List* 
</dt> <dd>

Gibt eine Liste mit einem oder mehreren Attributen, die durch Kommas getrennt sind, an, die auf den angegebenen Typ angewendet werden. Gültige Typattribute sind " **\[** [**zuordnen**](allocate.md)" **\]** .

</dd> <dt>

*typeName* 
</dt> <dd>

Gibt einen Typ an, der in der IDL-Datei definiert ist. Typattribute in der ACF können nur auf Typen angewendet werden, die zuvor in der IDL-Datei definiert wurden.

</dd> <dt>

*ACF-Function-Attribute* 
</dt> <dd>

Gibt Attribute an, die auf die Funktion als Ganzes angewendet werden, z. b. den **\[** [**comm- \_ Status**](comm-status.md) **\]** . Funktions Attribute werden in eckige Klammern eingeschlossen. Trennen Sie mehrere Funktions Attribute durch Kommas.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Funktion an, wie in der IDL-Datei definiert.

</dd> <dt>

*ACF-Parameter-Attribute* 
</dt> <dd>

Gibt ACF-Attribute an, die auf einen Parameter angewendet werden. Beachten Sie, dass NULL oder mehr Attribute auf den Parameter angewendet werden können. Trennen Sie mehrere Parameter Attribute durch Kommas. ACF-Parameter Attribute werden in eckige Klammern eingeschlossen.

</dd> <dt>

*Parameter Name* 
</dt> <dd>

Gibt einen Parameter der Funktion an, wie in der IDL-Datei definiert. Jeder Parameter für die Funktion muss in derselben Reihenfolge angegeben werden und denselben Namen verwenden, der in der IDL-Datei definiert ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **\[ NoCode \]** -Attribut kann im ACF-Header oder auf eine einzelne Funktion angewendet werden.

Wenn das **\[ NoCode \]** -Attribut im ACF-Header angezeigt wird, wird der Client-Stub-Code für keine Remote Funktion generiert, es sei denn, er verfügt über das **\[** [**Code**](code.md) **\]** Funktions Attribut. Sie können das **\[ NoCode \]** -Attribut im-Header für eine einzelne Funktion überschreiben, indem Sie das **\[ Code \]** -Attribut als Funktions Attribut angeben.

Wenn das **\[ NoCode \]** -Attribut in der Attribut Liste der Funktion angezeigt wird, wird kein Client-Stub-Code für die Funktion generiert.

Client-Stub-Code wird nicht generiert, wenn:

-   Der ACF-Header enthält das **\[ NoCode \]** -Attribut.
-   Das **\[ NoCode \]** -Attribut wird auf die-Funktion angewendet.
-   Das **\[** [**lokale**](local.md) **\]** Attribut gilt für die Funktion in der Schnittstellen Datei.

Entweder **\[** [](code.md) **\]** kann Code oder **\[ NoCode \]** in der Attribut Liste einer Funktion angezeigt werden, und der von Ihnen gewählte Wert kann genau einmal angezeigt werden.

Das **\[ NoCode \]** -Attribut wird ignoriert, wenn serverstubobjekte generiert werden. Sie können Sie nicht anwenden, wenn Sie serverstubdaten im DCE-Kompatibilitätsmodus erstellen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[**Automatisches \_ handle**](auto-handle.md)
</dt> <dt>

[**Ordnung**](code.md)
</dt> <dt>

[**Kommunikations \_ Status**](comm-status.md)
</dt> <dt>

[**implizites \_ handle**](implicit-handle.md)
</dt> </dl>

 

 




