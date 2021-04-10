---
title: Protokollieren von Streamdaten
description: Protokollieren von Streamdaten
ms.assetid: c902a755-afdd-4dea-bc3e-036555fdff10
keywords:
- Windows Media Metadatei-Wiedergabelisten, Protokollieren von Streamdaten
- Wiedergabelisten, Protokollieren von Streamdaten
- Metadatei-Wiedergabelisten, Protokollieren von Streamdaten
- Windows Media Metadatei-Wiedergabelisten, Datenstrom Protokollierung
- Wiedergabelisten, Datenstrom Protokollierung
- Metadatei-Wiedergabelisten, Datenstrom Protokollierung
- Protokollieren von Streamdaten
- Datenstrom Protokollierung
- Windows Media Player, Protokollieren von Streamdaten
- Windows Media Player, Datenstrom Protokollierung
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f234851cabf071ed2308fb5c96df2b53b60b9d45
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100814"
---
# <a name="logging-stream-data"></a><span data-ttu-id="db543-113">Protokollieren von Streamdaten</span><span class="sxs-lookup"><span data-stu-id="db543-113">Logging Stream Data</span></span>

<span data-ttu-id="db543-114">Protokollierte Informationen können abgerufen und verwendet werden, um das Viewer-Verhalten zu ermitteln, z. b. wie oft ein Stream angezeigt wird, oder ob ein bestimmter Benutzer einen Stream und die Dauer der Qualität angezeigt hat.</span><span class="sxs-lookup"><span data-stu-id="db543-114">Logged information can be acquired and used to determine viewer behavior, for example, how often a stream is viewed, or if a specific user viewed a stream and for how long at what quality.</span></span>

<span data-ttu-id="db543-115">Protokollierungs Informationen werden automatisch an den Server gesendet, von dem aus die Wiedergabeliste stammt.</span><span class="sxs-lookup"><span data-stu-id="db543-115">Logging information is automatically sent to the server from which the playlist originated.</span></span> <span data-ttu-id="db543-116">Sie können Protokollierungs Informationen auch an zusätzliche Server senden, einschließlich Webservern, die ausschließlich für die Protokollierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="db543-116">You can also send logging information to additional servers, including web servers you use exclusively for logging.</span></span> <span data-ttu-id="db543-117">Verwenden Sie hierzu das **LogURL** -Element, und geben Sie eine gültige URL für das **href** -Attribut an.</span><span class="sxs-lookup"><span data-stu-id="db543-117">To do this, use the **LOGURL** element, specifying a valid URL for the **HREF** attribute.</span></span> <span data-ttu-id="db543-118">Sie können **LogURL** -Elemente als untergeordnete Elemente des Elements **ASX** und als untergeordnete Elemente einzelner **Einstiegs** Elemente einschließen.</span><span class="sxs-lookup"><span data-stu-id="db543-118">You can include **LOGURL** elements as children of the **ASX** element and as children of individual **ENTRY** elements.</span></span> <span data-ttu-id="db543-119">Wenn die Wiedergabeliste erstmalig geöffnet wird, werden Protokollierungs Informationen an den Ursprungsserver und an jede URL gesendet **, die unter den unter** geordneten **LogURL** -Elementen des-Elements angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="db543-119">When the playlist is first opened, logging information is sent to the origin server and to each URL specified in **LOGURL** children of the **ASX** element.</span></span> <span data-ttu-id="db543-120">Wenn dann jeder Eintrag erreicht wird, werden für diesen Eintrag spezifische Protokollierungs Informationen an jede URL gesendet, die unter den untergeordneten **LogURL** -Daten des **Entry** -Elements angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="db543-120">Then, as each entry is reached, logging information specific to that entry is sent to each URL specified in **LOGURL** children of the **ENTRY** element.</span></span>

<span data-ttu-id="db543-121">Das Windows Media-Format-SDK unterstützt das **LogURL** -Element über die **iwmsreadernetworkconfig** -Schnittstelle und die folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="db543-121">The Windows Media Format SDK supports the **LOGURL** element through the **IWMSReaderNetworkConfig** interface and the following methods:</span></span>


```XML
HRESULT AddLoggingUrl(LPCWSTR pwszUrl);
HRESULT GetLoggingUrl(DWORD dwIndex, LPCWSTR pwszUrl, DWORD *pcchUrl);
HRESULT GetLoggingUrlCount(DWORD *pdwUrlCount);
HRESULT ResetLoggingUrlList();

```



<span data-ttu-id="db543-122">Zusätzlich zu den Informationen, die automatisch protokolliert werden, kann eine Metadatei-Wiedergabeliste benutzerdefinierte Informationen mithilfe des **param** -Elements protokollieren.</span><span class="sxs-lookup"><span data-stu-id="db543-122">In addition to the information that is automatically logged, a metafile playlist can log custom information through the use of the **PARAM** element.</span></span> <span data-ttu-id="db543-123">Wenn Sie das **param** -Element auf diese Weise verwenden möchten, legen Sie das **Name** -Attribut auf "Log:" gefolgt von einem Protokoll Feldnamen und einem optionalen XML-Namespace fest, der vom Feldnamen durch einen anderen Doppelpunkt (":") getrennt ist.</span><span class="sxs-lookup"><span data-stu-id="db543-123">To use the **PARAM** element in this way, set the **NAME** attribute to "log:" followed by a log field name and an optional XML namespace separated from the field name by another colon (":").</span></span> <span data-ttu-id="db543-124">Alles nach dem zweiten Doppelpunkt wird als Namespace behandelt, sodass der Feldname keinen Doppelpunkt enthalten sollte.</span><span class="sxs-lookup"><span data-stu-id="db543-124">Everything after the second colon is treated as a namespace, so the field name should not contain a colon.</span></span>

<span data-ttu-id="db543-125">Das im **Name** -Attribut angegebene Protokollfeld wird auf den Wert des **value** -Attributs festgelegt.</span><span class="sxs-lookup"><span data-stu-id="db543-125">The log field specified in the **NAME** attribute is set to the value of the **VALUE** attribute.</span></span> <span data-ttu-id="db543-126">Wenn das Protokoll nicht bereits ein Feld mit dem angegebenen Namen enthält, wird es hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="db543-126">If the log does not already contain a field with the specified name, it will be added.</span></span>

<span data-ttu-id="db543-127">**Beispiel Code**</span><span class="sxs-lookup"><span data-stu-id="db543-127">**Example Code**</span></span>


```XML

    <ASX version="3.0">
      <LOGURL href="https://www.proseware.com/log.asp?SomeArg=SomeVal" />
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media1.wma" />
        <LOGURL href="https://www.proseware.com/cgi-bin/logging.pl?SomeArg=SomeVal" />
        <LOGURL href="https://www.proseware.com/WMLogging.dll?SomeArg=SomeVal" />
        <PARAM name="log:cs-media-role" value="Advertisement"/>
        <PARAM name="log:cs-media-name:namespace" value="Music"/>
        <REF href=rtsp://ucast.proseware.com/Media1.wma"/>
      </ENTRY>
      <ENTRY>
        <REF href="mms://ucast.proseware.com/Media2.wma"/>
      </ENTRY>
    </ASX>
    

```



## <a name="related-topics"></a><span data-ttu-id="db543-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="db543-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db543-129">**Metafile-Wiedergabelisten**</span><span class="sxs-lookup"><span data-stu-id="db543-129">**Metafile Playlists**</span></span>](metafile-playlists.md)
</dt> <dt>

[<span data-ttu-id="db543-130">**Verweis auf Windows Media-Metadateielemente**</span><span class="sxs-lookup"><span data-stu-id="db543-130">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




