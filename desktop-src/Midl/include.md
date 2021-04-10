---
title: include-Attribut
description: Die ACF include-Anweisung gibt eine oder mehrere Header Dateien an, die in den generierten Stub-Code eingeschlossen werden sollen.
ms.assetid: f83a704b-2f6e-4498-97ff-593fef2e92dc
keywords:
- Include-Attribut-Mittel l
topic_type:
- apiref
api_name:
- include
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2aab7b7262bceb330e3f4645e4f16035b783197
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104100874"
---
# <a name="include-attribute"></a><span data-ttu-id="13520-104">include-Attribut</span><span class="sxs-lookup"><span data-stu-id="13520-104">include attribute</span></span>

<span data-ttu-id="13520-105">Die ACF **include** -Anweisung gibt eine oder mehrere Header Dateien an, die in den generierten Stub-Code eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="13520-105">The ACF **include** statement specifies one or more header files to be included in the generated stub code.</span></span>

``` syntax
include filenames;
```

## <a name="parameters"></a><span data-ttu-id="13520-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="13520-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13520-107">*Dateinamen*</span><span class="sxs-lookup"><span data-stu-id="13520-107">*filenames*</span></span> 
</dt> <dd>

<span data-ttu-id="13520-108">Gibt den Namen einer oder mehrerer C-sprach Header Dateien an.</span><span class="sxs-lookup"><span data-stu-id="13520-108">Specifies the name of one or more C-language header files.</span></span> <span data-ttu-id="13520-109">Verwenden Sie den vollständigen Dateinamen, einschließlich der. H-Erweiterung und schließen Sie jeden Dateinamen in Anführungszeichen ein.</span><span class="sxs-lookup"><span data-stu-id="13520-109">Use the full file name, including the .H extension and enclose each file name in quotation marks.</span></span> <span data-ttu-id="13520-110">Trennen Sie mehrere Header Dateinamen der C-Sprache durch Kommas.</span><span class="sxs-lookup"><span data-stu-id="13520-110">Separate multiple C-language header file names with commas.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="13520-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13520-111">Remarks</span></span>

<span data-ttu-id="13520-112">Als Ergebnis der **include** -Anweisung enthält der generierte Stub-Code eine **\# include** -Anweisung im C-Präprozessor.</span><span class="sxs-lookup"><span data-stu-id="13520-112">As a result of the **include** statement, the generated stub code will contain a C-preprocessor **\#include** statement.</span></span> <span data-ttu-id="13520-113">Sie stellen die Header Datei der C-Sprache bereit, wenn Sie die Stub kompilieren.</span><span class="sxs-lookup"><span data-stu-id="13520-113">You supply the C-language header file when compiling the stubs.</span></span> <span data-ttu-id="13520-114">Include-Anweisungen basieren auf dem C-compilermechanismus, der die Verzeichnisstruktur für enthaltene Dateien durchsucht.</span><span class="sxs-lookup"><span data-stu-id="13520-114">Include statements rely on the C-compiler mechanism of searching the directory structure for included files.</span></span>

> [!Note]  
> <span data-ttu-id="13520-115">Verwenden Sie die [**Import**](import.md) -Direktive anstelle der **include** -Direktive für Systemdateien, die Datentypen enthalten, die Sie der IDL-Datei zur Verfügung stellen möchten.</span><span class="sxs-lookup"><span data-stu-id="13520-115">Use the [**import**](import.md) directive rather than the **include** directive for system files that contain data types you want to make available to the IDL file.</span></span> <span data-ttu-id="13520-116">Die **Import** -Direktive ignoriert Funktionsprototypen und ermöglicht Ihnen die Verwendung von Mittell-Compilerschaltern, die die Generierung von Unterstützungs Routinen optimieren.</span><span class="sxs-lookup"><span data-stu-id="13520-116">The **import** directive ignores function prototypes and allows you to use MIDL compiler switches that optimize the generation of support routines.</span></span>

 

## <a name="examples"></a><span data-ttu-id="13520-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="13520-117">Examples</span></span>

``` syntax
include "local.h";
include "gendefs.h", "protos.h", "mystuff.h";
```

## <a name="see-also"></a><span data-ttu-id="13520-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="13520-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13520-119">Anwendungs Konfigurationsdatei (ACF)</span><span class="sxs-lookup"><span data-stu-id="13520-119">Application Configuration File (ACF)</span></span>](application-configuration-file-acf-.md)
</dt> <dt>

[<span data-ttu-id="13520-120">**Importieren**</span><span class="sxs-lookup"><span data-stu-id="13520-120">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="13520-121">Importieren von Dateien und Typbibliotheken</span><span class="sxs-lookup"><span data-stu-id="13520-121">Importing Files and Type Libraries</span></span>](importing-files-and-type-libraries.md)
</dt> <dt>

[<span data-ttu-id="13520-122">Importieren von System-Headerdateien</span><span class="sxs-lookup"><span data-stu-id="13520-122">Importing System Header Files</span></span>](importing-system-header-files.md)
</dt> </dl>

 

 




