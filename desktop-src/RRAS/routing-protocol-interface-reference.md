---
title: Referenz zur Routingprotokollschnittstelle
description: In dieser Dokumentation werden die Funktionen und Strukturen beschrieben, die zum Implementieren eines Routingprotokolls als DLL im Benutzermodus verwendet werden.
ms.assetid: 0429f5ca-6574-48f5-85ab-70b4677ca539
keywords:
- Routing- und RAS-Dienst RRAS, Routingprotokollschnittstelle, Referenz
- Routingprotokollschnittstelle RRAS , Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0196a5cbad8919a07a6e9a19ee5f7848eb6378ad2c56f7f0977125e5e79133a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027350"
---
# <a name="routing-protocol-interface-reference"></a>Referenz zur Routingprotokollschnittstelle

In dieser Dokumentation werden die Funktionen und Strukturen beschrieben, die zum Implementieren eines Routingprotokolls als DLL im Benutzermodus verwendet werden.

MPR50 sollte in der Make-Datei für das Routingprotokoll definiert werden.

Das **SIZEOF \_ IP \_ BINDING(x)-Makro** berechnet die Größe einer [**IP ADAPTER BINDING \_ \_ \_ INFO-Struktur,**](/windows/desktop/api/Routprot/ns-routprot-ip_adapter_binding_info) die die Anzahl der IP-Adressen enthält, in Bytes.

Diese Referenzelemente werden in den folgenden Themen beschrieben:

-   [Routingprotokollschnittstellenfunktionen](routing-protocol-interface-functions.md)
-   [Routingprotokollschnittstellenstrukturen](routing-protocol-interface-structures.md)
-   [IPX-Diensttabellenverwaltung](ipx-service-table-management.md)

 

 




