---
title: Strukturen (OLE und Datenübertragung)
description: Die folgenden Strukturen werden verwendet, um Verbund Dokumente zu implementieren und die Datenübertragung zwischen Anwendungen auszuführen.
ms.assetid: 76fef2dd-4cfb-4526-a1e0-8e3218aa6145
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa9dde7f81d388943dbc05b2d38065be262d7f29
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039950"
---
# <a name="structures-ole-and-data-transfer"></a><span data-ttu-id="94a87-103">Strukturen (OLE und Datenübertragung)</span><span class="sxs-lookup"><span data-stu-id="94a87-103">Structures (OLE and Data Transfer)</span></span>

<span data-ttu-id="94a87-104">Die folgenden Strukturen werden verwendet, um Verbund Dokumente zu implementieren und die Datenübertragung zwischen Anwendungen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="94a87-104">The following structures are used to implement compound documents and perform data transfer between applications.</span></span>

-   [<span data-ttu-id="94a87-105">**Dvaspectinfo**</span><span class="sxs-lookup"><span data-stu-id="94a87-105">**DVASPECTINFO**</span></span>](/windows/win32/api/ocidl/ne-ocidl-dvaspectinfoflag)
-   [<span data-ttu-id="94a87-106">**Dvextentinfo**</span><span class="sxs-lookup"><span data-stu-id="94a87-106">**DVEXTENTINFO**</span></span>](/windows/win32/api/ocidl/ns-ocidl-dvextentinfo)
-   [<span data-ttu-id="94a87-107">**DVTARGETDEVICE**</span><span class="sxs-lookup"><span data-stu-id="94a87-107">**DVTARGETDEVICE**</span></span>](/windows/win32/api/objidl/ns-objidl-dvtargetdevice)
-   [<span data-ttu-id="94a87-108">**Formatusw.**</span><span class="sxs-lookup"><span data-stu-id="94a87-108">**FORMATETC**</span></span>](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc)
-   [<span data-ttu-id="94a87-109">**Objectdescriptor**</span><span class="sxs-lookup"><span data-stu-id="94a87-109">**OBJECTDESCRIPTOR**</span></span>](/windows/win32/api/oleidl/ns-oleidl-objectdescriptor)
-   [<span data-ttu-id="94a87-110">**Olecmd**</span><span class="sxs-lookup"><span data-stu-id="94a87-110">**OLECMD**</span></span>](/windows/desktop/api/DocObj/ns-docobj-olecmd)
-   [<span data-ttu-id="94a87-111">**Olecmdtext**</span><span class="sxs-lookup"><span data-stu-id="94a87-111">**OLECMDTEXT**</span></span>](/windows/desktop/api/DocObj/ns-docobj-olecmdtext)
-   [<span data-ttu-id="94a87-112">**Oleinplaceframeinfo**</span><span class="sxs-lookup"><span data-stu-id="94a87-112">**OLEINPLACEFRAMEINFO**</span></span>](/windows/win32/api/oleidl/ns-oleidl-oleinplaceframeinfo)
-   [<span data-ttu-id="94a87-113">**Olemenugroupbreiten**</span><span class="sxs-lookup"><span data-stu-id="94a87-113">**OLEMENUGROUPWIDTHS**</span></span>](/windows/win32/api/oleidl/ns-oleidl-olemenugroupwidths)
-   [<span data-ttu-id="94a87-114">**Oleuibusy**</span><span class="sxs-lookup"><span data-stu-id="94a87-114">**OLEUIBUSY**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuibusya)
-   [<span data-ttu-id="94a87-115">**Oleuichangeicon**</span><span class="sxs-lookup"><span data-stu-id="94a87-115">**OLEUICHANGEICON**</span></span>](/windows/win32/api/oledlg/nf-oledlg-oleuichangeicona)
-   [<span data-ttu-id="94a87-116">**Oleuichangesource**</span><span class="sxs-lookup"><span data-stu-id="94a87-116">**OLEUICHANGESOURCE**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuichangesourcea)
-   [<span data-ttu-id="94a87-117">**OLEUICONVERT**</span><span class="sxs-lookup"><span data-stu-id="94a87-117">**OLEUICONVERT**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuiconverta)
-   [<span data-ttu-id="94a87-118">**Oleuieditlinks**</span><span class="sxs-lookup"><span data-stu-id="94a87-118">**OLEUIEDITLINKS**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuieditlinksa)
-   [<span data-ttu-id="94a87-119">**Oleuignrl-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="94a87-119">**OLEUIGNRLPROPS**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuignrlpropsa)
-   [<span data-ttu-id="94a87-120">**Oleuiinsertobject**</span><span class="sxs-lookup"><span data-stu-id="94a87-120">**OLEUIINSERTOBJECT**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuiinsertobjecta)
-   [<span data-ttu-id="94a87-121">**Oleuilink-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="94a87-121">**OLEUILINKPROPS**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuilinkpropsa)
-   [<span data-ttu-id="94a87-122">**Oleuiobject-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="94a87-122">**OLEUIOBJECTPROPS**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuiobjectpropsa)
-   [<span data-ttu-id="94a87-123">**Oleuipasteentry**</span><span class="sxs-lookup"><span data-stu-id="94a87-123">**OLEUIPASTEENTRY**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuipasteentrya)
-   [<span data-ttu-id="94a87-124">**Oleuipastespecial**</span><span class="sxs-lookup"><span data-stu-id="94a87-124">**OLEUIPASTESPECIAL**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuipastespeciala)
-   [<span data-ttu-id="94a87-125">**Oleuiview-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="94a87-125">**OLEUIVIEWPROPS**</span></span>](/windows/win32/api/oledlg/ns-oledlg-oleuiviewpropsa)
-   [<span data-ttu-id="94a87-126">**OLEVERB**</span><span class="sxs-lookup"><span data-stu-id="94a87-126">**OLEVERB**</span></span>](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)
-   [<span data-ttu-id="94a87-127">**POINTF**</span><span class="sxs-lookup"><span data-stu-id="94a87-127">**POINTF**</span></span>](/windows/win32/api/ocidl/ns-ocidl-pointf)
-   [<span data-ttu-id="94a87-128">**STATDATA**</span><span class="sxs-lookup"><span data-stu-id="94a87-128">**STATDATA**</span></span>](/windows/desktop/api/ObjIdl/nn-objidl-ienumstatdata)
-   [<span data-ttu-id="94a87-129">**STGMEDIUM**</span><span class="sxs-lookup"><span data-stu-id="94a87-129">**STGMEDIUM**</span></span>](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)

 

 




