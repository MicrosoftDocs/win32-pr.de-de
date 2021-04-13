---
title: Prozedur Header Deskriptor
description: Die Kopfzeile wurde im Laufe der Lebensdauer der NDR-Engine mehrmals erweitert. Der aktuelle Compiler generiert abhängig vom Modus des Compilers weiterhin verschiedene Header. Neuere Header sind jedoch eine supermenge der älteren Header.
ms.assetid: 05b152b9-bd6d-49d1-8484-d104949c67b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9c28878d82820e519242172496a7932ac4832e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473901"
---
# <a name="procedure-header-descriptor"></a>Prozedur Header Deskriptor

Die Kopfzeile wurde im Laufe der Lebensdauer der NDR-Engine mehrmals erweitert. Der aktuelle Compiler generiert abhängig vom Modus des Compilers weiterhin verschiedene Header. Neuere Header sind jedoch eine supermenge der älteren Header.

## <a name="the-old-oi-header"></a>Der alte – Oi-Header

Der Header weist das folgende Format auf:

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

Where Handle \_ Type<1> kann einer der in der folgenden Tabelle dargestellten Werte sein.



| Hex | Handle               |
|-----|----------------------|
| 31  | Allgemeine FC- \_ Bindung \_    |
| 32  | FC- \_ Bindungs \_ primitiv  |
| 33  | Automatisches FC- \_ \_ handle     |
| 34  | FC- \_ Rückruf \_ handle |
| 0   | (explizites handle)    |



 

Wenn der Handle- \_ Typ<1> Feld ungleich 0 (null) ist, verwendet die Prozedur ein implizites Handle der bestimmten Art. Weitere Informationen finden Sie im Thema [Handles](handles.md) . Wenn der Handle \_ -Typ<1> Feld 0 (null) ist, ist das für die Bindung verwendete Handle einer der Parameter der Prozedur.

Explizite Handles können primitiv, generisch und Kontext sein. die letzte hat das folgende FC-Token.



| Hex | Handle            |
|-----|-------------------|
| 30  | FC- \_ Bindungs \_ Kontext |



 

Gemäß der Konvention ist der Handle-Typ für DCOM-Schnittstellen das automatische FC- \_ \_ handle.

Das \_> Feld Oi Flags<1 ist eine 8-Bit-Maske der folgenden Flags.



| Hex | Flag                         | Bedeutung                                  |
|-----|------------------------------|------------------------------------------|
| 01  | Oi \_ Full \_ ptr \_ verwendet          | Verwendet das vollständige Zeiger Paket.           |
| 02  | \_Verwendete Oi RPCSS- \_ Zuweisung \_       | Verwendet das RPCSS-Speicher Paket.           |
| 04  | Oi- \_ Objekt Prozedur \_             | Eine Prozedur in einer Objektschnittstelle.      |
| 08  | Oi \_ hat \_ rpcflags            | Die Prozedur verfügt über nicht-NULL-RPC-Flags.     |
| 10  | Zählen\_\*                       | Überladen.                              |
| 20  | Zählen\_\*                       | Überladen.                              |
| 40  | Oi \_ verwenden \_ neuer \_ Init- \_ Routinen | Verwendet Windows NT 3.5 Beta2 + init-Routinen. |
| 80  |                              | Nicht verwendet.                                  |



 

Die folgenden Flags sind überladen.



| Hex | Flag                                    | Bedeutung                                             |
|-----|-----------------------------------------|-----------------------------------------------------|
| 10  | Codieren \_ wird \_ verwendet                        | Wird nur in Pickeln verwendet.                              |
| 20  | Decodieren \_ wird \_ verwendet                        | Wird nur in Pickeln verwendet.                              |
| 10  | Oi \_ - \_ \_ Ausnahme \_ Behandlung beim ignorieren von Objekten | Nicht mehr verwendet (altes OLE).                         |
| 20  | Oi hat eine Kommunikations- \_ \_ \_ oder \_ Fehlermeldung                | Nur in unformatierten RPC, \[ comm \_ und Fehler \_ Status \] .        |
| 20  | Oi \_ obj \_ verwendet \_ v2- \_ INTERPRETER           | Verwenden Sie in DCOM nur den [**– OIF**](/windows/desktop/Midl/-oi) -Interpreter. |



 

Im Feld RPC- \_ Flags<4> wird beschrieben, wie das **rpcflags** -Feld der [**RPC- \_ Nachrichten**](/windows/desktop/api/RpcdceP/ns-rpcdcep-rpc_message) Struktur festgelegt wird. Dieses Feld ist nur vorhanden, wenn für die Oi- \_ Flags<1> Feld Oi \_ \_ rpcflags festgelegt wurde. Wenn dieses Feld nicht vorhanden ist, sind die RPC-Flags für die Remote Prozedur 0 (null).

> [!Note]  
> Aus Leistungsgründen verfügen die Async-Interpreter immer über die RPC- \_ Flags<4> Feld vorhanden sind.

 

Das \_ Feld proc num<2> stellt die Prozedur Nummer der Prozedur bereit.

Die Stapel \_ Größe<2> liefert die Gesamtgröße aller Parameter im Stapel, einschließlich dieses Zeigers und/oder Rückgabewerts.

Die \_ Beschreibung<> Feld für explizites Handle wird weiter unten \_ in diesem Dokument beschrieben. Dieses Feld ist nicht vorhanden, wenn die Prozedur ein implizites Handle verwendet.

 

 