---
title: /SAL-Schalter
description: Der/SAL-Schalter leitet die mittlere Anmerkung in den generierten Stub-Dateien mit der-Option.
ms.assetid: 452A19CA-6F72-416F-8059-77937412DA88
keywords:
- /SAL-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /sal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ef52eb510c71bfdb153b95a5d05e992359e39b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106338229"
---
# <a name="sal-switch"></a>/SAL-Schalter

Der **/SAL** -Schalter leitet die mittlere Anmerkung in den generierten Stub-Dateien mit der-Option.

``` syntax
midl /sal
```

## <a name="switch-options"></a>Optionen wechseln

Dieser Switch hat keine Parameter.

## <a name="remarks"></a>Bemerkungen

In der mittleren l werden Zeiger-und Array Parameter mit Anmerkungen markiert, die die Parameter Beschreibung in der IDL-Datei entsprechend der von RPC und der NDR-Marshalling-Engine übergebenen Parameter Beschreibung widerspiegeln. In der mittleren l werden keine Anmerkungen für Parameter in Schnittstellen Methoden erstellt, die mit dem [**\[ lokalen \]**](local.md)Attribut markiert sind, es sei denn, [**/SAL \_ local**](-sal-local.md) ist auch in der Befehlszeile vorhanden. Verwenden Sie zum Überschreiben der in der Mitte generierten Anmerkung Das [**\[ kommentieren \]**](annotate.md) -Attribut.

Bei in der Mitte generierten Anmerkungen wird immer \_ \_ RPC \_ vorangestellt, und die Verwendung des **rpcsal. h** -Headers erfordert die Übersetzung der Anmerkung in standardmäßige SAL-Anmerkungen.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/SAL \_ lokal**](-sal-local.md)
</dt> <dt>

[**\[kommentieren\]**](annotate.md)
</dt> </dl>

 

 




