---
description: Der Installer speichert alle Informationen über die Benutzeroberfläche in den Tabellen der-Installations Datenbank.
ms.assetid: 56d8ecb4-6c95-46c6-98dc-3118d2061101
title: Anzeigen der Vorschau der Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c58f30dcd797064ef9b01217927fda96a758f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216357"
---
# <a name="previewing-the-user-interface"></a>Anzeigen der Vorschau der Benutzeroberfläche

Der Installer speichert alle Informationen über die [Benutzeroberfläche](user-interface.md) in den Tabellen der-Installations Datenbank. Um das Design der Benutzeroberfläche zu vereinfachen, bietet das Installationsprogramm außerdem einen Vorschaumodus zum Anzeigen dieser Informationen. Im folgenden Verfahren wird beschrieben, wie Sie den UI-Vorschaumodus aktivieren und die aktuelle Darstellung von Dialogfeldern und Bildschirm anzeigen.

**So zeigen Sie die Benutzeroberfläche im Vorschaumodus an**

1.  Aktivieren Sie den Vorschaumodus, indem Sie die [**msienableuipreview**](/windows/desktop/api/Msiquery/nf-msiquery-msienableuipreview) -Funktion aufrufen.
2.  Zeigen Sie die einzelnen Dialogfelder an, indem Sie die [**msipreviewdialog**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewdialoga) -Funktion aufrufen.
3.  Zeigen Sie bestimmte Billboards an, indem Sie die [**msipreviewbillboard**](/windows/desktop/api/Msiquery/nf-msiquery-msipreviewbillboarda) -Funktion aufrufen.

 

 



