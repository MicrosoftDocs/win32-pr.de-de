---
title: /sstub-Switch
description: Der Schalter /sstub gibt den Namen der Serverstubdatei für eine RPC-Schnittstelle an.
ms.assetid: 8e695e81-7c1b-40c0-aeaa-5390512fa099
keywords:
- /sstub switch MIDL
topic_type:
- apiref
api_name:
- /sstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd83776939e9746103b2f12598a53832d767cebb93767142649a09b804339a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014068"
---
# <a name="sstub-switch"></a>/sstub-Switch

Der Schalter **/sstub** gibt den Namen der Serverstubdatei für eine RPC-Schnittstelle an.

``` syntax
midl /sstub stub_file_name
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*\_ \_ Stubdateiname* 
</dt> <dd>

Gibt einen Dateinamen an, der den Standardnamen der Serverstubdatei überschreibt. Dateinamen können explizit mit doppelten Anführungszeichen (") angegeben werden, um zu verhindern, dass die Shell die Sonderzeichen interpretiert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der angegebene Dateiname ersetzt den Standarddateinamen. Standardmäßig wird der Dateiname abgerufen, indem \_ S.C zum Namen der IDL-Datei hinzugefügt wird. Dieser Schalter wirkt sich nicht auf OLE-Schnittstellen aus.

Beim Importieren von Dateien gilt der angegebene Dateiname nur für eine Stubdatei– die Stubdatei, die der in der Befehlszeile angegebenen IDL-Datei entspricht.

Wenn *der \_ \_ Stubdateiname* keinen expliziten Pfad enthält, wird die Datei in das aktuelle Verzeichnis oder das verzeichnis geschrieben, das durch den Schalter [**/out**](-out.md) angegeben wird. Ein expliziter Pfad im *\_ \_ Stubdateinamen* überschreibt die **/out-Switchspezifikation.**

Der Schalter **/server** none hat Vorrang vor dem Schalter **/sstub.**

## <a name="examples"></a>Beispiele

**midl /sstub my \_ sstub.c filename.idl**

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/out**](-out.md)
</dt> </dl>

 

 




