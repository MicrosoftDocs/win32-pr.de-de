---
description: Die Funktionen getupdatur und getupdatergn rufen den aktuellen Aktualisierungs Bereich für das Fenster ab.
ms.assetid: c0729c4f-3b00-4ab9-91b2-4a2fecee8727
title: Der Aktualisierungs Bereich wird abgerufen.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8115f47a6c585d5b660d73bbf4fb3de21334b6c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215172"
---
# <a name="retrieving-the-update-region"></a>Der Aktualisierungs Bereich wird abgerufen.

Die Funktionen [**getupdatur**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) und [**getupdatergn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) rufen den aktuellen Aktualisierungs Bereich für das Fenster ab. Getupdatter Ruft das kleinste Rechteck (in logischen Koordinaten) ab, das den gesamten Update Bereich einschließt. Getupdatergn Ruft den Update Bereich selbst ab. Diese Funktionen können verwendet werden, um die aktuelle Größe des Aktualisierungs Bereichs zu berechnen und zu bestimmen, wo ein Zeichnungs Vorgang durchgeführt werden soll.

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) ruft auch die Dimensionen des kleinsten Rechtecks ab, das den aktuellen Aktualisierungs Bereich einschließt, wobei die Dimensionen in den **rcpaint** -Member in der [**paintstruct**](/windows/win32/api/winuser/ns-winuser-paintstruct) -Struktur kopiert werden. Da **BeginPaint** den Update Bereich überprüft, gibt jeder Aufrufe von [**getupdatergn**](/windows/desktop/api/Winuser/nf-winuser-getupdaterect) und [**getupdatergn**](/windows/desktop/api/Winuser/nf-winuser-getupdatergn) unmittelbar nach einem Aufrufen von **BeginPaint** einen leeren Update Bereich zurück.

 

 



