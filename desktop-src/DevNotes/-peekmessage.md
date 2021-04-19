---
description: Sendet eingehende gesendete Nachrichten, überprüft die Thread Meldungs Warteschlange auf eine gesendete Nachricht und ruft die Nachricht (sofern vorhanden) ab.
ms.assetid: 6b20f354-413d-4197-8b49-e6f965121865
title: _PeekMessage-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _PeekMessage
api_type:
- DllExport
api_location:
- Msmdun80.dll
- Sqlunirl.dll
ms.openlocfilehash: d37e43078e429013d2c7efebf38dfcfa75a12236
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356363"
---
# <a name="_peekmessage-function"></a><span data-ttu-id="ed8fe-103">\_Peer Message-Funktion</span><span class="sxs-lookup"><span data-stu-id="ed8fe-103">\_PeekMessage function</span></span>

<span data-ttu-id="ed8fe-104">\[Diese Funktion ist ein Wrapper über die Funktion " **Peer Message** ".</span><span class="sxs-lookup"><span data-stu-id="ed8fe-104">\[This function is a wrapper over the **PeekMessage** function.</span></span> <span data-ttu-id="ed8fe-105">Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="ed8fe-106">Anwendungen sollten " **Peer-Message** " direkt aufrufen.\]</span><span class="sxs-lookup"><span data-stu-id="ed8fe-106">Applications should call **PeekMessage** directly.\]</span></span>

<span data-ttu-id="ed8fe-107">Sendet eingehende gesendete Nachrichten, überprüft die Thread Meldungs Warteschlange auf eine gesendete Nachricht und ruft die Nachricht (sofern vorhanden) ab.</span><span class="sxs-lookup"><span data-stu-id="ed8fe-107">Dispatches incoming sent messages, checks the thread message queue for a posted message, and retrieves the message (if any exist).</span></span> <span data-ttu-id="ed8fe-108">Siehe " [**Peer Message**](/windows/win32/api/winuser/nf-winuser-peekmessagea)".</span><span class="sxs-lookup"><span data-stu-id="ed8fe-108">See [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea).</span></span>

## <a name="syntax"></a><span data-ttu-id="ed8fe-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed8fe-109">Syntax</span></span>


```C++
BOOL _PeekMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="ed8fe-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed8fe-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed8fe-111">*...*</span><span class="sxs-lookup"><span data-stu-id="ed8fe-111">*...*</span></span> 
<span data-ttu-id="ed8fe-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ed8fe-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ed8fe-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed8fe-113">Requirements</span></span>



| <span data-ttu-id="ed8fe-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ed8fe-114">Requirement</span></span> | <span data-ttu-id="ed8fe-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ed8fe-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed8fe-116">DLL</span><span class="sxs-lookup"><span data-stu-id="ed8fe-116">DLL</span></span><br/> | <dl> <span data-ttu-id="ed8fe-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed8fe-117"><dt>Msmdun80.dll; </dt> <dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed8fe-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ed8fe-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed8fe-119">**PeekMessage**</span><span class="sxs-lookup"><span data-stu-id="ed8fe-119">**PeekMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> </dl>

 

 
