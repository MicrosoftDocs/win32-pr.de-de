---
title: Bindungshandles
description: Bindung ist der Prozess, bei dem eine logische Verbindung zwischen einem Clientprogramm und einem Serverprogramm erstellt wird. Die Informationen, aus denen die Bindung zwischen Client und Server besteht, werden durch eine Struktur dargestellt, die als Bindungshand handle bezeichnet wird.
ms.assetid: 802e6da7-a329-4010-91bd-003ad2169121
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09eae434fde790531a6f723cab6dc0b0613ee2fc99d680478d697cb550d6a18b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932340"
---
# <a name="binding-handles"></a>Bindungshandles

Bindung ist der Prozess, bei dem eine logische Verbindung zwischen einem Clientprogramm und einem Serverprogramm erstellt wird. Die Informationen, aus denen die Bindung zwischen Client und Server besteht, werden durch eine Struktur dargestellt, die als Bindungshand handle bezeichnet wird.

Ein Bindungshandl entspricht einem Dateihandl, das von der Fopen C-Laufzeitbibliotheksfunktion zurückgegeben wird, oder einem Fensterhandl, das von [**der CreateWindow-Funktion zurückgegeben**](/windows/win32/api/winuser/nf-winuser-createwindowa) wird.

Wie bei diesen Handles kann Ihre Anwendung nicht direkt auf die Informationen im Bindungshandles zugreifen und diese bearbeiten. Die Informationen in einer Bindungshandbücher-Datenstruktur sind nur für die RPC-Laufzeitbibliotheken verfügbar. Sie stellen das Handle und die Laufzeitbibliotheken für den Zugriff und die Bearbeitung der entsprechenden Daten zur Verfügung.

Dieser Abschnitt enthält eine Diskussion über Bindungshandles in den folgenden Themen:

-   [Typen von Bindungshandles](types-of-binding-handles.md)
-   [Clientseitige Bindung](client-side-binding.md)
-   [Serverseitige Bindung](server-side-binding.md)
-   [Vollständig und teilweise gebundene Handles](fully-and-partially-bound-handles.md)
-   [Interpretieren von Bindungsinformationen](interpreting-binding-information.md)
-   [Microsoft RPC Binding-Handle Extensions](microsoft-rpc-binding-handle-extensions.md)
-   [Binding-Handle-Funktionen](binding-handle-functions.md)
-   [Die RPC-Namensdienst-Datenbank](the-rpc-name-service-database.md)

 

 