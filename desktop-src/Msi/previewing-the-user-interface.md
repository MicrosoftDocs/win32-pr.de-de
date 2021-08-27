---
description: Das Installationsprogramm speichert alle Informationen zur Benutzeroberfläche in den Tabellen der Installationsdatenbank.
ms.assetid: 56d8ecb4-6c95-46c6-98dc-3118d2061101
title: Vorschau des Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738387ac834d4e9c26f4a413755dce0c5abdc5e421cc4ef88b1f9b41054f201d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082660"
---
# <a name="previewing-the-user-interface"></a>Vorschau des Benutzeroberfläche

Das Installationsprogramm speichert alle Informationen zur [Benutzeroberfläche](user-interface.md) in den Tabellen der Installationsdatenbank. Um den Entwurf der Benutzeroberfläche zu vereinfachen, stellt das Installationsprogramm auch einen Vorschaumodus zum Anzeigen dieser Informationen zur Verfügung. Im folgenden Verfahren wird beschrieben, wie Sie den Vorschaumodus der Benutzeroberfläche aktivieren und die aktuelle Darstellung von Dialogfeldern und Feldern anzeigen.

**So zeigen Sie die Benutzeroberfläche im Vorschaumodus an**

1.  Aktivieren Sie den Vorschaumodus, indem Sie die [**MsiEnableUIPreview-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview) aufrufen.
2.  Zeigen Sie die jeweiligen Dialogfelder an, indem Sie die [**MsiPreviewDialog-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga) aufrufen.
3.  Zeigen Sie bestimmte Tafeln an, indem Sie die [**MsiPreviewBillboard-Funktion**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) aufrufen.

 

 



