---
description: Die iwiapropertystorage-Schnittstelle stellt Methoden zum Lesen und Schreiben der Eigenschaften eines Windows-Abbild Erwerbs (WIA) dar. Zu den Element Eigenschaften zählen Geräte Befehle, Informationen zum Element Format und Geräteinformationen.
ms.assetid: 268d2298-bc9c-479b-b078-a8180cd38bc3
title: Lesen und Festlegen von WIA-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51df3e8fdb4b29abb6f64743ab8f7f2dd3776358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129401"
---
# <a name="reading-and-setting-wia-properties"></a><span data-ttu-id="e25ce-104">Lesen und Festlegen von WIA-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e25ce-104">Reading and Setting WIA Properties</span></span>

<span data-ttu-id="e25ce-105">Die [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) -Schnittstelle stellt Methoden zum Lesen und Schreiben der Eigenschaften eines Windows-Abbild Erwerbs (WIA) dar.</span><span class="sxs-lookup"><span data-stu-id="e25ce-105">The [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface provides methods for reading and writing a Windows Image Acquisition (WIA) item's properties.</span></span> <span data-ttu-id="e25ce-106">Zu den Element Eigenschaften zählen Geräte Befehle, Informationen zum Element Format und Geräteinformationen.</span><span class="sxs-lookup"><span data-stu-id="e25ce-106">Item properties include device commands, item format information, and device information.</span></span>

<span data-ttu-id="e25ce-107">Eine Anwendung kann einen Zeiger auf eine [**iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) -Schnittstelle eines Elements abrufen, indem Sie die Geräteinformationen oder Ereignis Informationen des Elements aufzählt, indem Sie [**iwiaitem:: enumdevicecapabilior**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) [**iwiaitem:: enumregistereventinfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) aufrufen oder indem Sie die [**iwiaitem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) -Schnittstelle des Elements Abfragen.</span><span class="sxs-lookup"><span data-stu-id="e25ce-107">An application can obtain a pointer to an [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface of an item either by enumerating the item's device information or event information by calling [**IWiaItem::EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) or [**IWiaItem::EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) or by querying the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interface of the item.</span></span> <span data-ttu-id="e25ce-108">(In WIA 2,0 rufen Sie dies durch Aufrufen von [**IWiaItem2:: enumdevicecapabilior**](-wia-iwiaitem2-enumdevicecapabilities.md) [**IWiaItem2:: enumregistereventinfo**](-wia-iwiaitem2-enumregistereventinfo.md) oder durch Abfragen der [**IWiaItem2**](-wia-iwiaitem2.md) -Schnittstelle des Elements auf.)</span><span class="sxs-lookup"><span data-stu-id="e25ce-108">(In WIA 2.0, do this by calling [**IWiaItem2::EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) or [**IWiaItem2::EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) or by querying the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the item.)</span></span>

<span data-ttu-id="e25ce-109">[**Iwiapropertystorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) erbt von [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) , und die geerbten Methoden werden implementiert, wie im Referenz Abschnitt von strukturiertem Speicher im Windows Software Development Kit (SDK) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e25ce-109">[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) inherits from [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) and the inherited methods are implemented as described in the reference section of Structured Storage in the Windows Software Development Kit (SDK).</span></span>

> [!Note]
>
> <span data-ttu-id="e25ce-110">WIA-Anwendungen sollten Bild Daten Header immer für genaue Bild Informationen lesen.</span><span class="sxs-lookup"><span data-stu-id="e25ce-110">WIA applications should always read image data headers for accurate image information.</span></span> <span data-ttu-id="e25ce-111">Der WIA-Treiber kann die WIA-Eigenschaften und Bild Daten Header während der Datenübertragung ändern.</span><span class="sxs-lookup"><span data-stu-id="e25ce-111">The WIA driver can alter the WIA properties and image data headers during data transfer.</span></span>
>
> <span data-ttu-id="e25ce-112">Wenn kein Bild Daten Header im angegebenen Format angegeben ist, sollte die WIA-Anwendung die WIA-Eigenschaften als Informationsquelle für die Datenübertragung verwenden.</span><span class="sxs-lookup"><span data-stu-id="e25ce-112">If there is no image data header supplied with the specified format, the WIA application should use the WIA properties as an information source about the data transfer.</span></span> <span data-ttu-id="e25ce-113">Die WIA-Anwendung sollte die benötigten WIA-Eigenschaften nach Abschluss der Überprüfung oder Erfassung erneut registrieren, um die aktualisierten Einstellungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e25ce-113">The WIA application should reread the needed WIA properties after the scan or capture completes to get the updated settings.</span></span>

 

<span data-ttu-id="e25ce-114">In den folgenden Abschnitten werden die verschiedenen WIA-Eigenschaften beschrieben:</span><span class="sxs-lookup"><span data-stu-id="e25ce-114">The following sections describe the various WIA properties:</span></span>

-   [<span data-ttu-id="e25ce-115">Überprüfung der WIA-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="e25ce-115">WIA Property Validation</span></span>](-wia-wia-property-validation.md)
-   [<span data-ttu-id="e25ce-116">Geräte Informations Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e25ce-116">Device Information Properties</span></span>](-wia-device-information-properties-wia-dip-xxxx.md)
-   [<span data-ttu-id="e25ce-117">Geräteeigenschaften</span><span class="sxs-lookup"><span data-stu-id="e25ce-117">Device Properties</span></span>](-wia-device-properties.md)
-   [<span data-ttu-id="e25ce-118">Element Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e25ce-118">Item Properties</span></span>](-wia-item-properties.md)
-   [<span data-ttu-id="e25ce-119">Zusätzliche WIA-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e25ce-119">Additional WIA Properties</span></span>](-wia-additional-wia-properties.md)
-   [<span data-ttu-id="e25ce-120">Definieren von benutzerdefinierten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e25ce-120">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
-   [<span data-ttu-id="e25ce-121">Verwenden von benutzerdefinierten Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e25ce-121">Using Custom Properties</span></span>](-wia-using-custom-properties.md)
-   [<span data-ttu-id="e25ce-122">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="e25ce-122">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)

 

 
