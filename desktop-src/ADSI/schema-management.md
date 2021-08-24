---
title: Schemaverwaltung
description: Die ADSI-Beispielanbieterkomponente definiert die Schemaklassen \ 0034;Organisationseinheit \ 0034; und \ 0034; User \ 0034; und verwaltet diese Schemaklassen auf folgende Weise.
ms.assetid: c3e07846-a11e-46d4-9863-a89810896ad7
ms.tgt_platform: multiple
keywords:
- Schemaverwaltung ADSI
- Schemaverwaltung ADSI
- Verwalten von Schemas ADSI
- Schemas, Verwalten von ADSI
- Verwalten eines Schemas ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ddb8fcc3d29dce27ac2b74c9c8e79d1cef2f9d2a23307e9b7626861ed3e7dd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770485"
---
# <a name="schema-management"></a>Schemaverwaltung

Die ADSI-Beispielanbieterkomponente definiert die Schemaklassen "Organisationseinheit" und "Benutzer" und verwaltet diese Schemaklassen auf folgende Weise.

Die Schemaklasse "Organisationseinheit" wird durch ein ADs-Containerobjekt dargestellt und kann andere "Organisationseinheiten" und "Benutzer" enthalten. Das Containerobjekt unterstützt die Schnittstellen [**IUnknown,**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**IDispatch,**](/windows/win32/api/oaidl/nn-oaidl-idispatch) [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)und [**IADsContainer.**](/windows/desktop/api/Iads/nn-iads-iadscontainer) Die Schemaklasse "User" wird durch ein generisches Active Directory-Objekt dargestellt und enthält keine anderen Objekttypen. In der Beispielanbieterkomponente wird das User-Objekt als generisches Active Directory-Objekt implementiert, das die Schnittstellen **IUnknown,** **IDispatch** und **IADs unterstützt.** Beachten Sie, dass das User-Objekt in diesem Fall die [**IADsUser-Schnittstelle nicht**](/windows/desktop/api/Iads/nn-iads-iadsuser) unterstützt.

Die Beispielanbieterkomponente muss auch das ADs-Namespaceobjekt implementieren, das die Schnittstellen [**IUnknown,**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**IADs,**](/windows/desktop/api/Iads/nn-iads-iads) [**IADsContainer,**](/windows/desktop/api/Iads/nn-iads-iadscontainer) [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)und [**IDispatch unterstützt.**](/windows/win32/api/oaidl/nn-oaidl-idispatch)

Die folgende Abbildung zeigt die Details des Schemas, das die schema-Klassen der beiden Beispielanbieterkomponenten darstellt.

![Adsi-Beispiel für Das Komponentenschema des Anbieters](images/dssmsch.png)

Beachten Sie, dass in der obigen Abbildung die Schemaklasse "Organisationseinheit" drei Eigenschaften definiert: "Beschreibung", "Mitarbeiterzahl" und "ID". Die Schemaklasse "User" definiert vier Eigenschaften: "ID", "Name", "PhoneNumber" und "Title". Die "ID"-Eigenschaft wird von beiden Schemaklassen gemeinsam verwendet. Jede Eigenschaft wird entweder durch das Syntaxobjekt "String" oder "Integer" definiert.

> [!Note]  
> Syntaxobjekte sind in der ersten Version der Beispielanbieterkomponente nicht vorhanden. In den meisten Microsoft ADSI-Schemaimplementierungen sind die Syntaxobjekte jedoch im Schemacontainerobjekt enthalten, genau wie die Schemaklasse und die Eigenschaftenobjekte. Aus diesem Grund werden sie hier angezeigt.

 

Diese Anbieterkomponente ermöglicht der ADSI-Clientanwendung den Zugriff auf Schemadaten in Form von ADs-Klassenobjekten, ADs-Eigenschaftenobjekten und ADs-Syntaxobjekten innerhalb eines Schemaklassencontainerobjekts, sodass Schemadaten zur Laufzeit abgerufen werden können.

Die für die Beispielanbieterkomponente definierten ADsPaths für die Schemaklassencontainerobjekte sind "Sample://Seattle/schema" und "Sample://Toronto/schema". In diesem Beispiel sind die Inhalte der Schemas identisch.

 

 