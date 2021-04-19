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
# <a name="inkpicture-control"></a><span data-ttu-id="af815-103">InkPicture-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="af815-103">InkPicture Control</span></span>

<span data-ttu-id="af815-104">Das [InkPicture](inkpicture-control-reference.md) -Steuerelement ermöglicht Ihnen das Platzieren eines Bilds (JPG-, BMP-, PNG-oder GIF-Format) in einer Anwendung, der Benutzer frei Hand Eingaben hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="af815-104">The [InkPicture](inkpicture-control-reference.md) control enables you to place an image (.jpg, .bmp, .png, or .gif format) in an application that users can add ink to.</span></span> <span data-ttu-id="af815-105">Es ist für Szenarien vorgesehen, in denen frei Hand Eingaben nicht als Text erkannt werden müssen, sondern als frei Hand Eingaben gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="af815-105">It is intended for scenarios in which ink need not be recognized as text but is stored as ink.</span></span>

<span data-ttu-id="af815-106">Benutzer fügen mithilfe eines Stifts frei Hand Eingaben zu einer transparenten Ebene hinzu.</span><span class="sxs-lookup"><span data-stu-id="af815-106">Users add ink to a transparent layer using a pen.</span></span> <span data-ttu-id="af815-107">Benutzer können die Größe eines [InkPicture](inkpicture-control-reference.md) -Fensters ändern, ohne frei Hand Informationen zu verlieren, auch wenn die frei Hand Eingaben bei der Größenanpassung abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="af815-107">Users can re-size an [InkPicture](inkpicture-control-reference.md) window without losing any ink information, even if the ink is cropped when re-sizing.</span></span>

<span data-ttu-id="af815-108">Das [InkPicture](inkpicture-control-reference.md) -Steuerelement enthält grundlegende Druckunterstützung. Allerdings müssen Sie die Druckvorschau oder andere erweiterte Druckfunktionen implementieren.</span><span class="sxs-lookup"><span data-stu-id="af815-108">The [InkPicture](inkpicture-control-reference.md) control includes basic printing support; however, it is up to you to implement print preview or other advanced printing capabilities.</span></span>

<span data-ttu-id="af815-109">Die verwaltete (.NET Framework)-Implementierung von [InkPicture](/previous-versions/ms583740(v=vs.100)) erbt von der [PictureBox](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="af815-109">The managed (.NET Framework) implementation of [InkPicture](/previous-versions/ms583740(v=vs.100)) inherits from the [PictureBox](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1) class.</span></span>

<span data-ttu-id="af815-110">Standardmäßig ist "Ink" schwarz gefärbt, wenn nicht im Modus für hohe Kontraste. Andernfalls wird der Wert auf den aktuellen System Farb Einstellungs Wert (Color \_ WindowText) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="af815-110">By default, ink is colored black if not in high-contrast mode; otherwise, it is set to the current system color setting (COLOR\_WINDOWTEXT) value.</span></span> <span data-ttu-id="af815-111">Standardmäßig ist " [**fittcurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) " standardmäßig " **false**".</span><span class="sxs-lookup"><span data-stu-id="af815-111">Also, by default [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) is **FALSE**.</span></span>

<span data-ttu-id="af815-112">Verwenden Sie im [InkPicture](inkpicture-control-reference.md) -Steuerelement das [**Ink**](inkdisp-class.md) -Objekt, um frei Hand Eingaben zu laden und zu speichern.</span><span class="sxs-lookup"><span data-stu-id="af815-112">Within the [InkPicture](inkpicture-control-reference.md) control, use the [**Ink**](inkdisp-class.md) object to load and save ink.</span></span>

> [!Note]  
> <span data-ttu-id="af815-113">Wenn Sie [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) auf **Delete** oder **Select** festlegen, werden andere Ereignisse ausgelöst (z. b. das [**Stroke**](inkpicture-stroke.md) -Ereignis).</span><span class="sxs-lookup"><span data-stu-id="af815-113">When you set the [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) to **Delete** or **Select**, other events (such as the [**Stroke**](inkpicture-stroke.md) event) are triggered.</span></span> <span data-ttu-id="af815-114">Diese Ereignisse sind nützlich, wenn Sie Ihre eigenen Lösch-oder SELECT-Modi implementieren möchten.</span><span class="sxs-lookup"><span data-stu-id="af815-114">These events are useful if you want to implement your own delete or select modes.</span></span>

 

<span data-ttu-id="af815-115">Ausführliche Referenzinformationen zum [InkPicture](inkpicture-control-reference.md) -Steuerelement finden Sie unter InkPicture.</span><span class="sxs-lookup"><span data-stu-id="af815-115">For detailed reference information about the [InkPicture](inkpicture-control-reference.md) control, see InkPicture.</span></span>

<span data-ttu-id="af815-116">In den folgenden Abschnitten wird die Verwendung des [InkPicture](inkpicture-control-reference.md) -Steuer Elements ausführlich erläutert:</span><span class="sxs-lookup"><span data-stu-id="af815-116">The following sections detail the use of the [InkPicture](inkpicture-control-reference.md) control:</span></span>

-   [<span data-ttu-id="af815-117">Arbeiten mit Bildern</span><span class="sxs-lookup"><span data-stu-id="af815-117">Working with Pictures</span></span>](working-with-pictures.md)
-   [<span data-ttu-id="af815-118">Verwenden von InkPicture in früheren Versionen von Windows</span><span class="sxs-lookup"><span data-stu-id="af815-118">Using InkPicture on Earlier Versions of Windows</span></span>](using-inkpicture-on-earlier-versions-of-windows.md)

 

 
