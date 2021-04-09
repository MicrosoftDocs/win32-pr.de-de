---
title: Client Richtlinien
description: Client Entwickler sollten die folgenden Funktionen verwenden, um Informationen zu den Elementen der Benutzeroberfläche zu erhalten.
ms.assetid: 0e102e60-4d11-490e-88d5-dfadba620781
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ced411c24ed0b7aa3ab97cbe1ce2511d4e6b05
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "103948383"
---
# <a name="client-guidelines"></a>Client Richtlinien

Client Entwickler sollten die folgenden Funktionen verwenden, um Informationen zu den Elementen der Benutzeroberfläche zu erhalten:

-   Zum Abrufen einer [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Schnittstelle zu Objekten müssen Sie [**accessibleobjectfromwindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow), [**accessibleobjectfrompoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)oder [**accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)aufrufen.
-   Verwenden Sie die Eigenschaften und Methoden von [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , um barrierefreie Objekte zu überprüfen und zu bearbeiten.
-   Um [WinEvents](winevents-overview.md)zu empfangen, rufen Sie [**setwineventhook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) auf, um eine WinEvent-Rückruffunktion für die Ereignisse zu registrieren, die für die Client Anwendung relevant sind.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Abrufen von untergeordneten IDs durch Clients](how-clients-obtain-child-ids.md)

 

 




