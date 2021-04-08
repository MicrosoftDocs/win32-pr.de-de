---
description: Wenn für die Installation eines Windows Installer Pakets erweiterte Berechtigungen nicht erforderlich sind, kann der Autor des Pakets das von der Benutzerkontensteuerung (User Account Control, UAC) angeforderte Dialogfeld unterdrücken, um Benutzer zur Autorisierung von Administratoren aufzufordern.
ms.assetid: cab30f95-cc93-46db-aba5-741b44adb6de
title: Erstellen von Paketen ohne das UAC-Dialog Feld
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dcd44bf7d2250e12e7cafde46b57978b48cceb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756229"
---
# <a name="authoring-packages-without-the-uac-dialog-box"></a>Erstellen von Paketen ohne das UAC-Dialog Feld

Wenn für die Installation eines Windows Installer Pakets erweiterte Berechtigungen nicht erforderlich sind, kann der Autor des Pakets das von der [*Benutzerkontensteuerung (User Account Control*](u-gly.md) , UAC) angeforderte Dialogfeld unterdrücken, um Benutzer zur Autorisierung von Administratoren aufzufordern.

Um die Anzeige des Dialog Felds UAC bei der Installation der Anwendung zu unterdrücken, sollte der Autor des Pakets folgende Aktionen ausführen:

-   Installieren Sie die Anwendung mithilfe von Windows Installer 4,0 oder höher unter Windows Vista.
-   Verwenden Sie keine erhöhten System Privilegien, um die Anwendung auf dem Computer zu installieren.
-   Installieren Sie die Anwendung im kontextbezogenen Kontext, und legen Sie diesen als Standard Installations Kontext des Pakets ab. Wenn die Eigenschaft " [**ALLUSERS**](allusers.md) " nicht festgelegt ist, wird das Paket vom Installationsprogramm im benutzerspezifischen Kontext installiert. Wenn Sie die Eigenschaft **ALLUSERS** nicht in die [Eigenschaften Tabelle](property-table.md)einschließen, wird diese Eigenschaft vom Installer nicht festgelegt, sodass die Installation pro Benutzer zum Standard Installations Kontext wird. Sie können diesen Standardwert überschreiben, indem Sie die Eigenschaft **ALLUSERS** in der Befehlszeile festlegen.
-   Legen Sie in der Eigenschaft [**Wort Zähl Zusammenfassung**](word-count-summary.md) den Wert Bit 3 fest, um anzugeben, dass für die Installation der Anwendung keine erhöhten Rechte erforderlich sind.

 

 



