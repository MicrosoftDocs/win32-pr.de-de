---
title: Treffertestoptionen
description: In diesem Abschnitt werden die Optionswerte aufgeführt, die mit dem dwOptions-Parameter der HitTestThemeBackground-Funktion verwendet werden. Eine Liste der Werte, die zurückgegeben werden, wenn Sie eine dieser Optionen angeben, finden Sie unter Treffertest-Rückgabewerte.
ms.assetid: a0d5c6c8-bb50-46e1-98ae-2374842344c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e3f9f3c7ba8b5c7a2c4468177befc3083bb2ed613b674cdb02f7fd3ad7f10c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166525"
---
# <a name="hit-test-options"></a>Treffertestoptionen

In diesem Abschnitt werden die Optionswerte aufgeführt, die mit dem *dwOptions-Parameter* der [**HitTestThemeBackground-Funktion verwendet**](/windows/desktop/api/Uxtheme/nf-uxtheme-hittestthemebackground) werden. Eine Liste der Werte, die zurückgegeben werden, wenn Sie eine dieser Optionen angeben, finden Sie unter [Treffertest-Rückgabewerte.](theme-hit-test-retval.md)

## <a name="option-values"></a>Optionswerte

In der folgenden Tabelle sind die Treffertestoptionen aufgeführt.



| Option                       | Wert                                                                                                                    | Beschreibung                                                                                                                                                                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HTTB \_ BACKGROUNDSEG          | 0x00000000                                                                                                               | Option "Treffertest für Designhintergrundsegment".                                                                                                                                           |
| HTTB \_ FIXEDBORDER            | 0x00000002                                                                                                               | Die Option "Border Hit Test" wurde korrigiert.                                                                                                                                                       |
| HTTB \_ CAPTION                | 0x00000004                                                                                                               | Beschriftungstreffertestoption.                                                                                                                                                            |
| HTTB \_ RESIZINGBORDER         | (HTTB \_ RESIZINGBORDER \_ LEFT \| HTTB \_ RESIZINGBORDER \_ TOP \| HTTB \_ RESIZINGBORDER \_ RIGHT \| HTTB \_ RESIZINGBORDER \_ BOTTOM) | Ändern der Größe von Rahmentreffertestoptionen.                                                                                                                                                   |
| HTTB \_ RESIZINGBORDER \_ LEFT   | 0x00000010                                                                                                               | Option zum Ändern der Größe des Links border-Treffertests.                                                                                                                                               |
| HTTB \_ RESIZINGBORDER \_ TOP    | 0x00000020                                                                                                               | Option zum Ändern der Größe des Treffertests für den oberen Rahmen.                                                                                                                                                |
| HTTB \_ RESIZINGBORDER \_ RIGHT  | 0x00000040                                                                                                               | Option zum Ändern der Größe des rechten Rahmens – Treffertestoption.                                                                                                                                              |
| HTTB \_ RESIZINGBORDER \_ BOTTOM | 0x00000080                                                                                                               | Option zum Ändern der Größe des Treffertests für den unteren Rahmen.                                                                                                                                             |
| HTTB \_ SIZINGTEMPLATE         | 0x00000100                                                                                                               | Das Ändern des Rahmens wird als Vorlage und nicht nur als Fensterrand angegeben. Diese Option ist mit HTTB \_ SYSTEMSIZINGMARGINS gegenseitig ausschließen. HTTB \_ SIZINGTEMPLATE hat Vorrang.         |
| HTTB \_ SYSTEMSIZINGMARGINS    | 0x00000200                                                                                                               | Verwendet die Rahmenbreite des Systems anstelle von Inhaltsrändern im visuellen Stil. Diese Option ist mit HTTB \_ SIZINGTEMPLATE gegenseitig ausschließend. HTTB \_ SIZINGTEMPLATE hat Vorrang. |



 

 

 




