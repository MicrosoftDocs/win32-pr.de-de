---
title: Hoher Kontrast Parameter
description: Mit dem Parameter "High Contrast" wird angegeben, ob der Benutzer einen hohen Kontrast zwischen den Farben für Vordergrund-und Hintergrund visuelle Elemente wünscht.
ms.assetid: ec89c4ce-4e8b-4e1f-a349-fbd47431d675
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f1255e8a99b3cb253146e2fa2c019a879c4a1b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948874"
---
# <a name="high-contrast-parameter"></a>Hoher Kontrast Parameter

Mit dem Parameter "High Contrast" wird angegeben, ob der Benutzer einen hohen Kontrast zwischen den Farben für Vordergrund-und Hintergrund visuelle Elemente wünscht.

Der Benutzer steuert die Einstellung des Parameters für hohe Kontraste mithilfe des Easy Access Centers in der Systemsteuerung oder einer anderen Anwendung für die Anpassung der Umgebung. Anwendungen verwenden die **SPI- \_ gethighcontrast** -und **SPI \_ sethighcontrast** -Flags mit der [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion, um den hohen Kontrast Parameter zu erhalten und festzulegen.

Während der Initialisierung und beim Verarbeiten von [**WM- \_ syscolorchange**](/windows/desktop/gdi/wm-syscolorchange) -Meldungen sollten Anwendungen den Status des Parameters für hohe Kontraste bestimmen. Um diese Entscheidung zu treffen, sollten Anwendungen [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) mit dem **SPI \_ gethighcontrast** -Flag aufrufen, um eine [**HighContrast**](/windows/win32/api/winuser/ns-winuser-highcontrasta) -Struktur zu erhalten. Wenn für den **dwFlags** -Member der **HighContrast** -Struktur das **HCF \_ highkontra Ston** -Bit festgelegt ist, wird die Funktion für hohe Kontraste aktiviert, und Anwendungen sollten folgende Aktionen ausführen:

-   Ordnen Sie alle Farben einem einzelnen paar von Vorder-und Hintergrundfarben zu. Verwenden Sie die [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) -Funktion, um die entsprechenden Vordergrund-und Hintergrundfarben zu bestimmen. verwenden Sie dazu entweder eine Kombination aus **Farbe \_ WindowText** und **Color \_ Window** oder eine Kombination aus **Farbe \_ btntext** und **Color \_ btnface**. Die **GetSysColor** -Funktion gibt die Farben zurück, die vom Benutzer über die Systemsteuerung ausgewählt wurden.
-   Lassen Sie alle Bitmapbilder aus, die normalerweise hinter dem Text angezeigt werden. Diese Bilder sind für einen Benutzer, der einen hohen Kontrast benötigt, visuell ablenkend.
-   Bilder, die in der Regel in mehreren Farben gezeichnet werden, sollten mithilfe der Vordergrund-und Hintergrundfarben gezeichnet werden, die für Text ausgewählt werden.

Außerdem verwenden Anwendungen die **SPI \_ getdisableoverlappedcontent** -und **SPI \_ setdisableoverlappedcontent** -Flags mit der [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion, um überlappende Inhalts Parameter zu erhalten und festzulegen. Anzeigen von Features wie Hintergrundbildern, strukturierten Hintergründen, Wasserzeichen in Dokumenten, Alpha Blending und Transparenz können den Kontrast zwischen dem Vordergrund und dem Hintergrund verringern. Dadurch wird es Benutzern mit Sehfähigkeit erschwert, Objekte auf dem Bildschirm anzuzeigen. Mit diesem Flag können Anwendungen bestimmen, ob dieser überlappende Inhalt deaktiviert wurde.

 

 