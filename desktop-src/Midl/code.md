---
title: Code-Attribut
description: Das Attribut \ Code \ ACF bewirkt, dass Client-Stub-Code für Remote Funktionen generiert wird.
ms.assetid: 735a8c25-29d4-4073-a2db-88bc8615ccc1
keywords:
- Code Attribute-Mittell
topic_type:
- apiref
api_name:
- code
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa041859c0bffca2771695b7055105b8ae846221
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104313031"
---
# <a name="code-attribute"></a>Code-Attribut

Das ACF- **\[ Code \]** Attribut bewirkt, dass Client-Stub-Code für Remote Funktionen generiert wird.

``` syntax
[
    code [ , ACF-interface-attributes ] 
] 
interface interface-name
{
  [ include filename-list ; ]
  [ typedef [type-attribute-list] typenam; ]
  [ [code [ , ACF-function-attributes ]] function-name (
            [ ACF-parameter-attributes ] parameter-name,
        ...);
  ]
    ...
}
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*ACF-Interface-Attribute* 
</dt> <dd>

Gibt eine Liste mit einem oder mehreren Attributen an, die auf die gesamte Schnittstelle angewendet werden. Gültige Attribute sind entweder [**\[ Automatisches \_ handle \]**](auto-handle.md) oder [**\[ implizites \_ handle \]**](implicit-handle.md) und entweder **\[ \] Code**, [**\[ NoCode \]**](nocode.md)oder [**\[ optimieren \]**](optimize.md). Wenn zwei oder mehr Schnittstellen Attribute vorhanden sind, müssen diese durch Kommas getrennt werden.

</dd> <dt>

*Schnittstellen Name* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> <dt>

*Dateiname-List* 
</dt> <dd>

Gibt eine Liste mit einem oder mehreren C-Header Dateinamen an, getrennt durch Kommas. Sie müssen den vollständigen Dateinamen angeben, einschließlich der Erweiterung.

</dd> <dt>

*Type-Attribute-List* 
</dt> <dd>

Gibt eine Liste mit einem oder mehreren Attributen, die durch Kommas getrennt sind, an, die auf den angegebenen Typ angewendet werden. Gültige Typattribute sind " [**\[ \] zuordnen**](allocate.md) " und " [**\[ darstellen \_ als \]**](represent-as.md)".

</dd> <dt>

*typeName* 
</dt> <dd>

Gibt einen Typ an, der in der IDL-Datei definiert ist. Typattribute in der ACF können nur auf Typen angewendet werden, die zuvor in der IDL-Datei definiert wurden.

</dd> <dt>

*ACF-Function-Attribute* 
</dt> <dd>

Gibt 0 (null) oder mehr Attribute an, die für die Funktion als Ganzes gelten, z. b. den [**\[ comm- \_ Status \]**](comm-status.md). Funktions Attribute werden in eckige Klammern eingeschlossen. Trennen Sie mehrere Funktions Attribute durch Kommas.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Funktion an, wie in der IDL-Datei definiert.

</dd> <dt>

*ACF-Parameter-Attribute* 
</dt> <dd>

Gibt ACF-Attribute an, die auf einen Parameter angewendet werden. Beachten Sie, dass 0 (null), ein oder mehrere Attribute auf den Parameter angewendet werden können. Trennen Sie mehrere Parameter Attribute durch Kommas. ACF-Parameter Attribute werden in eckige Klammern eingeschlossen.

</dd> <dt>

*Parameter Name* 
</dt> <dd>

Gibt einen Parameter der Funktion an, wie in der IDL-Datei definiert. Jeder Parameter für die Funktion muss in derselben Reihenfolge und mit dem gleichen Namen wie in der IDL-Datei angegeben werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **\[ Code \]** -Attribut kann im ACF-Header oder auf eine einzelne Funktion angewendet werden.

Wenn das **\[ Code \]** -Attribut im ACF-Header angezeigt wird, wird Client-Stub-Code für alle Remote Funktionen generiert, die nicht über das [**\[ NoCode \]**](nocode.md) -Funktions Attribut verfügen. Sie können das **\[ Code \]** -Attribut im-Header für eine einzelne Funktion überschreiben, indem Sie das **\[ NoCode \]** -Attribut als Funktions Attribut angeben.

Wenn das **\[ Code \]** -Attribut in der Attribut Liste der Remote Funktion angezeigt wird, wird der Client-Stub-Code für die Funktion generiert. Client-Stub-Code wird nicht generiert, wenn:

-   Der ACF-Header enthält das [**\[ NoCode \]**](nocode.md) -Attribut.
-   Das [**\[ NoCode \]**](nocode.md) -Attribut wird auf die-Funktion angewendet.
-   Das [**\[ lokale \]**](local.md) Attribut gilt für die Funktion in der Schnittstellen Datei.

Entweder kann **\[ Code \]** oder [**\[ NoCode \]**](nocode.md) in der Liste der Schnittstellen-oder Funktions Attribute angezeigt werden, aber der von Ihnen gewählte kann nur ein Mal in der Liste angezeigt werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[**Automatisches \_ handle**](auto-handle.md)
</dt> <dt>

[**Kommunikations \_ Status**](comm-status.md)
</dt> <dt>

[**implizites \_ handle**](implicit-handle.md)
</dt> <dt>

[**nah**](local.md)
</dt> <dt>

[**NoCode**](nocode.md)
</dt> <dt>

[**optimiert**](optimize.md)
</dt> <dt>

[**Darstellung \_ als**](represent-as.md)
</dt> </dl>

 

 




