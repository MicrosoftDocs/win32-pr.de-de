---
title: Referenz zur Routing Protokoll Schnittstelle
description: In dieser Dokumentation werden die Funktionen und Strukturen beschrieben, die zum Implementieren eines Routing Protokolls als benutzermodusdll verwendet werden.
ms.assetid: 0429f5ca-6574-48f5-85ab-70b4677ca539
keywords:
- Routing-und RAS-Dienst RRAS, Routing Protokoll Schnittstelle, Referenz
- Routing Protokoll Schnittstelle RRAS, Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9341dd8dbd304da84fd675aee92e378a44271056
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856096"
---
# <a name="routing-protocol-interface-reference"></a>Referenz zur Routing Protokoll Schnittstelle

In dieser Dokumentation werden die Funktionen und Strukturen beschrieben, die zum Implementieren eines Routing Protokolls als benutzermodusdll verwendet werden.

MPR50 sollte in der Make-Datei für das Routing Protokoll definiert werden.

Das **sizeof \_ -IP- \_ Bindungs (x)-** Makro berechnet die Größe einer [**IP- \_ Adapter \_ Bindungs \_ Informations**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info) Struktur, die die Anzahl der IP-Adressen enthält, in Byte.

Diese Verweis Elemente werden in den folgenden Themen beschrieben:

-   [Routing Protokoll Schnittstellen-Funktionen](routing-protocol-interface-functions.md)
-   [Routing Protokoll Schnittstellen Strukturen](routing-protocol-interface-structures.md)
-   [Verwaltung von IPX-Dienst Tabellen](ipx-service-table-management.md)

 

 




