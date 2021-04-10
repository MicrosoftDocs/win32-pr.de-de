---
title: Overrideeapcertifi| eselection
description: Der Registrierungsschlüssel overrideeapcertifi| eselection bestimmt, ob der Client das standardmäßige Smartcard-Zertifikat Auswahl Verhalten außer Kraft setzt, und stellt dem Benutzer mehr Zertifikate zur Auswahl bereit.
ms.assetid: 469FECA9-FF2A-46B1-9370-0FF28EF2FB33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d958eeeffba96e7a060ee4dd3edaf8a9935a15d1
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "103857855"
---
# <a name="overrideeapcertificateselection"></a><span data-ttu-id="0bd08-103">Overrideeapcertifi| eselection</span><span class="sxs-lookup"><span data-stu-id="0bd08-103">OverrideEAPCertificateSelection</span></span>

<span data-ttu-id="0bd08-104">Der Registrierungsschlüssel overrideeapcertifi| eselection bestimmt, ob der Client das standardmäßige Smartcard-Zertifikat Auswahl Verhalten außer Kraft setzt, und stellt dem Benutzer mehr Zertifikate zur Auswahl bereit.</span><span class="sxs-lookup"><span data-stu-id="0bd08-104">The OverrideEAPCertificateSelection registry key determines whether the client will override the default smart card certificate selection behavior and provide the user with more certificates to choose from.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="0bd08-105">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="0bd08-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   OverrideEAPCertificateSelection = value
```

## <a name="remarks"></a><span data-ttu-id="0bd08-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0bd08-106">Remarks</span></span>

<span data-ttu-id="0bd08-107">Dies ist ein **reg- \_ Binärwert** .</span><span class="sxs-lookup"><span data-stu-id="0bd08-107">This is a **REG\_BINARY** value.</span></span>



| <span data-ttu-id="0bd08-108">Wert</span><span class="sxs-lookup"><span data-stu-id="0bd08-108">Value</span></span> | <span data-ttu-id="0bd08-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0bd08-109">Description</span></span>                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bd08-110">0x000</span><span class="sxs-lookup"><span data-stu-id="0bd08-110">0x000</span></span> | <span data-ttu-id="0bd08-111">Überschreiben Sie nicht das Standardverhalten.</span><span class="sxs-lookup"><span data-stu-id="0bd08-111">Do not override the default behavior.</span></span>                                                                                                                                                                |
| <span data-ttu-id="0bd08-112">0x001</span><span class="sxs-lookup"><span data-stu-id="0bd08-112">0x001</span></span> | <span data-ttu-id="0bd08-113">Wählen Sie das zuletzt angefügte Zertifikat von der Smartcard aus.</span><span class="sxs-lookup"><span data-stu-id="0bd08-113">Choose the last attached certificate from the smart card.</span></span>                                                                                                                                            |
| <span data-ttu-id="0bd08-114">0x010</span><span class="sxs-lookup"><span data-stu-id="0bd08-114">0x010</span></span> | <span data-ttu-id="0bd08-115">Zeigt alle Zertifikate auf der Smartcard in der Benutzeroberfläche für die Zertifikat Auswahl an.</span><span class="sxs-lookup"><span data-stu-id="0bd08-115">Shows all certificates in the certificate selection UI from the smart card.</span></span>                                                                                                                          |
| <span data-ttu-id="0bd08-116">0x100</span><span class="sxs-lookup"><span data-stu-id="0bd08-116">0x100</span></span> | <span data-ttu-id="0bd08-117">Zeigt alle Zertifikate in der Benutzeroberfläche zur Zertifikat Auswahl aus der Registrierung an.</span><span class="sxs-lookup"><span data-stu-id="0bd08-117">Shows all certificates in the certificate selection UI from the registry.</span></span>                                                                                                                            |
| <span data-ttu-id="0bd08-118">0x101</span><span class="sxs-lookup"><span data-stu-id="0bd08-118">0x101</span></span> | <span data-ttu-id="0bd08-119">Zeigt alle Zertifikate in der Benutzeroberfläche zur Zertifikat Auswahl aus der Registrierung und das zuletzt angefügte Zertifikat von der Smartcard an.</span><span class="sxs-lookup"><span data-stu-id="0bd08-119">Shows all certificates in the certificate selection UI from the registry and the last attached certificate from the smart card.</span></span> <span data-ttu-id="0bd08-120">Zeigt das zuletzt angefügte Zertifikat von der Smartcard an, wie ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="0bd08-120">Shows the last attached certificate from the smart card as selected.</span></span> |
| <span data-ttu-id="0bd08-121">0x110</span><span class="sxs-lookup"><span data-stu-id="0bd08-121">0x110</span></span> | <span data-ttu-id="0bd08-122">Zeigt alle Zertifikate in der Benutzeroberfläche für die Zertifikat Auswahl aus der Registrierung und der Smartcard an.</span><span class="sxs-lookup"><span data-stu-id="0bd08-122">Shows all certificates in the certificate selection UI from the registry and the smart card.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="0bd08-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0bd08-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0bd08-124">EAPHost-Registrierungs Einstellungen</span><span class="sxs-lookup"><span data-stu-id="0bd08-124">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




