---
title: Is_Trusted
description: Das is \_ Trusted-Attribut ist ein Attribut auf Dateiebene, das angibt, ob die Lizenz Erwerbs-URL in der Datei vertrauenswürdig ist.
ms.assetid: 7b383b45-e992-4a07-af0b-9ef220ddd9af
keywords:
- Is_Trusted Windows Media-Format
topic_type:
- apiref
api_name:
- Is_Trusted
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e8dd4fdd638bad0908bb1bbf50135cde5bad6c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103948264"
---
# <a name="is_trusted"></a><span data-ttu-id="26a55-104">Ist \_ vertrauenswürdig</span><span class="sxs-lookup"><span data-stu-id="26a55-104">Is\_Trusted</span></span>

<span data-ttu-id="26a55-105">Das **is \_ Trusted** -Attribut ist ein Attribut auf Dateiebene, das angibt, ob die Lizenz Erwerbs-URL in der Datei vertrauenswürdig ist.</span><span class="sxs-lookup"><span data-stu-id="26a55-105">The **Is\_Trusted** attribute is a file-level attribute specifying whether the license acquisition URL in the file is trusted.</span></span>

## <a name="global-constant"></a><span data-ttu-id="26a55-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="26a55-106">Global Constant</span></span>

<span data-ttu-id="26a55-107">g \_ wszwmtrusted</span><span class="sxs-lookup"><span data-stu-id="26a55-107">g\_wszWMTrusted</span></span>

## <a name="data-type"></a><span data-ttu-id="26a55-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="26a55-108">Data Type</span></span>

<span data-ttu-id="26a55-109">**WMT- \_ Typ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="26a55-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="26a55-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26a55-110">Remarks</span></span>

<span data-ttu-id="26a55-111">Dies ist ein codiertes Attribut.</span><span class="sxs-lookup"><span data-stu-id="26a55-111">This is a coded attribute.</span></span>

<span data-ttu-id="26a55-112">Bevor Sie zu einer Lizenz Erwerbs-URL navigieren, die in einer DRM-geschützten Datei enthalten ist, muss eine Anwendung zunächst überprüfen, ob diese Eigenschaft true ist.</span><span class="sxs-lookup"><span data-stu-id="26a55-112">Before navigating to a license acquisition URL contained in a DRM-protected file, an application should first verify that this property is true.</span></span> <span data-ttu-id="26a55-113">Wenn der Wert false ist, sollte die Anwendung den Benutzer benachrichtigen, dass die URL möglicherweise manipuliert wurde.</span><span class="sxs-lookup"><span data-stu-id="26a55-113">If it is false, the application should notify the user that the URL has possibly been tampered with.</span></span>

<span data-ttu-id="26a55-114">Dieses Attribut kann nicht auf Dateiebene dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="26a55-114">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="26a55-115">Wenn dieses Attribut für einen einzelnen Stream verwendet wird, wird es als benutzerdefinierte Metadaten behandelt und gibt seine normale Bedeutung nicht an die Objekte des Windows Media Format SDK aus.</span><span class="sxs-lookup"><span data-stu-id="26a55-115">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="26a55-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26a55-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26a55-117">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="26a55-117">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




