---
title: Schnittstellen in verteilten Objekten
description: Bei der verteilten Verarbeitung ist eine Schnittstelle eine Auflistung von Definitionen und Remote Funktionen, die zwei oder mehr Programmen die Interaktion zwischen verschiedenen Kontexten ermöglicht.
ms.assetid: d7cd6bf3-58ec-426d-850a-9c5456ed816d
keywords:
- Schnittstellen-Mittell, in verteilten Objekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64cbee13dcbab9ccaa6ef6ad3ad3880daa9b14ce
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314991"
---
# <a name="interfaces-in-distributed-objects"></a>Schnittstellen in verteilten Objekten

Bei der verteilten Verarbeitung ist eine Schnittstelle eine Auflistung von Definitionen und Remote Funktionen, die zwei oder mehr Programmen die Interaktion zwischen verschiedenen Kontexten ermöglicht. In einer RPC-Anwendung gibt eine Schnittstelle Folgendes an:

-   Die Art und Weise, wie sich Client-und Server Anwendungen untereinander identifizieren.
-   Wie Daten zwischen Client und Server übertragen werden.
-   Remote Prozeduren, die von der Client Anwendung aufgerufen werden können.
-   Datentypen für die Parameter und Rückgabewerte der Remote Prozeduren.

Der Microsoft Interface Definition Language (Mittelwert) dient zum Implementieren von Schnittstellen, die in verteilten Anwendungen verwendet werden. Mit mittlerer l kann eine Anwendung über eine oder mehrere Schnittstellen verfügen. Jede Schnittstelle gibt einen eindeutigen verteilten Vertrag zwischen den Client-und Serverprogrammen an. Anwendungen, die auf Remote Prozedur aufrufen (RPC), Component Object Model (com) und verteiltem Component Object Model (DCOM) basieren, geben ihre Schnittstellen mithilfe von "Mittel l" an.

"Mittel l" ähnelt C und C++ in vielerlei Hinsicht. Eine Übersicht über das Schreiben von Mittel l-Schnittstellen finden Sie unter [entwickeln der-Schnittstelle](/windows/desktop/Rpc/developing-the-interface).

 

 