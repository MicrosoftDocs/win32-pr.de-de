---
title: WM/Containerformat
description: Das Attribut WM/Containerformat gibt den Dateityp an, der in das aufrufende Objekt geladen wird.
ms.assetid: fea5b2e4-f10d-4482-a7b3-7dabf58df085
keywords:
- WM/Containerformat Windows Media-Format
topic_type:
- apiref
api_name:
- WM/ContainerFormat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9394fca14c3e07eb1f867c7b8ac473b2b61a9a2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718593"
---
# <a name="wmcontainerformat"></a><span data-ttu-id="ca587-104">WM/Containerformat</span><span class="sxs-lookup"><span data-stu-id="ca587-104">WM/ContainerFormat</span></span>

<span data-ttu-id="ca587-105">Das Attribut **WM/Containerformat** gibt den Dateityp an, der in das aufrufende Objekt geladen wird.</span><span class="sxs-lookup"><span data-stu-id="ca587-105">The **WM/ContainerFormat** attribute specifies the type of file that is loaded in the calling object.</span></span>

## <a name="global-constant"></a><span data-ttu-id="ca587-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="ca587-106">Global Constant</span></span>

<span data-ttu-id="ca587-107">g \_ wszwmcontainerformat</span><span class="sxs-lookup"><span data-stu-id="ca587-107">g\_wszWMContainerFormat</span></span>

## <a name="data-type"></a><span data-ttu-id="ca587-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="ca587-108">Data Type</span></span>

<span data-ttu-id="ca587-109">[**WMT \_ Speicher \_ Format**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) (**WMT \_ - \_ typbinär Datei**)</span><span class="sxs-lookup"><span data-stu-id="ca587-109">[**WMT\_STORAGE\_FORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) (**WMT\_TYPE\_BINARY**)</span></span>

## <a name="remarks"></a><span data-ttu-id="ca587-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca587-110">Remarks</span></span>

<span data-ttu-id="ca587-111">Dieses Attribut wird anstelle von **IWMProfile3:: getstorageformat** und **IWMProfile3:: setstorageformat** verwendet, die nicht mehr unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ca587-111">This attribute is used in place of **IWMProfile3::GetStorageFormat** and **IWMProfile3::SetStorageFormat**, which are no longer supported.</span></span>

<span data-ttu-id="ca587-112">Dies ist ein codiertes Attribut.</span><span class="sxs-lookup"><span data-stu-id="ca587-112">This is a coded attribute.</span></span>

<span data-ttu-id="ca587-113">Dieses Attribut kann nicht auf Dateiebene dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="ca587-113">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="ca587-114">Wenn dieses Attribut für einen einzelnen Stream verwendet wird, wird es als benutzerdefinierte Metadaten behandelt und gibt seine normale Bedeutung nicht an die Objekte des Windows Media Format SDK aus.</span><span class="sxs-lookup"><span data-stu-id="ca587-114">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="ca587-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca587-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca587-116">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="ca587-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




