---
title: error_status_t-Attribut
description: Das Error \_ Status \_ t-Schlüsselwort kennzeichnet einen Typ für ein Objekt, das Informationen zum Kommunikations Status oder zum Fehlerstatus enthält.
ms.assetid: 7eff0d20-c058-4f16-a3db-0b4c82303135
keywords:
- error_status_t Attribut-Mittel l
topic_type:
- apiref
api_name:
- error_status_t
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0d017b4eaf460b5d5b7ecb8a0bd79201ac8bdee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312216"
---
# <a name="error_status_t-attribute"></a>Fehler \_ Status- \_ t-Attribut

Das **Error \_ Status \_ t** -Schlüsselwort kennzeichnet einen Typ für ein Objekt, das Informationen zum Kommunikations Status oder zum Fehlerstatus enthält.

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

*ACF-Function-Attribute* 
</dt> <dd>

Gibt 0 (null) oder mehr ACF-Funktions Attribute an, z. b. den **\[** [**comm- \_ Status**](comm-status.md) **\]** , den **\[** [**Fehler \_ Status**](fault-status.md) **\]** oder **\[** [**NoCode**](nocode.md) **\]** Funktions Attribute werden in eckige Klammern eingeschlossen. NULL oder mehr Attribute können auf eine Funktion angewendet werden. Trennen Sie mehrere Funktions Attribute durch Kommas.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Funktion an, wie in der IDL-Datei definiert.

</dd> <dt>

*ACF-Parameter-Attribute* 
</dt> <dd>

Gibt Attribute an, die auf einen Parameter angewendet werden. Beachten Sie, dass 0 (null), ein oder mehrere Attribute auf den Parameter angewendet werden können. Trennen Sie mehrere Parameter Attribute durch Kommas. Parameter Attribute werden in eckige Klammern eingeschlossen. IDL-Parameter Attribute, z. b. direktionale Attribute, sind in der ACF nicht zulässig.

</dd> <dt>

*Parameter Name* 
</dt> <dd>

Gibt den Parameter für die Funktion an, wie in der IDL-Datei definiert. Jeder Parameter für die Funktion muss in derselben Reihenfolge angegeben werden. dabei wird derselbe Name verwendet, der in der IDL-Datei definiert ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Typ " **Fehler \_ Status \_ t** " wird als Teil der Ausnahme Behandlungs Architektur in IDL verwendet. Dieser Typ wird einem [**Ganzzahl ohne Vorzeichen**](unsigned.md) [**Long**](long.md)-Typ zugeordnet. Anwendungen, die Fehlersituationen erfassen, verfügen über einen **\[** [**out**](out-idl.md) - **\]** Parameter oder einen Rückgabetyp einer Prozedur, der als **Fehler \_ Status \_ t** angegeben ist, und qualifizieren den **Fehler \_ Status \_ t** mit den **\[** [**\_ Status**](comm-status.md) Attributen "comm" oder " **\]** **\[** [**Fault \_ Status**](fault-status.md) " **\]** in der ACF. Wenn der Parameter oder der Rückgabetyp nicht mit den Status Attributen " **\[ comm \_ \]** " oder " **\[ Fault \_ \]** " gekennzeichnet wurde, verhält sich der Parameter so, als ob er "Ganzzahl ohne Vorzeichen long" wäre.

Ab Version 2,0 generiert der-Mittelwert Compiler stubzeichen, die die richtige Fehler Behandlungs Architektur enthalten. Frühere Versionen des compl-Compilers haben jedoch einen Parameter oder einen Rückgabetyp mit dem **Fehler \_ Status \_ t** behandelt, als ob die Attribute " **\[** [**comm \_ Status**](comm-status.md) " **\]** und " **\[** [**Fehler \_ Status**](fault-status.md) " **\]** angewendet wurden, auch wenn dies nicht der Fall war. Mit mittlerer l 2,0 oder höher müssen Sie explizit die Attribute " **\[ comm \_ Status \]** " und " **\[ Fehler \_ Status \]** " auf den Parameter oder die Prozedur in der ACF anwenden.

Der Typ " **Fehler \_ Status \_ t** " ist einer der vordefinierten Typen der Schnittstellen Definitions Sprache. Vordefinierte Typen können als Typspezifizierer in [**typedef**](typedef.md) -Deklarationen, in allgemeinen Deklarationen und in Funktionsdeklaratoren (entweder als Funktions Rückgabetyp oder als Parametertyp Spezifizierer) angezeigt werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Kommunikations \_ Status**](comm-status.md)
</dt> <dt>

[**Fehler \_ Status**](fault-status.md)
</dt> <dt>

[Schnittstellen Definitionsdatei (IDL)](interface-definition-idl-file.md)
</dt> <dt>

[**lange**](long.md)
</dt> <dt>

[**vorgenommen**](out-idl.md)
</dt> <dt>

[**typedef**](typedef.md)
</dt> <dt>

[**Ganzzahl ohne Vorzeichen**](unsigned.md)
</dt> </dl>

 

 




