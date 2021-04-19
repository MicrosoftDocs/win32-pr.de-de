---
title: Behandeln von Individualisierungs Ereignissen
description: Behandeln von Individualisierungs Ereignissen
ms.assetid: f533978f-f366-4900-b784-f51e88393984
keywords:
- Windows Media-Format-SDK, behandeln von Individualisierungs Ereignissen
- Windows Media-Format-SDK, Individualisierungs Ereignisse
- Advanced Systems Format (ASF), behandeln von Individualisierungs Ereignissen
- ASF (Advanced Systems Format), behandeln von Individualisierungs Ereignissen
- Advanced Systems Format (ASF), individualisierungsereignisse
- ASF (Advanced Systems Format), Individualisierungs Ereignisse
- Digital Rights Management (DRM), behandeln von Individualisierungs Ereignissen
- DRM (Digital Rights Management), behandeln von Individualisierungs Ereignissen
- Digital Rights Management (DRM), Individualisierungs Ereignisse
- DRM (Digital Rights Management), Individualisierungs Ereignisse
- Individualisierungs Ereignisse
- Ereignisse, Individualisierungs Ereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e74df94bf871ec62ec2acb94658785969812640
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106337209"
---
# <a name="handling-individualization-events"></a><span data-ttu-id="015c3-115">Behandeln von Individualisierungs Ereignissen</span><span class="sxs-lookup"><span data-stu-id="015c3-115">Handling Individualization Events</span></span>

<span data-ttu-id="015c3-116">Wenn eine DRM-fähige Anwendung versucht, eine geschützte Datei zu öffnen, untersucht die DRM-Komponente das [**DRM \_ drmHeader \_ Individual Version**](drm-drmheader-individualizedversion.md) -Attribut in der Datei, das die minimale Versions Ebene angibt, die für den Zugriff auf den Inhalt erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="015c3-116">When a DRM-enabled application attempts to open a protected file, the DRM component examines the [**DRM\_DRMHeader\_IndividualizedVersion**](drm-drmheader-individualizedversion.md) attribute in the file, which specifies the minimum version level required to access the content.</span></span> <span data-ttu-id="015c3-117">Alle Ebenen der DRM-Komponente funktionieren mit allen 7,0 und höheren Versionen von Windows Media Player und dem Windows Media-Format SDK.</span><span class="sxs-lookup"><span data-stu-id="015c3-117">All levels of the DRM component work with all 7.0 and later versions of Windows Media Player and the Windows Media Format SDK.</span></span> <span data-ttu-id="015c3-118">Wenn die individualisierte Versions Ebene der DRM-Komponente niedriger als die erforderliche Version ist, sendet die DRM-Komponente ein **WMT- \_ \_ Individualisierungs** Ereignis an die [**iwmstatuscallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) -Methode der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="015c3-118">If the DRM component's individualized version level is lower than the required version, the DRM component will send a **WMT\_NEEDS\_INDIVIDUALIZATION** event to the application's [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) method.</span></span> <span data-ttu-id="015c3-119">Die Anwendung muss dann eine Meldung oder ein Dialogfeld anzeigen, in der Benutzer dazu aufgefordert werden, das Sicherheits Upgrade entweder zu starten oder abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="015c3-119">The application must then display a message or dialog box prompting users to either start or cancel the security upgrade.</span></span> <span data-ttu-id="015c3-120">Diese Eingabeaufforderung ist erforderlich, da Benutzer aus Datenschutzgründen ihre Berechtigung erteilen müssen, bevor ein Sicherheits Upgrade auf dem Computer installiert wird.</span><span class="sxs-lookup"><span data-stu-id="015c3-120">This prompt is necessary because, for privacy reasons, users must give their permission before a security upgrade is installed on their computer.</span></span>

> [!Note]  
> <span data-ttu-id="015c3-121">Der Header des Inhalts gibt nur die ersten beiden Ziffern für DRM \_ drmversion \_ Individual Version an.</span><span class="sxs-lookup"><span data-stu-id="015c3-121">The header of the content specifies only the first two digits for DRM\_DRMVersion\_IndividualizedVersion.</span></span> <span data-ttu-id="015c3-122">Anders ausgedrückt: um eine DRM-Komponente der Ebene 2.2.0.1 anzufordern, würde der Header "2,2" enthalten.</span><span class="sxs-lookup"><span data-stu-id="015c3-122">In other words, to require a level 2.2.0.1 DRM component, the header would contain "2.2".</span></span>

 

<span data-ttu-id="015c3-123">Um das Sicherheits Upgrade und/oder die Initialisierung des Auslösers zu starten, müssen Sie die [**iwmdrmreader:: Individual**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) -Methode aufrufen, wobei der *dwFlags* -Parameter auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="015c3-123">To start the security upgrade and/or trigger individualization, call the [**IWMDRMReader::Individualize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-individualize) method with the *dwFlags* parameter set to 1.</span></span>

<span data-ttu-id="015c3-124">Sie müssen das **WMT \_ Individual** -Ereignis in Ihrer Anwendung behandeln.</span><span class="sxs-lookup"><span data-stu-id="015c3-124">You must handle the **WMT\_INDIVIDUALIZE** event in your application.</span></span> <span data-ttu-id="015c3-125">Dieses Ereignis wird von der DRM-Komponente mehrmals ausgelöst, wobei der Status des im *pValue* -Parameter aufgeführten Individualisierungs Vorgangs angegeben wird, der in einen Zeiger auf eine [**WM \_ Individual- \_ Status**](wm-individualize-status.md) Struktur umgewandelt wird.</span><span class="sxs-lookup"><span data-stu-id="015c3-125">This event will be fired multiple times by the DRM component with the status of the individualization process indicated in the *pValue* parameter, which is cast to a pointer to a [**WM\_INDIVIDUALIZE\_STATUS**](wm-individualize-status.md) structure.</span></span>

<span data-ttu-id="015c3-126">Nachdem die DRM-Komponente erfolgreich individualisiert wurde, empfängt die Anwendung ein **WMT \_ No \_ Rights \_ Ex** -Ereignis, das angibt, dass die Anwendung jetzt mit dem Erwerb einer Lizenz für den Inhalt fortfahren kann.</span><span class="sxs-lookup"><span data-stu-id="015c3-126">After the DRM component is successfully individualized, the application will receive a **WMT\_NO\_RIGHTS\_EX** event, indicating that the application can now proceed to acquire a license for the content.</span></span>

> [!Note]  
> <span data-ttu-id="015c3-127">DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="015c3-127">DRM is not supported by the x64-based version of this SDK.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="015c3-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="015c3-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="015c3-129">**Behandeln von Lizenz Erwerbs Ereignissen**</span><span class="sxs-lookup"><span data-stu-id="015c3-129">**Handling License Acquisition Events**</span></span>](handling-license-acquisition-events.md)
</dt> <dt>

[<span data-ttu-id="015c3-130">**Individualisieren von DRM-Anwendungen**</span><span class="sxs-lookup"><span data-stu-id="015c3-130">**Individualizing DRM Applications**</span></span>](individualizing-drm-applications.md)
</dt> <dt>

[<span data-ttu-id="015c3-131">**Iwmdrmreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="015c3-131">**IWMDRMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)
</dt> </dl>

 

 




