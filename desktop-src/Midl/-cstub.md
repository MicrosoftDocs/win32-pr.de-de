---
title: /cstub-Schalter
description: Der Schalter /cstub gibt den Namen der Clientstubdatei für eine RPC-Schnittstelle an.
ms.assetid: f2c9e083-3511-4e72-b1d1-14a3a662ffaf
keywords:
- /cstub switch MIDL
topic_type:
- apiref
api_name:
- /cstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47b4f635b6d09c85b345eea6dcb7320294e226ad6f2540f01af1e9b3e8098671
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105659"
---
# <a name="cstub-switch"></a>/cstub-Schalter

Der **Schalter /cstub** gibt den Namen der Clientstubdatei für eine RPC-Schnittstelle an.

``` syntax
midl /cstub stub_file_name
```

## <a name="switch-options"></a>Switch-Optionen

<dl> <dt>

*\_ \_ Stubdateiname* 
</dt> <dd>

Gibt einen Dateinamen an, der den Standardnamen der Clientstubdatei überschreibt. Dateinamen können explizit mit doppelten Anführungszeichen (") in Anführungszeichen angegeben werden, um zu verhindern, dass die Shell die Sonderzeichen interpretiert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der angegebene Dateiname ersetzt den Standarddateinamen. Standardmäßig wird der Dateiname durch Hinzufügen der Erweiterung \_ c.c zum Namen der IDL-Datei ermittelt. Dieser Schalter wirkt sich nicht auf OLE-Schnittstellen aus.

Beim Importieren von Dateien gilt der angegebene Dateiname nur für eine Stubdatei– die Stubdatei, die der in der Befehlszeile angegebenen IDL-Datei entspricht.

Wenn *der Name der \_ \_ Stubdatei* keinen expliziten Pfad enthält, wird die Datei in das aktuelle Verzeichnis oder das verzeichnis geschrieben, das durch den [**Schalter /out angegeben**](-out.md) wird. Ein expliziter Pfad im *\_ \_ Stubdateinamen* überschreibt die **/out-Switchspezifikation.**

Der **Schalter /client** none hat Vorrang vor dem **Schalter /cstub.**

## <a name="examples"></a>Beispiele

**midl /cstub my \_ cstub.c filename.idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**/header**](-header.md)
</dt> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/out**](-out.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




