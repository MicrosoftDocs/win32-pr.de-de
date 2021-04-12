---
description: Windows Installer können digitale Signaturen als Mittel zum erkennen beschädigter Ressourcen verwenden.
ms.assetid: fc982813-583b-4fcd-88d8-9de227994e7b
title: Msicert.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0a4df800bbcfa9ed2fb0d016794b3ebcf1535be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218534"
---
# <a name="msicertexe"></a><span data-ttu-id="41f6e-103">Msicert.exe</span><span class="sxs-lookup"><span data-stu-id="41f6e-103">Msicert.exe</span></span>

<span data-ttu-id="41f6e-104">Windows Installer können digitale Signaturen als Mittel zum erkennen beschädigter Ressourcen verwenden.</span><span class="sxs-lookup"><span data-stu-id="41f6e-104">Windows Installer can use digital signatures as a means to detect corrupted resources.</span></span> <span data-ttu-id="41f6e-105">Ein Signatur Geber Zertifikat kann mit dem Signatur Geber Zertifikat einer externen Ressource verglichen werden, die vom Paket installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="41f6e-105">A signer certificate may be compared to the signer certificate of an external resource to be installed by the package.</span></span> <span data-ttu-id="41f6e-106">Weitere Informationen finden Sie unter [digitale Signaturen und Windows Installer](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="41f6e-106">For more information, see [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span>

<span data-ttu-id="41f6e-107">MsiCert.exe ist ein Befehlszeilen-Hilfsprogramm, das verwendet werden kann, um die [msidigitalsignature-Tabelle](msidigitalsignature-table.md) und die [msidigitalcertificate-Tabelle](msidigitalcertificate-table.md) mit den digitalen Signatur Informationen einer externen CAB-Datei aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="41f6e-107">MsiCert.exe is a command line utility that can be used to populate the [MsiDigitalSignature table](msidigitalsignature-table.md) and [MsiDigitalCertificate table](msidigitalcertificate-table.md) with the digital signature information of an external cabinet file.</span></span> <span data-ttu-id="41f6e-108">Die CAB-Datei muss digital signiert und in der [Medien Tabelle](media-table.md)aufgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="41f6e-108">The cabinet file must by digitally signed and listed in the [Media table](media-table.md).</span></span> <span data-ttu-id="41f6e-109">MsiCert.exe verwendet die Signatur Geber Zertifikat Informationen aus der digital signierten CAB-Datei und erstellt und fügt die msidigitalsignature-und msidigitalcertificate-Tabellen der Datenbank hinzu, wenn diese nicht bereits vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="41f6e-109">MsiCert.exe uses the signer certificate information from the digitally signed cabinet and will create and add the MsiDigitalSignature and MsiDigitalCertificate tables to the database if they do not already exist.</span></span>

## <a name="syntax"></a><span data-ttu-id="41f6e-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="41f6e-110">Syntax</span></span>

<span data-ttu-id="41f6e-111">**msicert-d** *{Database}* **-m** *{Medien Eintrag}* **-c** *{CAB}* **\[ -h \]**</span><span class="sxs-lookup"><span data-stu-id="41f6e-111">**msicert -d** *{database}* **-m** *{media entry}* **-c** *{cabinet}* **\[-h\]**</span></span>

## <a name="command-line-options"></a><span data-ttu-id="41f6e-112">Befehlszeilenoptionen</span><span class="sxs-lookup"><span data-stu-id="41f6e-112">Command Line Options</span></span>

<span data-ttu-id="41f6e-113">Bei den Befehlszeilenoptionen wird die Groß-/Kleinschreibung nicht beachtet, und es können Schrägstriche anstelle eines Bindestrichs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="41f6e-113">The command line options are case-insensitive and slash delimiters may be used instead of a dash.</span></span>



| <span data-ttu-id="41f6e-114">Option</span><span class="sxs-lookup"><span data-stu-id="41f6e-114">Option</span></span> | <span data-ttu-id="41f6e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="41f6e-115">Parameter</span></span>        | <span data-ttu-id="41f6e-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="41f6e-116">Description</span></span>                                                                                             |
|--------|------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41f6e-117">-d</span><span class="sxs-lookup"><span data-stu-id="41f6e-117">-d</span></span>     | <database> | <span data-ttu-id="41f6e-118">Die zu Aktualisier Ende Datenbank (MSI-Datei).</span><span class="sxs-lookup"><span data-stu-id="41f6e-118">The database (.msi file) that is being updated.</span></span>                                                         |
| <span data-ttu-id="41f6e-119">-M</span><span class="sxs-lookup"><span data-stu-id="41f6e-119">-m</span></span>     | <media Id> | <span data-ttu-id="41f6e-120">Der Eintrag im DiskId-Feld der [Medien Tabelle](media-table.md) im Datensatz für die CAB-Datei.</span><span class="sxs-lookup"><span data-stu-id="41f6e-120">The entry in the DiskId field of the [Media table](media-table.md) in the record for the cabinet file.</span></span> |
| <span data-ttu-id="41f6e-121">-c</span><span class="sxs-lookup"><span data-stu-id="41f6e-121">-c</span></span>     | <cabinet>  | <span data-ttu-id="41f6e-122">Der Pfad zur digital signierten CAB-Datei.</span><span class="sxs-lookup"><span data-stu-id="41f6e-122">The path to the digitally signed cabinet file.</span></span>                                                          |
| <span data-ttu-id="41f6e-123">-h</span><span class="sxs-lookup"><span data-stu-id="41f6e-123">-h</span></span>     |                  | <span data-ttu-id="41f6e-124">Fügen Sie den Hash der digitalen Signatur ein.</span><span class="sxs-lookup"><span data-stu-id="41f6e-124">Include the hash of the digital signature.</span></span> <span data-ttu-id="41f6e-125">Diese Eingabe ist optional.</span><span class="sxs-lookup"><span data-stu-id="41f6e-125">This is optional.</span></span>                                            |



 

<span data-ttu-id="41f6e-126">Dieses Tool ist nur in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="41f6e-126">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="41f6e-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="41f6e-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41f6e-128">Entwicklungs Tools für Windows Installer</span><span class="sxs-lookup"><span data-stu-id="41f6e-128">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="41f6e-129">Veröffentlichte Versionen, Tools und verteilbare Dateien</span><span class="sxs-lookup"><span data-stu-id="41f6e-129">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



