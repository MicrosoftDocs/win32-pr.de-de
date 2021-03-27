---
description: Registriert eine neue appbar und gibt die Nachrichten-ID an, die vom System zum Senden von Benachrichtigungs Meldungen verwendet werden soll. Diese Nachricht sollte von einer appbar gesendet werden, bevor andere appbar-Meldungen gesendet werden.
ms.assetid: 1da9db13-6fdc-44b3-9985-de32d572675a
title: ABM_NEW Meldung (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fad11e6712d0afd0c1a5e9de07fd3d690800db13
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750312"
---
# <a name="abm_new-message"></a><span data-ttu-id="3c9f0-104">\_Neue Nachricht ABM</span><span class="sxs-lookup"><span data-stu-id="3c9f0-104">ABM\_NEW message</span></span>

<span data-ttu-id="3c9f0-105">Registriert eine neue appbar und gibt die Nachrichten-ID an, die vom System zum Senden von Benachrichtigungs Meldungen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3c9f0-105">Registers a new appbar and specifies the message identifier that the system should use to send it notification messages.</span></span> <span data-ttu-id="3c9f0-106">Diese Nachricht sollte von einer appbar gesendet werden, bevor andere appbar-Meldungen gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="3c9f0-106">An appbar should send this message before sending any other appbar messages.</span></span>


```C++
fRegistered = (BOOL) SHAppBarMessage(ABM_NEW, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="3c9f0-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c9f0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c9f0-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="3c9f0-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="3c9f0-109">Ein Zeiger auf eine [**appbardata**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) -Struktur, die das Fenster Handle und den Meldungs Bezeichner der neuen App-Leiste enthält.</span><span class="sxs-lookup"><span data-stu-id="3c9f0-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that contains the new appbar's window handle and message identifier.</span></span> <span data-ttu-id="3c9f0-110">Sie müssen die Member **CBSIZE**, **HWND** und **ucallbackmessage** angeben, wenn diese Nachricht gesendet wird. alle anderen Member werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="3c9f0-110">You must specify the **cbSize**, **hWnd**, and **uCallbackMessage** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c9f0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c9f0-111">Return value</span></span>

<span data-ttu-id="3c9f0-112">Gibt **true** zurück, wenn erfolgreich, oder **false** , wenn ein Fehler auftritt oder die appbar bereits registriert ist.</span><span class="sxs-lookup"><span data-stu-id="3c9f0-112">Returns **TRUE** if successful, or **FALSE** if an error occurs or if the appbar is already registered.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c9f0-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3c9f0-113">Requirements</span></span>



| <span data-ttu-id="3c9f0-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c9f0-114">Requirement</span></span> | <span data-ttu-id="3c9f0-115">Wert</span><span class="sxs-lookup"><span data-stu-id="3c9f0-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c9f0-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c9f0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3c9f0-117">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c9f0-117">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3c9f0-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c9f0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3c9f0-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c9f0-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3c9f0-120">Header</span><span class="sxs-lookup"><span data-stu-id="3c9f0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c9f0-121"><dt>Shellapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c9f0-121"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




