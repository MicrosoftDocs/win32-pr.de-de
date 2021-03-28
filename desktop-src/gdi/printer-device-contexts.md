---
description: Der Drucker-DC kann beim Drucken auf einem Punkt-Matrix-Drucker, einem frei Hand Strahl Drucker, einem Laserdrucker oder einem-Plotter verwendet werden.
ms.assetid: c53f15d8-5a02-4095-8f05-ae309d4553ff
title: Drucker Geräte Kontexte (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7475776a3d13394b210f8289b458b8e99c474c93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978385"
---
# <a name="printer-device-contexts-windows-gdi"></a>Drucker Geräte Kontexte (Windows GDI)

Der Drucker-DC kann beim Drucken auf einem Punkt-Matrix-Drucker, einem frei Hand Strahl Drucker, einem Laserdrucker oder einem-Plotter verwendet werden. Eine Anwendung erstellt einen Drucker-DC durch Aufrufen der [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) -Funktion und Bereitstellen der entsprechenden Argumente (der Name des Druckertreibers, der Name des Druckers, der Datei-oder Gerätename für das physische Ausgabe Medium und andere Initialisierungs Daten). Wenn eine Anwendung den Druckvorgang abgeschlossen hat, wird der Drucker-DC durch Aufrufen der [**DeleteDC**](/windows/desktop/api/Wingdi/nf-wingdi-deletedc) -Funktion gelöscht. Ein Drucker-DC muss von einer Anwendung gelöscht werden. die [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) -Funktion schlägt fehl, wenn eine Anwendung versucht, Sie zum Freigeben eines Drucker-DC zu verwenden.

Weitere Informationen finden Sie unter [Druckerausgabe](../printdocs/printer-output.md).

 

 
