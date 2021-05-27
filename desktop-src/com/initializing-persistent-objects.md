---
title: Initialisieren persistenter Objekte
description: Initialisieren persistenter Objekte
ms.assetid: 790cf133-ce86-4d02-b177-a538b4ee3f8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29bcb32bc049b5e0d5c2dab13e5ded6a743957e
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549196"
---
# <a name="initializing-persistent-objects"></a>Initialisieren persistenter Objekte

Einige der persistenten [**Objektschnittstellen, IPersistStreamInit,**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) [**IPersistStorage,**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage) [IPersistMemory](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85))und [IPersistPropertyBag,](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)ermöglichen Clients das Initialisieren von Objekten in einen "fresh"- oder "default"-Zustand. Dieser Anfangszustand ist anders als bei einem neu erstellten Objekt, das keinen Zustand auf hat.

Das Initialisieren des Zustands eines Objekts, selbst in den Standardzustand, kann ein rechen- oder ressourcenintensiver Vorgang sein. Durch die Trennung der Erstellung von der Initialisierung kann die Initialisierung nur ausgeführt werden, wenn sie tatsächlich benötigt wird, und Clients können das Initialisieren von Objekten in den Standardzustand vermeiden, um zuvor gespeicherte Daten sofort zu laden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Persistente Objektschnittstellen](persistent-object-interfaces.md)
</dt> </dl>

 

 