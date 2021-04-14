---
title: Herunterladen von Medieninhalten
description: Herunterladen von Medieninhalten
ms.assetid: 0a057e13-6e0c-4a8f-9cab-051183e6b222
keywords:
- Windows Media Player Online Stores, Herunterladen von Medieninhalten
- Online Stores, Herunterladen von Medieninhalten
- Typ 1 Online Stores, Herunterladen von Medieninhalten
- Windows Media Player Online Stores, Herunterladen von Medieninhalten
- Online Stores, Herunterladen von Medieninhalten
- Typ 1 Online Stores, Herunterladen von Medieninhalten
- Medieninhalt, herunterladen
- Herunterladen von Medieninhalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00efe44f2bac25a9eeda86f6adcc78b34beea7cd
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "104390044"
---
# <a name="downloading-media-content"></a><span data-ttu-id="06581-111">Herunterladen von Medieninhalten</span><span class="sxs-lookup"><span data-stu-id="06581-111">Downloading Media Content</span></span>

<span data-ttu-id="06581-112">Windows Media Player verarbeitet Musikdateien für den Online Shop.</span><span class="sxs-lookup"><span data-stu-id="06581-112">Windows Media Player handles music file downloads for the online store.</span></span> <span data-ttu-id="06581-113">Ein Download kann initiiert werden, wenn auf der Ermittlungs Seite " [extern. Download](external-download.md) " aufgerufen wird oder wenn der Benutzer im Player eine Gruppe von Spuren herunterlädt.</span><span class="sxs-lookup"><span data-stu-id="06581-113">A download can be initiated when the discovery page calls [External.download](external-download.md) or when the user chooses, in the Player, to download a set of tracks.</span></span> <span data-ttu-id="06581-114">In beiden Fällen ruft Windows Media Player [iwmpcontentpartner::D ownload](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download)auf und übergibt eine Inhalts Container Liste, die den Satz der herunter zuladenden Abrufe beschreibt, und ein Cookie, das die Download Transaktion darstellt.</span><span class="sxs-lookup"><span data-stu-id="06581-114">In either case, Windows Media Player calls [IWMPContentPartner::Download](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download), passing a content container list that describes the set of tracks to be downloaded and a cookie that represents the download transaction.</span></span> <span data-ttu-id="06581-115">Das Content Partner-Plug-in muss dann [iwmpcontentpartnercallback::D ownloadtrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) für jede Spur im Satz einmal aufruft.</span><span class="sxs-lookup"><span data-stu-id="06581-115">The content partner plug-in must then call [IWMPContentPartnerCallback::DownloadTrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) once for each track in the set.</span></span> <span data-ttu-id="06581-116">Wenn das Plug-in **downloadtrack** aufruft, übergibt es ein **HRESULT** in den *hrdownload* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="06581-116">When the plug-in calls **DownloadTrack**, it passes an **HRESULT** in the *hrDownload* parameter.</span></span> <span data-ttu-id="06581-117">Wenn das Plug-in einen Erfolgs Code in *hrdownload* übergibt, lädt Windows Media Player die Nachverfolgung herunter. Wenn das Plug-in einen Fehlercode in *hrdownload* übergibt, wird der Titel nicht vom Player heruntergeladen. Für jeden **Download Download** muss das Plug-in das Transaktions Cookie und die ID des fraglichen Titels bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="06581-117">If the plug-in passes a success code in *hrDownload*, Windows Media Player downloads the track. If the plug-in passes a failure code in *hrDownload*, the Player does not download the track. For each call to **Download**, the plug-in must supply the transaction cookie and the ID of the track in question.</span></span> <span data-ttu-id="06581-118">Bei nachverfolgen, die tatsächlich heruntergeladen werden, muss das Plug-in auch die URL des Titels bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="06581-118">For tracks that will actually be downloaded, the plug-in must also supply the URL of the track.</span></span>

<span data-ttu-id="06581-119">Nachdem eine Datei heruntergeladen wurde, wird die Bibliothek von Windows Media Player automatisch aktualisiert, um die neu erworbene Musik widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="06581-119">After a file is downloaded, Windows Media Player automatically updates the library to reflect the newly purchased music.</span></span> <span data-ttu-id="06581-120">Der Player stellt dem Plug-in über den Downloadvorgang Statusinformationen zur Verfügung, indem [iwmpcontentpartner::D ownloadtrackcomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete)aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="06581-120">The Player provides status information to the plug-in about the download operation by calling [IWMPContentPartner::DownloadTrackComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete).</span></span> <span data-ttu-id="06581-121">Bei dieser Methode stellt der Player ein **HRESULT** bereit, um den Erfolg oder Misserfolg des Downloads, die Spur-ID und die Zeichenfolge der benutzerdefinierten Parameter anzugeben, die der Online Shop beim Aufrufen von **downloadtrack** bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="06581-121">In this method, the Player provides an **HRESULT** to indicate success or failure of the download, the track ID, and the custom parameters string that the online store provided when it called **DownloadTrack**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06581-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="06581-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06581-123">**Programmier Handbuch für den Typ 1 Online Stores**</span><span class="sxs-lookup"><span data-stu-id="06581-123">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




