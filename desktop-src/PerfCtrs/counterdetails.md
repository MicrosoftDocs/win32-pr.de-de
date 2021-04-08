---
description: In der Tabelle Counter Details wird ein bestimmter Indikator auf einem bestimmten Computer beschrieben.
ms.assetid: e2a16a6e-8cd4-4fd3-adeb-461faed948e4
title: Counter Details
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 751073cdc2f2646ad1f2351bff0bdc02c498d428
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959770"
---
# <a name="counterdetails"></a>Counter Details

In der Tabelle **Counter Details** wird ein bestimmter Indikator auf einem bestimmten Computer beschrieben.

Die Tabelle **Counter Details** definiert die folgenden Felder:

-   **Counter ID:** Ein eindeutiger Bezeichner in der Datenbank, der einer bestimmten Text Zeichenfolge für den Counter-Namen entspricht. Dieses Feld ist der Primärschlüssel dieser Tabelle.
-   **MachineName:** Der Name des Computers, von dem dieses DataSet protokolliert wurde.
-   **ObjectName:** Der Name des Leistungsobjekts.
-   **Counter Name:** Der Name des Zählers.
-   **CounterType:** Der zähtertyp. Eine Liste der-Typen und ihrer Formeln finden Sie im Abschnitt Counter Types des [Windows Server 2003 Deployment Kits](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)).
-   **DEFAULTSCALE:** Die Standard Skalierung, die auf die Rohdaten des Leistungs Zählers angewendet werden soll.
-   **InstanceName:** Der Name der Counter-Instanz.
-   **Instancin:** Die Indexnummer der Indikator Instanz.
-   **Name des Parametern:** Einige Leistungsindikatoren sind logisch mit anderen verknüpft und werden als übergeordnete Elemente bezeichnet. Beispielsweise ist das übergeordnete Element eines Threads ein Prozess, und das übergeordnete Element eines logischen Datenträger Treibers ist ein physisches Laufwerk. Dieses Feld enthält den Namen des übergeordneten Elements. Entweder der Wert in diesem Feld oder das Feld " **parametriobjectid** " identifiziert eine bestimmte übergeordnete Instanz. Wenn der Wert in diesem Feld **null** ist, muss der Wert im Feld " **parametriobjectid** " so geprüft werden, dass das übergeordnete Element identifiziert wird. Wenn die Werte in beiden Feldern **null** sind, verfügt der-Counter nicht über ein übergeordnetes Element.
-   **Parametriobjectid:** Der eindeutige Bezeichner des übergeordneten Elements. Der Wert in diesem Feld oder im Feld " **Parser Name** " identifiziert eine bestimmte übergeordnete Instanz. Wenn der Wert in diesem Feld **null** ist, muss der Wert im Feld "Element **Name** " geprüft werden, um das übergeordnete Element zu identifizieren.

 

 
