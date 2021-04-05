---
description: Verwenden von von einem Besitzer gezeichneten Menüs zur Unterstützung der sprach Funktionalität für den Tablet PC.
ms.assetid: fbe2d420-f667-416b-bff3-0fee9ae22203
title: Verwenden von Owner-Drawn Menüs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42f16f9328fadfedccee2c730678fc4cd2d8ab3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751272"
---
# <a name="using-owner-drawn-menus"></a>Verwenden von Owner-Drawn Menüs

Wenn Sie von einem Besitzer gezeichnete Menüs verwenden, müssen Sie die Menü Namen zur Unterstützung der sprach Funktionalität zur Verfügung stellen. Hierfür gibt es zwei Möglichkeiten:

-   Machen Sie den Menü Elementnamen mithilfe der msaamenuinfo-Struktur verfügbar.
-   Stellen Sie eine Option bereit, um grafische Menüs durch Standard Textmenüs zu ersetzen, wenn eine Barrierefreiheits Hilfe aktiv ist. Wenn die [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) -Funktion " **true** " zurückgibt, wobei der *uiaction* -Parameter auf SPI \_ getscreenreader festgelegt ist, verwenden Sie Standardmenüs. Die Anwendung sollte die WM \_ settingschange-Nachricht überwachen und reagieren, indem Sie den Status dieser Option Abfragen und die Anzeige entsprechend anpassen. Microsoft Visual Studio bietet z. b. eine Option, mit der Standardmenüs anstelle der benutzerdefinierten Menüs verwendet werden, die standardmäßig angezeigt werden.

 

 
