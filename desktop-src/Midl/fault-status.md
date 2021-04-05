---
title: fault_status-Attribut
description: Das Attribut \ Fault \_ Status \ ACF gibt an, dass ein Fehlercode des Typs Fehler \_ Status \_ t auf einen Fehler der Remote Prozedur hinweist, nicht auf andere Arten von Problemen, wie z. b. Kommunikationsfehler.
ms.assetid: 9da7bd3d-cef0-4ad4-b2a4-3f8aa156e8e0
keywords:
- fault_status Attribut-Mittel l
topic_type:
- apiref
api_name:
- fault_status
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 134d9772e167fe63e133d569b9985a7735668d3c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718077"
---
# <a name="fault_status-attribute"></a>Fault \_ Status-Attribut

Mit dem ACF-Attribut für den **\[ Fehler \_ Status \]** wird angegeben, dass ein Fehlercode des Typs " [**Fehler \_ Status \_ t**](error-status-t.md) " auf einen Fehler der Remote Prozedur hinweist, nicht auf andere Arten von Problemen wie Kommunikationsfehler.

``` syntax
[fault_status [ , ACF-function-attributes ] ] function-name(
    [ [ ACF-parameter-attributes ] ] parameter-name
    , ... );

[ [ ACF-function-attributes ] ] function-name(
    [fault_status [ , ACF-parameter-attributes ] ] parameter-name
    , ... );
```

## <a name="parameters"></a>Parameter

<dl> <dt>

*ACF-Function-Attribute* 
</dt> <dd>

Gibt NULL oder mehr ACF-Funktions Attribute an, wie z. b. **\[ Fehler \_ Status \]** und **\[** [**NoCode**](nocode.md) **\]** . Funktions Attribute werden in eckige Klammern eingeschlossen. Beachten Sie, dass 0 (null) oder mehr Attribute auf eine Funktion angewendet werden können. Trennen Sie mehrere Funktions Attribute durch Kommas. Beachten Sie auch Folgendes: Wenn der **\[ Fehler \_ Status \]** als Funktions Attribut angezeigt wird, kann er nicht auch als Parameter Attribut angezeigt werden.

</dd> <dt>

*function-name* 
</dt> <dd>

Gibt den Namen der Funktion an, wie in der IDL-Datei definiert.

</dd> <dt>

*ACF-Parameter-Attribute* 
</dt> <dd>

Gibt Attribute an, die auf einen Parameter angewendet werden. Beachten Sie, dass NULL oder mehr Attribute auf den Parameter angewendet werden können. Parameter Attribute werden in eckige Klammern eingeschlossen. Trennen Sie mehrere Parameter Attribute durch Kommas. IDL-Parameter Attribute, z. b. direktionale Attribute, sind in der ACF nicht zulässig. Beachten Sie Folgendes: Wenn der **\[ Fehler \_ Status \]** als Parameter Attribut angezeigt wird, kann er nicht auch als Funktions Attribut angezeigt werden.

</dd> <dt>

*Parameter Name* 
</dt> <dd>

Gibt den Parameter für die Funktion an, wie in der IDL-Datei definiert. Jeder Parameter für die Funktion muss in derselben Reihenfolge angegeben werden. dabei wird derselbe Name verwendet, der in der IDL-Datei definiert ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das **\[ Fault \_ Status \]** -Attribut kann entweder als Funktions Attribut oder als Parameter Attribut verwendet werden, es kann jedoch nur einmal pro Funktion angezeigt werden. Sie kann entweder auf die Funktion selbst oder auf einen Parameter in jeder Funktion angewendet werden.

Das **\[ Fault \_ Status \]** -Attribut kann nur auf Funktionen angewendet werden, die den [**Typfehler \_ Status \_ t**](error-status-t.md)zurückgeben. Wenn die Remote Prozedur auf eine Weise fehlschlägt, die bewirkt, dass ein Fehler-PDU zurückgegeben wird, wird ein Fehlercode zurückgegeben.

Wenn der **\[ Fehler \_ \] Status** als Parameter Attribut verwendet wird, muss der Parameter ein **\[** [**out**](out-idl.md) - **\]** Parameter vom Typ " [**Error \_ Status \_ t**](error-status-t.md)" sein. Wenn ein Server Fehler auftritt, wird der-Parameter auf den Fehlercode festgelegt. Wenn der Remote-Befehl erfolgreich abgeschlossen wurde, legt die Prozedur den Wert fest.

Der Parameter, der dem **\[ Fault \_ Status \]** -Attribut zugeordnet ist, muss nicht in der IDL-Datei angegeben werden. Wenn der-Parameter nicht angegeben wird, wird ein neuer [**out**](out-idl.md) -Parameter vom Typ [**Fehler \_ Status \_ t**](error-status-t.md) nach dem letzten Parameter generiert, der in der DCE-IDL-Datei definiert ist.

Es ist möglich, dass die Attribute " **\[ Fault \_ Status \]** " und " **\[** [**comm \_ Status**](comm-status.md) " **\]** in einer einzelnen Funktion als Funktions Attribute oder Parameter Attribute angezeigt werden. Wenn beide Attribute Funktions Attribute sind oder wenn Sie auf denselben Parameter angewendet werden und kein Fehler auftritt, hat die Funktion oder der Parameter den Wert **Fehler \_ Status \_ OK**. Andernfalls enthält Sie den entsprechenden Statuscode Wert. Da die für den **\[ Fehler \_ Status \]** zurückgegebenen Werte sich von den Werten unterscheiden, die für den Kommunikations **\[ \_ Status \]** zurückgegeben werden, werden die zurückgegebenen Werte leicht interpretiert

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Anwendungs Konfigurationsdatei (ACF)](application-configuration-file-acf-.md)
</dt> <dt>

[**Kommunikations \_ Status**](comm-status.md)
</dt> <dt>

[**Fehler \_ Status \_ t**](error-status-t.md)
</dt> <dt>

[**NoCode**](nocode.md)
</dt> <dt>

[**vorgenommen**](out-idl.md)
</dt> </dl>

 

 




