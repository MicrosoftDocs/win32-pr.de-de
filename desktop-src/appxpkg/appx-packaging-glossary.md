---
title: Glossar für Verpacken, Bereitstellung und Abfrage
description: Enthält Definitionen für Begriffe im Zusammenhang mit der Paket Erstellung, Bereitstellung und Abfrage von Windows-apps.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 15E35DCF-C6C1-446A-B09B-6428F9C8A677
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83a2112b593e2d2a5aaf4f06525160e2d799bad1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104390135"
---
# <a name="packaging-deployment-and-query-glossary"></a><span data-ttu-id="f7e9a-103">Glossar für Verpacken, Bereitstellung und Abfrage</span><span class="sxs-lookup"><span data-stu-id="f7e9a-103">Packaging, deployment, and query glossary</span></span>

<dl> <dt>

<span data-ttu-id="f7e9a-104"><span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**ID des Anwendungs Benutzer Modells**</span><span class="sxs-lookup"><span data-stu-id="f7e9a-104"><span id="appxpkg.appx_packaging_glossary_application_user_model_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_APPLICATION_USER_MODEL_ID"></span>**application user model ID**</span></span>
</dt> <dd>

<span data-ttu-id="f7e9a-105">Mit der App-Benutzer Modell-ID wird eine APP auf dem Betriebssystem eindeutig identifiziert, damit das Betriebssystem Benachrichtigungen an die APP senden kann.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-105">The application user model ID uniquely identifies an app on the operating system so the operating system can send notifications and so on to the app.</span></span>

</dd> <dt>

<span data-ttu-id="f7e9a-106"><span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**Zuordnung blockieren**</span><span class="sxs-lookup"><span data-stu-id="f7e9a-106"><span id="appxpkg.appx_packaging_glossary_block_map"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_BLOCK_MAP"></span>**block map**</span></span>
</dt> <dd>

<span data-ttu-id="f7e9a-107">Definiert die Indizes und kryptografischen Hashes für Blöcke ausführbaren Codes und Daten, die in den Dateien eines App-Pakets gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-107">Defines the indices and cryptographic hashes for blocks of executable code and data that are stored in the files of an app package.</span></span> <span data-ttu-id="f7e9a-108">Für jedes app-Paket ist eine BlockMap.xml-Datei erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-108">A BlockMap.xml file is required for every app package.</span></span>

</dd> <dt>

<span data-ttu-id="f7e9a-109"><span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**Abhängigkeits Paket**</span><span class="sxs-lookup"><span data-stu-id="f7e9a-109"><span id="appxpkg.appx_packaging_glossary_dependency_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENCY_PACKAGE"></span>**dependency package**</span></span>
</dt> <dd>

<span data-ttu-id="f7e9a-110">Ein Paket, von dem ein anderes Paket abhängt.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-110">A package on which another package depends.</span></span> <span data-ttu-id="f7e9a-111">Die Abhängigkeit wird im Manifest des abhängigen Pakets deklariert, nicht im Manifest des Abhängigkeits Pakets.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-111">The dependency is declared in the dependent package's manifest and not in the dependency package's manifest.</span></span>

</dd> <dt>

<span data-ttu-id="f7e9a-112"><span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**abhängiges Paket**</span><span class="sxs-lookup"><span data-stu-id="f7e9a-112"><span id="appxpkg.appx_packaging_glossary_dependent_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_DEPENDENT_PACKAGE"></span>**dependent package**</span></span>
</dt> <dd>

<span data-ttu-id="f7e9a-113">Ein Paket, das eine Abhängigkeit von einem anderen Paket annimmt.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-113">A package that takes a dependency on another package.</span></span> <span data-ttu-id="f7e9a-114">Die Abhängigkeit wird im Manifest des abhängigen Pakets deklariert.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-114">The dependency is declared in the dependent package's manifest.</span></span>

</dd> <dt>

<span data-ttu-id="f7e9a-115"><span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**Dateien mit Speicherbedarf**</span><span class="sxs-lookup"><span data-stu-id="f7e9a-115"><span id="appxpkg_packaging_glossary_footpint_files"></span><span id="APPXPKG_PACKAGING_GLOSSARY_FOOTPINT_FILES"></span>**footprint files**</span></span>
</dt> <dd>

<span data-ttu-id="f7e9a-116">Dateien innerhalb eines App-Pakets, die nicht Teil der APP sind, die bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-116">Files within an app package that are not part of the app to be deployed.</span></span> <span data-ttu-id="f7e9a-117">Diese Dateien stellen Metadaten für das Paket bereit.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-117">These files provide metadata pertaining to the package.</span></span> <span data-ttu-id="f7e9a-118">Standard Dateien für den Speicherbedarf sind das Manifest, Block Map, Stream Map und digitale Signatur.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-118">Standard footprint files include the manifest, block map, stream map, and digital signature.</span></span> <span data-ttu-id="f7e9a-119">Die Speicherbedarf-Dateien werden im Rahmen des paketbuildprozesses erstellt.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-119">Footprint files are created as part of the package build process.</span></span> <span data-ttu-id="f7e9a-120">Zusätzlich zu den OPC \[ -Spezifikationen sind Inhalts \_ Typen \] . XML und Dateien, deren Namen dem \* \\ \_ Muster "rels \\ \* . rels" entsprechen, Dateien für den Speicherbedarf.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-120">In addition per the OPC specification, \[Content\_Types\].xml and files whose names match the "\*\\\_rels\\\*.rels" pattern are footprint files.</span></span>

