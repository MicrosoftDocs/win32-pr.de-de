---
description: Benutzerdefinierte Aktionen werden auf die gleiche Weise wie Standardaktionen aufgerufen, entweder durch expliziten Aufruf oder während der Ausführung einer Sequenztabelle.
ms.assetid: 05f15bae-983a-4763-840d-f2590f4e2a7a
title: Aufrufen benutzerdefinierter Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba80afbd573ffb77fddb7723c433b7476055da2dc11deda39bb3cae4148b7f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629753"
---
# <a name="invoking-custom-actions"></a>Aufrufen benutzerdefinierter Aktionen

Benutzerdefinierte Aktionen werden auf die gleiche Weise wie Standardaktionen aufgerufen, entweder durch expliziten Aufruf oder während der Ausführung einer Sequenztabelle. Es gibt zwei Methoden zum Aufrufen von Aktionen:

-   Sie rufen die angegebene Aktion direkt mit der [**MsiDoAction-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) auf.
-   Eine Aktion der obersten Ebene ruft die Sequenztabelle auf, die die benutzerdefinierte Aktion enthält. Weitere Informationen zum Planen einer benutzerdefinierten Aktion in einer Sequenztabelle finden Sie unter [Sequenzieren von benutzerdefinierten Aktionen.](sequencing-custom-actions.md)

Wenn das Installationsprogramm einen Aktionsnamen aus der [**MsiDoAction-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) oder aus einer Sequenztabelle erhält, sucht es zunächst nach einer Standardaktion dieses Namens. Wenn die Standardaktion nicht gefunden werden kann, fragt das Installationsprogramm die [Tabelle CustomAction](customaction-table.md) ab, um zu überprüfen, ob es sich bei der angegebenen Aktion um eine benutzerdefinierte Aktion handelt. Wenn es sich bei der angegebenen Aktion nicht um eine benutzerdefinierte Aktion handelt, fragt das Installationsprogramm die [Tabelle Dialog](dialog-table.md) nach einem Dialogfeld ab.

 

 



