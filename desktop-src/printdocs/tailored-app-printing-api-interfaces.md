---
description: Die folgenden Schnittstellen werden von einer App zum Verwalten des Druckdokumentpakets verwendet.
ms.assetid: 576B4527-A753-4A73-899B-896DCB8B8945
title: Drucken von Dokumentpaket-API-Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc37fa31cbda1be6927cbb24bf4b5707d10d9f2d74ed152ef630a2ad6ed588c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118470122"
---
# <a name="print-document-package-api-interfaces"></a>Drucken von Dokumentpaket-API-Schnittstellen

Die folgenden Schnittstellen werden von einer App zum Verwalten des Druckdokumentpakets verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                       | BESCHREIBUNG                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintDocumentPackageStatusEvent**](/windows/desktop/api/Documenttarget/nn-documenttarget-iprintdocumentpackagestatusevent)<br/>     | Stellt den Fortschritt des Druckauftrags dar.<br/>                                                                                                                                                                        |
| [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)<br/>               | Ermöglicht Benutzern das Aufzählen der unterstützten Paketzieltypen und das Erstellen eines Pakets mit einer bestimmten Typ-ID. **IPrintDocumentPackageTarget unterstützt** auch die Nachverfolgung des Paketdruckfortschritts und des Abbruchs.<br/> |
| [**IPrintDocumentPackageTargetFactory**](/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetargetfactory)<br/> | Wird mit [IPrintDocumentPackageTarget zum Starten](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) eines Druckauftrags verwendet.<br/>                                                                                                               |



 

 

