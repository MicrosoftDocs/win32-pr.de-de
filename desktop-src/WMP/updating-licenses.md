---
title: Aktualisieren von Lizenzen
description: Aktualisieren von Lizenzen
ms.assetid: b298badf-efcf-423c-8cc7-c3f50ab288a0
keywords:
- Windows Media Player Online Stores, Aktualisieren von Lizenzen
- Online Stores, Aktualisieren von Lizenzen
- Geben Sie 1 Online Stores ein, aktualisieren Sie Lizenzen.
- Windows Media Player Online Stores, Lizenz Aktualisierung
- Online Stores, Lizenz Aktualisierung
- Typ 1 Online Stores, Lizenz Aktualisierung
- Aktualisieren von Lizenzen
- Lizenzen, aktualisieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 154959b01c93719184e310b60dffaa91fe2dcfa0
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314273"
---
# <a name="updating-licenses"></a><span data-ttu-id="3b57e-111">Aktualisieren von Lizenzen</span><span class="sxs-lookup"><span data-stu-id="3b57e-111">Updating Licenses</span></span>

<span data-ttu-id="3b57e-112">Online Stores können Inhalte bereitzustellen, die für einen bestimmten Zeitraum oder bis zu einem bestimmten Zeitpunkt lizenziert sind.</span><span class="sxs-lookup"><span data-stu-id="3b57e-112">Online stores can deliver content that is licensed for a specific period of time or until a certain date.</span></span> <span data-ttu-id="3b57e-113">Dies wäre normal für Musikinhalte, die als Teil einer Abonnement Dienstvereinbarung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3b57e-113">This would be normal for music content delivered as part of a subscription service agreement.</span></span> <span data-ttu-id="3b57e-114">In diesem Fall benötigt der Online Shop eine Gelegenheit, diese Lizenzen zu aktualisieren, bevor Sie ablaufen. dabei wird davon ausgegangen, dass der Benutzer zum erneuern seines Abonnements bezahlt hat.</span><span class="sxs-lookup"><span data-stu-id="3b57e-114">In this case, the online store needs an opportunity to update these licenses before they expire, assuming, of course, that the user has paid to renew his or her subscription.</span></span> <span data-ttu-id="3b57e-115">(Wenn der Benutzer das Abonnement nicht erneuert hat, kann es sein, dass die Lizenzen einfach ablaufen lassen.)</span><span class="sxs-lookup"><span data-stu-id="3b57e-115">(If the user has not renewed the subscription, the licenses can simply be left to expire.)</span></span>

<span data-ttu-id="3b57e-116">Windows Media Player fragt das Content Partner-Plug-in darüber ab, wie weit die vorab Warnung angezeigt werden soll, die der Player über eine zu ablaufende Lizenz bereitstellen sollte.</span><span class="sxs-lookup"><span data-stu-id="3b57e-116">Windows Media Player queries the content partner plug-in about how much advance warning the Player should provide about a license that is about to expire.</span></span> <span data-ttu-id="3b57e-117">Dies erfolgt durch Aufrufen von [iwmpcontentpartner:: getcontentpartnerinfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo), wobei die Konstante g \_ szcontentpartnerinfo \_ licenserefreshadvancewarning über den *bstrinfoname* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3b57e-117">It does this by calling [IWMPContentPartner::GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo), passing the constant g\_szContentPartnerInfo\_LicenseRefreshAdvanceWarning through the *bstrInfoName* parameter.</span></span> <span data-ttu-id="3b57e-118">Um das Plug-in über die ablaufenden Lizenzen zu benachrichtigen, ruft Windows Media Player die [iwmpcontentpartner:: erfrischendes-Lizenz](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense)auf.</span><span class="sxs-lookup"><span data-stu-id="3b57e-118">To alert the plug-in about licenses that are about to expire, Windows Media Player calls [IWMPContentPartner::RefreshLicense](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-refreshlicense).</span></span> <span data-ttu-id="3b57e-119">Dieser Befehl erfordert Parameter, die Details zu der aktualisierten Datei bereitstellen, z. b. ob sich die Datei auf dem Computer des Benutzers befindet, und den Pfad zur Datei.</span><span class="sxs-lookup"><span data-stu-id="3b57e-119">This call takes parameters that provide details about the file being refreshed, such as whether the file is on the user's computer, and the path to the file.</span></span> <span data-ttu-id="3b57e-120">Wenn die Lizenz im Rahmen eines Geräte Synchronisierungs Vorgangs aktualisiert wird, gibt der *preasoncontext* -Parameter den kanonischen Namen des Geräts an.</span><span class="sxs-lookup"><span data-stu-id="3b57e-120">If the license is being refreshed as part of a device synchronization operation, the *pReasonContext* parameter supplies the cannonical name of the device</span></span>

<span data-ttu-id="3b57e-121">Wenn Windows Media Player die Aktualisierungs **Lizenz** aufruft, übergibt es ein Cookie, das die Aktualisierungs Anforderung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="3b57e-121">When Windows Media Player calls **RefreshLicence**, it passes a cookie that identifies the update request.</span></span> <span data-ttu-id="3b57e-122">Wenn das Plug-in die Verarbeitung der Update Anforderung abgeschlossen hat, benachrichtigt es Windows Media Player durch den Aufruf von [iwmpcontentpartnercallback:: erfrischendes licensecomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete), übergibt das Cookie, die ID des Medien Elements und ein **HRESULT** , das angibt, ob das Update erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="3b57e-122">When the plug-in has finished processing the update request, it notifies Windows Media Player by calling [IWMPContentPartnerCallback::RefreshLicenseComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-refreshlicensecomplete), passing the cookie, the ID of the media item, and an **HRESULT** that indicates whether the update was successful.</span></span>

<span data-ttu-id="3b57e-123">Online Store-Plug-Ins können auch eine Lizenz Überprüfung und Updates als Hintergrundprozess durchführen.</span><span class="sxs-lookup"><span data-stu-id="3b57e-123">Online store plug-ins can also do license inspection and updates as a background process.</span></span> <span data-ttu-id="3b57e-124">Das Plug-in wird von Windows Media Player benachrichtigt, wenn es zulässig ist, Hintergrund Verarbeitungsaufgaben durch Aufrufen von [iwmpcontentpartner:: notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify)auszuführen.</span><span class="sxs-lookup"><span data-stu-id="3b57e-124">Windows Media Player notifies the plug-in about times when it is permissible to perform background processing tasks by calling [IWMPContentPartner::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify).</span></span> <span data-ttu-id="3b57e-125">Um dem Plug-in zu signalisieren, dass die Hintergrundverarbeitung gestartet werden soll, übergibt der Spieler den [wmppartnernotification](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification) -Enumerationswert "wmpsnbackgroundprocessingbegin;". um dem Plug-in zu signalisieren, dass die Hintergrundverarbeitung beendet werden soll, übergibt der Spieler den Wert wmpsnbackgroundprocessingend.</span><span class="sxs-lookup"><span data-stu-id="3b57e-125">To signal the plug-in to start background processing, the Player passes the [WMPPartnerNotification](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmppartnernotification) enumeration value wmpsnBackgroundProcessingBegin; to signal the plug-in to stop background processing, the Player passes the value wmpsnBackgroundProcessingEnd.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b57e-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3b57e-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b57e-127">**Programmier Handbuch für den Typ 1 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="3b57e-127">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




