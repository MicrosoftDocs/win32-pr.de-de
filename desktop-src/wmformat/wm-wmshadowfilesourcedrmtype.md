---
title: WM/wmshadowfilesourcedrmtype (Windows Media Format 11 SDK)
description: Das Attribut WM/wmshadowfilesourcedrmtype enthält den Typ von Rights Management, der zum Schutz der ursprünglichen Datei verwendet wird, von der die ASF-Datei abgeleitet ist.
ms.assetid: 58e7a383-6e80-42fc-bc75-5920dbe67a40
keywords:
- WM/wmshadowfilesourcedrmtype Windows Media-Format
topic_type:
- apiref
api_name:
- WM/WMShadowFileSourceDRMType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0f33d961e8cd3645e4949980d91fe4de79119f
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039992"
---
# <a name="wmwmshadowfilesourcedrmtype-windows-media-format-11-sdk"></a><span data-ttu-id="da068-104">WM/wmshadowfilesourcedrmtype (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="da068-104">WM/WMShadowFileSourceDRMType (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="da068-105">Das Attribut **WM/wmshadowfilesourcedrmtype** enthält den Typ von Rights Management, der zum Schutz der ursprünglichen Datei verwendet wird, von der die ASF-Datei abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="da068-105">The **WM/WMShadowFileSourceDRMType** attribute contains the type of rights management that is used to protect the original file that the ASF file is derived from.</span></span>

## <a name="global-constant"></a><span data-ttu-id="da068-106">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="da068-106">Global Constant</span></span>

<span data-ttu-id="da068-107">g \_ wszwmwmshadowfilesourcedrmtype</span><span class="sxs-lookup"><span data-stu-id="da068-107">g\_wszWMWMShadowFileSourceDRMType</span></span>

## <a name="data-type"></a><span data-ttu-id="da068-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="da068-108">Data Type</span></span>

<span data-ttu-id="da068-109">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="da068-109">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="da068-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="da068-110">Remarks</span></span>

<span data-ttu-id="da068-111">Inhalte, die sich in einem anderen Dateiformat als "ASF" befinden und durch eine Art von Rights Management geschützt sind, können durch einen Prozess namens "Lizenz Import" in eine Windows Media-Datei konvertiert werden, die von Windows Media DRM geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="da068-111">Content that exists in a file format other than ASF and is protected with some sort of rights management can be converted to a Windows Media file protected by Windows Media DRM through a process called license importing.</span></span> <span data-ttu-id="da068-112">Eine solche ASF-Datei sollte dieses Attribut sowie WM/wmshadowfilesourcefiletype enthalten, um zu verfolgen, woher der Inhalt stammt.</span><span class="sxs-lookup"><span data-stu-id="da068-112">Such an ASF file should contain this attribute as well as WM/WMShadowFileSourceFileType to track where the content came from.</span></span>

## <a name="see-also"></a><span data-ttu-id="da068-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="da068-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da068-114">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="da068-114">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




