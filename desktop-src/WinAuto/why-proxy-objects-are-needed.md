---
title: Gründe für die Verwendung von Proxyobjekten
description: Bei barrierefreien Objekten wird die DLL, in der die Hookfunktion des Clients implementiert ist, in den Adressraum des Servers geladen, wenn ein Client eine Kontexthookfunktion legt.
ms.assetid: e8e93271-1da6-42cd-9200-23a3e08b490b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7038a43bf238d9baebee81e13cd82d904dc1b8a4c9ed7fb0c1576f42cbdfdfb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860990"
---
# <a name="why-proxy-objects-are-needed"></a>Gründe für die Verwendung von Proxyobjekten

Bei barrierefreien Objekten wird [](in-context-and-out-of-context-hook-functions.md)die DLL, in der die Hookfunktion des Clients implementiert ist, in den Adressraum des Servers geladen, wenn ein Client eine Kontexthookfunktion fest legt. In diesem Fall zeigt der zurückgegebene Schnittstellenzeiger direkt auf Code im Adressraum des Servers, wenn der Client [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) aus der Hookfunktion aufruft. Wenn der Client eine Schnittstelleneigenschaft mit diesem Zeiger aufruft, ist die Component Object Model-Bibliothek (COM) nicht am Marshalling oder Unmarshaling beteiligt und kann nicht erkennen, ob ein Objekt zerstört wird. Daher muss der Server diese Situation erkennen und einen Fehlercode an den Client zurückgeben.

 

 




