---
title: Namenssyntax
description: RPC-Syntax (Remote Procedure Call) und Namenssyntax.
ms.assetid: eb370106-bd88-4c21-b287-7b2b174185d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f63c86e6fe9283855e886014787fe36361bfbcdea3bc53e4078bbb43d193293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927819"
---
# <a name="name-syntax"></a>Namenssyntax

Microsoft RPC akzeptiert Namen, die der folgenden Syntax entsprechen:

``` syntax
/.:/name[/name...]/.../domainname/name[/name...]
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="name"></span><span id="NAME"></span>Namen
</dt> <dd>

Gibt einen Bezeichner an, der ein beliebiges Zeichen mit Ausnahme des durch Trennzeichen getrennten Schrägstrichs (/) enthalten kann.

</dd> <dt>

<span id="domainname"></span><span id="DOMAINNAME"></span>Domänenname
</dt> <dd>

Gibt den Namen der Domäne an.

</dd> </dl>

Ein Parameter, der den Name-Syntax-Typ und die Zeichenfolge auswählt, die den Namen angibt, werden für viele der NSI-RPC-Funktionen (Name Service Interface) bereitgestellt.

Microsoft RPC unterstützt nur einen Namenssyntaxtyp, wie von der konstanten RPC \_ C \_ NS \_ SYNTAX \_ DCE angegeben. Diese Konstante wird in der Headerdatei RPCNSI.H definiert.

Die von RPC C NS SYNTAX DCE angegebene Namenssyntax \_ ist eine Erweiterung der \_ \_ \_ \_ NAMENSsyntax des OSF DCE Cell Directory Service (CDS). Die Möglichkeit, einen Domänennamen anzugeben, stellt eine Erweiterung dieser Syntax dar. Es gibt keine absolute Beschränkung für die Anzahl der Namen, die durch Schrägstriche getrennt werden können, solange die Gesamtzeichenfolge kleiner als 256 Zeichen ist.

Mit den Schrägstrichen können Sie eine logische Struktur für den Namen angeben, aber sie entsprechen keiner logischen Struktur in den Objekten selbst.

 

 




