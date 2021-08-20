---
description: Wenn zum Installieren eines Windows Installer-Pakets keine erhöhten Rechte erforderlich sind, kann der Autor des Pakets das Dialogfeld unterdrücken, das von der Benutzerkontensteuerung (User Account Control, UAC) angezeigt wird, um Benutzer zur Administratorautorisierung aufforderungen.
ms.assetid: cab30f95-cc93-46db-aba5-741b44adb6de
title: Erstellen von Paketen ohne das Dialogfeld "UAC"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5064589a49327db263158b10ff9377e0f7b69232b0e3679d5bd86c7bd2f2e3f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066090"
---
# <a name="authoring-packages-without-the-uac-dialog-box"></a>Erstellen von Paketen ohne das Dialogfeld "UAC"

Wenn zum Installieren eines Windows Installer-Pakets keine erhöhten Rechte erforderlich sind, kann der Autor des Pakets das Dialogfeld unterdrücken, das von der Benutzerkontensteuerung (User [*Account Control,*](u-gly.md) UAC) angezeigt wird, um Benutzer zur Administratorautorisierung aufforderungen.

Um die Anzeige des UAC-Dialogfelds bei der Installation der Anwendung zu unterdrücken, sollte der Autor des Pakets folgende Schritte unternehmen:

-   Installieren Sie die Anwendung mithilfe von Window Installer 4.0 oder höher auf Windows Vista.
-   Verwenden Sie keine erhöhten Systemberechtigungen, um die Anwendung auf dem Computer zu installieren.
-   Installieren Sie die Anwendung im Benutzerkontext, und machen Sie dies zum Standardinstallationskontext des Pakets. Wenn die [**ALLUSERS-Eigenschaft**](allusers.md) nicht festgelegt ist, installiert das Installationsprogramm das Paket im Kontext pro Benutzer. Wenn Sie die **ALLUSERS-Eigenschaft** nicht in die [Eigenschaftstabelle](property-table.md)setzen, wird diese Eigenschaft vom Installationsprogramm nicht festgelegt, sodass die benutzerspezifische Installation zum Standardinstallationskontext wird. Sie können diese Standardeinstellung überschreiben, indem Sie die **ALLUSERS-Eigenschaft** in der Befehlszeile festlegen.
-   Legen Sie Bit 3 in der [**Eigenschaft Zusammenfassung**](word-count-summary.md) der Wortanzahl fest, um anzugeben, dass zum Installieren der Anwendung keine erhöhten Berechtigungen erforderlich sind.

 

 



