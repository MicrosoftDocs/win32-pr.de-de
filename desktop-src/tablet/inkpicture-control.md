---
description: Referenzthema für das InkPicture-Steuerelement für den Tablet PC.
ms.assetid: 1ced9779-dae5-4f9a-8a68-b2c0d041d5b4
title: InkPicture-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef9cb4b5e1919e111e84cc6b654b56b14eff93cfb5aedacc15400fb3ef1af07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451099"
---
# <a name="inkpicture-control"></a>InkPicture-Steuerelement

Mit dem [InkPicture-Steuerelement](inkpicture-control-reference.md) können Sie ein Bild (.jpg, .bmp, .png oder .gif-Format) in einer Anwendung platzieren, der Benutzer Ink hinzufügen können. Sie ist für Szenarien vorgesehen, in denen Ink nicht als Text erkannt werden muss, sondern als Ink gespeichert wird.

Benutzer fügen mithilfe eines Stifts Ink zu einer transparenten Ebene hinzu. Benutzer können die Größe eines [InkPicture-Fensters](inkpicture-control-reference.md) neu anpassen, ohne dass Diekinformationen verloren geht, auch wenn die Ink-Datei beim Ändern der Größe zugeschnitten wird.

Das [InkPicture-Steuerelement](inkpicture-control-reference.md) enthält grundlegende Druckunterstützung. Es liegt jedoch an Ihnen, die Druckvorschau oder andere erweiterte Druckfunktionen zu implementieren.

Die verwaltete (.NET Framework) Implementierung von [InkPicture](/previous-versions/ms583740(v=vs.100)) erbt von der [PictureBox-Klasse.](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1)

In der Standardeinstellung ist Die Farbe für Die Farbe "Ink" schwarz, wenn sie sich nicht im Modus mit hohem Kontrast befindet. Andernfalls wird er auf den aktuellen Wert der Systemfarbeinstellung (COLOR \_ WINDOWTEXT) festgelegt. Außerdem ist [**FitToCurve standardmäßig**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) **FALSE.**

Verwenden Sie [im InkPicture-Steuerelement](inkpicture-control-reference.md) das [**Ink-Objekt,**](inkdisp-class.md) um Ink zu laden und zu speichern.

> [!Note]  
> Wenn Sie [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) auf Löschen **oder** **Auswählen** festlegen, werden andere Ereignisse (z. B. das [**Stroke-Ereignis)**](inkpicture-stroke.md) ausgelöst. Diese Ereignisse sind nützlich, wenn Sie Ihre eigenen Lösch- oder Auswahlmodi implementieren möchten.

 

Ausführliche Referenzinformationen zum [InkPicture-Steuerelement](inkpicture-control-reference.md) finden Sie unter InkPicture.

In den folgenden Abschnitten wird die Verwendung des [InkPicture-Steuerelements](inkpicture-control-reference.md) ausführlich beschrieben:

-   [Arbeiten mit Bildern](working-with-pictures.md)
-   [Verwenden von InkPicture in früheren Versionen Windows](using-inkpicture-on-earlier-versions-of-windows.md)

 

 
