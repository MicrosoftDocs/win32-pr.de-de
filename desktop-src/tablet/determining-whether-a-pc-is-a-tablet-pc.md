---
description: Möglicherweise müssen Sie gelegentlich ermitteln, ob Ihre Anwendung auf einem Tablet PC ausgeführt wird, da Sie möchten, dass Ihre Anwendungen inhärente Freihand-, Erkennungs-und Stift Funktionen nutzen.
ms.assetid: 86a3eddb-6541-4b73-b2ca-6adedad1a1e5
title: Ermitteln, ob ein PC ein Tablet PC ist
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c793d5531d6091d4bce73d99bfa32d100c2b9304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351029"
---
# <a name="determining-whether-a-pc-is-a-tablet-pc"></a><span data-ttu-id="6073c-103">Ermitteln, ob ein PC ein Tablet PC ist</span><span class="sxs-lookup"><span data-stu-id="6073c-103">Determining Whether a PC is a Tablet PC</span></span>

<span data-ttu-id="6073c-104">Möglicherweise müssen Sie gelegentlich ermitteln, ob Ihre Anwendung auf einem Tablet PC ausgeführt wird, da Sie möchten, dass Ihre Anwendungen inhärente Freihand-, Erkennungs-und Stift Funktionen nutzen.</span><span class="sxs-lookup"><span data-stu-id="6073c-104">You may occasionally need to determine whether your application is running on a Tablet PC because you may want your applications to take advantage of inherent ink, recognition, and pen capabilities.</span></span> <span data-ttu-id="6073c-105">Um Ihnen zu helfen, zu bestimmen, ob Ihre Anwendung auf die Tablet PC-Features zugreifen kann, können Sie den GetSystemMetrics ()-Windows-API-Befehl verwenden, wie in diesem Thema beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6073c-105">To help you determine whether your application has access to the Tablet PC features, you can use the GetSystemMetrics() Windows API call as described in this topic.</span></span>

## <a name="client-side-applications"></a><span data-ttu-id="6073c-106">Client-Side Anwendungen</span><span class="sxs-lookup"><span data-stu-id="6073c-106">Client-Side Applications</span></span>

<span data-ttu-id="6073c-107">Mithilfe der folgenden Verfahren können Sie feststellen, ob Ihr Code auf einem Tablet PC ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6073c-107">You can use the following techniques to determine whether your code is running on a Tablet PC.</span></span>

