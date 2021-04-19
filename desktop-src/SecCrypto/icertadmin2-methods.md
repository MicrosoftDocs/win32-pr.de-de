---
description: Die ICertAdmin2-Schnittstelle stellt die folgenden Methoden zur Verfügung.
ms.assetid: F6E0D863-5A78-48D5-8AED-DAEF80101B7E
title: ICertAdmin2-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 619e2afc9ee8e5e2eeab91893394e21e6c33ba14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356955"
---
# <a name="icertadmin2-methods"></a><span data-ttu-id="e6e40-103">ICertAdmin2-Methoden</span><span class="sxs-lookup"><span data-stu-id="e6e40-103">ICertAdmin2 Methods</span></span>

<span data-ttu-id="e6e40-104">Die [**ICertAdmin2**](/windows/desktop/api/Certadm/nn-certadm-icertadmin2) -Schnittstelle stellt die folgenden Methoden zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="e6e40-104">The [**ICertAdmin2**](/windows/desktop/api/Certadm/nn-certadm-icertadmin2) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e6e40-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="e6e40-105">In this section</span></span>

-   [<span data-ttu-id="e6e40-106">**DeleteRow-Methode**</span><span class="sxs-lookup"><span data-stu-id="e6e40-106">**DeleteRow Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-deleterow)
-   [<span data-ttu-id="e6e40-107">**Denyrequest-Methode**</span><span class="sxs-lookup"><span data-stu-id="e6e40-107">**DenyRequest Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-denyrequest)
-   [<span data-ttu-id="e6e40-108">**Getarchivedkey-Methode**</span><span class="sxs-lookup"><span data-stu-id="e6e40-108">**GetArchivedKey Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getarchivedkey)
-   [<span data-ttu-id="e6e40-109">**Getcaproperty-Methode**</span><span class="sxs-lookup"><span data-stu-id="e6e40-109">**GetCAProperty Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getcaproperty)
-   [<span data-ttu-id="e6e40-110">**Getcapropertydisplayname-Methode**</span><span class="sxs-lookup"><span data-stu-id="e6e40-110">**GetCAPropertyDisplayName Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getcapropertydisplayname)
-   [<span data-ttu-id="e6e40-111">**Getcapropertyflags-Methode**</span><span class="sxs-lookup"><span data-stu-id="e6e40-111">**GetCAPropertyFlags Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getcapropertyflags)
-   [<span data-ttu-id="e6e40-112">**Getconfigentry-Methode**</span><span class="sxs-lookup"><span data-stu-id="e6e40-112">**GetConfigEntry Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getconfigentry)
-   [<span data-ttu-id="e6e40-113">**Getcrl-Methode**</span><span class="sxs-lookup"><span data-stu-id="e6e40-113">**GetCRL Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-getcrl)
-   [<span data-ttu-id="e6e40-114">**Getmyrollen-Methode**</span><span class="sxs-lookup"><span data-stu-id="e6e40-114">**GetMyRoles Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-getmyroles)
-   [<span data-ttu-id="e6e40-115">**Getrevocationreason-Methode**</span><span class="sxs-lookup"><span data-stu-id="e6e40-115">**GetRevocationReason Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-getrevocationreason)
-   [<span data-ttu-id="e6e40-116">**Importcertificate-Methode**</span><span class="sxs-lookup"><span data-stu-id="e6e40-116">**ImportCertificate Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-importcertificate)
-   [<span data-ttu-id="e6e40-117">**Importkey-Methode**</span><span class="sxs-lookup"><span data-stu-id="e6e40-117">**ImportKey Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-importkey)
-   [<span data-ttu-id="e6e40-118">**Isvalidcertificate-Methode**</span><span class="sxs-lookup"><span data-stu-id="e6e40-118">**IsValidCertificate Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-isvalidcertificate)
-   [<span data-ttu-id="e6e40-119">**Publishcrl-Methode**</span><span class="sxs-lookup"><span data-stu-id="e6e40-119">**PublishCRL Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-publishcrl)
-   [<span data-ttu-id="e6e40-120">**Publishcrls-Methode**</span><span class="sxs-lookup"><span data-stu-id="e6e40-120">**PublishCRLs Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-publishcrls)
-   [<span data-ttu-id="e6e40-121">**Resubmitrequest-Methode**</span><span class="sxs-lookup"><span data-stu-id="e6e40-121">**ResubmitRequest Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-resubmitrequest)
-   [<span data-ttu-id="e6e40-122">**Revokecertificate-Methode**</span><span class="sxs-lookup"><span data-stu-id="e6e40-122">**RevokeCertificate Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-revokecertificate)
-   [<span data-ttu-id="e6e40-123">**Setcaproperty-Methode**</span><span class="sxs-lookup"><span data-stu-id="e6e40-123">**SetCAProperty Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-setcaproperty)
-   [<span data-ttu-id="e6e40-124">**Setcertificateextension-Methode**</span><span class="sxs-lookup"><span data-stu-id="e6e40-124">**SetCertificateExtension Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-setcertificateextension)
-   [<span data-ttu-id="e6e40-125">**Setconfigentry-Methode**</span><span class="sxs-lookup"><span data-stu-id="e6e40-125">**SetConfigEntry Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin2-setconfigentry)
-   [<span data-ttu-id="e6e40-126">**Methode "-Methode"**</span><span class="sxs-lookup"><span data-stu-id="e6e40-126">**SetRequestAttributes Method**</span></span>](/windows/desktop/api/Certadm/nf-certadm-icertadmin-setrequestattributes)

 

 



