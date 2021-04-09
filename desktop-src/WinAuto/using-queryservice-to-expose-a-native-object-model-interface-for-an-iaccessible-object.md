---
title: Verwenden von QueryService zum Abrufen einer systemeigenen Schnittstelle für ein IAccessible-Objekt
description: Server Entwickler können diese Technik verwenden, um einen Zeiger auf einen benutzerdefinierten Dokument Knoten für ein IAccessible-Objekt verfügbar zu machen. Dabei wird davon ausgegangen, dass Sie bereits IAccessible-Objekte verfügbar machen. Dieses Verfahren ermöglicht es Clients, ein benutzerdefiniertes Objekt von einem Objekt zu erhalten, das nicht zugänglich ist.
ms.assetid: aaa0e840-f8c2-4f3d-9d97-1910f00c1041
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d971462154eb12789a74e8cc6edb5aed68c84b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039286"
---
# <a name="use-queryservice-to-retrieve-a-native-interface-for-an-iaccessible-object"></a>Verwenden von QueryService zum Abrufen einer systemeigenen Schnittstelle für ein IAccessible-Objekt

Server Entwickler können diese Technik verwenden, um einen Zeiger auf einen benutzerdefinierten Dokument Knoten für ein [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt verfügbar zu machen. Dabei wird davon ausgegangen, dass Sie bereits **IAccessible** -Objekte verfügbar machen. Dieses Verfahren ermöglicht es Clients, ein benutzerdefiniertes Objekt von einem Objekt zu erhalten, das nicht **zugänglich** ist.

**So machen Sie ein System eigenes Objektmodell für eine IAccessible (Server) verfügbar**

1.  Fügen Sie Unterstützung für die **IServiceProvider** -Schnittstelle für Ihr [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt hinzu.
2.  Definieren Sie eine GUID, die die Funktionalität des Abrufens der benutzerdefinierten Schnittstelle von einem [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt darstellt. Dies wird als Dienst-ID bezeichnet. Sie können GUIDGEN.EXE verwenden, um eine Dienst-ID zu generieren oder die Schnittstellen-ID wiederzuverwenden, wenn Sie über eine benutzerdefinierte Schnittstelle verfügen.
3.  Implementieren Sie die **IServiceProvider:: QueryService** -Methode, sodass Sie einen Zeiger auf die benutzerdefinierte Schnittstelle zurückgibt, wenn Sie mit der zuvor in diesem Verfahren definierten Dienst-ID aufgerufen wird. **QueryService** sollte **null** für alle anderen Dienst-ID-Werte zurückgeben.
4.  Veröffentlichen Sie die Dienst-ID, damit Sie von Clients verwendet werden kann.

Clients können diese Funktion verwenden, um einen Zeiger auf das benutzerdefinierte Objekt aus einem Objekt zu erhalten, das nicht [**zugänglich**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ist.

**So rufen Sie einen Zeiger auf ein benutzerdefiniertes Objekt von einem IAccessible (Clients) ab**

1.  Rufen Sie [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))(IID \_ IServiceProvider) auf einem [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstellen Zeiger auf, um einen **IServiceProvider** -Schnittstellen Zeiger zu erhalten.
2.  Rufen Sie **IServiceProvider:: QueryService** mit der veröffentlichten Dienst-ID auf, um einen Zeiger auf das benutzerdefinierte Objekt für die [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)zu erhalten.
3.  Geben Sie die **IServiceProvider** -Schnittstelle frei, wenn Sie nicht mehr benötigt wird.

Um Prozess übergreifend verwendet werden zu können, müssen Server möglicherweise die zurückgegebene Schnittstelle mit Component Object Model (com) registrieren.

Diese Technik wird von Microsoft Internet Explorer 4,0 und höher verwendet. Sie ermöglicht Clients das Abrufen eines **IHTMLElement2** -Schnittstellen Zeigers, der einem [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt entspricht.

 

 