-   [<span data-ttu-id="6073c-108">Verwenden von GetSystemMetrics (SM \_ TabletPC)</span><span class="sxs-lookup"><span data-stu-id="6073c-108">Using GetSystemMetrics (SM\_TABLETPC)</span></span>](/windows)
-   [<span data-ttu-id="6073c-109">Verwenden von Tablet Platform-Binärdateien</span><span class="sxs-lookup"><span data-stu-id="6073c-109">Using the Presence of Tablet Platform Binaries</span></span>](#using-the-presence-of-tablet-platform-binaries)
-   [<span data-ttu-id="6073c-110">Webbasierte Anwendungen</span><span class="sxs-lookup"><span data-stu-id="6073c-110">Web-Based Applications</span></span>](#web-based-applications)

### <a name="using-getsystemmetrics-sm_tabletpc"></a><span data-ttu-id="6073c-111">Verwenden von GetSystemMetrics (SM \_ TabletPC)</span><span class="sxs-lookup"><span data-stu-id="6073c-111">Using GetSystemMetrics (SM\_TABLETPC)</span></span>

### <a name="windows-xp-tablet-pc-edition"></a><span data-ttu-id="6073c-112">Windows XP Tablet PC Edition</span><span class="sxs-lookup"><span data-stu-id="6073c-112">Windows XP Tablet PC Edition</span></span>

<span data-ttu-id="6073c-113">Verwenden Sie in Microsoft Windows XP Tablet PC Edition die Funktion GetSystemMetrics (SM \_ TabletPC), um zu bestimmen, ob ein Computer ein Tablet PC ist.</span><span class="sxs-lookup"><span data-stu-id="6073c-113">In Microsoft Windows XP Tablet PC Edition, use the GetSystemMetrics(SM\_TABLETPC) function to determine whether a computer is a Tablet PC.</span></span> <span data-ttu-id="6073c-114">GetSystemMetrics (SM \_ TabletPC) soll auf einem Computer, auf dem Windows XP Tablet PC Edition ausgeführt wird, "true" zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6073c-114">GetSystemMetrics(SM\_TABLETPC) is designed to return TRUE on a computer running Windows XP Tablet PC Edition.</span></span>

### <a name="windows-vista"></a><span data-ttu-id="6073c-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6073c-115">Windows Vista</span></span>

<span data-ttu-id="6073c-116">In Windows Vista ist kein eindeutiges Tablet PC SDK mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6073c-116">In Windows Vista, there is no longer a distinct Tablet PC SDK.</span></span> <span data-ttu-id="6073c-117">Die Windows SDK enthält jetzt den Abschnitt "Tablet PC and Touchscreen Technology", und die Logik von GetSystemMetrics (SM \_ TabletPC) wurde geändert, um dies widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="6073c-117">The Windows SDK now contains a section called "Tablet PC and Touch Technology" and the logic of GetSystemMetrics(SM\_TABLETPC) has been changed to reflect this.</span></span> <span data-ttu-id="6073c-118">GetSystemMetrics (SM \_ TabletPC) gibt jetzt true zurück, wenn Folgendes zutrifft:</span><span class="sxs-lookup"><span data-stu-id="6073c-118">GetSystemMetrics(SM\_TABLETPC) now returns true if all of the following are true:</span></span>

-   <span data-ttu-id="6073c-119">Es gibt einen integrierten Digitalisierer (Pen oder Touchscreen) auf dem System.</span><span class="sxs-lookup"><span data-stu-id="6073c-119">There is an integrated digitizer, either pen or touch, on the system.</span></span>
-   <span data-ttu-id="6073c-120">Die optionale Komponente Tablet PC ist installiert.</span><span class="sxs-lookup"><span data-stu-id="6073c-120">The Tablet PC optional component is installed.</span></span> <span data-ttu-id="6073c-121">Diese Komponente enthält Features wie Tablet PC Input Panel und Windows Journal.</span><span class="sxs-lookup"><span data-stu-id="6073c-121">This component contains features such as Tablet PC Input Panel and Windows Journal.</span></span>
-   <span data-ttu-id="6073c-122">Der Computer ist für die Verwendung der optionalen Komponente lizenziert.</span><span class="sxs-lookup"><span data-stu-id="6073c-122">The computer is licensed to use the optional component.</span></span> <span data-ttu-id="6073c-123">Premium-Versionen von Windows Vista – z. b. Windows Vista Home Premium, Windows Vista Small Business, Windows Vista Professional, Windows Vista Enterprise und Windows Vista Ultimate – sind für die Verwendung der optionalen Komponente lizenziert.</span><span class="sxs-lookup"><span data-stu-id="6073c-123">Premium versions of Windows Vista—such as Windows Vista Home Premium, Windows Vista Small Business, Windows Vista Professional, Windows Vista Enterprise, and Windows Vista Ultimate—are licensed to use the optional component.</span></span>
-   <span data-ttu-id="6073c-124">Der Tablet PC-Eingabe Dienst wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6073c-124">Tablet PC Input Service is running.</span></span> <span data-ttu-id="6073c-125">Der Tablet PC-Eingabe Dienst ist ein neuer Dienst für Windows Vista, der die Tablet PC-Eingabe steuert.</span><span class="sxs-lookup"><span data-stu-id="6073c-125">Tablet PC Input Service is a new service for Windows Vista that controls Tablet PC input.</span></span>

<span data-ttu-id="6073c-126">Mit dieser zunehmenden Genauigkeit ist GetSystemMetrics (SM \_ TabletPC) weiterhin die empfohlene Methode, um zu bestimmen, ob ein Computer, auf dem Windows Vista ausgeführt wird, ein Tablet PC ist.</span><span class="sxs-lookup"><span data-stu-id="6073c-126">With this increased accuracy, GetSystemMetrics(SM\_TABLETPC) continues to be the recommended way to determine whether a computer running Windows Vista is a Tablet PC.</span></span>

### <a name="using-the-presence-of-tablet-platform-binaries"></a><span data-ttu-id="6073c-127">Verwenden von Tablet Platform-Binärdateien</span><span class="sxs-lookup"><span data-stu-id="6073c-127">Using the Presence of Tablet Platform Binaries</span></span>

<span data-ttu-id="6073c-128">In Windows XP Tablet PC Edition und Windows Vista können Sie nach dem vorhanden sein der frei Hand Binärdateien suchen – z. b. inkobj.dll und Microsoft.Ink.dll – und ihre unterstützten Funktionen verwenden, sofern diese vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="6073c-128">In both Windows XP Tablet PC Edition and Windows Vista, you can search for the presence of the ink binaries—such as inkobj.dll and Microsoft.Ink.dll—and use their supported functionality if they are present.</span></span>

<span data-ttu-id="6073c-129">In Windows Vista werden die Binärdateien der Tablet PC-Plattform standardmäßig auf allen Client Versionen installiert.</span><span class="sxs-lookup"><span data-stu-id="6073c-129">In Windows Vista, the Tablet PC Platform binaries are installed on all client versions by default.</span></span> <span data-ttu-id="6073c-130">Eingabe-und Freihand-Funktionen sind für diese Versionen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6073c-130">Input and inking functionality are available on those versions.</span></span> <span data-ttu-id="6073c-131">Die Erkennung ist nur in Premium-Versionen von Windows Vista verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6073c-131">Recognition is available only in premium versions of Windows Vista.</span></span>

### <a name="web-based-applications"></a><span data-ttu-id="6073c-132">Web-Based Anwendungen</span><span class="sxs-lookup"><span data-stu-id="6073c-132">Web-Based Applications</span></span>

<span data-ttu-id="6073c-133">In Windows Vista enthält die von Internet Explorer gemeldete Benutzer-Agent-Zeichenfolge "Tablet PC 2,0", wenn das Gerät gemäß GetSystemMetrics (SM \_ TabletPC) ein Tablet PC ist.</span><span class="sxs-lookup"><span data-stu-id="6073c-133">In Windows Vista, the user-agent string reported by Internet Explorer includes "Tablet PC 2.0" if, according to GetSystemMetrics(SM\_TABLETPC), the device is a Tablet PC.</span></span>

<span data-ttu-id="6073c-134">In Windows XP Tablet PC Edition 2005 enthält die Benutzer-Agent-Zeichenfolge Tablet PC 1,7.</span><span class="sxs-lookup"><span data-stu-id="6073c-134">In Windows XP Tablet PC Edition 2005, the user-agent string includes Tablet PC 1.7.</span></span> <span data-ttu-id="6073c-135">Die Benutzer-Agent-Zeichenfolge sieht in etwa wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="6073c-135">The user-agent string looks something like the following:</span></span>

`Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1; .NET CLR 1.0.3705; Tablet PC 2.0)`

<span data-ttu-id="6073c-136">Verwenden Sie diesen Wert, um zu bestimmen, ob es sich bei dem Client Computer um einen Tablet PC handelt</span><span class="sxs-lookup"><span data-stu-id="6073c-136">Use this value to determine whether the client computer is a Tablet PC and supports Web-based inking controls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6073c-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6073c-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6073c-138">**GetSystemMetrics**</span><span class="sxs-lookup"><span data-stu-id="6073c-138">**GetSystemMetrics**</span></span>](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics)
</dt> </dl>

 

 
