---
description: Mithilfe des Smartcard-Subsystems können Sie mit Karten kommunizieren, die möglicherweise nicht den ISO 7816-Spezifikationen entsprechen.
ms.assetid: ea6cfa5a-2abf-4b7f-b3f4-99655266f030
title: Direct Card Access Functions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d72b606cd766ea9a8930599bd2a44e117dea0bffdef6474c038b39294c08acf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008458"
---
# <a name="direct-card-access-functions"></a>Direct Card Access Functions

Mithilfe des [*Smartcard-Subsystems*](/windows/desktop/SecGloss/s-gly) können Sie mit Karten kommunizieren, die möglicherweise nicht den ISO 7816-Spezifikationen entsprechen. Zu diesem Ziel können Sie mit den folgenden Funktionen die Attribute der Kommunikation zwischen der Anwendung und der Karte steuern, indem Sie die direkte Bearbeitung des Readers auf niedriger Ebene [*ermöglichen.*](/windows/desktop/SecGloss/r-gly)

Um diese Funktionen verwenden zu können, müssen Sie einen Bezeichner für das in Frage stellende Attribut angeben. Gültige Attributbezeichner und -werte finden Sie in Tabelle 3-1 unter Anforderungen *für PC-Connected Interface Devices*.



| Thema                                    | BESCHREIBUNG                           |
|------------------------------------------|---------------------------------------|
| [**SCardControl**](/windows/desktop/api/Winscard/nf-winscard-scardcontrol)     | Bereitstellen der direkten Kontrolle über den Reader. |
| [**SCardGetAttrib**](/windows/desktop/api/Winscard/nf-winscard-scardgetattrib) | Erhalten von Readerattributen.                |
| [**SCardSetAttrib**](/windows/desktop/api/Winscard/nf-winscard-scardsetattrib) | Festlegen des Readerattributs.                 |



 

 

 
