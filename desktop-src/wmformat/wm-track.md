---
title: WM/Nachverfolgung
description: Das WM/Track-Attribut enthält die Nachverfolgung der Inhalte. Dieses Attribut ist NULL basiert und wird aus Gründen der Abwärtskompatibilität unterstützt. Neuer Inhalt sollte stattdessen das WM/tracknumber-Attribut verwenden.
ms.assetid: c763d7b0-9d12-4a4e-8c9f-9cf67bd2a02b
keywords:
- WM/Nachverfolgen des Windows Media-Formats
topic_type:
- apiref
api_name:
- WM/Track
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 244426175ea74bc0281f8822964c2fc0bfa37aa7
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104388900"
---
# <a name="wmtrack"></a><span data-ttu-id="25194-106">WM/Nachverfolgung</span><span class="sxs-lookup"><span data-stu-id="25194-106">WM/Track</span></span>

<span data-ttu-id="25194-107">Das **WM/Track-** Attribut enthält die Nachverfolgung der Inhalte.</span><span class="sxs-lookup"><span data-stu-id="25194-107">The **WM/Track** attribute contains the track number of the content.</span></span> <span data-ttu-id="25194-108">Dieses Attribut ist NULL basiert und wird aus Gründen der Abwärtskompatibilität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="25194-108">This attribute is zero-based and is supported for backward compatibility.</span></span> <span data-ttu-id="25194-109">Neuer Inhalt sollte stattdessen das [**WM/tracknumber-**](wm-tracknumber.md) Attribut verwenden.</span><span class="sxs-lookup"><span data-stu-id="25194-109">New content should use the [**WM/TrackNumber**](wm-tracknumber.md) attribute instead.</span></span>

## <a name="global-constant"></a><span data-ttu-id="25194-110">Globale Konstante</span><span class="sxs-lookup"><span data-stu-id="25194-110">Global Constant</span></span>

<span data-ttu-id="25194-111">g \_ wszwmtrack</span><span class="sxs-lookup"><span data-stu-id="25194-111">g\_wszWMTrack</span></span>

## <a name="data-type"></a><span data-ttu-id="25194-112">Datentyp</span><span class="sxs-lookup"><span data-stu-id="25194-112">Data Type</span></span>

<span data-ttu-id="25194-113">**WMT \_ - \_ Typzeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="25194-113">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="25194-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25194-114">Remarks</span></span>

<span data-ttu-id="25194-115">Viele vorhandene Anwendungen schreiben den Wert für **WM/Track** als **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="25194-115">Many existing applications write the value for **WM/Track** as a **DWORD**.</span></span> <span data-ttu-id="25194-116">Wenn Sie eine Anwendung erstellen, die Dateien aus unbekannten Quellen wieder gibt, sollten Sie Code einschließen, um sowohl Zeichen folgen-als auch **DWORD** -Werte zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="25194-116">If you create an application that plays files from unknown sources, you should include code to handle both string and **DWORD** values.</span></span>

## <a name="see-also"></a><span data-ttu-id="25194-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25194-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25194-118">**Attributliste**</span><span class="sxs-lookup"><span data-stu-id="25194-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




