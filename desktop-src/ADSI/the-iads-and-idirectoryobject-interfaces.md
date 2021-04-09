---
title: IADs und IDirectoryObject-Schnittstellen
description: ADSI-Clients verwalten und bearbeiten Verzeichnisdienst Objekte mithilfe einer der beiden com-Schnittstellen IADs oder IDirectoryObject.
ms.assetid: f9c486b0-3dfb-4abf-afbf-08749e04315f
ms.tgt_platform: multiple
keywords:
- IADs ADSI, Informationen zu
- IDirectoryObject ADSI, Informationen zu
- ADSI ADSI, using, IADs und IDirectoryObject-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32dfef47fe1c66e4303725deecec14fe93d1fd92
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103858476"
---
# <a name="the-iads-and-idirectoryobject-interfaces"></a>IADs und IDirectoryObject-Schnittstellen

ADSI-Clients verwalten und bearbeiten Verzeichnisdienst Objekte mithilfe einer von zwei COM-Schnittstellen: [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) oder [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject). **IADs** ist eine [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle, die von spät gebundenen Clients verwendet werden soll, wie z. b. in Microsoft Visual Basic, Java und verschiedenen Skriptsprachen. **IDirectoryObject** ist eine Vtable-Schnittstelle, die über früh gebundene Clients (z. b. in C und C++ geschriebene) direkten Zugriff auf Objekte bereitstellt.

Jedes ADSI-Objekt muss sowohl [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) als auch [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)implementieren. In Sprachen wie z. b. C oder C++ geschriebene ADSI-Clients, die direkt auf vtables zugreifen können, können beide Schnittstellen verwenden, aber nicht beides in derselben Anwendung. In Visual Basic oder Java geschriebene ADSI-Clients sind auf die Verwendung von **IADs** beschränkt.

Mithilfe der [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) -Schnittstelle können spät gebundene Clients die inhärenten Funktionen für die Unterbrechung des ADSI-Objektmodells nutzen. Zu diesen Features gehört der Eigenschafts Cache, der es Clients ermöglicht, Eigenschaften zu lesen und zu schreiben, ohne die Übertragung für jeden-Befehl durchlaufen zu müssen. Außerdem erhalten Client Anwendungen die Verwendung leistungsfähiger UI-und ActiveX-Steuerelement Bibliotheken und einen einfacheren Programmierstil. In der Rückgabe müssen spät gebundene Clients den **Variant** -Datentyp verwenden, der die Verwendung der umfassenderen systemeigenen Datentypen von ADSI ausschließt.

Mithilfe der [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) -Schnittstelle können früh gebundene Clients die Vorteile der systemeigenen Verzeichnisdienst Datentypen nutzen, wenn ein geringfügiger Leistungsvorteil durch die Verwendung des Eigenschafts Caches verursacht wird. In der Rückgabe bietet die **IDirectoryObject** -Schnittstelle direkten Netzwerk Zugriff auf Objekteigenschaften über eine einzelne Anforderung anstelle von einzelnen **Get** -und **Put** -aufrufen.

 

 