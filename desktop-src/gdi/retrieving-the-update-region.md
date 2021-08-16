---
description: Die Funktionen GetUpdateRect und GetUpdateRgn rufen den aktuellen Updatebereich für das Fenster ab.
ms.assetid: c0729c4f-3b00-4ab9-91b2-4a2fecee8727
title: Abrufen der Updateregion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28bf72bfcfd28ec0fc9a90485a94e19d0514bb0206de660c11a56d12f33671e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117698243"
---
# <a name="retrieving-the-update-region"></a>Abrufen der Updateregion

Die Funktionen [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) und [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) rufen den aktuellen Updatebereich für das Fenster ab. GetUpdateRect ruft das kleinste Rechteck (in logischen Koordinaten) ab, das den gesamten Updatebereich einschließt. GetUpdateRgn ruft den Updatebereich selbst ab. Diese Funktionen können verwendet werden, um die aktuelle Größe des Aktualisierungsbereichs zu berechnen, um zu bestimmen, wo ein Zeichnungsvorgang ausgeführt werden soll.

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) ruft auch die Dimensionen des kleinsten Rechtecks ab, das den aktuellen Updatebereich umschließt, und kopiert die Dimensionen in das **rcPaint-Element** in der [**PAINTSTRUCT-Struktur.**](/windows/win32/api/winuser/ns-winuser-paintstruct) Da **BeginPaint** den Updatebereich überprüft, gibt jeder Aufruf von [**GetUpdateRect**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) und [**GetUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) unmittelbar nach einem Aufruf von **BeginPaint** einen leeren Updatebereich zurück.

 

 



