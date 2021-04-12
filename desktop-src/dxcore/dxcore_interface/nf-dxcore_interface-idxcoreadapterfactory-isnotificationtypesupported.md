---
title: IDXCoreAdapterFactory::IsNotificationTypeSupported
description: Bestimmt, ob ein angegebener Benachrichtigungstyp vom Betriebssystem unterstützt wird.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 78730167e7ec139733ee1e4011d2e5e59c32782b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315968"
---
# <a name="idxcoreadapterfactoryisnotificationtypesupported-method"></a><span data-ttu-id="978ab-103">Idxcoreadapterfactory:: isnotificationtypesupportiert-Methode</span><span class="sxs-lookup"><span data-stu-id="978ab-103">IDXCoreAdapterFactory::IsNotificationTypeSupported method</span></span>

<span data-ttu-id="978ab-104">Bestimmt, ob ein angegebener Benachrichtigungstyp vom Betriebssystem unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="978ab-104">Determines whether a specified notification type is supported by the operating system (OS).</span></span> <span data-ttu-id="978ab-105">Programmieranleitungen und Codebeispiele finden [Sie unter Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="978ab-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="978ab-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="978ab-106">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsNotificationTypeSupported(
  DXCoreNotificationType notificationType) = 0;
```

## <a name="parameters"></a><span data-ttu-id="978ab-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="978ab-107">Parameters</span></span>

### <a name="notificationtype"></a><span data-ttu-id="978ab-108">notificationType</span><span class="sxs-lookup"><span data-stu-id="978ab-108">notificationType</span></span>

<span data-ttu-id="978ab-109">Typ: **[dxcorenotificationtype](./ne-dxcore_interface-dxcorenotificationtype.md)**</span><span class="sxs-lookup"><span data-stu-id="978ab-109">Type: **[DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md)**</span></span>

<span data-ttu-id="978ab-110">Der Typ der Benachrichtigung, die Sie für die Unterstützung von Abfragen.</span><span class="sxs-lookup"><span data-stu-id="978ab-110">The type of notification that you're querying about support for.</span></span> <span data-ttu-id="978ab-111">Informationen zu den Benachrichtigungs Typen finden Sie in der Tabelle unter [dxcorenotificationtype](./ne-dxcore_interface-dxcorenotificationtype.md) .</span><span class="sxs-lookup"><span data-stu-id="978ab-111">See the table in [DXCoreNotificationType](./ne-dxcore_interface-dxcorenotificationtype.md) for info about the notification types.</span></span>

## <a name="returns"></a><span data-ttu-id="978ab-112">Gibt zurück</span><span class="sxs-lookup"><span data-stu-id="978ab-112">Returns</span></span>

<span data-ttu-id="978ab-113">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="978ab-113">Type: **bool**</span></span>

<span data-ttu-id="978ab-114">Gibt zurück,  `true`   Wenn der Benachrichtigungstyp vom System unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="978ab-114">Returns `true` if the notification type is supported by the system.</span></span> <span data-ttu-id="978ab-115">Andernfalls wird zurückgegeben  `false` .</span><span class="sxs-lookup"><span data-stu-id="978ab-115">Otherwise, returns `false`.</span></span>

## <a name="remarks"></a><span data-ttu-id="978ab-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="978ab-116">Remarks</span></span>

<span data-ttu-id="978ab-117">Sie können **isnotificationtypesupportiert** anrufen, um zu bestimmen, ob ein bestimmter Benachrichtigungstyp dieser Version des Betriebssystems bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="978ab-117">You can call **IsNotificationTypeSupported** to determine whether a given notification type is known to this version of the OS.</span></span> <span data-ttu-id="978ab-118">Beispielsweise ist ein Benachrichtigungstyp, der in einer bestimmten Version von Windows eingeführt wurde, in früheren Versionen von Windows unbekannt.</span><span class="sxs-lookup"><span data-stu-id="978ab-118">For example, a notification type that's introduced in a particular version of Windows is unknown to previous versions of Windows.</span></span>

## <a name="see-also"></a><span data-ttu-id="978ab-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="978ab-119">See also</span></span>

<span data-ttu-id="978ab-120">[Idxcoreadapterfactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore-Referenz](../dxcore-reference.md), [DXCore-Adapter Attribut-GUIDs](../dxcore-adapter-attribute-guids.md), [Verwenden von DXCore zum Aufzählen von Adaptern](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="978ab-120">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>