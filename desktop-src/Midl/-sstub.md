---
title: /sstub-Schalter
description: Der/sstub-Schalter gibt den Namen der Server-Stub-Datei für eine RPC-Schnittstelle an.
ms.assetid: 8e695e81-7c1b-40c0-aeaa-5390512fa099
keywords:
- /sstub-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /sstub
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 131be3dd1890967f7107bea64c3dc2634833653d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106340668"
---
# <a name="sstub-switch"></a>/sstub-Schalter

Der **/sstub** -Schalter gibt den Namen der Server-Stub-Datei für eine RPC-Schnittstelle an.

``` syntax
midl /sstub stub_file_name
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*Stub- \_ Dateiname \_* 
</dt> <dd>

Gibt einen Dateinamen an, der den Standard Dateinamen der Server-Stub-Datei überschreibt. Dateinamen können mit doppelten Anführungszeichen (") explizit angegeben werden, um zu verhindern, dass die Shell die Sonderzeichen interpretiert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der angegebene Dateiname ersetzt den Standard Dateinamen. Standardmäßig wird der Dateiname abgerufen, indem \_ S. C dem Namen der IDL-Datei hinzugefügt wird. Dieser Schalter wirkt sich nicht auf OLE-Schnittstellen aus.

Wenn Sie Dateien importieren, gilt der angegebene Dateiname nur für eine Stubdatei – die Stubdatei, die der IDL-Datei entspricht, die in der Befehlszeile angegeben ist.

Wenn der *Stub- \_ Dateiname \_* keinen expliziten Pfad enthält, wird die Datei in das aktuelle Verzeichnis oder das durch den [**/out**](-out.md) -Schalter angegebene Verzeichnis geschrieben. Ein expliziter Pfad im *\_ stubdateinamen \_* überschreibt die **/out** -Switch-Spezifikation.

Der Schalter **/Server** None hat Vorrang vor dem **/sstub** -Schalter.

## <a name="examples"></a>Beispiele

**Mittel l/sstub My \_ sstub. c filename. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/Header**](-header.md)
</dt> <dt>

[**/Out**](-out.md)
</dt> </dl>

 

 




