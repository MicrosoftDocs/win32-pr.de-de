---
description: Sendet eine Meldung an das angegebene Steuerelement in einem Dialogfeld.
ms.assetid: 7c91e432-662c-4dd0-980c-892ce1092077
title: _SendDlgItemMessage-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendDlgItemMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: ea5595ecef953d81ee947042e6265178c1feecd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365964"
---
# <a name="_senddlgitemmessage-function"></a><span data-ttu-id="f75a6-103">\_SendDlgItemMess-Funktion</span><span class="sxs-lookup"><span data-stu-id="f75a6-103">\_SendDlgItemMessage function</span></span>

<span data-ttu-id="f75a6-104">\[Diese Funktion ist ein Wrapper über die **SendDlgItemMess** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="f75a6-104">\[This function is a wrapper over the **SendDlgItemMessage** function.</span></span> <span data-ttu-id="f75a6-105">Diese Funktion kann in Zukunft geändert oder nicht mehr verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="f75a6-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="f75a6-106">Anwendungen sollten **SendDlgItemMess** direkt aufzurufen.\]</span><span class="sxs-lookup"><span data-stu-id="f75a6-106">Applications should call **SendDlgItemMessage** directly.\]</span></span>

<span data-ttu-id="f75a6-107">Sendet eine Meldung an das angegebene Steuerelement in einem Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="f75a6-107">Sends a message to the specified control in a dialog box.</span></span> <span data-ttu-id="f75a6-108">Siehe [**SendDlgItemMess**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea).</span><span class="sxs-lookup"><span data-stu-id="f75a6-108">See [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea).</span></span>

## <a name="syntax"></a><span data-ttu-id="f75a6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="f75a6-109">Syntax</span></span>


```C++
LRESULT _SendDlgItemMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="f75a6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f75a6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f75a6-111">*...*</span><span class="sxs-lookup"><span data-stu-id="f75a6-111">*...*</span></span> 
<span data-ttu-id="f75a6-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="f75a6-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="f75a6-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f75a6-113">Requirements</span></span>



| <span data-ttu-id="f75a6-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f75a6-114">Requirement</span></span> | <span data-ttu-id="f75a6-115">Wert</span><span class="sxs-lookup"><span data-stu-id="f75a6-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f75a6-116">DLL</span><span class="sxs-lookup"><span data-stu-id="f75a6-116">DLL</span></span><br/> | <dl> <span data-ttu-id="f75a6-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f75a6-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f75a6-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f75a6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f75a6-119">**SendDlgItemMess age**</span><span class="sxs-lookup"><span data-stu-id="f75a6-119">**SendDlgItemMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)
</dt> </dl>

 

 
