---
title: comm_status-Attribut
description: Das Attribut \ comm \_ Status \ ACF bewirkt, dass ein Fehlercode zurückgegeben wird, wenn während der Ausführung einer Funktion ein Kommunikationsfehler auftritt.
ms.assetid: 3ea9ce62-8bd4-40fe-b838-bfebd52b5a15
keywords:
- comm_status Attribut-Mittel l
topic_type:
- apiref
api_name:
- comm_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd4952d03a80dbbffb135043d024b0c0eb18966f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718779"
---
# <a name="comm_status-attribute"></a>comm- \_ Status Attribut

Das **\[ \_ Status \]** -ACF-Attribut von comm bewirkt, dass ein Fehlercode zurückgegeben wird, wenn während der Ausführung einer Funktion ein Kommunikationsfehler auftritt.

``` syntax
[comm_status [ , ACF-function-attributes ] ] 
    error_status_t function-name(
        [ [ ACF-parameter-attributes ] ] parameter-name
        , ...);

[ [ ACF-function-attributes ] ] function-name(
    [comm_status [ , ACF-parameter-attributes ] ] error_status_t name
    , ...);
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*ACF-Function-Attribute* 
</dt> <dd>

Gibt NULL oder mehr ACF-Funktions Attribute an, wie z. b. den **\[ comm- \_ Status \]** und **\[** [**NoCode**](nocode.md) **\]** . Funktions Attribute werden in eckige Klammern eingeschlossen. NULL oder mehr Attribute können auf eine Funktion angewendet werden. Trennen Sie mehrere Funktions Attribute durch Kommas. Beachten Sie Folgendes: Wenn der Kommunikations **\[ \_ Status \]** als Funktions Attribut angezeigt wird, kann er nicht auch als Parameter Attribut angezeigt werden.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Funktion an, wie in der IDL-Datei definiert.

</dd> <dt>

*ACF-Parameter-Attribute* 
</dt> <dd>

Gibt Attribute an, die auf einen Parameter angewendet werden. Beachten Sie, dass 0 (null), ein oder mehrere Attribute auf den Parameter angewendet werden können. Trennen Sie mehrere Parameter Attribute durch Kommas. Parameter Attribute werden in eckige Klammern eingeschlossen. IDL-Parameter Attribute, z. b. direktionale Attribute, sind in der ACF nicht zulässig. Beachten Sie Folgendes: Wenn der Kommunikations **\[ \_ Status \]** als Parameter Attribut angezeigt wird, kann er nicht auch als Funktions Attribut angezeigt werden.

</dd> <dt>

*Parameter Name* 
</dt> <dd>

Gibt den Parameter für die Funktion an, wie in der IDL-Datei definiert. Jeder Parameter für die Funktion muss in derselben Reihenfolge angegeben werden. dabei wird derselbe Name verwendet, der in der IDL-Datei definiert ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **\[ comm \_ - \] Status** Attribut kann entweder als Funktions Attribut oder als Parameter Attribut verwendet werden, es kann jedoch nur einmal pro Funktion angezeigt werden. Sie kann entweder auf die Funktion oder auf einen Parameter in jeder Funktion angewendet werden.

Das **\[ comm \_ - \] Status** Attribut kann nur auf Funktionen angewendet werden, die den [**Typfehler \_ Status \_ t**](error-status-t.md)zurückgeben. Wenn während der Ausführung der Funktion ein Kommunikationsfehler auftritt, wird ein Fehlercode zurückgegeben.

Wenn der **\[ \_ Status \] "comm** " als Parameter Attribut verwendet wird, muss der Parameter in der IDL-Datei definiert werden, und er muss ein **\[** [**out**](out-idl.md) - **\]** Parameter vom Typ " [**Error \_ Status \_ t**](error-status-t.md)" sein. Wenn während der Ausführung der Funktion ein Kommunikationsfehler auftritt, wird der-Parameter auf den Fehlercode festgelegt. Wenn der Remote-Befehl erfolgreich abgeschlossen wurde, legt die Prozedur den Wert fest.

Die Attribute " **\[ comm \_ \] Status** " und " **\[** [**Fehler \_ Status**](fault-status.md) " können **\]** in einer einzelnen Funktion, entweder als Funktions Attribute oder Parameter Attribute, angezeigt werden. Wenn beide Attribute Funktions Attribute sind oder wenn Sie auf denselben Parameter angewendet werden und kein Fehler auftritt, hat die Funktion oder der Parameter den Wert **Fehler \_ Status \_ OK**. Andernfalls enthält Sie den entsprechenden Statuswert für den **\[ comm \_ \]** -oder **\[ Fehler \_ Status \]** . Da die für den Kommunikations **\[ \_ Status \]** zurückgegebenen Werte sich von den für den **\[ Fehler \_ \] Status** zurückgegebenen Werten unterscheiden, werden die zurückgegebenen Werte leicht interpretiert.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Fehler \_ Status \_ t**](error-status-t.md)
</dt> <dt>

[**Fehler \_ Status**](fault-status.md)
</dt> <dt>

[**NoCode**](nocode.md)
</dt> <dt>

[**vorgenommen**](out-idl.md)
</dt> </dl>

 

 




