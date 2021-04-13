---
title: /IID-Schalter
description: Der Schalter/IID gibt den Namen der schnittstellenbezeichnerdatei für eine COM-Schnittstelle an und überschreibt den Standardnamen, der durch Hinzufügen von \_ i. c zum Namen der IDL-Datei abgerufen wird.
ms.assetid: 051593f5-e612-4b19-94e5-d7885dbede21
keywords:
- /IID-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /iid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 631a28f1bc5a1a24253c9416104df9941cd8da33
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389255"
---
# <a name="iid-switch"></a>/IID-Schalter

Der Schalter **/IID** gibt den Namen der schnittstellenbezeichnerdatei für eine COM-Schnittstelle an und überschreibt den Standardnamen, der durch Hinzufügen von \_ i. c zum Namen der IDL-Datei abgerufen wird.

``` syntax
midl /iid filename
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*filename* 
</dt> <dd>

Gibt einen Dateinamen für den Schnittstellen Bezeichner an, der den Dateinamen des Standardschnittstellen Bezeichners für eine COM-Schnittstelle überschreibt Dateinamen können mit doppelten Anführungszeichen (") explizit angegeben werden, um zu verhindern, dass die Shell die Sonderzeichen interpretiert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der **/IID** -Schalter wirkt sich nicht auf RPC-Schnittstellen aus.

Wenn *filename* keinen expliziten Pfad enthält, wird die Datei in das aktuelle Verzeichnis oder in das durch den Schalter [**/out**](-out.md) angegebene Verzeichnis geschrieben. Ein expliziter Pfad in *filename* überschreibt die **/out** -Switch-Spezifikation.

## <a name="examples"></a>Beispiele

**Mittel l/iid "My \_ IID. c" Dateiname. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Header**](-header.md)
</dt> <dt>

[**/Out**](-out.md)
</dt> <dt>

[**/Proxy**](-proxy.md)
</dt> </dl>

 

 




