---
title: /proxy switch
description: Der Schalter /proxy gibt den Namen der Schnittstellenproxydatei für eine COM-Schnittstelle an.
ms.assetid: 3428f723-81e1-441a-93d5-24034251830c
keywords:
- /proxy switch MIDL
topic_type:
- apiref
api_name:
- /proxy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dc3483706369837d96d14cf30b2f0c6ee307e376f8c422e11d56e06451a22e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811210"
---
# <a name="proxy-switch"></a>/proxy switch

Der Schalter **/proxy** gibt den Namen der Schnittstellenproxydatei für eine COM-Schnittstelle an.

``` syntax
midl /proxy proxy_file_name
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*\_ \_ Proxydateiname* 
</dt> <dd>

Gibt einen Dateinamen an, der den Proxydateinamen der Standardschnittstelle überschreibt. Dateinamen können explizit mit doppelten Anführungszeichen (") angegeben werden, um zu verhindern, dass die Shell die Sonderzeichen interpretiert.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der angegebene Dateiname ersetzt den Standarddateinamen, der durch Hinzufügen von \_ P.C zum Namen der IDL-Datei abgerufen wird. Der Schalter [**/proxy**](proxy.md) wirkt sich nicht auf RPC-Schnittstellen aus.

Wenn der *\_ \_ Proxydateiname* keinen expliziten Pfad enthält, wird die Datei in das aktuelle Verzeichnis oder in das Verzeichnis geschrieben, das durch den Schalter [**/out**](-out.md) angegeben wird. Ein expliziter Pfad im *\_ \_ Proxydateinamen* überschreibt die **/out-Switchspezifikation.**

Eine ausführlichere Beschreibung der Schnittstellenproxydatei und anderer Dateien, die vom MIDL-Compiler generiert werden, finden Sie unter [Allgemeine MIDL-Befehlszeilensyntax.](general-midl-command-line-syntax.md)

## <a name="examples"></a>Beispiele

**midl /proxy my \_ proxy.c filename.idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/header**](-header.md)
</dt> <dt>

[**/iid**](-iid.md)
</dt> <dt>

[**/out**](-out.md)
</dt> </dl>

 

 




