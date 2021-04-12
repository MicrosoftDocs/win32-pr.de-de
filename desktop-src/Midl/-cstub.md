---
title: /cstub-Schalter
description: Der/cstub-Schalter gibt den Namen der Client-Stub-Datei für eine RPC-Schnittstelle an.
ms.assetid: f2c9e083-3511-4e72-b1d1-14a3a662ffaf
keywords:
- /cstub-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /cstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 878f6eee47deaac3887c3f9936c18b0185cc807a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312959"
---
# <a name="cstub-switch"></a>/cstub-Schalter

Der **/cstub** -Schalter gibt den Namen der Client-Stub-Datei für eine RPC-Schnittstelle an.

``` syntax
midl /cstub stub_file_name
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*Stub- \_ Dateiname \_* 
</dt> <dd>

Gibt einen Dateinamen an, der den standardmäßigen Client-Stub-Dateinamen überschreibt. Dateinamen können mit doppelten Anführungszeichen (") explizit angegeben werden, um zu verhindern, dass die Shell die Sonderzeichen interpretiert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der angegebene Dateiname ersetzt den Standard Dateinamen. Standardmäßig wird der Dateiname durch Hinzufügen der Erweiterung \_ c. c zum Namen der IDL-Datei abgerufen. Dieser Schalter wirkt sich nicht auf OLE-Schnittstellen aus.

Wenn Sie Dateien importieren, gilt der angegebene Dateiname nur für eine Stubdatei – die Stubdatei, die der IDL-Datei entspricht, die in der Befehlszeile angegeben ist.

Wenn der *Stub- \_ Dateiname \_* keinen expliziten Pfad enthält, wird die Datei in das aktuelle Verzeichnis oder das durch den [**/out**](-out.md) -Schalter angegebene Verzeichnis geschrieben. Ein expliziter Pfad im *\_ stubdateinamen \_* überschreibt die **/out** -Switch-Spezifikation.

Der Schalter **/Client** None hat Vorrang vor dem **/cstub** -Schalter.

## <a name="examples"></a>Beispiele

**Mittel l/cstub My \_ cstub. c filename. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**/Header**](-header.md)
</dt> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Out**](-out.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> </dl>

 

 




