---
title: CENUMOBJ. Cpp
description: In der Beispielanbieterkomponente verwendet die Enumeration eines Containerobjekts die Routinen aus cenumobj.cpp, die in der folgenden Tabelle aufgeführt sind.
ms.assetid: 7166230d-0bf8-4f7d-9781-72f125a3dd21
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fad1e91a58080dc11f7d8da11f3e3fd59dc2ce75431ee2998d8d4e11011bbb32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023678"
---
# <a name="cenumobjcpp"></a>CENUMOBJ. Cpp

In der Beispielanbieterkomponente verwendet die Enumeration eines Containerobjekts die Routinen aus cenumobj.cpp, die in der folgenden Tabelle aufgeführt sind.



| Methode                                                 | BESCHREIBUNG                                                                                                                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CSampleDSGenObjectEnum::Create**                     | Erstellen Sie ein -Objekt, um die Enumeration generischer Active Directory-Objekte zu aktivieren.                                                                                           |
| **CSampleDSGenObjectEnum::CSampleDSGenObjectEnum**     | Initialisierung.                                                                                                                                                       |
| **CSampleDSGenObjectEnum::EnumGenericObjects**         | Verwalten des Abrufens von Objekten.                                                                                                                                          |
| **CSampleDSGenObjectEnum::FetchObjects**               | Ruft den Satz von [**IDispatch-Zeigern**](/windows/win32/api/oaidl/nn-oaidl-idispatch) ab, die mit dem Filter übereinstimmen.                                                             |
| **CSampleDSGenObjectEnum::FetchNextObject**            | Rufen Sie ein Objekt ab, und stimmen Sie mit dem Filter überein. Wenn eine Übereinstimmung vorüber ist, umschließen Sie sie in einem generischen Objekt, und geben Sie einen [**IDispatch-Zeiger**](/windows/win32/api/oaidl/nn-oaidl-idispatch) zurück. |
| **CSampleDSGenObjectEnum::EnumGenericObjects**         | Verwalten sie das Abrufen der Objekte.                                                                                                                                        |
| **CSampleDSGenObjectEnum::Next**                       | Rufen Sie die angegebene Anzahl von Elementen aus dem angegebenen Enumerationsobjekt ab.                                                                                      |
| **CSampleDSGenObjectEnum::IsValidDSFilter**            | Stellen Sie sicher, dass die Objektklasse mit einer in der Filterliste entspricht.                                                                                                              |
| **CSampleDSGenObjectEnum::BuildDSFilterArray**         | Verwalten Sie das Filterarray.                                                                                                                                              |
| **CSampleDSGenObjectEnum::CreateAndAppendFilterEntry** | Fügen Sie dem Filter eine neue Objektklasse hinzu, und legen Sie den Filter als zusammenhängend fest.                                                                                                |
| **FreeFilterList**                                     | Geben Sie den Filter frei.                                                                                                                                                      |



 

 

 