---
title: Install-Element
description: In diesem Abschnitt werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Das install-Element gibt Werte an, die von Windows Media Player verwendet werden, um einen Online Shop zu installieren.
ms.assetid: 9a5e15ee-ec36-48d3-a1c2-bf20b6d2da48
keywords:
- Element Windows-Media Player installieren
topic_type:
- apiref
api_name:
- Install Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bba56240651f789b45c18b006b16e5e07b10676e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372257"
---
# <a name="install-element"></a><span data-ttu-id="c6036-106">Install-Element</span><span class="sxs-lookup"><span data-stu-id="c6036-106">Install Element</span></span>

> [!Note]  
> <span data-ttu-id="c6036-107">In diesem Abschnitt werden die-Funktionen beschrieben, die für die Verwendung durch Online Stores</span><span class="sxs-lookup"><span data-stu-id="c6036-107">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="c6036-108">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c6036-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="c6036-109">Das **install** -Element gibt Werte an, die von Windows Media Player verwendet werden, um einen Online Shop zu installieren.</span><span class="sxs-lookup"><span data-stu-id="c6036-109">The **Install** element specifies values used by Windows Media Player to install an online store.</span></span>

``` syntax
<Install
    EULAURL = "URL"
    CodeURL = "URL"
    PrivacyInfoURL = "URL"
    InstallApp = "filename"
    InstallData = "commandline"
    CatalogURL = "URL"
/>
```

## <a name="attributes"></a><span data-ttu-id="c6036-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="c6036-110">Attributes</span></span>

<dl> <dt>

<span data-ttu-id="c6036-111"><span id="EULAURL__required_"></span><span id="eulaurl__required_"></span><span id="EULAURL__REQUIRED_"></span>**Eulaurl** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="c6036-111"><span id="EULAURL__required_"></span><span id="eulaurl__required_"></span><span id="EULAURL__REQUIRED_"></span>**EULAURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="c6036-112">Voll qualifizierte URL für eine Datei mit der Dateinamenerweiterung ". txt", die Windows Media Player verwendet, um einen Endbenutzer-Lizenzvertrag (EULA) anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c6036-112">Fully qualified URL for a file with a .txt file name extension that Windows Media Player uses to display an End User License Agreement (EULA).</span></span> <span data-ttu-id="c6036-113">Diese Datei muss im ANSI-Format codiert werden.</span><span class="sxs-lookup"><span data-stu-id="c6036-113">This file must be encoded in ANSI format.</span></span>

</dd> <dt>

<span data-ttu-id="c6036-114"><span id="CodeURL__required_"></span><span id="codeurl__required_"></span><span id="CODEURL__REQUIRED_"></span>**Codeurl** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="c6036-114"><span id="CodeURL__required_"></span><span id="codeurl__required_"></span><span id="CODEURL__REQUIRED_"></span>**CodeURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="c6036-115">Voll qualifizierte URL für ein Paket mit der Dateinamenerweiterung ". cab", die zur Installation des Online Ladens verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c6036-115">Fully qualified URL for a package, with a .cab file name extension, that is used to install the online store.</span></span> <span data-ttu-id="c6036-116">Das Paket und alle Code Module im Paket müssen signiert sein.</span><span class="sxs-lookup"><span data-stu-id="c6036-116">The package and all code modules in the package must be signed.</span></span> <span data-ttu-id="c6036-117">Weitere Informationen zum Signieren von Code finden Sie unter Einführung in die [Code Signatur](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) in der MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="c6036-117">For information about code signing, see [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) in the MSDN Library.</span></span>

</dd> <dt>

<span data-ttu-id="c6036-118"><span id="PrivacyInfoURL__required_"></span><span id="privacyinfourl__required_"></span><span id="PRIVACYINFOURL__REQUIRED_"></span>**Privacyinfourl** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="c6036-118"><span id="PrivacyInfoURL__required_"></span><span id="privacyinfourl__required_"></span><span id="PRIVACYINFOURL__REQUIRED_"></span>**PrivacyInfoURL** (required)</span></span>
</dt> <dd>

