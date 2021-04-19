---
description: MTP-Erweiterungs Eigenschaften
ms.assetid: 58fc8741-261a-4e63-9fd3-8f0ca05866ad
title: MTP-Erweiterungs Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86a653d05285d62c7660bd914a785807a2341a01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356237"
---
# <a name="mtp-extension-properties"></a><span data-ttu-id="b72fa-103">MTP-Erweiterungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b72fa-103">MTP Extension Properties</span></span>

<span data-ttu-id="b72fa-104">Eigenschaften beschreiben Objekte, Eigenschaften, Ressourcen und Geräte.</span><span class="sxs-lookup"><span data-stu-id="b72fa-104">Properties describe objects, properties, resources, and devices.</span></span>

## <a name="vendor-extended-object-properties"></a><span data-ttu-id="b72fa-105">Vom Hersteller erweiterte Objekteigenschaften</span><span class="sxs-lookup"><span data-stu-id="b72fa-105">Vendor-Extended Object Properties</span></span>

<span data-ttu-id="b72fa-106">Wenn ein Gerätehersteller eine vom Hersteller erweiterte Eigenschaft für ein Geräte Objekt erstellt, werden die **\_ Eigenschaften des \_ MTP-Herstellers \_ für \_ Erweiterte \_ Objekte \_ des MTP** -Herstellers mit dem Eigenschafts Code des Objekts kombiniert, um eine **PropertyKey** -Struktur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b72fa-106">When a device manufacturer creates a vendor-extended property for a device object, they combine the **WPD\_PROPERTIES\_MTP\_VENDOR\_EXTENDED\_OBJECT\_PROPS** GUID with the object's property code to construct a **PROPERTYKEY** structure.</span></span>

<span data-ttu-id="b72fa-107">Wenn z. b. der Eigenschafts Code des Objekts 0xd801 ist, würde der resultierende **PropertyKey** wie im folgenden Beispiel gezeigt lauten:</span><span class="sxs-lookup"><span data-stu-id="b72fa-107">For example, if the object's property code is 0xD801, the resulting **PROPERTYKEY** would be as shown in the following example:</span></span>


```C++
{4D545058-4FCE-4578-95C8-8698A9BC0F49}\D801
```



## <a name="vendor-extended-device-properties"></a><span data-ttu-id="b72fa-108">Vom Hersteller erweiterte Geräteeigenschaften</span><span class="sxs-lookup"><span data-stu-id="b72fa-108">Vendor-Extended Device Properties</span></span>

<span data-ttu-id="b72fa-109">Wenn ein Gerätehersteller eine vom Hersteller erweiterte Eigenschaft für ein Gerät erstellt, kombiniert er die **Eigenschaften des \_ \_ MTP- \_ Herstellers \_ für \_ Erweiterte \_ Geräteeigenschaften des MTP** -Herstellers mit dem Eigenschafts Code des Objekts, um eine **PropertyKey** -Struktur zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b72fa-109">When a device manufacturer creates a vendor-extended property for a device, they combine the **WPD\_PROPERTIES\_MTP\_VENDOR\_EXTENDED\_DEVICE\_PROPS** GUID with the object's property code to construct a **PROPERTYKEY** structure.</span></span>

<span data-ttu-id="b72fa-110">Wenn z. b. der Eigenschafts Code des Objekts 0xd001 ist, würde der resultierende **PropertyKey** wie im folgenden Beispiel gezeigt lauten:</span><span class="sxs-lookup"><span data-stu-id="b72fa-110">For example, if the object's property code is 0xD001, the resulting **PROPERTYKEY** would be as shown in the following example:</span></span>


```C++
{4D545058-8900-40b3-8F1D-DC246E1E8370}\D001
```



## <a name="related-topics"></a><span data-ttu-id="b72fa-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b72fa-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b72fa-112">Unterstützen von MTP-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="b72fa-112">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 



