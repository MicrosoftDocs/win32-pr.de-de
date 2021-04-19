---
description: Referenz Thema für das InkPicture-Steuerelement für den Tablet PC.
ms.assetid: 1ced9779-dae5-4f9a-8a68-b2c0d041d5b4
title: InkPicture-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded5295d48e4bb14b3c0d83713f33939a360cff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363680"
---
# <a name="inkpicture-control"></a>InkPicture-Steuerelement

Das [InkPicture](inkpicture-control-reference.md) -Steuerelement ermöglicht Ihnen das Platzieren eines Bilds (JPG-, BMP-, PNG-oder GIF-Format) in einer Anwendung, der Benutzer frei Hand Eingaben hinzufügen können. Es ist für Szenarien vorgesehen, in denen frei Hand Eingaben nicht als Text erkannt werden müssen, sondern als frei Hand Eingaben gespeichert werden.

Benutzer fügen mithilfe eines Stifts frei Hand Eingaben zu einer transparenten Ebene hinzu. Benutzer können die Größe eines [InkPicture](inkpicture-control-reference.md) -Fensters ändern, ohne frei Hand Informationen zu verlieren, auch wenn die frei Hand Eingaben bei der Größenanpassung abgeschnitten werden.

Das [InkPicture](inkpicture-control-reference.md) -Steuerelement enthält grundlegende Druckunterstützung. Allerdings müssen Sie die Druckvorschau oder andere erweiterte Druckfunktionen implementieren.

Die verwaltete (.NET Framework)-Implementierung von [InkPicture](/previous-versions/ms583740(v=vs.100)) erbt von der [PictureBox](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1) -Klasse.

Standardmäßig ist "Ink" schwarz gefärbt, wenn nicht im Modus für hohe Kontraste. Andernfalls wird der Wert auf den aktuellen System Farb Einstellungs Wert (Color \_ WindowText) festgelegt. Standardmäßig ist " [**fittcurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) " standardmäßig " **false**".

Verwenden Sie im [InkPicture](inkpicture-control-reference.md) -Steuerelement das [**Ink**](inkdisp-class.md) -Objekt, um frei Hand Eingaben zu laden und zu speichern.

> [!Note]  
> Wenn Sie [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) auf **Delete** oder **Select** festlegen, werden andere Ereignisse ausgelöst (z. b. das [**Stroke**](inkpicture-stroke.md) -Ereignis). Diese Ereignisse sind nützlich, wenn Sie Ihre eigenen Lösch-oder SELECT-Modi implementieren möchten.

 

Ausführliche Referenzinformationen zum [InkPicture](inkpicture-control-reference.md) -Steuerelement finden Sie unter InkPicture.

In den folgenden Abschnitten wird die Verwendung des [InkPicture](inkpicture-control-reference.md) -Steuer Elements ausführlich erläutert:

-   [Arbeiten mit Bildern](working-with-pictures.md)
-   [Verwenden von InkPicture in früheren Versionen von Windows](using-inkpicture-on-earlier-versions-of-windows.md)

 

 
