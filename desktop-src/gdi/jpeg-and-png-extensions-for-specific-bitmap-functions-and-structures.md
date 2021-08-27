---
description: In bestimmten Versionen von Microsoft Windows ermöglichen die Funktionen StretchDIBits und SetDIBitsToDevice das Übergeben von JPEG- und PNG-Bildern als Quellbild an Druckergeräte.
ms.assetid: a38a807d-44df-40a2-8af7-0ce5e532cba2
title: JPEG- und PNG-Erweiterungen für bestimmte Bitmapfunktionen und -strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fd7dcd2713b737d86f90ab0d49fdf4eed1216f807a4debdffa1963e43a42a9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120115290"
---
# <a name="jpeg-and-png-extensions-for-specific-bitmap-functions-and-structures"></a>JPEG- und PNG-Erweiterungen für bestimmte Bitmapfunktionen und -strukturen

In bestimmten Versionen von Microsoft Windows ermöglichen die [**Funktionen StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) und [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) die Übergeben von JPEG- und PNG-Bildern als Quellbild an Druckergeräte. Diese Erweiterung ist nicht als Mittel zur Bereitstellung der allgemeinen JPEG- und PNG-Dekomprimierung für Anwendungen gedacht, sondern soll Es Anwendungen ermöglichen, JPEG- und PNG-komprimierte Bilder direkt an Drucker mit Hardwareunterstützung für JPEG- und PNG-Bilder zu senden.

Die [**Strukturen BITMAPINFOHEADER,**](/previous-versions//dd183376(v=vs.85)) [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) und [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) wurden erweitert, um die Angabe von **biCompression-Werten** zu ermöglichen, die angeben, dass es sich bei den Bitmapdaten um ein JPEG- oder PNG-Bild handelt. Diese Komprimierungswerte sind nur für [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) und [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) gültig, wenn der *hdc-Parameter* ein Druckergerät angibt. Um das Metafilespooling des Druckers zu unterstützen, sollte die Anwendung nicht auf den Rückgabewert angewiesen sein, um zu bestimmen, ob das Gerät die JPEG- oder PNG-Datei unterstützt. Die Anwendung muss QUERYESCSUPPORT mit dem entsprechenden Escape-Zeichen aus geben, bevor **SetDIBitsToDevice** und **StretchDIBits aufrufen.** Wenn bei der Überprüfung ein Escapefehler auftritt, muss die Anwendung auf ihre eigene JPEG- oder PNG-Unterstützung zurückfallen, um das Bild in eine Bitmap zu dekomprimieren.

 

 
