---
title: Fensterlose Rich Edit-Steuerelemente
description: Dieser Abschnitt enthält Informationen zu den Programmierelementen, die mit fensterlosen Rich-Edit-Steuerelementen verwendet werden.
ms.assetid: vs|controls|~\controls\richedit\windowlessricheditcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d03cbc4c694ce8e10a5b877298f148cd9ac47bd24c364aa3cde7fc19bc994e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655790"
---
# <a name="windowless-rich-edit-controls"></a>Fensterlose Rich Edit-Steuerelemente

Dieser Abschnitt enthält Informationen zu den Programmierelementen, die mit fensterlosen Rich-Edit-Steuerelementen verwendet werden. Der Component Object Model (COM) definiert einen Satz von Schnittstellen, um fensterlose Objekte zu unterstützen. Fensterlose Objekte können in den aktiven Zustand "In-Place" gelangen, ohne ein eigenes Fenster zu haben, sondern stattdessen das Fenster ihres Containers zu verwenden. Folglich verwendet ein fensterloses Objekt weniger Systemressourcen und bietet eine bessere Leistung durch schnellere Aktivierung und Deaktivierung. Darüber hinaus können fensterlose Objekte nichtrectangular und transparent sein.

### <a name="overviews"></a>Übersichten



| Thema                                                                          | Inhalte                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu fensterlosen Rich Edit-Steuerelementen](about-windowless-rich-edit-controls.md) | Ein fensterloses Rich Edit-Steuerelement, auch als Textdienstobjekt bezeichnet, ist [](rich-edit-controls.md) ein Objekt, das die Funktionalität eines rich-Bearbeitungssteuerfelds ohne Angabe des Fensters bietet.<br/> |



 

### <a name="functions"></a>Functions



| Thema                                            | Inhalte                                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) | Die [**CreateTextServices-Funktion**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) erstellt eine Instanz eines Textdienstobjekts. Das Textdienstobjekt unterstützt eine Vielzahl von Schnittstellen, einschließlich [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) und dem Textobjektmodell (Text Object Model, TOM).<br/> |



 

### <a name="interfaces"></a>Schnittstellen



| Thema                                  | Inhalte                                                                                                                |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost)         | Die [**ITextHost-Schnittstelle**](/windows/desktop/api/Textserv/nl-textserv-itexthost) wird von einem Textdienstobjekt verwendet, um Texthostdienste zu erhalten.<br/> |
| [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) | Erweitert das TOM, um zusätzliche Funktionen für den fensterlosen Betrieb zu bieten.<br/>                                     |



 

 

 





