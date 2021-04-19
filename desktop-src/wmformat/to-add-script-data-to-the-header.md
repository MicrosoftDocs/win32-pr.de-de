---
title: So fügen Sie dem Header Skript Daten hinzu
description: So fügen Sie dem Header Skript Daten hinzu
ms.assetid: 25f63d9e-c81a-4098-81d4-e848659a60e5
keywords:
- Windows Media-Format-SDK, Hinzufügen von Skript Daten zu Headern
- Advanced Systems Format (ASF), Hinzufügen von Skript Daten zu Headern
- ASF (Advanced Systems Format), Hinzufügen von Skript Daten zu Headern
- Skripts, Hinzufügen von Daten zu Headern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8052d8a5ae04b0ea821d716bf1931352c591f892
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "106339874"
---
# <a name="to-add-script-data-to-the-header"></a><span data-ttu-id="06b03-107">So fügen Sie dem Header Skript Daten hinzu</span><span class="sxs-lookup"><span data-stu-id="06b03-107">To Add Script Data to the Header</span></span>

<span data-ttu-id="06b03-108">Sie können Skript Befehle in den Header einer ASF-Datei einschließen.</span><span class="sxs-lookup"><span data-stu-id="06b03-108">You can include script commands in the header of an ASF file.</span></span> <span data-ttu-id="06b03-109">Um Skript Befehle zum Zeitpunkt der Codierung in den Header zu schreiben, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="06b03-109">To write script commands to the header at the time of encoding, perform the following steps.</span></span> <span data-ttu-id="06b03-110">Führen Sie diese Schritte vor dem Aufrufen von [**iwmwriter:: BeginWrite**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)aus.</span><span class="sxs-lookup"><span data-stu-id="06b03-110">Perform these steps prior to calling [**IWMWriter::BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

1.  <span data-ttu-id="06b03-111">Abrufen eines Zeigers auf die **iwmheaderinfo** -Schnittstelle durch Aufrufen von **iwmwriter:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="06b03-111">Obtain a pointer to the **IWMHeaderInfo** interface by calling **IWMWriter::QueryInterface**.</span></span>
2.  <span data-ttu-id="06b03-112">Fügen Sie jeden gewünschten Skript Befehl hinzu, indem Sie [**iwmheaderinfo:: addScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="06b03-112">Add each desired script command by calling [**IWMHeaderInfo::AddScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript).</span></span> <span data-ttu-id="06b03-113">Bei jedem Aufruf werden die beiden Zeichen folgen separat und die Darstellungs Zeit für den Befehl als Parameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="06b03-113">Each call takes the two strings separately and the presentation time to be used for the command as parameters.</span></span>

<span data-ttu-id="06b03-114">Wenn eine Anwendung die Datei liest, muss Sie alle Skript Befehle abrufen.</span><span class="sxs-lookup"><span data-stu-id="06b03-114">When an application reads the file, it will need to retrieve all of the script commands.</span></span> <span data-ttu-id="06b03-115">Führen Sie die folgenden Schritte aus, um alle Skript Befehle im Header einer Datei zu suchen.</span><span class="sxs-lookup"><span data-stu-id="06b03-115">To find all script commands in the header of a file, perform the following steps.</span></span> <span data-ttu-id="06b03-116">Dies sollte vor dem Starten der Wiedergabe erfolgen.</span><span class="sxs-lookup"><span data-stu-id="06b03-116">This should be done before starting playback.</span></span>

1.  <span data-ttu-id="06b03-117">Rufen Sie einen Zeiger auf die **iwmheaderinfo** -Schnittstelle des Reader-Objekts (oder des synchronen Reader-Objekts) ab, indem Sie die **QueryInterface** -Methode einer anderen Schnittstelle im-Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="06b03-117">Obtain a pointer to the **IWMHeaderInfo** interface of the reader object (or synchronous reader object) by calling the **QueryInterface** method of another interface in the object.</span></span>
2.  <span data-ttu-id="06b03-118">Rufen Sie die Gesamtanzahl der Skripts im Header ab, indem Sie [**iwmheaderinfo:: getscriptcount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="06b03-118">Get the total number of scripts in the header by calling [**IWMHeaderInfo::GetScriptCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount).</span></span>
3.  <span data-ttu-id="06b03-119">Durchlaufen Sie alle Skripts im Header einzeln mithilfe von Aufrufen von [**iwmheaderinfo:: GetScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript).</span><span class="sxs-lookup"><span data-stu-id="06b03-119">Loop through all of the scripts in the header one at a time using calls to [**IWMHeaderInfo::GetScript**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript).</span></span>
4.  <span data-ttu-id="06b03-120">Erstellen Sie eine Liste der Präsentations Zeiten, damit Ihre Anwendung zum richtigen Zeitpunkt auf die Befehle reagieren kann.</span><span class="sxs-lookup"><span data-stu-id="06b03-120">Create a list of the presentation times so that your application can react to the commands at the appropriate time.</span></span>

> [!Note]  
> <span data-ttu-id="06b03-121">Wenn Sie DRM zum Verschlüsseln einer Datei verwenden, kann kein Skript Befehl eine Präsentationszeit von 0 aufweisen.</span><span class="sxs-lookup"><span data-stu-id="06b03-121">When using DRM to encrypt a file, no script command can have a presentation time of 0.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="06b03-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="06b03-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06b03-123">**Iwmheaderinfo-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="06b03-123">**IWMHeaderInfo Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[<span data-ttu-id="06b03-124">**Iwmwriter-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="06b03-124">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="06b03-125">**Verwenden von Skript Befehlen**</span><span class="sxs-lookup"><span data-stu-id="06b03-125">**Using Script Commands**</span></span>](using-script-commands.md)
</dt> </dl>

 

 




