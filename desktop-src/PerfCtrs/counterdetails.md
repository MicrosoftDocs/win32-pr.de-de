---
description: In der Tabelle CounterDetails wird ein bestimmter Leistungsindikator auf einem bestimmten Computer beschrieben.
ms.assetid: e2a16a6e-8cd4-4fd3-adeb-461faed948e4
title: CounterDetails
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef429f7f90c38d53f085ed0243e1c799c1d1cfa808c7aa052d8a37ed3a1faf1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011358"
---
# <a name="counterdetails"></a>CounterDetails

In der Tabelle **CounterDetails** wird ein bestimmter Leistungsindikator auf einem bestimmten Computer beschrieben.

**Die Tabelle CounterDetails** definiert die folgenden Felder:

-   **CounterID:** Ein eindeutiger Bezeichner in der Datenbank, der einer bestimmten Indikatornamen-Textzeichenfolge zugeordnet ist. Dieses Feld ist der Primärschlüssel dieser Tabelle.
-   **MachineName:** Der Name des Computers, auf dem dieses DataSet protokolliert wurde.
-   **ObjectName:** Der Name des Leistungsobjekts.
-   **CounterName:** Der Name des Leistungsindikators.
-   **CounterType:** Der Indikatortyp. Eine Liste der Indikatortypen und deren Formeln finden Sie im Abschnitt Indikatortypen des [Windows Server 2003 Deployment Kit.](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10))
-   **DefaultScale:** Die Standardskalierung, die auf die Rohdaten des Leistungsindikators angewendet werden soll.
-   **InstanceName:** Der Name der Indikatorinstanz.
-   **InstanceIndex:** Die Indexnummer der Indikatorinstanz.
-   **ParentName:** Einige Leistungsindikatoren sind logisch mit anderen verknüpft und werden als "Eltern" bezeichnet. Beispielsweise ist das übergeordnete Element eines Threads ein Prozess, und das übergeordnete Element eines logischen Datenträgertreibers ist ein physisches Laufwerk. Dieses Feld enthält den Namen des übergeordneten Elements. Entweder der Wert in diesem Feld oder das **ParentObjectID-Feld** identifiziert eine bestimmte übergeordnete Instanz. Wenn der Wert in diesem Feld **NULL** ist, muss der Wert im **ParentObjectID-Feld** überprüft werden, um das übergeordnete Element zu identifizieren. Wenn die Werte in beiden Feldern **NULL** sind, verfügt der Leistungsindikator nicht über ein übergeordnetes Element.
-   **ParentObjectID:** Der eindeutige Bezeichner des übergeordneten Elements. Der Wert in diesem Feld oder im **ParentName-Feld** identifiziert eine bestimmte übergeordnete Instanz. Wenn der Wert in diesem Feld **NULL** ist, muss der Wert im **Feld ParentName** überprüft werden, um das übergeordnete Element zu identifizieren.

 

 
