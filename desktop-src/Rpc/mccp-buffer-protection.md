---
title: MCCP-Pufferschutz
description: Ab Windows Vista führt die RPC-Marshalling-Engine weitere Schritte aus, um clientseitige Pufferüberläufe aufgrund zurückgegebener Daten zu verhindern. Diese Einrichtung wird als Mini Compute Conformance Protection (MCCP) bezeichnet.
ms.assetid: 37fe743b-c64e-469d-b8f4-abab9f05c813
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b95234eed76c3d8f0fdc34b0b53e9cf02bcae2fd6db62694e1a3aadd602076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928406"
---
# <a name="mccp-buffer-protection"></a>MCCP-Pufferschutz

Ab Windows Vista führt die RPC-Marshalling-Engine weitere Schritte aus, um clientseitige Pufferüberläufe aufgrund zurückgegebener Daten zu verhindern. Diese Einrichtung wird als Mini Compute Conformance Protection (MCCP) bezeichnet.

Wenn der Client einen Zeiger auf einen vorhandenen Puffer an einen \[ [**out-**](/windows/desktop/Midl/out-idl) oder out-Parameter übergibt, werden zurückgegebene Daten für diesen Parameter in \] \[ [](/windows/desktop/Midl/in)den vorhandenen Puffer \] kopiert. Wenn die zurückgegebenen Daten größer als der übergebene Puffer sind, kann ein Pufferüberlauf auftreten, wenn RPC die zurückgegebenen Daten in den zu kleinen Puffer kopiert. Weitere Informationen [finden Sie unter Top-Level and Embedded Pointers (Zeiger auf oberster Ebene und eingebettete Zeiger).](top-level-and-embedded-pointers.md)

Bei MCCP versucht RPC, diese Bedingung zu erkennen und den Aufruf abzulehnen, wenn sie erkannt wird. Für Puffer mit einem Korrelationswert, z. B. die Größe ist , wird der Aufruf abgelehnt und eine RPC X BAD STUB DATA-Ausnahme ausgelöst, wenn die zurückgegebenen Daten nicht in die angegebene Puffergröße \[ [**\_**](/windows/desktop/Midl/size-is) \] \_ \_ \_ \_ passen. Bei nicht formatierten Zeichenfolgen wird der Aufruf abgelehnt,  wenn die vorhandene Zeichenfolgengröße (Länge bis zum NULL-Abschlusszeichen) nicht ausreicht, um die zurückgegebene Zeichenfolge zu enthalten. Der Aufruf wird abgelehnt. RPC kann keine Pufferüberläufe unter allen Bedingungen erkennen, daher wird dem Entwickler empfohlen, weiterhin normale Vorsichtsmaßnahmen gegen Pufferüberläufe zu treffen.

Wenn der Client keinen vorhandenen Puffer für einen out-Parameter übergibt, sondern stattdessen einen dereferenzierten Zeiger auf \[ [](/windows/desktop/Midl/out-idl) \] **NULL** übergibt, folgt RPC den normalen Regeln, um einen neuen Puffer im Auftrag des Clients zu zuordnen. Dieser Puffer wird mit genügend Speicherplatz zugeordnet, um die zurückgegebenen Daten zu halten.

Ein zweiter Schutz ist, dass RPC für korrelierte Parameter erzwingt, dass ein **Nicht-NULL-Puffer** übergeben wird, wenn die Korrelationsanzahlvariable nicht NULL **ist.**

``` syntax
HRESULT PassString( [in] DWORD Length, [in, unique, string, size_is( Length )]LPWSTR MyString );
```

Wenn *MyString* NULL **ist,** lehnt RPC den Aufruf ab, es sei *denn, Length* ist auf 0 festgelegt. Beachten Sie, dass RPC *die Länge* auf 0 erlaubt, *während MyString* nicht **NULL** ist und RPC *MyString* als Pufferzuordnung der Länge 0 behandelt.

 

 