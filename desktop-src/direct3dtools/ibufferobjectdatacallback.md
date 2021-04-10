---
description: Rückruf, der den Inhalt eines Objekts in einem Puffer Formular für diejenigen zurückgibt, die es unterstützen (Puffer, Texturen).
MS-HAID: vspixengine.IBufferObjectDataCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Ibufferobjectdatacallback-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: AAE4CE9A-B8EB-4ED6-9F48-D00C19B27A2E
api_name:
- IBufferObjectDataCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6e5fb7deebd7d1b16d333ae59edab9372b54ad8c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124166"
---
# <a name="span-idvspixengineibufferobjectdatacallbackspanibufferobjectdatacallback-interface"></a><span data-ttu-id="e918f-103"><span id="vspixengine.ibufferobjectdatacallback"></span>Ibufferobjectdatacallback-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e918f-103"><span id="vspixengine.ibufferobjectdatacallback"></span>IBufferObjectDataCallback interface</span></span>

<span data-ttu-id="e918f-104">Rückruf, der den Inhalt eines Objekts in einem Puffer Formular für diejenigen zurückgibt, die es unterstützen (Puffer, Texturen).</span><span class="sxs-lookup"><span data-stu-id="e918f-104">Callback to return the contents of an object in buffer form for those that support it (buffers, textures).</span></span>

## <a name="members"></a><span data-ttu-id="e918f-105">Member</span><span class="sxs-lookup"><span data-stu-id="e918f-105">Members</span></span>

<span data-ttu-id="e918f-106">Die **ibufferobjectdatacallback** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e918f-106">The **IBufferObjectDataCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e918f-107">**Ibufferobjectdatacallback** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="e918f-107">**IBufferObjectDataCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="e918f-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="e918f-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="e918f-109"><span id="methods"></span>Methoden</span><span class="sxs-lookup"><span data-stu-id="e918f-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="e918f-110">Die **ibufferobjectdatacallback** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="e918f-110">The **IBufferObjectDataCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="e918f-111">Methode</span><span class="sxs-lookup"><span data-stu-id="e918f-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="e918f-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e918f-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="e918f-113"><a href="/windows/desktop/direct3dtools/ibufferobjectdatacallback-resultcallback-bstr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="e918f-113"><a href="/windows/desktop/direct3dtools/ibufferobjectdatacallback-resultcallback-bstr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="e918f-114">Ein Rückruf, der den Host über Puffer Informationen benachrichtigt, die von der assocaas-Anforderung in eine Datei geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="e918f-114">A callback that notifies the host of buffer information written to a file by the assocaited request.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="e918f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e918f-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="e918f-116">Header</span><span class="sxs-lookup"><span data-stu-id="e918f-116">Header</span></span></p></td><td><span data-ttu-id="e918f-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="e918f-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
