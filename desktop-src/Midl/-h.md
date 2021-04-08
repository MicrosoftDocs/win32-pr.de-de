---
title: /h-Schalter
description: Die/h-Option ist funktionell gleichwertig mit der/Header-Option.
ms.assetid: 1b74d5f2-6624-4b71-832d-fb55a0e84c86
keywords:
- /h-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /h
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7ff2cd7aa5e4b8386e0c9faecfaccd860207403
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038085"
---
# <a name="h-switch"></a>/h-Schalter

Die **/h** -Option ist funktionell gleichwertig mit der [**/Header**](-header.md) -Option.

``` syntax
midl /h filename
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

*filename* 
</dt> <dd>

Gibt einen Header Dateinamen an, der den Standard Header Dateinamen überschreibt. Dateinamen können mit doppelten Anführungszeichen (") explizit angegeben werden, um zu verhindern, dass die Shell Sonderzeichen interpretiert.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Schalter **/h** gibt *filename* als Namen für eine Header Datei an, die alle Definitionen enthält, die in der IDL-Datei enthalten sind, ohne die IDL-Syntax. Diese Datei kann als C-oder C++-Header Datei verwendet werden.

## <a name="examples"></a>Beispiele

**Mittel l/h tlibhead. h Dateiname. idl**

**Mittel l/h "mittlerer l. h" Dateiname. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Header**](-header.md)
</dt> </dl>

 

 




