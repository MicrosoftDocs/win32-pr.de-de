---
title: /Header-Schalter
description: Der/Header-Schalter gibt den Namen der Header Datei an.
ms.assetid: d36cb6c9-df57-4ef4-aff3-9968ac8ac001
keywords:
- /Header-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /header
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 816310f0b584f3c30d351e0d036e1f18c2f23962
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389257"
---
# <a name="header-switch"></a>/Header-Schalter

Der **/Header** -Schalter gibt den Namen der Header Datei an.

``` syntax
midl /header filename
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*filename* 
</dt> <dd>

Gibt einen Header Dateinamen an, der den Standard Header Dateinamen überschreibt. Dateinamen können mit doppelten Anführungszeichen (") explizit angegeben werden, um zu verhindern, dass die Shell Sonderzeichen interpretiert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der angegebene Dateiname ersetzt den Standard Dateinamen. Der Standard Dateiname wird durch Ersetzen der IDL-Dateinamenerweiterung (i. d. d. d. h. idl) durch die Dateinamenerweiterung. h abgerufen. Bei OLE-Schnittstellen überschreibt der Schalter **/Header** den Standardnamen der Schnittstellen Header Datei.

Wenn Sie Dateien importieren, gilt der angegebene Dateiname nur für eine Header Datei – die Header Datei, die der IDL-Datei entspricht, die in der Befehlszeile angegeben ist.

Wenn *filename* keinen expliziten Pfad enthält, wird die Datei in das aktuelle Verzeichnis oder das durch den Schalter [**/out**](-out.md) angegebene Verzeichnis geschrieben. Ein expliziter Pfad in *filename* überschreibt die **/out** -Switch-Spezifikation.

## <a name="examples"></a>Beispiele

**Mittel l/Header "Bar. h" Dateiname. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/h**](-h.md)
</dt> <dt>

[**/cstub**](-cstub.md)
</dt> <dt>

[**/Out**](-out.md)
</dt> <dt>

[**/sstub**](-sstub.md)
</dt> <dt>

[**/Proxy**](-proxy.md)
</dt> </dl>

 

 




