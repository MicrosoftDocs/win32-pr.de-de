---
title: disable_consistency_check-Attribut
description: Weist RPC an, keine Korrelations Konsistenzprüfung zu erzwingen.
ms.assetid: 33ba331d-56e5-4965-a844-7780ea81623d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc55197b5eb680533745a09d4fca4f5827574a7c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309564"
---
# <a name="disable_consistency_check-attribute"></a>\_Attribut für Konsistenz \_ Prüfung deaktivieren

Weist RPC an, keine Korrelations Konsistenzprüfung zu erzwingen.

``` syntax
interface interface-name
{
  return-type function-name(
        [[attribute-list,] disable_consistency_check] param-type param-name
}
```

Bei korrelierten Parametern erzwingt RPC, dass ein nicht-NULL-Puffer übermittelt wird, wenn die Korrelations Anzahl Variable nicht NULL ist.

## <a name="example"></a>Beispiel

``` syntax
HRESULT PassString( [in] DWORD Length, [in, unique, string, 
    size_is( Length )]LPWSTR MyString );
```

Wenn *MyString* **null** ist, lehnt RPC den Aufruf ab, sofern die Länge nicht auf 0 festgelegt ist. Beachten Sie, dass RPC eine *Länge* von 0 (null) zulässt, während *MyString* nicht NULL ist, und RPC behandelt *MyString* als Puffer Zuordnung mit einer Länge von 0 (null).

## <a name="remarks"></a>Bemerkungen

Um diese Überprüfung zu deaktivieren, kann die IDL das \[ Attribut zum Deaktivieren der \_ Konsistenz \_ Prüfung \] für einen Parameter, eine typedef oder einen Zeigertyp enthalten. Dadurch wird RPC umgeleitet, um die Konsistenz zwischen dem Puffer Zeiger und der Korrelations Variablen für den Puffer, auf den der-Parameter oder-Zeiger zeigt, nicht zu erzwingen.

Um die Konsistenzprüfung für eine vollständige Mittel l-Kompilierung zu deaktivieren (und die Erzwingung der Überprüfung in allen Fällen zu deaktivieren), kann der Befehl für die Mittel l-Befehlszeile [/Backward \_ Kompatibilitäts maybenull \_ sizeis](-backward-compat.md) verwendet werden. Hierfür ist es erforderlich, dass das Ziel der Mittell-Kompilierung mindestens "target nt60" ist.

 

 




