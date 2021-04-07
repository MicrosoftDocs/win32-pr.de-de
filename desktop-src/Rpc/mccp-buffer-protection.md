---
title: Schutz von MCCP-Puffern
description: Ab Windows Vista führt das RPC-Marshalling-Modul weitere Schritte aus, um zu versuchen, Client seitige Pufferüberläufe aufgrund von zurückgegebenen Daten zu verhindern. Diese Funktion wird als Mini Server-Konformitäts Schutz (Mini Compute Conformance Protection, MCCP) bezeichnet.
ms.assetid: 37fe743b-c64e-469d-b8f4-abab9f05c813
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70d04de57974bd9665d659129590d72513eb83e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729800"
---
# <a name="mccp-buffer-protection"></a>Schutz von MCCP-Puffern

Ab Windows Vista führt das RPC-Marshalling-Modul weitere Schritte aus, um zu versuchen, Client seitige Pufferüberläufe aufgrund von zurückgegebenen Daten zu verhindern. Diese Funktion wird als Mini Server-Konformitäts Schutz (Mini Compute Conformance Protection, MCCP) bezeichnet.

Wenn der Client einen Zeiger an einen vorhandenen Puffer an einen \[ [**out**](/windows/desktop/Midl/out-idl) - \] oder \[ [**in**](/windows/desktop/Midl/in)-,**out** - \] Parameter übergibt, werden die zurückgegebenen Daten für diesen Parameter in den vorhandenen Puffer kopiert. Wenn die zurückgegebenen Daten größer als der übergebenen Puffer sind, kann ein Pufferüberlauf auftreten, wenn die zurückgegebenen Daten von RPC in den zu kleinen Puffer kopiert werden. Siehe [Top-Level-und Embedded-Zeiger](top-level-and-embedded-pointers.md).

Bei der Verwendung von MCCP versucht RPC, diesen Zustand zu erkennen und den Aufruf abzulehnen, wenn er erkannt wird. Bei Puffern mit einem Korrelations Wert, z. b. \[ [**Größe \_**](/windows/desktop/Midl/size-is) \] , wird der Aufruf abgelehnt, wenn die zurückgegebenen Daten nicht in die angegebene Puffergröße \_ passen \_ \_ \_ . Bei nicht großen Zeichen folgen wird der-Rückruf zurückgewiesen, wenn die vorhandene Zeichen folgen Größe (Länge bis zum **null** -Terminator) nicht ausreicht, um die zurückgegebene Zeichenfolge zu speichern. der-Rückruf wird zurückgewiesen. RPC kann in allen Bedingungen keine Pufferüberläufe erkennen, daher wird empfohlen, die normalen Vorsichtsmaßnahmen gegen Pufferüberläufe weiterhin zu übernehmen.

Wenn der Client keinen vorhandenen Puffer für einen \[ [**out**](/windows/desktop/Midl/out-idl) - \] Parameter übergibt, sondern stattdessen einen dereferenzierten Zeiger an **null** übergibt, befolgt RPC die normalen Regeln, um im Auftrag des Clients einen neuen Puffer zuzuweisen. Dieser Puffer wird mit ausreichendem Speicherplatz zum Speichern der zurückgegebenen Daten zugeordnet.

Ein zweiter Schutz besteht darin, dass RPC bei korrelierten Parametern erzwingt, dass ein nicht-**null** -Puffer übermittelt wird, wenn die Korrelations Anzahl Variable nicht **null** ist.

``` syntax
HRESULT PassString( [in] DWORD Length, [in, unique, string, size_is( Length )]LPWSTR MyString );
```

Wenn *MyString* **null** ist, lehnt RPC den Aufruf ab, sofern die *Länge* nicht auf 0 festgelegt ist. Beachten Sie, dass RPC eine *Länge* von 0 (null) zulässt, während *MyString* nicht **null** ist, und RPC behandelt *MyString* als Puffer Zuordnung mit einer Länge von 0 (null).

 

 