---
title: Schnittstellen in verteilten Objekten
description: Beim verteilten Computing ist eine Schnittstelle eine Sammlung von Definitionen und Remotefunktionen, die es zwei oder mehr Programmen ermöglicht, zwischen verschiedenen Kontexten zu arbeiten.
ms.assetid: d7cd6bf3-58ec-426d-850a-9c5456ed816d
keywords:
- schnittstellen MIDL in verteilten Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8661e7e07f08d35151afe8fb256539ed574b0a0162178e3a9e63dc8c43c59ce8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117807137"
---
# <a name="interfaces-in-distributed-objects"></a>Schnittstellen in verteilten Objekten

Beim verteilten Computing ist eine Schnittstelle eine Sammlung von Definitionen und Remotefunktionen, die es zwei oder mehr Programmen ermöglicht, zwischen verschiedenen Kontexten zu arbeiten. In einer RPC-Anwendung gibt eine Schnittstelle Folgendes an:

-   Wie sich Client- und Serveranwendungen gegenseitig identifizieren.
-   Übertragen von Daten zwischen Client und Server
-   Remoteprozeduren, die von der Clientanwendung aufgerufen werden können.
-   Datentypen für die Parameter und Rückgabewerte der Remoteprozeduren.

Der Microsoft Interface Definition Language (MIDL) dient zum Implementieren von Schnittstellen, die in verteilten Anwendungen verwendet werden. Mit MIDL kann eine Anwendung über eine Oder mehrere Schnittstellen verfügen. Jede Schnittstelle gibt einen eindeutigen verteilten Vertrag zwischen Client- und Serverprogrammen an. Anwendungen, die auf Remoteprozeduraufrufen (RPC), Component Object Model (COM) und Distributed Component Object Model (DCOM) basieren, geben ihre Schnittstellen mit MIDL an.

MIDL ähnelt C und C++ in vielerlei Hinsicht. Eine Übersicht über das Schreiben von MIDL-Schnittstellen finden Sie unter [Entwickeln der Schnittstelle](/windows/desktop/Rpc/developing-the-interface).

 

 