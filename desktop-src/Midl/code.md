---
title: Codeattribut
description: Das Attribut \code\ ACF bewirkt, dass Clientstubcode für Remotefunktionen generiert wird.
ms.assetid: 735a8c25-29d4-4073-a2db-88bc8615ccc1
keywords:
- Codeattribut MIDL
topic_type:
- apiref
api_name:
- code
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1d94f4f764fb25e5e2a5a43d1cdbe76f5288901846c2291daa4497947a486f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991814"
---
# <a name="code-attribute"></a>Codeattribut

Das **\[ \] Code-ACF-Attribut** bewirkt, dass Clientstubcode für Remotefunktionen generiert wird.

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

*ACF-interface-attributes* 
</dt> <dd>

Gibt eine Liste mit einem oder mehr Attributen an, die für die Schnittstelle als Ganzes gelten. Gültige Attribute sind entweder auto [**\[ \_ \] handle**](auto-handle.md) oder [**\[ implicit \_ \] handle**](implicit-handle.md) und **\[ \]** code , [**\[ nocode \]**](nocode.md)oder [**\[ optimize. \]**](optimize.md) Wenn mindestens zwei Schnittstellenattribute vorhanden sind, müssen sie durch Kommas getrennt werden.

</dd> <dt>

*Schnittstellenname* 
</dt> <dd>

Gibt den Namen der Schnittstelle an.

</dd> <dt>

*filename-list* 
</dt> <dd>

Gibt eine Liste von C-Header-Dateinamen an, die durch Kommas getrennt sind. Sie müssen den vollständigen Dateinamen einschließlich der Erweiterung angeben.

</dd> <dt>

*type-attribute-list* 
</dt> <dd>

Gibt eine Durch Kommas getrennte Liste von Attributen an, die für den angegebenen Typ gelten. Gültige Typattribute umfassen [**\[ "allocate" und \]**](allocate.md) [**\[ "represent" \_ als \]**](represent-as.md).

</dd> <dt>

*Typename* 
</dt> <dd>

Gibt einen in der IDL-Datei definierten Typ an. Typattribute im ACF können nur auf Typen angewendet werden, die zuvor in der IDL-Datei definiert wurden.

</dd> <dt>

*ACF-function-attributes* 
</dt> <dd>

Gibt null oder mehr Attribute an, die für die Funktion als Ganzes gelten, z. B. [**\[ den \_ Kommastatus \]**](comm-status.md). Funktionsattribute werden in eckige Klammern eingeschlossen. Trennen Sie mehrere Funktionsattribute durch Kommas.

</dd> <dt>

*Funktionsname* 
</dt> <dd>

Gibt den Namen der Funktion an, wie in der IDL-Datei definiert.

</dd> <dt>

*ACF-parameter-attributes* 
</dt> <dd>

Gibt ACF-Attribute an, die für einen Parameter gelten. Beachten Sie, dass null, ein oder mehrere Attribute auf den Parameter angewendet werden können. Trennen Sie mehrere Parameterattribute durch Kommas. ACF-Parameterattribute werden in eckige Klammern eingeschlossen.

</dd> <dt>

*Parametername* 
</dt> <dd>

Gibt einen Parameter der Funktion an, wie in der IDL-Datei definiert. Jeder Parameter für die Funktion muss in derselben Sequenz und mit dem gleichen Namen angegeben werden, der in der IDL-Datei definiert ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das **\[ \] Codeattribut** kann im ACF-Header angezeigt oder auf eine einzelne Funktion angewendet werden.

Wenn das **\[ \] Codeattribut** im ACF-Header angezeigt wird, wird Clientstubcode für alle Remotefunktionen generiert, die nicht über das [**\[ Nocode-Funktionsattribut \]**](nocode.md) verfügen. Sie können das **\[ Codeattribut \]** im Header für eine einzelne Funktion überschreiben, indem Sie das **\[ Nocode-Attribut \]** als Funktionsattribut angeben.

Wenn das **\[ \] Codeattribut** in der Attributliste der Remotefunktion angezeigt wird, wird der Clientstubcode für die Funktion generiert. Clientstubcode wird nicht generiert, wenn:

-   Der ACF-Header enthält das [**\[ \] Nocode-Attribut.**](nocode.md)
-   Das [**\[ nocode-Attribut \]**](nocode.md) wird auf die Funktion angewendet.
-   Das [**\[ lokale \]**](local.md) Attribut gilt für die Funktion in der Schnittstellendatei.

Entweder **\[ Code oder \]** [**\[ Nocode kann \]**](nocode.md) in der Liste der Schnittstellen- oder Funktionsattribute angezeigt werden, aber der von Ihnen wähle kann nur einmal in der Liste angezeigt werden.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Anwendungskonfigurationsdatei (Application Configuration File, ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**allocate**](allocate.md)
</dt> <dt>

[**Automatisches \_ Handle**](auto-handle.md)
</dt> <dt>

[**\_Comm-Status**](comm-status.md)
</dt> <dt>

[**implizites \_ Handle**](implicit-handle.md)
</dt> <dt>

[**lokal**](local.md)
</dt> <dt>

[**nocode**](nocode.md)
</dt> <dt>

[**Optimieren**](optimize.md)
</dt> <dt>

[**darstellen \_ als**](represent-as.md)
</dt> </dl>

 

 




