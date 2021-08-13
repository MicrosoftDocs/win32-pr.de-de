---
title: /Systemschalter
description: Der Schalter /system weist den MIDL-Compiler an, eine Typbibliothek für das angegebene System zu generieren. Der Standardwert ist das aktuelle Betriebssystem.
ms.assetid: 0fb69ffc-5ab4-49f3-b34d-859da776ce9e
keywords:
- /Systemschalter MIDL
topic_type:
- apiref
api_name:
- / system
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31def6297a1a91f6ed28943290a66b544dc368d5a00a91932035a338af50bac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118643778"
---
# <a name="system-switch"></a>/<system> Wechseln

Der **/<system>** Schalter weist den MIDL-Compiler an, eine Typbibliothek für das angegebene System zu generieren. Der Standardwert ist das aktuelle Betriebssystem.

``` syntax
midl /{win32 | ia64 | amd64}
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span id="win32"></span><span id="WIN32"></span>win32


</dt> <dd>

Windows 2000, Windows XP, Windows Vista, Windows 7

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span id="ia64"></span><span id="IA64"></span>ia64


</dt> <dd>

Eine Intel-basierte 64-Bit-Windows-Umgebung wie Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista oder Windows 7.

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span id="amd64"></span><span id="AMD64"></span>amd64®


</dt> <dd>

Eine 64-Bit-basierte 64-Bit-Windows-Umgebung für amerikanische Mikrogeräte, z. B. Windows 2000, Windows Server 2003, Windows XP Professional x64 Edition, Windows Vista oder Windows 7.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Der **/<system>** Schalter ist funktionell identisch mit der MIDL-Option [**/env**](-env.md) und wird vom MIDL-Compiler ausschließlich aus Gründen der Abwärtskompatibilität mit MkTypLib erkannt. Wenn Sie ein neues Makefile generieren, verwenden Sie den Schalter **/env.**

## <a name="examples"></a>Beispiele

**midl /win32 filename.idl**

## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[Allgemeine MIDL-Befehlszeilensyntax](general-midl-command-line-syntax.md)
</dt> <dt>

[**/env**](-env.md)
</dt> </dl>

 

 