</dd> <dt>

<span data-ttu-id="f7e9a-121"><span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**kundiger**</span><span class="sxs-lookup"><span data-stu-id="f7e9a-121"><span id="appxpkg_packaging_glossary_manifest"></span><span id="APPXPKG_PACKAGING_GLOSSARY_MANIFEST"></span>**manifest**</span></span>
</dt> <dd>

<span data-ttu-id="f7e9a-122">Eine XML-Datei, in der die Inhalte und Metadaten beschrieben werden, die einem Paket einschließlich der Paket-ID zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-122">An XML file that describes the contents and metadata associated with a package including the package ID.</span></span> <span data-ttu-id="f7e9a-123">Für jedes app-Paket ist eine Manifest-XML-Datei erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-123">A manifest XML file is required for every app package.</span></span>

</dd> <dt>

<span data-ttu-id="f7e9a-124"><span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**OPC**</span><span class="sxs-lookup"><span data-stu-id="f7e9a-124"><span id="appxpkg_packaging_glossary_opc"></span><span id="APPXPKG_PACKAGING_GLOSSARY_OPC"></span>**OPC**</span></span>
</dt> <dd>

<span data-ttu-id="f7e9a-125">In den Open Packaging Conventions (OPC) wird eine Containerdatei Technologie beschrieben, die in den ISO/IEC 29500-und ECMA 376-Standards dokumentiert ist.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-125">Open Packaging Conventions (OPC) describes a container-file technology that is documented in the ISO/IEC 29500 and ECMA 376 standards.</span></span> <span data-ttu-id="f7e9a-126">App-Pakete sind OPC-kompatibel.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-126">App packages are OPC-compliant.</span></span>

</dd> <dt>

<span data-ttu-id="f7e9a-127"><span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**Paketen**</span><span class="sxs-lookup"><span data-stu-id="f7e9a-127"><span id="appxpkg.appx_packaging_glossary_package"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE"></span>**package**</span></span>
</dt> <dd>

<span data-ttu-id="f7e9a-128">Die Einheit für die Bereitstellung, Verwaltung und Wartung von Software, die dem App-Paket Modell zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-128">The unit of deployment, management, and servicing software associated with the app packaging model.</span></span> <span data-ttu-id="f7e9a-129">Ein Paket enthält die Dateien, die die APP bilden, sowie eine Manifest-Datei, in der die Software für Windows beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-129">A package contains the files that constitute the app, along with a manifest file that describes the software to Windows.</span></span>

</dd> <dt>

<span data-ttu-id="f7e9a-130"><span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**Paket Familienname**</span><span class="sxs-lookup"><span data-stu-id="f7e9a-130"><span id="appxpkg.appx_packaging_glossary_package_family_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_FAMILY_MONIKER"></span>**package family name**</span></span>
</dt> <dd>

<span data-ttu-id="f7e9a-131">Eine serialisierte Form der Paket-ID, die die Paket Familie auf dem Computer eindeutig darstellt.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-131">A serialized form of the package ID that uniquely represents the package family on the computer.</span></span> <span data-ttu-id="f7e9a-132">Sie eignet sich für das Benennen von Objekten wie z. b. Dateien und Ordnern.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-132">It is suitable for naming objects such as files and folders.</span></span> <span data-ttu-id="f7e9a-133">Der Paket Familienname ähnelt dem vollständigen Paketnamen, enthält jedoch nur den Namen und den Verleger.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-133">The package family name is similar to the package full name, but includes only the name and publisher.</span></span> <span data-ttu-id="f7e9a-134">Da Informationen ausgeschlossen werden, die sich durch die Wartung (Version, Architektur und Ressourcen Informationen) ändern, ist es für Versions unabhängige Verweise auf das Paket nützlich.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-134">Because it excludes info that changes with servicing (version, architecture, and resource info), it is useful for version-independent references to the package.</span></span>

</dd> <dt>

<span data-ttu-id="f7e9a-135"><span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**vollständiger Paketname**</span><span class="sxs-lookup"><span data-stu-id="f7e9a-135"><span id="appxpkg.appx_packaging_glossary_package_moniker"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_MONIKER"></span>**package full name**</span></span>
</dt> <dd>

