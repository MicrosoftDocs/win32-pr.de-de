---
title: DRM_Level
description: DRM- \_ Ebene ist ein Lizenz Attribut, das das Windows Media-Format SDK festlegt, wenn es eine lokale Lizenz für Dateien erstellt, die mit DRM-Version 1 geschützt sind.
ms.assetid: 05357378-4d73-48df-a3b5-bdb2c543ec66
keywords:
- DRM_Level Windows Media-Format
topic_type:
- apiref
api_name:
- DRM_Level
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3177197b9c149c2fca2c7678a8fe03c6b412e2d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314350"
---
# <a name="drm_level"></a><span data-ttu-id="f193d-104">DRM- \_ Ebene</span><span class="sxs-lookup"><span data-stu-id="f193d-104">DRM\_Level</span></span>

<span data-ttu-id="f193d-105">**DRM \_ Level** ist ein Lizenz Attribut, das vom Windows Media-Format SDK festgelegt wird, wenn es eine lokale Lizenz für Dateien erstellt, die mit DRM-Version 1 geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="f193d-105">**DRM\_Level** is a license attribute that the Windows Media Format SDK sets when it creates a local license for files protected with DRM version 1.</span></span> <span data-ttu-id="f193d-106">Sie enthält die Sicherheitsstufe, die von der aufrufenden Anwendung benötigt werden muss, um auf den Inhalt in der Datei zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="f193d-106">It contains the security level that the calling application must have to access the content in the file.</span></span> <span data-ttu-id="f193d-107">Der Standardwert ist 150.</span><span class="sxs-lookup"><span data-stu-id="f193d-107">The default value is 150.</span></span>

## <a name="global-constant"></a><span data-ttu-id="f193d-108">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="f193d-108">Global Constant</span></span>

<span data-ttu-id="f193d-109">g \_ wszwmdrm- \_ Ebene</span><span class="sxs-lookup"><span data-stu-id="f193d-109">g\_wszWMDRM\_Level</span></span>

## <a name="data-type"></a><span data-ttu-id="f193d-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f193d-110">Data Type</span></span>

<span data-ttu-id="f193d-111">**WMT- \_ Typ \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="f193d-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="f193d-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f193d-112">Remarks</span></span>

<span data-ttu-id="f193d-113">Die DRM-Sicherheitsstufe einer Anwendung wird von der jeweiligen wmstubdrm-Bibliothek bestimmt, mit der zum Zeitpunkt der Kompilierung eine Verknüpfung besteht.</span><span class="sxs-lookup"><span data-stu-id="f193d-113">An application's DRM security level is determined by the particular wmstubdrm library that it links to at compile time.</span></span> <span data-ttu-id="f193d-114">Weitere Informationen zu diesen Sicherheitsstufen finden Sie unter Abrufen [der erforderlichen DRM-Bibliothek](obtaining-the-required-drm-library.md).</span><span class="sxs-lookup"><span data-stu-id="f193d-114">For more information on these security levels, see [Obtaining the Required DRM Library](obtaining-the-required-drm-library.md).</span></span> <span data-ttu-id="f193d-115">Verwenden Sie [**iwmheaderinfo:: setAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) , um diese Eigenschaft beim Schutz von ASF-Dateien mit DRM-Version 1 festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f193d-115">Use [**IWMHeaderInfo::SetAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute) to set this property when protecting ASF files with DRM version 1.</span></span>

## <a name="see-also"></a><span data-ttu-id="f193d-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f193d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f193d-117">**DRM-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="f193d-117">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




