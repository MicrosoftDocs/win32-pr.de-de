---
title: WM/Bild
description: Das WM/Bild-Attribut enthält ein Bild, das sich auf den Inhalt bezieht.
ms.assetid: ec82dfdf-7755-4758-9771-096aac114f78
keywords:
- WM/Bild Windows Media-Format
topic_type:
- apiref
api_name:
- WM/Picture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ba3f74378112c8e3f58958db8b22c970e8e099
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103948194"
---
# <a name="wmpicture"></a><span data-ttu-id="52bca-104">WM/Bild</span><span class="sxs-lookup"><span data-stu-id="52bca-104">WM/Picture</span></span>

<span data-ttu-id="52bca-105">Das **WM/Bild-** Attribut enthält ein Bild, das sich auf den Inhalt bezieht.</span><span class="sxs-lookup"><span data-stu-id="52bca-105">The **WM/Picture** attribute contains a picture related to the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="52bca-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="52bca-106">Global Constant</span></span>

<span data-ttu-id="52bca-107">g \_ wszwmpicture</span><span class="sxs-lookup"><span data-stu-id="52bca-107">g\_wszWMPicture</span></span>

## <a name="data-type"></a><span data-ttu-id="52bca-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="52bca-108">Data Type</span></span>

<span data-ttu-id="52bca-109">[**WM \_ Bild**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) (**WMT \_ - \_ typbinär Datei**)</span><span class="sxs-lookup"><span data-stu-id="52bca-109">[**WM\_PICTURE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture) (**WMT\_TYPE\_BINARY**)</span></span>

## <a name="remarks"></a><span data-ttu-id="52bca-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52bca-110">Remarks</span></span>

<span data-ttu-id="52bca-111">Dieses Attribut ist mit dem ID3-Frame (APIC) kompatibel.</span><span class="sxs-lookup"><span data-stu-id="52bca-111">This attribute is compatible with the ID3 frame, APIC.</span></span> <span data-ttu-id="52bca-112">Die ID3-Spezifikation für den APIC-Frame gibt an, dass es möglicherweise eine beliebige Anzahl von APIC-Frames gibt, die einer Datei zugeordnet sind, aber nur eine vom Typ "1" und nur eine vom Typ "2" sein kann.</span><span class="sxs-lookup"><span data-stu-id="52bca-112">The ID3 specification for the APIC frame stipulates that, while there may be any number of APIC frames associated with a file, only one may be of type 1 and only one may be of type 2.</span></span> <span data-ttu-id="52bca-113">Die Spezifikation gibt auch an, dass die Beschreibung des Bilds nicht länger als 64 Zeichen sein kann, aber leer sein kann.</span><span class="sxs-lookup"><span data-stu-id="52bca-113">The specification also states that the description of the picture can be no longer than 64 characters, but can be empty.</span></span>

<span data-ttu-id="52bca-114">Die mit den Objekten des Windows Media SDK-SDKs hinzugefügten WM/Bild-Attribute werden nicht automatisch entsprechend den ID3-Spezifikationen überprüft.</span><span class="sxs-lookup"><span data-stu-id="52bca-114">WM/Picture attributes added with the objects of the Windows Media Format SDK are not automatically validated to conform to ID3 specifications.</span></span> <span data-ttu-id="52bca-115">Sie müssen in Ihrer Anwendung Code hinzufügen, um Validierungen auszuführen, wenn Sie die vollständige Kompatibilität mit ID3 beibehalten möchten.</span><span class="sxs-lookup"><span data-stu-id="52bca-115">You must add code in your application to perform validations if you want to maintain complete compatibility with ID3.</span></span>

## <a name="see-also"></a><span data-ttu-id="52bca-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52bca-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52bca-117">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="52bca-117">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="52bca-118">**WM- \_ Bild**</span><span class="sxs-lookup"><span data-stu-id="52bca-118">**WM\_PICTURE**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_picture)
</dt> </dl>

 

 




