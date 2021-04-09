---
title: Fensterlose Rich Edit-Steuerelemente
description: Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit fensterlosen Bearbeitungs Steuerelementen verwendet werden.
ms.assetid: vs|controls|~\controls\richedit\windowlessricheditcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0431c5cb513aff003098e3d022fe73c6b6d83e9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036566"
---
# <a name="windowless-rich-edit-controls"></a>Fensterlose Rich Edit-Steuerelemente

Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit fensterlosen Bearbeitungs Steuerelementen verwendet werden. Der Component Object Model (com) definiert einen Satz von Schnittstellen, um fensterlose Objekte zu unterstützen. Fensterlose Objekte können den direkt aktiven Zustand ohne eigenes Fenster eingeben, sondern das Fenster des Containers verwenden. Folglich verwendet ein fensterloses Objekt weniger Systemressourcen und bietet eine bessere Leistung durch schnellere Aktivierung und Aktivierung. Außerdem können fensterlose Objekte nicht rechteckig und transparent sein.

### <a name="overviews"></a>Übersichten



| Thema                                                                          | Inhalte                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu fensterlosen Bearbeitungs Steuerelementen](about-windowless-rich-edit-controls.md) | Ein fensterloses Rich Edit-Steuerelement, das auch als Text Dienste-Objekt bezeichnet wird, ist ein Objekt, das die Funktionalität eines [Rich-Edit-Steuer](rich-edit-controls.md) Elements bereitstellt, ohne das Fenster bereitzustellen.<br/> |



 

### <a name="functions"></a>Functions



| Thema                                            | Inhalte                                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Kreatetextservices"**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) | Die Funktion " [**kreatetextservices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) " erstellt eine Instanz eines Text Dienst Objekts. Das Text Services-Objekt unterstützt eine Vielzahl von Schnittstellen, einschließlich [**itextservices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) und dem Textobjekt Modell (Tom).<br/> |



 

### <a name="interfaces"></a>Schnittstellen



| Thema                                  | Inhalte                                                                                                                |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Itexthost**](/windows/desktop/api/Textserv/nl-textserv-itexthost)         | Die [**itexthost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) -Schnittstelle wird von einem Text Dienst Objekt zum Abrufen von Text Host Diensten verwendet.<br/> |
| [**Itextservices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) | Erweitert den Tom, um zusätzliche Funktionen für den fensterlosen Betrieb bereitzustellen.<br/>                                     |



 

 

 





