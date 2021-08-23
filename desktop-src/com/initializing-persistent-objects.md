---
title: Initialisieren persistenter Objekte
description: Initialisieren persistenter Objekte
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee98b01c6c9eab28f8f96f98ea1a2980c9eb5d10988c2efbe495a920c98c51e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756180"
---
# <a name="initializing-persistent-objects"></a>Initialisieren persistenter Objekte

Einige der persistenten Objektschnittstellen [**IPersistStreamInit,**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) [**IPersistStorage,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))und [IPersistPropertyBag](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)ermöglichen Clients das Initialisieren von Objekten in den Zustand "fresh" oder "default". Dieser anfängliche Zustand unterscheidet sich von dem eines neu erstellten -Objekts, das keinen Zustand hat.

Das Initialisieren des Zustands eines Objekts, auch im Standardzustand, kann ein rechen- oder ressourcenintensiver Vorgang sein. Durch die Trennung der Erstellung von der Initialisierung kann die Initialisierung nur ausgeführt werden, wenn sie tatsächlich benötigt wird, und Clients können das Initialisieren von Objekten in den Standardzustand nur vermeiden, um zuvor gespeicherte Daten sofort zu laden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Persistente Objektschnittstellen](persistent-object-interfaces.md)
</dt> </dl>

 

 