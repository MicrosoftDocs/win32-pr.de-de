---
title: Unterstützung für Abfragen
description: Durch die Implementierung der IDirectorySearch-Schnittstelle erhalten ADSI-Anbieter Zugriff auf eine Teilmenge OLE DB schreibgeschützten Features.
ms.assetid: 73ebed18-0e56-4902-a229-3b03f9be1cf6
ms.tgt_platform: multiple
keywords:
- Unterstützung für Abfragen ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ad1892cf7c0e619ef55b9c3e5af6885d4cbdc7ac68fbcbd206524128b283d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023228"
---
# <a name="support-for-queries"></a>Unterstützung für Abfragen

Durch die Implementierung der [**IDirectorySearch-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) erhalten ADSI-Anbieter Zugriff auf eine Teilmenge OLE DB schreibgeschützten Features.

Die ADSI-Implementierung der Methoden von [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) selbst verwendet die OLE DB-Schnittstellen, die in ADSI Version 1.0 beschrieben sind, einschließlich der folgenden Liste von COM-Objekten:

-   Datenquellenobjekt (der Verzeichnisdienst), das **IDBInitialize,** **IDBCreateSession,** **IDBProperties** und **IPersist unterstützt.**
-   DBSessions-Objekt, das **IOpenRowSet,** **ISessionProperties** und **ICreateCommand unterstützt.**
-   Befehlsobjekt, das **ICommand,** **IAccessor,** **IColumnsInfo,** **ICommandProperties,** **ICommandText** und **IConvertType unterstützt.**
-   Rowsetobjekt, das **IAccessor,** **IColumnsInfo,** **IConvertType,** **IRowset** und **IRowsetInfo unterstützt.**

Weitere Informationen zu OLE DB finden Sie in der OLE DB-Programmiererreferenz im Platform Software Development Kit (SDK).

 

 




