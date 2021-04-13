---
title: Initialisieren von persistenten Objekten
description: Initialisieren von persistenten Objekten
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 211d9d89b7a8f36ab06d9930e45f365e0fb5d4dc
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104391058"
---
# <a name="initializing-persistent-objects"></a>Initialisieren von persistenten Objekten

Einige der persistenten Objekt Schnittstellen ( [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [ipersistmemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))und [IPersistPropertyBag](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85))) ermöglichen Clients die Initialisierung von Objekten mit dem Zustand "neu" oder "Standard". Dieser Anfangszustand unterscheidet sich von dem eines neu erstellten Objekts, das keinen Status aufweist.

Die Initialisierung des Zustands eines Objekts, auch im Standardzustand, kann ein Rechen intensiver oder ressourcenintensiver Vorgang sein. Durch die Trennung der Erstellung von der Initialisierung kann die Initialisierung nur ausgeführt werden, wenn Sie tatsächlich benötigt wird. Clients können die Initialisierung von Objekten nur im Standardzustand vermeiden, um zuvor gespeicherte Daten sofort zu laden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Persistente Objekt Schnittstellen](persistent-object-interfaces.md)
</dt> </dl>

 

 