---
title: Verwenden von QueryService zum Abrufen einer nativen Schnittstelle für ein IAccessible-Objekt
description: Serverentwickler können dieses Verfahren verwenden, um einen Zeiger auf einen benutzerdefinierten Dokumentknoten für ein IAccessible-Objekt verfügbar zu machen. Dabei wird davon ausgegangen, dass Sie IAccessible-Objekte bereits verfügbar machen. Mit dieser Technik können Clients ein benutzerdefiniertes Objekt aus einem IAccessible-Objekt abrufen.
ms.assetid: aaa0e840-f8c2-4f3d-9d97-1910f00c1041
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22c55e503bdda05692b13548d2d63eaeb3246562b4f4e8fc1e8645d25941a7f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098070"
---
# <a name="use-queryservice-to-retrieve-a-native-interface-for-an-iaccessible-object"></a>Verwenden von QueryService zum Abrufen einer nativen Schnittstelle für ein IAccessible-Objekt

Serverentwickler können dieses Verfahren verwenden, um einen Zeiger auf einen benutzerdefinierten Dokumentknoten für ein [**IAccessible-Objekt**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) verfügbar zu machen. Dabei wird davon ausgegangen, dass Sie **IAccessible-Objekte** bereits verfügbar machen. Mit dieser Technik können Clients ein benutzerdefiniertes Objekt aus einem **IAccessible-Objekt** abrufen.

**So machen Sie ein systemeigenes Objektmodell für IAccessible (Server) verfügbar**

1.  Fügen Sie Unterstützung für die **IServiceProvider-Schnittstelle** für Ihr [**IAccessible-Objekt**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) hinzu.
2.  Definieren Sie eine GUID, die die Funktionalität des Abrufens der benutzerdefinierten Schnittstelle aus einem [**IAccessible-Objekt**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) darstellt. Dies wird als Dienst-ID bezeichnet. Sie können GUIDGEN.EXE verwenden, um eine Dienst-ID zu generieren, oder die Schnittstellen-ID wiederverwenden, wenn Sie über eine benutzerdefinierte Schnittstelle verfügen.
3.  Implementieren Sie die **IServiceProvider::QueryService-Methode,** sodass sie einen Zeiger auf die benutzerdefinierte Schnittstelle zurückgibt, wenn sie mit der zuvor in dieser Prozedur definierten Dienst-ID aufgerufen wird. **QueryService** sollte **NULL** für alle anderen Dienst-ID-Werte zurückgeben.
4.  Veröffentlichen Sie die Dienst-ID, damit Clients sie verwenden können.

Clients können diese Funktion verwenden, um einen Zeiger auf das benutzerdefinierte Objekt aus einem [**IAccessible-Objekt**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) abzurufen.

**So rufen Sie einen Zeiger auf ein benutzerdefiniertes Objekt von einem IAccessible -Objekt (Clients) ab**

1.  Rufen Sie [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))(IID \_ IServiceProvider) für einen [**IAccessible-Schnittstellenzeiger**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) auf, um einen **IServiceProvider-Schnittstellenzeiger** abzurufen.
2.  Rufen Sie **IServiceProvider::QueryService** mit der veröffentlichten Dienst-ID auf, um einen Zeiger auf das benutzerdefinierte Objekt für [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)abzurufen.
3.  Geben Sie die **IServiceProvider-Schnittstelle** frei, wenn sie nicht mehr benötigt wird.

Um prozessübergreifend verwendet werden zu können, müssen Server möglicherweise die zurückgegebene Schnittstelle bei Component Object Model (COM) registrieren.

Dieses Verfahren wird von Microsoft Internet Explorer 4.0 und höher verwendet. Clients können einen **IHTMLElement2-Schnittstellenzeiger** abrufen, der einem [**IAccessible-Objekt**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) entspricht.

 

 