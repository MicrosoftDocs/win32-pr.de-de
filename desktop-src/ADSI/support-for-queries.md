---
title: Unterstützung für Abfragen
description: Durch Implementieren der idirector ysearch-Schnittstelle erhalten ADSI-Anbieter Zugriff auf eine Teilmenge OLE DB schreibgeschützten Features.
ms.assetid: 73ebed18-0e56-4902-a229-3b03f9be1cf6
ms.tgt_platform: multiple
keywords:
- Unterstützung für Abfragen ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1304dcabd9c008b0f645982e695554225f59bac9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337751"
---
# <a name="support-for-queries"></a>Unterstützung für Abfragen

Durch Implementieren der [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle erhalten ADSI-Anbieter Zugriff auf eine Teilmenge OLE DB schreibgeschützten Features.

Die ADSI-Implementierung der Methoden von [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) selbst verwendet die in ADSI Version 1,0 beschriebenen OLE DB Schnittstellen, einschließlich der folgenden COM-Objekte:

-   Datenquellen Objekt (Verzeichnisdienst), Unterstützung für **IDBInitialize**, **idbkreatesession**, **IDBProperties** und **ipersistent**.
-   Dbsessions-Objekt, Unterstützung für **IOpenRowset**, **ISessionProperties** und **ikreatecommand**.
-   Command-Objekt, Unterstützung für **ICommand**, **IAccessor**, **IColumnsInfo**, **ICommandProperties**, **ICommandText** und **IConvertType**.
-   Rowset-Objekt, unterstützender **IAccessor**, **IColumnsInfo**, **IConvertType**, **IRowset** und **IRowsetInfo**.

Weitere Informationen zu OLE DB finden Sie in der OLE DB Programmierer-Referenz im Platform Software Development Kit (SDK).

 

 




