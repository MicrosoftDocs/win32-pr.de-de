---
title: nocode-Attribut
description: Das \nocode\-Attribut wird in ACF-Headern oder mit einzelnen Funktionen verwendet, um die Generierung von Clientstubcode zu verhindern.
ms.assetid: d3b6e4c8-103c-4ea2-8748-11d844fdda97
keywords:
- nocode-Attribut MIDL
topic_type:
- apiref
api_name:
- nocode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86ec4612bc1bd5db1a8cdcbecdced51911591cdf5c482c83381f86deafd66a9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066960"
---
# <a name="nocode-attribute"></a>nocode-Attribut

Das **\[ Nocode-Attribut \]** wird in ACF-Headern oder mit einzelnen Funktionen verwendet, um die Generierung von Clientstubcode zu verhindern.

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

*ACF-Schnittstellenattribute* 
</dt> <dd>

Gibt eine Liste mit einem oder mehreren Attributen an, die für die gesamte Schnittstelle gelten. Gültige Attribute sind entweder **\[** [**\_ automatisches Handle**](auto-handle.md) **\]** oder **\[** [**implizites \_ Handle**](implicit-handle.md) **\]** und entweder **\[** [**Code**](code.md) **\]** oder **\[ Nocode. \]** Wenn zwei oder mehr Schnittstellenattribute vorhanden sind, müssen sie durch Kommas getrennt werden.

</dd> <dt>

*Schnittstellenname* 
</dt> <dd>

Gibt den Namen der Schnittstelle an. Im DCE-Kompatibilitätsmodus muss der Schnittstellenname mit dem Namen der Schnittstelle übereinstimmen, die in der IDL-Datei angegeben ist. Wenn Sie den MIDL-Compilerschalter [**/acf**](-acf.md)verwenden, können sich der Schnittstellenname im ACF und der Schnittstellenname in der IDL-Datei unterscheiden.

</dd> <dt>

*filename-list* 
</dt> <dd>

Gibt eine Liste mit einem oder mehreren Headerdateinamen der C-Sprache an, die durch Kommas getrennt sind. Der vollständige Dateiname, einschließlich der Erweiterung, muss angegeben werden.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Gibt eine Durch Kommas getrennte Liste von Attributen an, die für den angegebenen Typ gelten. Gültige Typattribute sind das **\[** [**Zuordnen**](allocate.md) **\]** von .

</dd> <dt>

*Typename* 
</dt> <dd>

Gibt einen in der IDL-Datei definierten Typ an. Typattribute im ACF können nur auf Typen angewendet werden, die zuvor in der IDL-Datei definiert wurden.

</dd> <dt>

*ACF-funktionsattribute* 
</dt> <dd>

Gibt Attribute an, die für die Funktion als Ganzes gelten, z. B. **\[** [**comm \_ status**](comm-status.md) **\]** . Funktionsattribute werden in eckige Klammern eingeschlossen. Trennen Sie mehrere Funktionsattribute durch Kommas.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Funktion an, wie in der IDL-Datei definiert.

</dd> <dt>

*ACF-parameter-attributes* 
</dt> <dd>

Gibt ACF-Attribute an, die für einen Parameter gelten. Beachten Sie, dass null oder mehr Attribute auf den Parameter angewendet werden können. Trennen Sie mehrere Parameterattribute durch Kommas. ACF-Parameterattribute werden in eckige Klammern eingeschlossen.

</dd> <dt>

*Parametername* 
</dt> <dd>

Gibt einen Parameter der Funktion an, wie in der IDL-Datei definiert. Jeder Parameter für die Funktion muss in der gleichen Sequenz und mit dem gleichen Namen angegeben werden, wie in der IDL-Datei definiert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das **\[ Nocode-Attribut \]** kann im ACF-Header angezeigt oder auf eine einzelne Funktion angewendet werden.

Wenn das **\[ Nocode-Attribut \]** im ACF-Header angezeigt wird, wird für keine Remotefunktion Clientstubcode generiert, es sei denn, er verfügt über das **\[** [](code.md) **\]** Codefunktionsattribut. Sie können das **\[ \] nocode-Attribut** im Header für eine einzelne Funktion überschreiben, indem Sie das **\[ \] Codeattribut** als Funktionsattribut angeben.

Wenn das **\[ Nocode-Attribut \]** in der Attributliste der Funktion angezeigt wird, wird kein Clientstubcode für die Funktion generiert.

Clientstubcode wird nicht generiert, wenn:

-   Der ACF-Header enthält das **\[ \] nocode-Attribut.**
-   Das **\[ Nocode-Attribut \]** wird auf die Funktion angewendet.
-   Das **\[** [**lokale**](local.md) **\]** Attribut gilt für die Funktion in der Schnittstellendatei.

Code **\[** [](code.md) **\]** oder **\[ Nocode \]** kann in der Attributliste einer Funktion angezeigt werden, und der von Ihnen gewünschte Code kann genau einmal angezeigt werden.

Das **\[ Nocode-Attribut \]** wird ignoriert, wenn Serverstubs generiert werden. Sie können sie nicht anwenden, wenn Sie Serverstubs im DCE-Kompatibilitätsmodus generieren.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungskonfigurationsdatei (Application Configuration File, ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**/acf**](-acf.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[**Automatisches \_ Handle**](auto-handle.md)
</dt> <dt>

[**Code**](code.md)
</dt> <dt>

[**\_comm-Status**](comm-status.md)
</dt> <dt>

[**Implizites \_ Handle**](implicit-handle.md)
</dt> </dl>

 

 




