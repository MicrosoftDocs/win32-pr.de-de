---
title: Serverrichtlinien
description: Damit Microsoft Active Accessibility wie vorgesehen funktionieren, müssen Server Informationen zur Barrierefreiheit für Clients bereitstellen.
ms.assetid: 88be4bae-fdeb-467c-b5b1-19f2adc0575d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b92d70a33dc8d397ff84fc3b9901dba044741d3044f6a7b7f6d1226aa5b683
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119614550"
---
# <a name="server-guidelines"></a>Serverrichtlinien

Damit Microsoft Active Accessibility wie vorgesehen funktionieren, müssen Server Informationen zur Barrierefreiheit für Clients bereitstellen.

Um [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)zu implementieren, müssen Serverentwickler diesen grundlegenden Prozess befolgen.

1.  Erstellen Sie barrierefreie Objekte, indem Sie die [**IAccessible-Eigenschaften**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) und -Methoden für Ihre benutzerdefinierten Benutzeroberflächenelemente und für den Client Ihrer Anwendung implementieren. Stellen Sie sicher, dass Sie eine duale Schnittstelle bereitstellen, die sowohl **IAccessible** als auch [**IDispatch**](idispatch-interface.md) unterstützt, damit Clients, die in Microsoft Visual Basic und verschiedenen Skriptsprachen geschrieben wurden, Informationen zu den Objekten abrufen können.
2.  Rufen Sie [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) auf, um Clients über Änderungen an Ihren benutzerdefinierten Benutzeroberflächenelementen zu benachrichtigen.
3.  Behandeln Sie [**WM \_ GETOBJECT,**](wm-getobject.md) um Zugriff auf Ihre barrierefreien Objekte bereitzustellen.

Vorschläge und Richtlinien zum Entwerfen barrierefreier Objekte finden Sie im [Entwicklerhandbuch für Active Accessibility Server.](developer-s-guide-for-active-accessibility-servers.md)

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Implementieren untergeordneter IDs durch Server](how-servers-implement-child-ids.md)

 

 




