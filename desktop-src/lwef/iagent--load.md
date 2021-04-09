---
title: Iagent-Auslastung
description: Iagent-Auslastung
ms.assetid: 8f25e6b6-a117-4b37-969a-d8f80c7be224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e30a25abb631714384f8349a9d260deade0d6d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948719"
---
# <a name="iagentload"></a><span data-ttu-id="144f7-103">Iagent:: Load</span><span class="sxs-lookup"><span data-stu-id="144f7-103">IAgent::Load</span></span>

<span data-ttu-id="144f7-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="144f7-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Load(
   VARIANT vLoadKey,  // data provider
   long * pdwCharID,  // address of a variable for character ID
   long * pdwReqID    // address of a variable for request ID
);
```

<span data-ttu-id="144f7-105">Lädt ein Zeichen in die [**Zeichen**](./iagent.md) Auflistung.</span><span class="sxs-lookup"><span data-stu-id="144f7-105">Loads a character into the [**Characters**](./iagent.md) collection.</span></span>

-   <span data-ttu-id="144f7-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="144f7-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="144f7-107"><span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vloadkey*</span><span class="sxs-lookup"><span data-stu-id="144f7-107"><span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*</span></span>
</dt> <dd>

<span data-ttu-id="144f7-108">Ein Variant-Datentyp, bei dem es sich um einen der folgenden Typen handeln muss:</span><span class="sxs-lookup"><span data-stu-id="144f7-108">A variant datatype that must be one of the following:</span></span>



|            |                                                                       |
|------------|-----------------------------------------------------------------------|
| <span data-ttu-id="144f7-109">*Datei Angabe*</span><span class="sxs-lookup"><span data-stu-id="144f7-109">*filespec*</span></span> | <span data-ttu-id="144f7-110">Der lokale Datei Speicherort der Definitionsdatei des angegebenen Zeichens.</span><span class="sxs-lookup"><span data-stu-id="144f7-110">The local file location of the specified character's definition file.</span></span> |
| <span data-ttu-id="144f7-111">*URL*</span><span class="sxs-lookup"><span data-stu-id="144f7-111">*URL*</span></span>      | <span data-ttu-id="144f7-112">Die http-Adresse für die Definitionsdatei des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="144f7-112">The HTTP address for the character's definition file.</span></span>                 |



 

</dd> <dt>

<span data-ttu-id="144f7-113"><span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwcharid*</span><span class="sxs-lookup"><span data-stu-id="144f7-113"><span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="144f7-114">Adresse einer Variablen, die die ID des Zeichens empfängt.</span><span class="sxs-lookup"><span data-stu-id="144f7-114">Address of a variable that receives the character's ID.</span></span>

</dd> <dt>

<span data-ttu-id="144f7-115"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwreqid*</span><span class="sxs-lookup"><span data-stu-id="144f7-115"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="144f7-116">Adresse einer Variablen, die die [**Auslastungs**](load-method.md) Anforderungs-ID empfängt.</span><span class="sxs-lookup"><span data-stu-id="144f7-116">Address of a variable that receives the [**Load**](load-method.md) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="144f7-117">Sie können Zeichen aus dem Unterverzeichnis Microsoft Agent laden, indem Sie einen relativen Pfad angeben (einer, der keinen Doppelpunkt oder vorangestellenden Schrägstrich enthält).</span><span class="sxs-lookup"><span data-stu-id="144f7-117">You can load characters from the Microsoft Agent subdirectory by specifying a relative path (one that does not include a colon or leading slash character).</span></span> <span data-ttu-id="144f7-118">Dadurch wird der Pfad mit dem Zeichen Verzeichnis des Agents (befindet sich im lokalisierten% Windows% \\ MSAgent-Verzeichnis) als Präfix versehen.</span><span class="sxs-lookup"><span data-stu-id="144f7-118">This prefixes the path with Agent's characters directory (located in the localized %windows%\\msagent directory).</span></span> <span data-ttu-id="144f7-119">Sie können auch eine relative Adresse verwenden, um Ihr eigenes Verzeichnis im chars-Verzeichnis des Agents anzugeben.</span><span class="sxs-lookup"><span data-stu-id="144f7-119">You can also use a relative address to specify your own directory in Agent's Chars directory.</span></span>

<span data-ttu-id="144f7-120">Es ist nicht möglich, dasselbe Zeichen (ein Zeichen mit derselben GUID) mehrmals aus einer einzelnen Verbindung zu laden.</span><span class="sxs-lookup"><span data-stu-id="144f7-120">You cannot load the same character (a character having the same GUID) more than once from a single connection.</span></span> <span data-ttu-id="144f7-121">Ebenso können Sie das Standard Zeichen und andere Zeichen nicht gleichzeitig von einer einzelnen Verbindung laden, da das Standard Zeichen mit dem anderen Zeichen identisch sein könnte.</span><span class="sxs-lookup"><span data-stu-id="144f7-121">Similarly, you cannot load the default character and other characters at the same time from a single connection, because the default character could be the same as the other character.</span></span> <span data-ttu-id="144f7-122">Sie können jedoch eine weitere Verbindung (mit cokreatanstance) erstellen und das gleiche Zeichen laden.</span><span class="sxs-lookup"><span data-stu-id="144f7-122">However, you can create another connection (using CoCreateInstance) and load the same character.</span></span>

<span data-ttu-id="144f7-123">Der Microsoft Agent-Datenanbieter unterstützt das Laden von Zeichendaten, die als einzelne strukturierte Datei () gespeichert sind. ACS) mit Zeichendaten und Animationsdaten oder als separate Zeichendaten (. ACF) und Animation (. ACA-Dateien.</span><span class="sxs-lookup"><span data-stu-id="144f7-123">Microsoft Agent's data provider supports loading character data stored as a single structured file (.ACS) with character data and animation data together, or as separate character data (.ACF) and animation (.ACA) files.</span></span> <span data-ttu-id="144f7-124">Verwenden Sie im Allgemeinen die strukturierte Struktur. Die ACS-Datei zum Laden eines Zeichens, das auf einem lokalen Laufwerk oder Netzwerk gespeichert ist und auf das ein herkömmliches Datei Protokoll (z. b. UNC-Pfadnamen) zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="144f7-124">Generally, use the single structured .ACS file to load a character that is stored on a local disk drive or network and accessed using conventional file protocol (such as UNC pathnames).</span></span> <span data-ttu-id="144f7-125">Verwenden Sie die separate. ACF und. ACA-Dateien, wenn Sie die Animationsdateien einzeln von einer Remote Site laden möchten, auf die über das HTTP-Protokoll zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="144f7-125">Use the separate .ACF and .ACA files when you want to load the animation files individually from a remote site where they are accessed using HTTP protocol.</span></span>

<span data-ttu-id="144f7-126">Damit. ACS-Dateien, die die [**Load**](load-method.md) -Methode verwenden, bieten Zugriff auf die Animationen eines Zeichens. nach dem Laden können Sie das Zeichen mit der [**Play**](play-method.md) -Methode animieren.</span><span class="sxs-lookup"><span data-stu-id="144f7-126">For .ACS files, using the [**Load**](load-method.md) method provides access a character's animations; once loaded, you can use the [**Play**](play-method.md) method to animate the character.</span></span> <span data-ttu-id="144f7-127">Damit. ACF-Dateien verwenden Sie auch die [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) -Methode, um Animationsdaten zu laden.</span><span class="sxs-lookup"><span data-stu-id="144f7-127">For .ACF files, you also use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to load animation data.</span></span> <span data-ttu-id="144f7-128">Die **Load** -Methode unterstützt nicht das herunterladen. ACS-Dateien von einer HTTP-Site.</span><span class="sxs-lookup"><span data-stu-id="144f7-128">The **Load** method does not support downloading .ACS files from an HTTP site.</span></span>

<span data-ttu-id="144f7-129">Beim Laden eines Zeichens wird das Zeichen nicht automatisch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="144f7-129">Loading a character does not automatically display the character.</span></span> <span data-ttu-id="144f7-130">Verwenden Sie zuerst die [**Show**](show-method.md) -Methode, um das Zeichen sichtbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="144f7-130">Use the [**Show**](show-method.md) method first to make the character visible.</span></span>

 

 