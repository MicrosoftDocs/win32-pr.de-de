---
title: Namens Syntax
description: Remote Prozedur Aufruf (RPC) und namens Syntax.
ms.assetid: eb370106-bd88-4c21-b287-7b2b174185d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d024130a5b8a873c6bfbb2194542344953625d5e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947899"
---
# <a name="name-syntax"></a>Namens Syntax

Microsoft RPC akzeptiert Namen, die der folgenden Syntax entsprechen:

``` syntax
/.:/name[/name...]/.../domainname/name[/name...]
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="name"></span><span id="NAME"></span>Benennen
</dt> <dd>

Gibt einen Bezeichner an, der ein beliebiges Zeichen außer dem Trennzeichen-Schrägstrich (/) enthalten kann.

</dd> <dt>

<span id="domainname"></span><span id="DOMAINNAME"></span>Domain Name
</dt> <dd>

Gibt den Namen der Domäne an.

</dd> </dl>

Ein Parameter, mit dem der Name der Syntax ausgewählt wird, und die Zeichenfolge, die den Namen angibt, werden für viele der NSI-RPC-Funktionen (Name Service Interface) bereitgestellt.

Nur ein Name-Syntax-Typ wird von Microsoft RPC unterstützt, wie in der DCE-Syntax des Konstanten RPC \_ C \_ NS angegeben \_ \_ . Diese Konstante wird in der Header Datei "rpcnsi. H" definiert.

Die von der RPC- \_ C- \_ NS-Syntax DCE angegebene namens Syntax \_ \_ ist eine Erweiterung der namens Syntax des OSF- \_ DCE-Zell Verzeichnis Dienstanbieter (CDs). Die Möglichkeit, einen Domänen Namen anzugeben, stellt eine Erweiterung dieser Syntax dar. Es gibt keine absolute Beschränkung für die Anzahl von Namen, die durch Schrägstriche getrennt werden können, solange die Gesamt Zeichenfolge kleiner als 256 Zeichen ist.

Mithilfe der Schrägstriche können Sie eine logische Struktur zum Namen angeben, aber Sie entsprechen nicht einer logischen Struktur in den Objekten selbst.

 

 




