---
title: Kommunikation mit MCI-Geräten
description: Kommunikation mit MCI-Geräten
ms.assetid: a2532c29-553f-4ae3-8ad5-319fd9470e76
keywords:
- MCI-Geräte, kommunizieren
- Mciwndgetde viceid-Makro
- mciSendCommand-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1b5bfb7909b94bf8e71745adeeaeda61cae20ae
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314709"
---
# <a name="communication-with-mci-devices"></a><span data-ttu-id="f5b5d-106">Kommunikation mit MCI-Geräten</span><span class="sxs-lookup"><span data-stu-id="f5b5d-106">Communication with MCI Devices</span></span>

<span data-ttu-id="f5b5d-107">Für jedes MCI-Gerät ist es möglich, einen oder mehrere der folgenden als Bezeichner zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="f5b5d-107">It is possible for each MCI device to use one or more of the following as identifiers:</span></span>

-   <span data-ttu-id="f5b5d-108">ein Geräte Bezeichner</span><span class="sxs-lookup"><span data-stu-id="f5b5d-108">a device identifier</span></span>
-   <span data-ttu-id="f5b5d-109">ein Gerätename</span><span class="sxs-lookup"><span data-stu-id="f5b5d-109">a device name</span></span>
-   <span data-ttu-id="f5b5d-110">Alias</span><span class="sxs-lookup"><span data-stu-id="f5b5d-110">an alias</span></span>
-   <span data-ttu-id="f5b5d-111">der Dateiname des aktuell geladenen Inhalts.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-111">the filename of the currently loaded content.</span></span>

<span data-ttu-id="f5b5d-112">Mciwnd bietet Makros, die Sie verwenden können, um diese Informationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-112">MCIWnd provides macros you can use to retrieve this information.</span></span> <span data-ttu-id="f5b5d-113">Sie können diese Informationen dann verwenden, um direkt über MCI mit MCI-Geräten zu kommunizieren, die mciwnd-Fenstern zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-113">You can then use this information to communicate through MCI directly with MCI devices associated with MCIWnd windows.</span></span>

<span data-ttu-id="f5b5d-114">Sie können den Bezeichner des aktuellen MCI-Geräts abrufen, indem Sie das [**mciwndgetdebug**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-114">You can retrieve the identifier of the current MCI device by using the [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) macro.</span></span> <span data-ttu-id="f5b5d-115">Der MCI-Geräte Bezeichner ist ein numerischer Wert, der die Instanz des MCI-Geräts identifiziert, das von Ihrer Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-115">The MCI device identifier is a numerical value that identifies the instance of the MCI device your application is using.</span></span> <span data-ttu-id="f5b5d-116">Die Anwendung kann diesen Bezeichner verwenden, wenn Sie mit einem MCI-Gerät über die [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) -Funktion kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-116">Your application can use this identifier when communicating with an MCI device by using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>

<span data-ttu-id="f5b5d-117">Verwenden Sie das [**mciwndgetdevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) -Makro, um den Namen des aktuellen MCI-Geräts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-117">To retrieve the name of the current MCI device, use the [**MCIWndGetDevice**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdevice) macro.</span></span> <span data-ttu-id="f5b5d-118">Der MCI-Gerätename ist eine NULL-terminierte Zeichenfolge, die den Gerätetyp identifiziert, der einem mciwnd-Fenster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-118">The MCI device name is a null-terminated string that identifies the device type associated with an MCIWnd window.</span></span> <span data-ttu-id="f5b5d-119">Die Anwendung kann diesen Namen verwenden, wenn Sie mithilfe von **mciSendCommand** mit einem MCI-Gerät kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-119">Your application can use this name when communicating with an MCI device by using **mciSendCommand**.</span></span>

<span data-ttu-id="f5b5d-120">Sie können den Alias des aktuellen MCI-Geräts abrufen, indem Sie das Makro [**mciwndgetalias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-120">You can retrieve the alias of the current MCI device by using the [**MCIWndGetAlias**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetalias) macro.</span></span> <span data-ttu-id="f5b5d-121">Die Anwendung kann diesen Alias bei der Kommunikation mit einem MCI-Gerät mithilfe der [**mciSendString**](/previous-versions//dd757161(v=vs.85)) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-121">Your application can use this alias when communicating with an MCI device by using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span>

<span data-ttu-id="f5b5d-122">Schließlich können Sie den Dateinamen abrufen, der von einem MCI-Gerät verwendet wird, indem Sie das [**mciwndgetfilename**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-122">Finally, you can retrieve the filename used by an MCI device by using the [**MCIWndGetFileName**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetfilename) macro.</span></span> <span data-ttu-id="f5b5d-123">Der Dateiname identifiziert den aktuell einem mciwnd-Fenster zugeordneten Inhalt.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-123">The filename identifies the content currently associated with an MCIWnd window.</span></span> <span data-ttu-id="f5b5d-124">Die Anwendung kann diesen Dateinamen bei der Kommunikation mit einem MCI-Gerät mithilfe von **mciSendCommand** oder **mciSendString** verwenden.</span><span class="sxs-lookup"><span data-stu-id="f5b5d-124">Your application can use this filename when communicating with a MCI device by using **mciSendCommand** or **mciSendString**.</span></span>

 

 