<span data-ttu-id="f7e9a-136">Eine serialisierte Form der Paket-ID, die diese Version des Pakets auf dem Computer eindeutig darstellt.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-136">A serialized form of the package ID that uniquely represents this version of the package on the computer.</span></span> <span data-ttu-id="f7e9a-137">Sie eignet sich für das Benennen von Objekten wie z. b. Dateien und Ordnern.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-137">It is suitable for naming objects such as files and folders.</span></span>

</dd> <dt>

<span data-ttu-id="f7e9a-138"><span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**Paket-ID**</span><span class="sxs-lookup"><span data-stu-id="f7e9a-138"><span id="appxpkg.appx_packaging_glossary_package_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_ID"></span>**package ID**</span></span>
</dt> <dd>

<span data-ttu-id="f7e9a-139">Eine Globally Unique Identifier für ein Paket.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-139">A globally unique identifier for a package.</span></span> <span data-ttu-id="f7e9a-140">Sie besteht aus einem Tupel von Attributen für das Paket, einschließlich Name, Herausgeber, unterstützte Architektur, Ressourcen Informationen und Version.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-140">It is composed of a tuple of attributes for the package including name, publisher, supported architecture, resource info, and version.</span></span> <span data-ttu-id="f7e9a-141">Siehe den vollständigen Namen des Pakets und den Paket Familiennamen für serialisierte Formen der Paket-ID.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-141">See package full name and package family name for serialized forms of the package ID.</span></span>

</dd> <dt>

<span data-ttu-id="f7e9a-142"><span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**Paket relative Anwendungs-ID**</span><span class="sxs-lookup"><span data-stu-id="f7e9a-142"><span id="appxpkg.appx_packaging_glossary_package_relative_application_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PACKAGE_RELATIVE_APPLICATION_ID"></span>**package relative application ID**</span></span>
</dt> <dd>

<span data-ttu-id="f7e9a-143">Das **ID** -Attribut für das [**Application**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) -Element im Paket Manifest, das auch als "Praid" bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-143">The **Id** attribute on the [**Application**](/uwp/schemas/appxpackage/appxmanifestschema2010-v2/element-application) element within the package manifest, which is also known as PRAID.</span></span> <span data-ttu-id="f7e9a-144">Mit dieser Zeichenfolge wird eine APP innerhalb eines Pakets eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-144">This string uniquely identifies an app within a package.</span></span> <span data-ttu-id="f7e9a-145">Dieses Attribut ist für das **Application** -Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-145">This attribute is required for the **Application** element.</span></span>

</dd> <dt>

<span data-ttu-id="f7e9a-146"><span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**Nutz Last Dateien**</span><span class="sxs-lookup"><span data-stu-id="f7e9a-146"><span id="appxpkg.appx_packaging_glossary_payload_file"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_PAYLOAD_FILE"></span>**payload files**</span></span>
</dt> <dd>

<span data-ttu-id="f7e9a-147">Die Dateien innerhalb eines App-Pakets, die Teil der APP sind, die bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-147">The files within an app package that are part of the app to be deployed.</span></span> <span data-ttu-id="f7e9a-148">Diese Dateien werden extrahiert und im Installationsordner des Benutzers abgelegt.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-148">These files are extracted and placed in the user's installation folder.</span></span>

</dd> <dt>

<span data-ttu-id="f7e9a-149"><span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**Ressourcen-ID**</span><span class="sxs-lookup"><span data-stu-id="f7e9a-149"><span id="appxpkg.appx_packaging_glossary_resource_id"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_RESOURCE_ID"></span>**resource ID**</span></span>
</dt> <dd>

<span data-ttu-id="f7e9a-150">Ein optionaler Teil einer Paket-ID, der verwendet wird, um die Ressourcen im Paket zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-150">An optional part of a package ID that is used to differentiate the resources in the package.</span></span> <span data-ttu-id="f7e9a-151">Beispielsweise kann eine Ressourcen-ID verwendet werden, um die Sprache oder das Gebiets Schema anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-151">For example, a resource ID can be used to specify the language or locale.</span></span>

</dd> <dt>

<span data-ttu-id="f7e9a-152"><span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**Zentrales Zip-Verzeichnis**</span><span class="sxs-lookup"><span data-stu-id="f7e9a-152"><span id="appxpkg.appx_packaging_glossary_zip_central_directory"></span><span id="APPXPKG.APPX_PACKAGING_GLOSSARY_ZIP_CENTRAL_DIRECTORY"></span>**ZIP central directory**</span></span>
</dt> <dd>

<span data-ttu-id="f7e9a-153">Die Byte Sequenzen in einer ZIP-Datei, in der Metadaten zum ZIP-Archiv und dessen Inhalt gespeichert werden, einschließlich Name, Größe, Komprimierungs Einstellungen und Speicherort innerhalb des Archivs.</span><span class="sxs-lookup"><span data-stu-id="f7e9a-153">The byte sequences in a ZIP file that store metadata about the ZIP archive and its contents including name, size, compression settings, and location within the archive.</span></span>

</dd> </dl>

 

 