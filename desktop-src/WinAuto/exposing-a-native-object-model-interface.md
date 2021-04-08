---
title: Verfügbar machen einer systemeigenen Objektmodell Schnittstelle
description: Wenn ein Benutzeroberflächen Element ein anderes System eigenes Objektmodell als Microsoft Active Accessibility oder eine Benutzeroberflächen Automatisierung unterstützt, kann es die benutzerdefinierte Schnittstelle verfügbar machen, indem auf die WM- \_ GetObject-Nachrichten reagiert wird, die den objID \_ nativeom-Objekt
ms.assetid: 430abeaf-e5ca-48c4-aa35-8d52a8cee2f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e52543908e89a1cea57c981d60bf7cb2b9fbd1fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037192"
---
# <a name="exposing-a-native-object-model-interface"></a>Verfügbar machen einer systemeigenen Objektmodell Schnittstelle

Wenn ein Benutzeroberflächen Element ein anderes System eigenes Objektmodell als Microsoft Active Accessibility oder eine Benutzeroberflächen Automatisierung unterstützt, kann es die benutzerdefinierte Schnittstelle verfügbar machen, indem auf die [**WM- \_ GetObject**](wm-getobject.md) -Nachrichten reagiert wird, die den [**objID \_ nativeom**](object-identifiers.md) -Objekt Um zu reagieren, sollte das UI-Element den Wert zurückgeben, der durch einen aufgerufenen der [**lresultfrobobject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) -Funktion abgerufen wird.

Ein Client kann eine Schnittstelle von einem Benutzeroberflächen Element abrufen, das ein System eigenes Objektmodell unterstützt, indem die [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) -Funktion aufgerufen und [**objID \_ nativeom**](object-identifiers.md) als zweiter Parameter angegeben wird.

 

 




