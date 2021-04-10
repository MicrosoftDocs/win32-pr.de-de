---
title: Warum Proxy Objekte erforderlich sind
description: Bei zugänglichen Objekten wird die dll, in der die Hook-Funktion des Clients implementiert ist, in den Adressbereich des Servers geladen, wenn ein Client eine kontextbasierte Hook-Funktion festlegt.
ms.assetid: e8e93271-1da6-42cd-9200-23a3e08b490b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28d672f48e9c41f23599a8a64585062a126dafb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309999"
---
# <a name="why-proxy-objects-are-needed"></a>Warum Proxy Objekte erforderlich sind

Bei zugänglichen Objekten wird die dll, in der die Hook-Funktion des Clients implementiert ist, in den Adressbereich des Servers geladen, wenn ein Client eine [kontextbasierte Hook-Funktion](in-context-and-out-of-context-hook-functions.md)festlegt. Wenn der Client in diesem Fall [**accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) von der Hook-Funktion aus aufruft, zeigt der Schnittstellen Zeiger, der zurückgegeben wird, direkt auf den Code im Adressbereich des Servers. Wenn der Client eine Schnittstellen Eigenschaft mithilfe dieses Zeigers aufruft, ist die Component Object Model (com)-Bibliothek nicht an Marshalling oder Unmarshalling beteiligt und kann nicht erkennen, ob ein Objekt zerstört wird. Daher muss der Server diese Situation erkennen und einen Fehlercode an den Client zurückgeben.

 

 




