---
title: Schema Verwaltung
description: Die ADSI-Beispiel Anbieter Komponente definiert die Schema Klassen \ 0034; Organisationseinheit \ 0034; und \ 0034; Benutzer \ 0034; und verwaltet diese Schema Klassen auf folgende Weise.
ms.assetid: c3e07846-a11e-46d4-9863-a89810896ad7
ms.tgt_platform: multiple
keywords:
- Schema Verwaltung ADSI
- Schema Verwaltung ADSI
- Verwalten von Schemas ADSI
- Schemas, Verwalten von ADSI
- Verwalten eines Schema-ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d398f8eb056498977f886e836c0f97c95f0b9b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104556703"
---
# <a name="schema-management"></a>Schema Verwaltung

Die ADSI-Beispiel Anbieter Komponente definiert die Schema Klassen "Organisationseinheit" und "Benutzer" und verwaltet diese Schema Klassen wie folgt.

Die Schema Klasse "Organisationseinheit" wird durch ein ADS-Container Objekt dargestellt und kann andere "Organisationseinheiten" und "Benutzer" enthalten. Das Container Objekt unterstützt die Schnittstellen [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)und [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer). Die Schema Klasse "User" wird durch ein generisches Active Directory Objekt dargestellt und enthält keine anderen Typen von Objekten. In der Beispiel Anbieter Komponente wird das User-Objekt als generisches Active Directory Objekt implementiert, das die Schnittstellen **IUnknown**, **IDispatch** und **IADs** unterstützt. Beachten Sie, dass das Benutzerobjekt, in diesem Fall, die [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) -Schnittstelle nicht unterstützt.

Die Beispiel Anbieter Komponente muss auch das ADS-Namespace Objekt implementieren, das die Schnittstellen [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**iadsopendsobject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)und [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)unterstützt.

In der folgenden Abbildung werden die Details des Schemas veranschaulicht, das die beiden Beispiel Schema Klassen für Anbieter Komponenten darstellt.

![ADSI-Beispiel Anbieter-Komponenten Schema](images/dssmsch.png)

Beachten Sie, dass in der obigen Abbildung die Schema Klasse "Organisationseinheit" drei Eigenschaften definiert: "Description", "Headcounts" und "ID". Die Schema Klasse "User" definiert vier Eigenschaften: "ID", "Name", "PhoneNumber" und "Title". Die "ID"-Eigenschaft wird von beiden Schema Klassen gemeinsam verwendet. Jede Eigenschaft wird entweder durch das Zeichen "String" oder das "Integer"-Syntax Objekt definiert.

> [!Note]  
> Syntax Objekte sind nicht in der ersten Version der Beispiel Anbieter Komponente vorhanden. In den meisten Microsoft ADSI-Schema Implementierungen sind die Syntax Objekte jedoch im Schema Container Objekt enthalten, genauso wie die Schema Klasse und die Eigenschafts Objekte. Aus diesem Grund werden Sie hier angezeigt.

 

Diese Anbieter Komponente macht Schema Daten für die ADSI-Client Anwendung in Form von ADS-Klassen Objekten, ADS-Eigenschafts Objekten und ADS-Syntax Objekten verfügbar, sodass Schema Daten zur Laufzeit abgerufen werden können.

Die für die Beispiel Anbieter Komponente definierten adspaths für die Schema Klassen-Containerobjekte sind "Sample://Seattle/Schema" und "Sample://Toronto/Schema". In diesem Beispiel sind die Inhalte der Schemas identisch.

 

 