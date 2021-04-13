---
title: /System Switch
description: Der Schalter/System leitet den Mittel l-Compiler, um eine Typbibliothek für das angegebene System zu generieren. Der Standardwert ist das aktuelle Betriebssystem.
ms.assetid: 0fb69ffc-5ab4-49f3-b34d-859da776ce9e
keywords:
- /System Schalter-Mittel l
topic_type:
- apiref
api_name:
- / system
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e09f2cf97f8edb86ad831cff35420fad9a07d76
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312654"
---
# <a name="system-switch"></a>/<system> Not

Der- **/<system>** Schalter weist den Mittel l-Compiler an, eine Typbibliothek für das angegebene System zu generieren. Der Standardwert ist das aktuelle Betriebssystem.

``` syntax
midl /{win32 | ia64 | amd64}
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span id="win32"></span><span id="WIN32"></span>Win32 * * * *


</dt> <dd>

Windows 2000, Windows XP, Windows Vista, Windows 7

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span id="ia64"></span><span id="IA64"></span>ia64 * * * *


</dt> <dd>

Eine Intel-basierte 64-Bit-Windows-Umgebung, z. b. Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista oder Windows 7.

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span id="amd64"></span><span id="AMD64"></span>amd64 * * * *


</dt> <dd>

Eine Windows-64 basierte Windows-Umgebung (Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista oder Windows 7).

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der **/<system>** Switch ist funktional identisch mit der Option "Mittel l [**/env**](-env.md) " und wird vom Mittelwert Compiler ausschließlich aus Gründen der Abwärtskompatibilität mit MkTypLib erkannt. Wenn Sie ein neues Makefile-Skript erstellen, verwenden Sie den **/env** -Schalter.

## <a name="examples"></a>Beispiele

**Mittel l/Win32 Dateiname. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/ENV**](-env.md)
</dt> </dl>

 

 




