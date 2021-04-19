---
description: Die Dokument Schnittstellen ermöglichen den Zugriff auf die XPS-Paket Komponenten, die die Struktur eines Dokuments in einem XPS-OM bestimmen.
ms.assetid: 3302d164-81ad-4198-a116-f967e7a14147
title: XPS-OM-Dokument Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc191c4c0b8ec5571331022321a8ae829587022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348902"
---
# <a name="xps-om-document-interfaces"></a>XPS-OM-Dokument Schnittstellen

Die Dokument Schnittstellen ermöglichen den Zugriff auf die XPS-Paket Komponenten, die die Struktur eines Dokuments in einem XPS-OM bestimmen. In der folgenden Tabelle sind die Dokument Schnittstellen aufgeführt.



| Schnittstellen Name                                                      | Logische untergeordnete Schnittstellen                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ixpsomdocumentsequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)<br/> | [**Ixpsomdocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>           | Stellt einen Satz von Dokumenten dar, die in einer geordneten Liste verknüpft sind.<br/> Untergeordnete Schnittstellen werden in einer [**ixpsomdocumentcollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection) -Schnittstelle erfasst.<br/>                                                                                                                                                                                                  |
| [**Ixpsomdocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)<br/>                 | [**Ixpsompagereferenzierung**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/> | Stellt einen einzelnen FixedDocument-Teil dar und bindet die Auflistung der Seiten Verweise der Seiten in einem Dokument.<br/> Untergeordnete Schnittstellen werden in einer [**ixpsompagereferencecollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection) -Schnittstelle erfasst.<br/> Die Dokumentstruktur wird in einer [**ixpsomdocumentstructureresource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource) -Schnittstelle verfügbar gemacht.<br/> |
| [**Ixpsompagereferenzierung**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)<br/>       | [**Ixpsompage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)<br/>                   | Eine leichte, virtualisierte Version einer Seite im Dokument. Ein Seiten Verweis beschreibt die Hauptmerkmale der Seite (z. b. die Dimensionen), enthält jedoch keinen Inhalt der Seite.<br/>                                                                                                                                                                                             |
| [**Ixpsomnamecollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)<br/>     | Keine<br/>                                               | Eine Auflistung der Objekte der Seite, die Hyperlink-Ziele sind.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**Ixpsomparametresources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)<br/>       | Keine<br/>                                               | Eine Auflistung der Teile Ressourcen, die einer Seite zugeordnet sind.<br/>                                                                                                                                                                                                                                                                                                                                |



 

## <a name="contents"></a>Inhalte

-   Das [Arbeiten mit ixpsomdocumentsequence-Schnittstellen](working-with-xpsomdocumentsequence-interfaces.md) enthält Informationen zur Verwendung der folgenden Schnittstellen:
    -   [**Ixpsomdocumentsequence**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentsequence)
    -   [**Ixpsomdocumentcollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentcollection)
-   Das [Arbeiten mit ixpsomdocument-Schnittstellen](working-with-xpsomdocument-interfaces.md) enthält Informationen zur Verwendung der folgenden Schnittstellen:
    -   [**Ixpsomdocument**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocument)
    -   [**Ixpsompagereferencecollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereferencecollection)
    -   [**Ixpsomdocumentstructureresource**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdocumentstructureresource)
-   [Beim Arbeiten mit ixpsompagereferenzierungsschnittstellen](working-with-xpsompagereference-interfaces.md) finden Sie Informationen zur Verwendung der folgenden Schnittstellen:
    -   [**Ixpsompagereferenzierung**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompagereference)
    -   [**Ixpsompage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
    -   [**Ixpsomnamecollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomnamecollection)
    -   [**Ixpsomparametresources**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompartresources)

 

 