<span data-ttu-id="c6036-119">Voll qualifizierte URL für eine Webseite, die Informationen zu Datenschutzbestimmungen für den Online Store enthält.</span><span class="sxs-lookup"><span data-stu-id="c6036-119">Fully qualified URL for a webpage that contains privacy policy information for the online store.</span></span>

</dd> <dt>

<span data-ttu-id="c6036-120"><span id="InstallApp__required_"></span><span id="installapp__required_"></span><span id="INSTALLAPP__REQUIRED_"></span>**Installapp** (erforderlich)</span><span class="sxs-lookup"><span data-stu-id="c6036-120"><span id="InstallApp__required_"></span><span id="installapp__required_"></span><span id="INSTALLAPP__REQUIRED_"></span>**InstallApp** (required)</span></span>
</dt> <dd>

<span data-ttu-id="c6036-121">Der Name der exe-oder INF-Datei, die ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c6036-121">Name of the EXE or INF file to run.</span></span> <span data-ttu-id="c6036-122">Diese Datei muss in der vom Attribut " **codeurl** " angegebenen CAB-Datei enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="c6036-122">This file must be contained in the CAB file specified by the **CodeURL** attribute.</span></span>

</dd> <dt>

<span data-ttu-id="c6036-123"><span id="InstallData__optional_"></span><span id="installdata__optional_"></span><span id="INSTALLDATA__OPTIONAL_"></span>**Installdata** (optional)</span><span class="sxs-lookup"><span data-stu-id="c6036-123"><span id="InstallData__optional_"></span><span id="installdata__optional_"></span><span id="INSTALLDATA__OPTIONAL_"></span>**InstallData** (optional)</span></span>
</dt> <dd>

<span data-ttu-id="c6036-124">Befehlszeilen Zeichenfolge, die an die durch das **installapp** -Attribut angegebene Anwendung übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="c6036-124">Command-line string that is passed to the application specified by the **InstallApp** attribute.</span></span> <span data-ttu-id="c6036-125">Dieses Attribut ist nur anwendbar, wenn der Wert für **installapp** eine ausführbare Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="c6036-125">This attribute is only applicable when the value for **InstallApp** specifies an executable.</span></span>

</dd> <dt>

<span data-ttu-id="c6036-126"><span id="CatalogURL__required_for_type_1__ignored_for_type_2_"></span><span id="catalogurl__required_for_type_1__ignored_for_type_2_"></span><span id="CATALOGURL__REQUIRED_FOR_TYPE_1__IGNORED_FOR_TYPE_2_"></span>**Catalogurl** (erforderlich für Typ 1, wird für Typ 2 ignoriert)</span><span class="sxs-lookup"><span data-stu-id="c6036-126"><span id="CatalogURL__required_for_type_1__ignored_for_type_2_"></span><span id="catalogurl__required_for_type_1__ignored_for_type_2_"></span><span id="CATALOGURL__REQUIRED_FOR_TYPE_1__IGNORED_FOR_TYPE_2_"></span>**CatalogURL** (required for type 1, ignored for type 2)</span></span>
</dt> <dd>

<span data-ttu-id="c6036-127">Voll qualifizierte URL für den kompilierten Katalog des Online Stores.</span><span class="sxs-lookup"><span data-stu-id="c6036-127">Fully qualified URL for the online store's compiled catalog.</span></span>

</dd> </dl>

## <a name="parentchild-elements"></a><span data-ttu-id="c6036-128">Über-/unterordnungselemente</span><span class="sxs-lookup"><span data-stu-id="c6036-128">Parent/Child Elements</span></span>



