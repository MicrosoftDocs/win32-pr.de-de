---
description: In bestimmten Versionen von Microsoft Windows ermöglichen die Funktionen "StretchDIBits" und "SetDIBitsToDevice", dass JPEG-und PNG-Bilder als Quell Abbild an Drucker Geräte übergeben werden.
ms.assetid: a38a807d-44df-40a2-8af7-0ce5e532cba2
title: JPEG-und PNG-Erweiterungen für bestimmte Bitmap-Funktionen und-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1625dcde0e673c85dcaef65c2f1aa825121bf871
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528322"
---
# <a name="jpeg-and-png-extensions-for-specific-bitmap-functions-and-structures"></a>JPEG-und PNG-Erweiterungen für bestimmte Bitmap-Funktionen und-Strukturen

In bestimmten Versionen von Microsoft Windows ermöglichen die Funktionen " [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) " und " [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) ", dass JPEG-und PNG-Bilder als Quell Abbild an Drucker Geräte übergeben werden. Diese Erweiterung ist nicht als Mittel zum Bereitstellen allgemeiner JPEG-und PNG-Dekomprimierungen für Anwendungen gedacht, sondern ermöglicht es Anwendungen, JPEG-und PNG-komprimierte Bilder direkt an Drucker zu senden, die über Hardwareunterstützung für JPEG-und PNG-Bilder verfügen.

Die [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85))-, [**BITMAPV4HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv4header) -und [**BITMAPV5HEADER**](/windows/desktop/api/Wingdi/ns-wingdi-bitmapv5header) -Strukturen werden erweitert, um die Angabe von **bikomprimierungswerten** zuzulassen, die angeben, dass die Bitmapdaten ein JPEG-oder PNG-Bild darstellen. Diese Komprimierungs Werte sind nur für [**SetDIBitsToDevice**](/windows/desktop/api/Wingdi/nf-wingdi-setdibitstodevice) und [**StretchDIBits**](/windows/desktop/api/Wingdi/nf-wingdi-stretchdibits) gültig, wenn der *hdc* -Parameter ein Druckergerät angibt. Zur Unterstützung der metadatenspoolerung des Druckers sollte die Anwendung nicht auf den Rückgabewert zurückgreifen, um zu bestimmen, ob das Gerät die JPEG-oder PNG-Datei unterstützt. Die Anwendung muss queryescsupport mit dem entsprechenden Escape ausgeben, bevor **SetDIBitsToDevice** und **StretchDIBits** aufgerufen werden. Wenn bei der Validierung ein Fehler auftritt, muss die Anwendung dann auf Ihre eigene JPEG-oder PNG-Unterstützung zurückgreifen, um das Bild in eine Bitmap zu dekomprimieren.

 

 
