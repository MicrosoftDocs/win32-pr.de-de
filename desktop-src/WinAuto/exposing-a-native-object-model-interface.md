---
title: Verfügbar machen einer nativen Objektmodellschnittstelle
description: Wenn ein Benutzeroberflächenelement ein anderes natives Objektmodell als Microsoft Active Accessibility oder Benutzeroberflächenautomatisierung unterstützt, kann es die benutzerdefinierte Schnittstelle verfügbar machen, indem es auf WM GETOBJECT-Meldungen reagiert, die den \_ OBJID NATIVEOM-Objektbezeichner \_ enthalten.
ms.assetid: 430abeaf-e5ca-48c4-aa35-8d52a8cee2f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 701ed721e8259aa3b707fa1d7a6f2e80b9da13a3760b9850edef22b169d772e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644920"
---
# <a name="exposing-a-native-object-model-interface"></a>Verfügbar machen einer nativen Objektmodellschnittstelle

Wenn ein Benutzeroberflächenelement ein anderes natives Objektmodell als Microsoft Active Accessibility oder Benutzeroberflächenautomatisierung unterstützt, kann es die benutzerdefinierte Schnittstelle verfügbar machen, indem es auf [**WM \_ GETOBJECT-Nachrichten**](wm-getobject.md) reagiert, die den [**OBJID \_ NATIVEOM-Objektbezeichner**](object-identifiers.md) enthalten. Um zu antworten, sollte das Benutzeroberflächenelement den Wert zurückgeben, der durch einen Aufruf der [**LresultFromObject-Funktion abgerufen**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) wurde.

Ein Client kann eine Schnittstelle aus einem Benutzeroberflächenelement abrufen, das ein natives Objektmodell unterstützt, indem er die [**AccessibleObjectFromWindow-Funktion**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) aufruft und [**OBJID \_ NATIVEOM**](object-identifiers.md) als zweiten Parameter angibt.

 

 




