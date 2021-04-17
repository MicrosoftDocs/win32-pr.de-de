---
title: WM/streamtypeingangs Info
description: Das WM/streamtypeinfo-Attribut enthält die Konfigurationsinformationen für den angegebenen Datenstrom in der ASF-Datei.
ms.assetid: 4d7f18d4-d76d-4e2e-b8a9-eb96844a2fa1
keywords:
- WM/streamtypeingangs Info Windows Media-Format
topic_type:
- apiref
api_name:
- WM/StreamTypeInfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c410b470e9ddb4ec874325d9c1cca2839c00b1d
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104389061"
---
# <a name="wmstreamtypeinfo"></a><span data-ttu-id="2cbed-104">WM/streamtypeingangs Info</span><span class="sxs-lookup"><span data-stu-id="2cbed-104">WM/StreamTypeInfo</span></span>

<span data-ttu-id="2cbed-105">Das **WM/streamtypeinfo-** Attribut enthält die Konfigurationsinformationen für den angegebenen Datenstrom in der ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="2cbed-105">The **WM/StreamTypeInfo** attribute contains the configuration information for the specified stream in the ASF file.</span></span>

## <a name="global-constant"></a><span data-ttu-id="2cbed-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="2cbed-106">Global Constant</span></span>

<span data-ttu-id="2cbed-107">g \_ wszwmstreamtypeingangs Info</span><span class="sxs-lookup"><span data-stu-id="2cbed-107">g\_wszWMStreamTypeInfo</span></span>

## <a name="data-type"></a><span data-ttu-id="2cbed-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="2cbed-108">Data Type</span></span>

<span data-ttu-id="2cbed-109">[**WM \_ \_Streamtyp \_ Info**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**WMT \_ - \_ typbinär Datei**)</span><span class="sxs-lookup"><span data-stu-id="2cbed-109">[**WM\_STREAM\_TYPE\_INFO**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_stream_type_info) (**WMT\_TYPE\_BINARY**)</span></span>

## <a name="remarks"></a><span data-ttu-id="2cbed-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2cbed-110">Remarks</span></span>

<span data-ttu-id="2cbed-111">Dieses Attribut gilt für bestimmte Datenströme.</span><span class="sxs-lookup"><span data-stu-id="2cbed-111">This attribute applies to specific streams.</span></span> <span data-ttu-id="2cbed-112">Dieses Attribut kann für Stream 0 nicht abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="2cbed-112">You cannot retrieve this attribute for stream 0.</span></span>

<span data-ttu-id="2cbed-113">Dieses Attribut ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="2cbed-113">This attribute is read-only.</span></span>

<span data-ttu-id="2cbed-114">Das Metadateneditor-Objekt kann auf **WM/streamtypeinfo** zugreifen.</span><span class="sxs-lookup"><span data-stu-id="2cbed-114">**WM/StreamTypeInfo** can be accessed by the metadata editor object.</span></span> <span data-ttu-id="2cbed-115">Dies ist die einzige Möglichkeit, auf Informationen zur Datenstrom Konfiguration zuzugreifen, ohne die Datei mit dem Reader-Objekt (oder dem synchronen Reader-Objekt) zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="2cbed-115">This is the only way to access stream configuration information without opening the file with the reader object (or the synchronous reader object).</span></span>

## <a name="see-also"></a><span data-ttu-id="2cbed-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2cbed-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cbed-117">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="2cbed-117">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




