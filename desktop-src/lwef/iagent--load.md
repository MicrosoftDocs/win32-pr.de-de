---
title: IAgent Load
description: IAgent Load
ms.assetid: 8f25e6b6-a117-4b37-969a-d8f80c7be224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ce2835d60f3edce6f45d181927437ba6e58b18
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120933"
---
# <a name="iagentload"></a><span data-ttu-id="e42c8-103">IAgent::Load</span><span class="sxs-lookup"><span data-stu-id="e42c8-103">IAgent::Load</span></span>

<span data-ttu-id="e42c8-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="e42c8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Load(
   VARIANT vLoadKey,  // data provider
   long * pdwCharID,  // address of a variable for character ID
   long * pdwReqID    // address of a variable for request ID
);
```

<span data-ttu-id="e42c8-105">Lädt ein Zeichen in die [**Characters-Auflistung.**](./iagent.md)</span><span class="sxs-lookup"><span data-stu-id="e42c8-105">Loads a character into the [**Characters**](./iagent.md) collection.</span></span>

-   <span data-ttu-id="e42c8-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="e42c8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e42c8-107"><span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*</span><span class="sxs-lookup"><span data-stu-id="e42c8-107"><span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*</span></span>
</dt> <dd>

<span data-ttu-id="e42c8-108">Ein variant-Datentyp, der einen der folgenden Sein muss:</span><span class="sxs-lookup"><span data-stu-id="e42c8-108">A variant datatype that must be one of the following:</span></span>



| <span data-ttu-id="e42c8-109">Wert</span><span class="sxs-lookup"><span data-stu-id="e42c8-109">Value</span></span>           | <span data-ttu-id="e42c8-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e42c8-110">Description</span></span>                                                                      |
|------------|-----------------------------------------------------------------------|
| <span data-ttu-id="e42c8-111">*Dateinamen*</span><span class="sxs-lookup"><span data-stu-id="e42c8-111">*filespec*</span></span> | <span data-ttu-id="e42c8-112">Der lokale Dateispeicherort der Definitionsdatei des angegebenen Zeichens.</span><span class="sxs-lookup"><span data-stu-id="e42c8-112">The local file location of the specified character's definition file.</span></span> |
| <span data-ttu-id="e42c8-113">*URL*</span><span class="sxs-lookup"><span data-stu-id="e42c8-113">*URL*</span></span>      | <span data-ttu-id="e42c8-114">Die HTTP-Adresse für die Definitionsdatei des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="e42c8-114">The HTTP address for the character's definition file.</span></span>                 |



 

</dd> <dt>

<span data-ttu-id="e42c8-115"><span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*</span><span class="sxs-lookup"><span data-stu-id="e42c8-115"><span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="e42c8-116">Adresse einer Variablen, die die ID des Zeichens empfängt.</span><span class="sxs-lookup"><span data-stu-id="e42c8-116">Address of a variable that receives the character's ID.</span></span>

</dd> <dt>

<span data-ttu-id="e42c8-117"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="e42c8-117"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="e42c8-118">Adresse einer Variablen, die die [**Load-Anforderungs-ID**](load-method.md) empfängt.</span><span class="sxs-lookup"><span data-stu-id="e42c8-118">Address of a variable that receives the [**Load**](load-method.md) request ID.</span></span>

</dd> </dl>

<span data-ttu-id="e42c8-119">Sie können Zeichen aus dem Microsoft-Agent-Unterverzeichnis laden, indem Sie einen relativen Pfad angeben (einen Pfad, der keinen Doppelpunkt oder führenden Schrägstrich enthält).</span><span class="sxs-lookup"><span data-stu-id="e42c8-119">You can load characters from the Microsoft Agent subdirectory by specifying a relative path (one that does not include a colon or leading slash character).</span></span> <span data-ttu-id="e42c8-120">Dadurch wird dem Pfad das Zeichenverzeichnis des -Agents vorangestellt (im lokalisierten Verzeichnis %windows% \\ msagent).</span><span class="sxs-lookup"><span data-stu-id="e42c8-120">This prefixes the path with Agent's characters directory (located in the localized %windows%\\msagent directory).</span></span> <span data-ttu-id="e42c8-121">Sie können auch eine relative Adresse verwenden, um Ihr eigenes Verzeichnis im Chars-Verzeichnis des Agents anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e42c8-121">You can also use a relative address to specify your own directory in Agent's Chars directory.</span></span>

<span data-ttu-id="e42c8-122">Sie können das gleiche Zeichen (ein Zeichen mit derselben GUID) nicht mehr als einmal aus einer einzelnen Verbindung laden.</span><span class="sxs-lookup"><span data-stu-id="e42c8-122">You cannot load the same character (a character having the same GUID) more than once from a single connection.</span></span> <span data-ttu-id="e42c8-123">Ebenso können Sie das Standardzeichen und andere Zeichen nicht gleichzeitig aus einer einzelnen Verbindung laden, da das Standardzeichen mit dem anderen Zeichen identisch sein kann.</span><span class="sxs-lookup"><span data-stu-id="e42c8-123">Similarly, you cannot load the default character and other characters at the same time from a single connection, because the default character could be the same as the other character.</span></span> <span data-ttu-id="e42c8-124">Sie können jedoch eine weitere Verbindung (mit CoCreateInstance) erstellen und das gleiche Zeichen laden.</span><span class="sxs-lookup"><span data-stu-id="e42c8-124">However, you can create another connection (using CoCreateInstance) and load the same character.</span></span>

<span data-ttu-id="e42c8-125">Der Datenanbieter des Microsoft-Agents unterstützt das Laden von Zeichendaten, die als einzelne strukturierte Datei gespeichert sind (. ACS) mit Zeichendaten und Animationsdaten zusammen oder als separate Zeichendaten (. ACF) und Animation (. ACA)-Dateien.</span><span class="sxs-lookup"><span data-stu-id="e42c8-125">Microsoft Agent's data provider supports loading character data stored as a single structured file (.ACS) with character data and animation data together, or as separate character data (.ACF) and animation (.ACA) files.</span></span> <span data-ttu-id="e42c8-126">Verwenden Sie im Allgemeinen die einzelne strukturierte . ACS-Datei zum Laden eines Zeichens, das auf einem lokalen Laufwerk oder Netzwerk gespeichert ist und auf das mithilfe eines herkömmlichen Dateiprotokolls (z. B. UNC-Pfadnamen) zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="e42c8-126">Generally, use the single structured .ACS file to load a character that is stored on a local disk drive or network and accessed using conventional file protocol (such as UNC pathnames).</span></span> <span data-ttu-id="e42c8-127">Verwenden Sie die separate . ACF und . ACA-Dateien, wenn Sie die Animationsdateien einzeln von einem Remotestandort laden möchten, auf den über das HTTP-Protokoll zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="e42c8-127">Use the separate .ACF and .ACA files when you want to load the animation files individually from a remote site where they are accessed using HTTP protocol.</span></span>

<span data-ttu-id="e42c8-128">Für. ACS-Dateien, die die [**Load-Methode**](load-method.md) verwenden, bieten Zugriff auf die Animationen eines Zeichens. Nach dem Laden können Sie die [**Play-Methode**](play-method.md) verwenden, um das Zeichen zu animieren.</span><span class="sxs-lookup"><span data-stu-id="e42c8-128">For .ACS files, using the [**Load**](load-method.md) method provides access a character's animations; once loaded, you can use the [**Play**](play-method.md) method to animate the character.</span></span> <span data-ttu-id="e42c8-129">Für. ACF-Dateien verwenden Sie auch die [**Prepare-Methode,**](/windows/desktop/lwef/iagentcharacter--prepare) um Animationsdaten zu laden.</span><span class="sxs-lookup"><span data-stu-id="e42c8-129">For .ACF files, you also use the [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) method to load animation data.</span></span> <span data-ttu-id="e42c8-130">Das Herunterladen von wird von der **Load-Methode** nicht unterstützt. ACS-Dateien von einer HTTP-Website.</span><span class="sxs-lookup"><span data-stu-id="e42c8-130">The **Load** method does not support downloading .ACS files from an HTTP site.</span></span>

<span data-ttu-id="e42c8-131">Beim Laden eines Zeichens wird das Zeichen nicht automatisch angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e42c8-131">Loading a character does not automatically display the character.</span></span> <span data-ttu-id="e42c8-132">Verwenden [](show-method.md) Sie zuerst die Show-Methode, um das Zeichen sichtbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="e42c8-132">Use the [**Show**](show-method.md) method first to make the character visible.</span></span>

 

 