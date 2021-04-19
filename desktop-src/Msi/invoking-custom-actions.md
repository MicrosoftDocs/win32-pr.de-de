---
description: Benutzerdefinierte Aktionen werden auf die gleiche Weise wie Standard Aktionen aufgerufen, entweder durch expliziten Aufruf oder während der Ausführung einer Sequenz Tabelle.
ms.assetid: 05f15bae-983a-4763-840d-f2590f4e2a7a
title: Aufrufen von benutzerdefinierten Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02f1e9a575d32cbb8fe22323d4a741eb7936ef9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349681"
---
# <a name="invoking-custom-actions"></a>Aufrufen von benutzerdefinierten Aktionen

Benutzerdefinierte Aktionen werden auf die gleiche Weise wie Standard Aktionen aufgerufen, entweder durch expliziten Aufruf oder während der Ausführung einer Sequenz Tabelle. Es gibt zwei Methoden zum Aufrufen von Aktionen:

-   Die angegebene Aktion wird direkt mit der [**msidoaction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) -Funktion aufgerufen.
-   Durch eine Aktion der obersten Ebene wird die Sequenz Tabelle aufgerufen, die die benutzerdefinierte Aktion enthält. Weitere Informationen zum Planen einer benutzerdefinierten Aktion in einer Sequenz Tabelle finden Sie unter [Sequenzieren von benutzerdefinierten Aktionen](sequencing-custom-actions.md).

Wenn das Installationsprogramm einen Aktions Namen aus der [**msidoaction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) -Funktion oder aus einer Sequenz Tabelle erhält, sucht er zuerst nach einer Standardaktion mit diesem Namen. Wenn die Standardaktion nicht gefunden werden kann, fragt das Installationsprogramm die [Tabelle CustomAction](customaction-table.md) ab, um zu überprüfen, ob die angegebene Aktion eine benutzerdefinierte Aktion ist. Wenn es sich bei der angegebenen Aktion nicht um eine benutzerdefinierte Aktion handelt, fragt das Installationsprogramm die [Dialogfeld Tabelle](dialog-table.md) nach einem Dialogfeld ab.

 

 