| <span data-ttu-id="c6036-129">Hierarchy</span><span class="sxs-lookup"><span data-stu-id="c6036-129">Hierarchy</span></span>       | <span data-ttu-id="c6036-130">Element</span><span class="sxs-lookup"><span data-stu-id="c6036-130">Element</span></span>         |
|-----------------|-----------------|
| <span data-ttu-id="c6036-131">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c6036-131">Parent elements</span></span> | <span data-ttu-id="c6036-132">**ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="c6036-132">**ServiceInfo**</span></span> |
| <span data-ttu-id="c6036-133">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c6036-133">Child elements</span></span>  | <span data-ttu-id="c6036-134">Keine</span><span class="sxs-lookup"><span data-stu-id="c6036-134">None</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="c6036-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6036-135">Remarks</span></span>

<span data-ttu-id="c6036-136">Wenn eines der erforderlichen Attribute fehlt oder nicht verfügbar ist, versucht das Windows Media Player-Setup nicht, den Code des Online Store-Anbieters herunterzuladen und zu installieren.</span><span class="sxs-lookup"><span data-stu-id="c6036-136">If any of the required attributes are missing or not available, Windows Media Player setup will not attempt to download and install the online store provider code.</span></span> <span data-ttu-id="c6036-137">Setup konfiguriert die Offline Standardwerte entsprechend den Angaben im **serviceInfo** -Dokument.</span><span class="sxs-lookup"><span data-stu-id="c6036-137">Setup will configure the offline default values as specified in the **ServiceInfo** document.</span></span> <span data-ttu-id="c6036-138">**ServiceInfo** kann verwendet werden, wenn keine Internet Verbindung besteht, indem der Standardanbieter Name und die **serviceInfo** -Informationen als Befehlszeilenparameter übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="c6036-138">**ServiceInfo** can be used when not connected to the Internet by passing the default provider name and the **ServiceInfo** information as command-line parameters.</span></span> <span data-ttu-id="c6036-139">Ausführliche Informationen zu Befehlszeilenoptionen finden Sie unter [Neuverteilen von Windows Media Player-Software](redistributing-windows-media-player-software.md) .</span><span class="sxs-lookup"><span data-stu-id="c6036-139">See [Redistributing Windows Media Player Software](redistributing-windows-media-player-software.md) for details about command-line options.</span></span>

> [!Note]  
> <span data-ttu-id="c6036-140">Die Verwendung dieses Elements erfordert, dass Sie eine Verteilungs Vereinbarung mit Microsoft signieren.</span><span class="sxs-lookup"><span data-stu-id="c6036-140">Use of this element requires that you sign a redistribution agreement with Microsoft.</span></span> <span data-ttu-id="c6036-141">Weitere Informationen erhalten Sie von Ihrem Unternehmens Beauftragten.</span><span class="sxs-lookup"><span data-stu-id="c6036-141">Contact your business representative for details.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c6036-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c6036-142">Requirements</span></span>



| <span data-ttu-id="c6036-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c6036-143">Requirement</span></span> | <span data-ttu-id="c6036-144">Wert</span><span class="sxs-lookup"><span data-stu-id="c6036-144">Value</span></span> |
|--------------------|----------------------------------------------|
| <span data-ttu-id="c6036-145">Version</span><span class="sxs-lookup"><span data-stu-id="c6036-145">Version</span></span><br/> | <span data-ttu-id="c6036-146">Windows Media Player 10 oder höher.</span><span class="sxs-lookup"><span data-stu-id="c6036-146">Windows Media Player 10 or later.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c6036-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6036-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6036-148">**Beispiel eines serviceInfo-Dokuments für einen Online Store vom Typ 1**</span><span class="sxs-lookup"><span data-stu-id="c6036-148">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="c6036-149">**Beispiel eines serviceInfo-Dokuments für einen Typ 2-Online Store**</span><span class="sxs-lookup"><span data-stu-id="c6036-149">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="c6036-150">**Servicinfo-Dokument**</span><span class="sxs-lookup"><span data-stu-id="c6036-150">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

