---
title: /Proxy-Schalter
description: Der/Proxy-Schalter gibt den Namen der Schnittstellen Proxy Datei für eine COM-Schnittstelle an.
ms.assetid: 3428f723-81e1-441a-93d5-24034251830c
keywords:
- /Proxy-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27bff2103e22952e456976c6e0a88e7d232e42c3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857588"
---
# <a name="proxy-switch"></a>/Proxy-Schalter

Der **/Proxy** -Schalter gibt den Namen der Schnittstellen Proxy Datei für eine COM-Schnittstelle an.

``` syntax
midl /proxy proxy_file_name
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*Name der Proxy \_ Datei \_* 
</dt> <dd>

Gibt einen Dateinamen an, der den Standardnamen der Schnittstellen Proxy Datei überschreibt. Dateinamen können mit doppelten Anführungszeichen (") explizit angegeben werden, um zu verhindern, dass die Shell die Sonderzeichen interpretiert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der angegebene Dateiname ersetzt den Standard Dateinamen, der durch das Hinzufügen von \_ P. C abgerufen wird, zum Namen der IDL-Datei. Der Schalter/ [**Proxy**](proxy.md) wirkt sich nicht auf RPC-Schnittstellen aus.

Wenn *der \_ Proxy \_ Dateiname* keinen expliziten Pfad enthält, wird die Datei in das aktuelle Verzeichnis oder in das durch den Schalter [**/out**](-out.md) angegebene Verzeichnis geschrieben. Ein expliziter Pfad im *\_ \_ Namen der Proxy Datei* überschreibt die **/out** -switchspezifikation.

Eine ausführlichere Beschreibung der Schnittstellen Proxy Datei und anderer Dateien, die vom-Mittell-Compiler generiert werden, finden Sie unter [allgemeine Syntax für die Befehlszeilen](general-midl-command-line-syntax.md)Schnittstelle.

## <a name="examples"></a>Beispiele

**Mittel l/Proxy My \_ Proxy. c filename. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Header**](-header.md)
</dt> <dt>

[**/IID**](-iid.md)
</dt> <dt>

[**/Out**](-out.md)
</dt> </dl>

 

 




