---
title: HKEY_LOCAL_MACHINESOFTWAREClasses
description: Die Unterschlüssel und Registrierungs Werte, die dem Schlüssel HKEY \_ Local Machine Classes zugeordnet sind, \_ \\ \\ enthalten Informationen zu einer Anwendung, die zur Unterstützung der com-Funktionalität benötigt wird.
ms.assetid: a5b271d6-f445-45df-a8e4-f6e0194ac824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c16fdbc97b32d01af9c96b5670cb5a19c09c89a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714099"
---
# <a name="hkey_local_machinesoftwareclasses"></a><span data-ttu-id="e5a7d-103">HKEY \_ - \_ \\ Software \\ Klassen für lokale Computer</span><span class="sxs-lookup"><span data-stu-id="e5a7d-103">HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes</span></span>

<span data-ttu-id="e5a7d-104">Die Unterschlüssel und Registrierungs Werte, die dem Schlüssel **HKEY \_ local \_ Machine \\ \\ Classes** zugeordnet sind, enthalten Informationen zu einer Anwendung, die zur Unterstützung der com-Funktionalität benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="e5a7d-104">The subkeys and registry values associated with the **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes** key contain information about an application that is needed to support COM functionality.</span></span> <span data-ttu-id="e5a7d-105">Diese Informationen umfassen Themen wie Unterstützte Datenformate, Kompatibilitätsinformationen, programmgesteuerte Bezeichner, DCOM und Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="e5a7d-105">This information includes such topics as supported data formats, compatibility information, programmatic identifiers, DCOM, and controls.</span></span>



| <span data-ttu-id="e5a7d-106">Unterschlüssel</span><span class="sxs-lookup"><span data-stu-id="e5a7d-106">Subkey</span></span>                                                                         | <span data-ttu-id="e5a7d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5a7d-107">Description</span></span>                                                                                                       |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5a7d-108">**AppID**</span><span class="sxs-lookup"><span data-stu-id="e5a7d-108">**AppID**</span></span>](appid-key.md)                                                     | <span data-ttu-id="e5a7d-109">Konfigurationsoptionen für COM-basierte Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="e5a7d-109">Configuration options for COM-based applications.</span></span>                                                                 |
| [<span data-ttu-id="e5a7d-110">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="e5a7d-110">**CLSID**</span></span>](clsid-key-hklm.md)                                                | <span data-ttu-id="e5a7d-111">Konfigurationsoptionen für COM-Klassen.</span><span class="sxs-lookup"><span data-stu-id="e5a7d-111">Configuration options for COM classes.</span></span>                                                                            |
| [<span data-ttu-id="e5a7d-112">**<Datei \_ Erweiterung>**</span><span class="sxs-lookup"><span data-stu-id="e5a7d-112">**<file\_extension>**</span></span>](-file-extension--key.md)                        | <span data-ttu-id="e5a7d-113">Ordnet eine Dateinamenerweiterung einer ProgID zu.</span><span class="sxs-lookup"><span data-stu-id="e5a7d-113">Associates a file name extension with a ProgID.</span></span>                                                                   |
| [<span data-ttu-id="e5a7d-114">**FileType**</span><span class="sxs-lookup"><span data-stu-id="e5a7d-114">**FileType**</span></span>](filetype-key.md)                                               | <span data-ttu-id="e5a7d-115">Wird von [**getclassfile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) verwendet, um Muster mit verschiedenen Datei Bytes in einer nicht Verbund Datei abzugleichen.</span><span class="sxs-lookup"><span data-stu-id="e5a7d-115">Used by [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) to match patterns against various file bytes in a non-compound file.</span></span> |
| [<span data-ttu-id="e5a7d-116">**Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e5a7d-116">**Interface**</span></span>](interface-key.md)                                             | <span data-ttu-id="e5a7d-117">Ordnet einen Schnittstellennamen einer Schnittstellen-ID (IID) zu.</span><span class="sxs-lookup"><span data-stu-id="e5a7d-117">Associates an interface name with an interface ID (IID).</span></span>                                                          |
| [**<ProgID>**](-progid--key.md)                                         | <span data-ttu-id="e5a7d-118">Identifiziert eine Klasse.</span><span class="sxs-lookup"><span data-stu-id="e5a7d-118">Identifies a class.</span></span> <span data-ttu-id="e5a7d-119">Beachten Sie, dass es im Gegensatz zu einer CLSID nicht garantiert wird, dass die ProgID global eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="e5a7d-119">Note that the ProgID is not guaranteed to be globally unique, unlike a CLSID.</span></span>                 |
| [<span data-ttu-id="e5a7d-120">**<Versions unabhängige ProgID>**</span><span class="sxs-lookup"><span data-stu-id="e5a7d-120">**<version-independent ProgID>**</span></span>](-version-independent-progid--key.md) | <span data-ttu-id="e5a7d-121">Wird verwendet, um die neueste Version einer Objekt Anwendung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="e5a7d-121">Used to determine the latest version of an object application.</span></span>                                                    |



 

 

 




