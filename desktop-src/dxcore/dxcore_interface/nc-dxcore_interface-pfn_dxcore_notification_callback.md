---
title: PFN_DXCORE_NOTIFICATION_CALLBACK
description: Eine Rückruffunktion (implementiert von Ihrer Anwendung), die von einem DXCore-Objekt für Benachrichtigungs Ereignisse aufgerufen wird.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 01d65f6907c60d6c68b612308b9105d18bbe037f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948993"
---
# <a name="pfn_dxcore_notification_callback-callback"></a><span data-ttu-id="e2ddd-103">PFN_DXCORE_NOTIFICATION_CALLBACK Rückruf</span><span class="sxs-lookup"><span data-stu-id="e2ddd-103">PFN_DXCORE_NOTIFICATION_CALLBACK callback</span></span>

<span data-ttu-id="e2ddd-104">Eine Rückruffunktion (implementiert von Ihrer Anwendung), die von einem DXCore-Objekt für Benachrichtigungs Ereignisse aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e2ddd-104">A callback function (implemented by your application), which is called by a DXCore object for notification events.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2ddd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2ddd-105">Syntax</span></span>

```cpp
typedef void (STDMETHODCALLTYPE *PFN_DXCORE_NOTIFICATION_CALLBACK)(
  DXCoreNotificationType notificationType,
  _In_ IUnknown *object,
  _In_opt_ void *context);
```

## <a name="parameters"></a><span data-ttu-id="e2ddd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2ddd-106">Parameters</span></span>

### <a name="notificationtype"></a><span data-ttu-id="e2ddd-107">notificationType</span><span class="sxs-lookup"><span data-stu-id="e2ddd-107">notificationType</span></span>

<span data-ttu-id="e2ddd-108">Typ: **[dxcorenotificationtype](./ne-dxcore_interface-dxcorenotificationtype.md)**</span><span class="sxs-lookup"><span data-stu-id="e2ddd-108">Type: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span></span>

<span data-ttu-id="e2ddd-109">Der Typ der Benachrichtigung, die diesen Aufruf darstellt.</span><span class="sxs-lookup"><span data-stu-id="e2ddd-109">The type of notification representing this invocation.</span></span> <span data-ttu-id="e2ddd-110">Informationen zu den Typen, die für welche Arten von Objekten gültig sind, finden Sie in der Tabelle unter [dxcorenotificationtype](./ne-dxcore_interface-dxcorenotificationtype.md) .</span><span class="sxs-lookup"><span data-stu-id="e2ddd-110">See the table in [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) for info about what types are valid with which kinds of objects.</span></span>

### <a name="object"></a><span data-ttu-id="e2ddd-111">Objekt (object)</span><span class="sxs-lookup"><span data-stu-id="e2ddd-111">object</span></span>

<span data-ttu-id="e2ddd-112">Typ: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span><span class="sxs-lookup"><span data-stu-id="e2ddd-112">Type: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***</span></span>

<span data-ttu-id="e2ddd-113">Das [idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md) -oder [idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md) -Objekt, das die Benachrichtigung erhöht.</span><span class="sxs-lookup"><span data-stu-id="e2ddd-113">The [IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md) or [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) object raising the notification.</span></span>

### <a name="context-in"></a><span data-ttu-id="e2ddd-114">Kontext [in]</span><span class="sxs-lookup"><span data-stu-id="e2ddd-114">context [in]</span></span>

<span data-ttu-id="e2ddd-115">Typ: **void \***</span><span class="sxs-lookup"><span data-stu-id="e2ddd-115">Type: **void\***</span></span>

<span data-ttu-id="e2ddd-116">Ein Zeiger `nullptr` auf ein Objekt, das Kontextinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="e2ddd-116">A pointer, which may be `nullptr`, to an object containing context info.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2ddd-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2ddd-117">See also</span></span>

<span data-ttu-id="e2ddd-118">[Idxcoreadapter](./nn-dxcore_interface-idxcoreadapter.md), [idxcoreadapterlist](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore-Referenz](../dxcore-reference.md), [Verwenden von DXCore zum Auflisten von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="e2ddd-118">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md), [DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>