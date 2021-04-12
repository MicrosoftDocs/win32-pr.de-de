---
title: Iwmdrmnettransmitter-Schnittstelle
description: Die iwmdrmnettransmitter-Schnittstelle stellt Methoden bereit, die erforderlich sind, um Windows Media DRM für Netzwerkgeräte als Sender zu verwenden. Um eine Instanz dieser Schnittstelle zu erhalten, rufen Sie iwmdrmprovider-Erstellungsobjekt auf. Übergeben Sie IID \_ iwmdrmnettransmitter als riid-Parameter.
ms.assetid: e93db52a-8829-4d16-b839-824e34b3e582
keywords:
- Iwmdrmnettransmitter-Schnittstelle Windows Media-Format
- Iwmdrmnettransmitter-Schnittstelle Windows Media-Format, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a56db31bb7c03aa70aa136dcd07a8f41f1d9b84d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315753"
---
# <a name="iwmdrmnettransmitter-interface"></a><span data-ttu-id="cd594-106">Iwmdrmnettransmitter-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="cd594-106">IWMDRMNetTransmitter interface</span></span>

<span data-ttu-id="cd594-107">Die **iwmdrmnettransmitter** -Schnittstelle stellt Methoden bereit, die erforderlich sind, um Windows Media DRM für Netzwerkgeräte als Sender zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cd594-107">The **IWMDRMNetTransmitter** interface provides methods needed to use Windows Media DRM for Network Devices as a transmitter.</span></span>

<span data-ttu-id="cd594-108">Um eine Instanz dieser Schnittstelle abzurufen, rufen Sie [**iwmdrmprovider:: builateobject**](iwmdrmprovider-createobject.md)auf.</span><span class="sxs-lookup"><span data-stu-id="cd594-108">To obtain an instance of this interface, call [**IWMDRMProvider::CreateObject**](iwmdrmprovider-createobject.md).</span></span> <span data-ttu-id="cd594-109">Übergeben Sie **IID \_ iwmdrmnettransmitter** als *riid* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="cd594-109">Pass **IID\_IWMDRMNetTransmitter** as the *riid* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="cd594-110">Member</span><span class="sxs-lookup"><span data-stu-id="cd594-110">Members</span></span>

<span data-ttu-id="cd594-111">Die **iwmdrmnettransmitter** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cd594-111">The **IWMDRMNetTransmitter** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="cd594-112">**Iwmdrmnettransmitter** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="cd594-112">**IWMDRMNetTransmitter** also has these types of members:</span></span>

-   [<span data-ttu-id="cd594-113">Methoden</span><span class="sxs-lookup"><span data-stu-id="cd594-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cd594-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="cd594-114">Methods</span></span>

<span data-ttu-id="cd594-115">Die **iwmdrmnettransmitter** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="cd594-115">The **IWMDRMNetTransmitter** interface has these methods.</span></span>



| <span data-ttu-id="cd594-116">Methode</span><span class="sxs-lookup"><span data-stu-id="cd594-116">Method</span></span>                                                                        | <span data-ttu-id="cd594-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd594-117">Description</span></span>                                                                                                 |
|:------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd594-118">**Getleaflicenseresponse**</span><span class="sxs-lookup"><span data-stu-id="cd594-118">**GetLeafLicenseResponse**</span></span>](iwmdrmnettransmitter-getleaflicenseresponse.md) | <span data-ttu-id="cd594-119">Generiert eine Blatt Lizenz-Antwortnachricht.</span><span class="sxs-lookup"><span data-stu-id="cd594-119">Generates a leaf license response message.</span></span><br/>                                                       |
| [<span data-ttu-id="cd594-120">**Getrootlicenseresponse**</span><span class="sxs-lookup"><span data-stu-id="cd594-120">**GetRootLicenseResponse**</span></span>](iwmdrmnettransmitter-getrootlicenseresponse.md) | <span data-ttu-id="cd594-121">Generiert eine Stamm Lizenz-Antwortnachricht.</span><span class="sxs-lookup"><span data-stu-id="cd594-121">Generates a root license response message</span></span><br/>                                                        |
| [<span data-ttu-id="cd594-122">**Setlicensechallenge**</span><span class="sxs-lookup"><span data-stu-id="cd594-122">**SetLicenseChallenge**</span></span>](iwmdrmnettransmitter-setlicensechallenge.md)       | <span data-ttu-id="cd594-123">Verarbeitet eine Lizenzanfrage, die von einem Microsoft Windows Media DRM für Netzwerkgeräte Empfänger gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="cd594-123">Processes a license challenge sent by a Microsoft Windows Media DRM for Network Devices receiver</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="cd594-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd594-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd594-125">**Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="cd594-125">**Interfaces**</span></span>](drm-interfaces.md)
</dt> <dt>

[<span data-ttu-id="cd594-126">**Iwmdrmnetreceiver-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="cd594-126">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> </dl>

 

