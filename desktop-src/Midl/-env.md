---
title: /ENV-Schalter
description: Der Schalter/env wählt die Umgebung aus, in der die Anwendung ausgeführt wird.
ms.assetid: 70a548c8-fdc3-48f3-a865-14ba9b29fb02
keywords:
- /ENV-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /env
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59da7185900d4b75781916bd6b4a9d70bf39dc85
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390185"
---
# <a name="env-switch"></a>/ENV-Schalter

Der Schalter **/env** wählt die Umgebung aus, in der die Anwendung ausgeführt wird.

``` syntax
midl /env { win32 | ia64 | amd64 | win64 }
```

## <a name="switch-options"></a>Optionen wechseln

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="win32"></span><span id="WIN32"></span>

<span id="win32"></span><span id="WIN32"></span>Win32 * * * *


</dt> <dd>

Weist den Mittelwert Compiler an, Stub-Dateien oder eine Typbibliotheks Datei für eine 32-Bit-Umgebung zu generieren.

</dd> <dt>

<span id="ia64"></span><span id="IA64"></span>

<span id="ia64"></span><span id="IA64"></span>ia64 * * * *


</dt> <dd>

Weist den Mittelwert Compiler an, Stub-Dateien oder eine Typbibliotheks Datei für eine Intel Architecture 64-Bit (ia64)-Umgebung zu generieren.

</dd> <dt>

<span id="amd64"></span><span id="AMD64"></span>

<span id="amd64"></span><span id="AMD64"></span>amd64 * * * *


</dt> <dd>

Weist den Mittelwert Compiler an, Stub-Dateien oder eine Typbibliotheks Datei für eine Advanced Micro Devices 64-Bit-Umgebung (amd64) zu generieren.

</dd> <dt>

<span id="win64"></span><span id="WIN64"></span>

<span id="win64"></span><span id="WIN64"></span>Win64 * * * *


</dt> <dd>

Gleiches Verhalten wie *ia64*.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der **/env** -Switch wirkt sich hauptsächlich auf die Verpackungs Ebene aus, die für Strukturen in dieser Umgebung verwendet wird Stellen Sie sicher, dass Sie dieselbe Einstellung auf Verpackungs Ebene sowohl für den Mittelwert Compiler als auch für den C-Compiler angeben.

Der Schalter **/env** bestimmt die Verpackungs Ebene und andere Einstellungen wie folgt:

-   Wenn Sie **Win32** angeben, verwenden generierte Stub für alle Typen, die an Remote Vorgängen beteiligt sind, C-Compiler Packaging-Level 8. Die [**int**](int.md) -Datentypen sind 32 Bits. Zeiger sind 32 Bits.
-   Wenn Sie **ia64** oder **amd64** angeben, wird der mittlerer l-Compiler in einem Kreuz Compilermodus für die angegebene (Intel oder AMD) 64-Bit-Plattform ausgeführt. Die generierten Stub verwenden C-Compiler-Komprimierungs Ebene 8 für alle Typen, die an Remote Vorgängen beteiligt sind. Die [**Long**](long.md) -und [**int**](int.md) -Datentypen sind 32 Bits. Zeiger sind 64 Bits.

Die Schalter [**/align**](-align.md), [**/Pack**](-pack.md)und [**/ZP**](-zp.md) haben Vorrang vor den **/env** -Einstellungen.

Weitere Informationen zur 64-Bit-Unterstützung für die mittlere und RPC finden Sie unter [Entwerfen von 64-Bit-kompatiblen Schnittstellen](/windows/desktop/WinProg64/designing-64-bit-compatible-interfaces).

## <a name="examples"></a>Beispiele

**Mittel l/env Win32 filename. idl**

**Mittel l/env ia64 filename. idl**

**Mittel l/env amd64 Dateiname. idl**

**Mittel l/env Win64 filename. idl**

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Allgemeine Syntax der Mittell-Befehlszeile](general-midl-command-line-syntax.md)
</dt> <dt>

[**/Pack**](-pack.md)
</dt> <dt>

[**/ZP**](-zp.md)
</dt> </dl>

 

 