---
description: Verwenden von vom Besitzer gezeichneten Menüs zur Unterstützung der Sprachfunktionalität für den Tablet PC.
ms.assetid: fbe2d420-f667-416b-bff3-0fee9ae22203
title: Verwenden von Owner-Drawn Menüs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a14e63e3602e31edc506a6c9c070fa0bfcce670ec2248c73d68944a2f83a12f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842800"
---
# <a name="using-owner-drawn-menus"></a>Verwenden von Owner-Drawn Menüs

Wenn Sie vom Besitzer gezeichnete Menüs verwenden, müssen Sie die Menünamen zur Unterstützung der Sprachfunktionalität verfügbar machen. Hierfür gibt es zwei Möglichkeiten:

-   Machen Sie den Namen des Menüelements mithilfe der MSAAMENUINFO-Struktur verfügbar.
-   Stellen Sie eine Option bereit, um Grafikmenüs durch Standardtextmenüs zu ersetzen, wenn eine Barrierefreiheitshilfe aktiv ist. Wenn die [**SystemParametersInfo-Funktion**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) **TRUE** zurückgibt und der *uiAction-Parameter* auf SPI \_ GETSCREENREADER festgelegt ist, verwenden Sie Standardmenüs. Die Anwendung sollte auf die WM \_ SETTINGSCHANGE-Nachricht achten und antworten, indem sie den Status dieser Option abfragt und die Anzeige entsprechend anpasst. Beispielsweise bietet Microsoft Visual Studio eine Option zum Verwenden von Standardmenüs anstelle der standardmäßig angezeigten benutzerdefinierten Menüs.

 

 
