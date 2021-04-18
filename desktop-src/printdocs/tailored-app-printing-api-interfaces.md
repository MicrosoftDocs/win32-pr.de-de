---
description: Die folgenden Schnittstellen werden von einer App verwendet, um das Paket zum Drucken von Dokumenten zu verwalten.
ms.assetid: 576B4527-A753-4A73-899B-896DCB8B8945
title: API-Schnittstellen für Dokument Pakete drucken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adc495be5c58598d00250568ff852cf4f897e0b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351491"
---
# <a name="print-document-package-api-interfaces"></a>API-Schnittstellen für Dokument Pakete drucken

Die folgenden Schnittstellen werden von einer App verwendet, um das Paket zum Drucken von Dokumenten zu verwalten.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                                       | BESCHREIBUNG                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iprintdocumentpackagestatus-Ereignis**](/windows/desktop/api/Documenttarget/nn-documenttarget-iprintdocumentpackagestatusevent)<br/>     | Stellt den Status des Druckauftrags dar.<br/>                                                                                                                                                                        |
| [**Iprintdocumentpackagetarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)<br/>               | Ermöglicht es Benutzern, die unterstützten Paket Zieltypen aufzulisten und eine mit der angegebenen Typ-ID zu erstellen. **Iprintdocumentpackagetarget** unterstützt auch das Nachverfolgen des Paket Druck Fortschritts und das Abbrechen.<br/> |
| [**Iprintdocumentpackagetargetfactory**](/windows/desktop/api/documenttarget/nn-documenttarget-iprintdocumentpackagetargetfactory)<br/> | Wird mit [iprintdocumentpackagetarget](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) zum Starten eines Druckauftrags verwendet.<br/>                                                                                                               |



 

 

