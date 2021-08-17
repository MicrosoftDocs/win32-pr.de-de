---
title: Prozedurheaderdeskriptor
description: Der Header wurde mehrmals über die Lebensdauer der NDR-Engine erweitert. Der aktuelle Compiler generiert abhängig vom Compilermodus weiterhin unterschiedliche Header. Neuere Header sind jedoch eine Obermenge der älteren Header.
ms.assetid: 05b152b9-bd6d-49d1-8484-d104949c67b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd9572c9a29ea8477f1d06d8786d50f6abf920de140b6d1663c2431b2ad0c76f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927133"
---
# <a name="procedure-header-descriptor"></a>Prozedurheaderdeskriptor

Der Header wurde mehrmals über die Lebensdauer der NDR-Engine erweitert. Der aktuelle Compiler generiert abhängig vom Compilermodus weiterhin unterschiedliche Header. Neuere Header sind jedoch eine Obermenge der älteren Header.

## <a name="the-old-oi-header"></a>Der alte –Oi-Header

Der Header hat das folgende Format:

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

Wobei handle type<1> kann einer der in der folgenden \_ Tabelle gezeigten Werte sein.



| Hex | Handle               |
|-----|----------------------|
| 31  | FC \_ BIND \_ GENERIC    |
| 32  | FC \_ BIND \_ PRIMITIVE  |
| 33  | FC \_ AUTO \_ HANDLE     |
| 34  | FC \_ CALLBACK \_ HANDLE |
| 0   | (explizites Handle)    |



 

Wenn der Handletyp<1> ist, verwendet die Prozedur ein implizites Handle \_ der angegebenen Art. Weitere Informationen [finden Sie](handles.md) im Thema Handles. Wenn der Handletyp<1> Null ist, ist das für die Bindung verwendete Handle einer der \_ Parameter der Prozedur.

Explizite Handles können primitiv, generisch und Kontext sein. Die letzte verfügt über das folgende FC-Token.



| Hex | Handle            |
|-----|-------------------|
| 30  | \_FC-BINDUNGSKONTEXT \_ |



 

Standardmäßig ist der Handletyp für DCOM-Schnittstellen FC \_ AUTO \_ HANDLE.

Die \_ Oi-Flags<1> ist eine 8-Bit-Maske der folgenden Flags.



| Hex | Flag                         | Bedeutung                                  |
|-----|------------------------------|------------------------------------------|
| 01  | Oi \_ FULL \_ PTR \_ USED          | Verwendet das vollständige Zeigerpaket.           |
| 02  | Oi \_ RPCSS \_ ALLOC \_ USED       | Verwendet das RpcSs-Speicherpaket.           |
| 04  | Oi \_ OBJECT \_ PROC             | Eine Prozedur in einer Objektschnittstelle.      |
| 08  | Oi \_ VERFÜGT \_ ÜBER RPCFLAGS            | Die Prozedur verfügt über RPC-Flags ungleich 0 (null).     |
| 10  | Oi\_\*                       | Überladen.                              |
| 20  | Oi\_\*                       | Überladen.                              |
| 40  | Oi \_ VERWENDEN \_ NEUE \_ INIT-ROUTINEN \_ | Verwendet Windows NT3.5 Beta2+ init-Routinen. |
| 80  |                              | Nicht verwendet.                                  |



 

Die folgenden Flags sind überladen.



| Hex | Flag                                    | Bedeutung                                             |
|-----|-----------------------------------------|-----------------------------------------------------|
| 10  | ENCODE \_ WIRD \_ VERWENDET.                        | Wird nur bei der Auswahl verwendet.                              |
| 20  | DECODE \_ WIRD \_ VERWENDET.                        | Wird nur bei der Auswahl verwendet.                              |
| 10  | Oi \_ IGNORE \_ OBJECT \_ EXCEPTION \_ HANDLING | Wird nicht mehr verwendet (altes OLE).                         |
| 20  | Oi \_ VERFÜGT \_ ÜBER COMM ODER \_ \_ FEHLER                | Nur in UN-RPC, \[ \_ comm, \_ Fehlerstatus \] .        |
| 20  | Oi \_ OBJ \_ USE \_ V2 \_ INTERPRETER           | Verwenden Sie nur in DCOM den [**–Oif-Interpreter.**](/windows/desktop/Midl/-oi) |



 

Das Feld rpc flags<4> beschreibt, wie das \_ **Feld RpcFlags** der [**RPC \_ MESSAGE-Struktur festgelegt**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message) wird. Dieses Feld ist nur vorhanden, wenn für die Oi-Flags<1> \_ Oi \_ HAD \_ RPCFLAGS festgelegt ist. Wenn dieses Feld nicht vorhanden ist, sind die RPC-Flags für die Remoteprozedur 0 (null).

> [!Note]  
> Zur Leistungssteigerung verfügen die asynchronen Interpreter immer über die rpc-Flags<4> \_ feld vorhanden sind.

 

Das Feld proc \_ num<2> gibt die Prozedurnummer der Prozedur an.

Die Stapelgröße<2> die Gesamtgröße aller Parameter im Stapel, einschließlich dieses Zeigers \_ und/oder Rückgabewerts.

Die \_ explizite \_ Handlebeschreibung<> feld wird weiter unten in diesem Dokument beschrieben. Dieses Feld ist nicht vorhanden, wenn die Prozedur ein implizites Handle verwendet.

 

 