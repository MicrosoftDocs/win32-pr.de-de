---
description: Elliptische Kurven in den Windows 10-Versionen 1507 und 1511.
title: Elliptische TLS-Kurven in Windows 10, Version 1507 und 1511
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: c38d1014433e1274d8dff52be09d59761d3b1761
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359446"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1507-and-1511"></a><span data-ttu-id="2f3eb-103">Elliptische TLS-Kurven in Windows 10, Version 1507 und 1511</span><span class="sxs-lookup"><span data-stu-id="2f3eb-103">TLS Elliptic Curves in Windows 10 version 1507 and 1511</span></span>

<span data-ttu-id="2f3eb-104">Für Windows 10, Version 1507 und 1511, sind die folgenden elliptischen Kurven aktiviert, und in dieser Prioritäts Reihenfolge wird standardmäßig der Microsoft SChannel-Anbieter verwendet:</span><span class="sxs-lookup"><span data-stu-id="2f3eb-104">For Windows 10, versions 1507 and 1511, the following elliptic curves are enabled and in this priority order by default using the Microsoft Schannel Provider:</span></span>

| <span data-ttu-id="2f3eb-105">Zeichenfolge mit elliptischer Kurve</span><span class="sxs-lookup"><span data-stu-id="2f3eb-105">Elliptic curve string</span></span> | <span data-ttu-id="2f3eb-106">Verfügbar im PPS-Modus</span><span class="sxs-lookup"><span data-stu-id="2f3eb-106">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="2f3eb-107">Benannte nistp256</span><span class="sxs-lookup"><span data-stu-id="2f3eb-107">NistP256</span></span> | <span data-ttu-id="2f3eb-108">Ja</span><span class="sxs-lookup"><span data-stu-id="2f3eb-108">Yes</span></span> |
| <span data-ttu-id="2f3eb-109">Benannte nistp384</span><span class="sxs-lookup"><span data-stu-id="2f3eb-109">NistP384</span></span> | <span data-ttu-id="2f3eb-110">Ja</span><span class="sxs-lookup"><span data-stu-id="2f3eb-110">Yes</span></span> |


<span data-ttu-id="2f3eb-111">Die folgenden elliptischen Kurven werden vom Microsoft SChannel-Anbieter unterstützt, sind jedoch nicht standardmäßig aktiviert:</span><span class="sxs-lookup"><span data-stu-id="2f3eb-111">The following elliptic curves are supported by the Microsoft Schannel Provider, but not enabled by default:</span></span>

| <span data-ttu-id="2f3eb-112">Zeichenfolge mit elliptischer Kurve</span><span class="sxs-lookup"><span data-stu-id="2f3eb-112">Elliptic curve string</span></span> | <span data-ttu-id="2f3eb-113">Verfügbar im PPS-Modus</span><span class="sxs-lookup"><span data-stu-id="2f3eb-113">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="2f3eb-114">benannte brainpoolp256r1</span><span class="sxs-lookup"><span data-stu-id="2f3eb-114">brainpoolP256r1</span></span> | <span data-ttu-id="2f3eb-115">Nein</span><span class="sxs-lookup"><span data-stu-id="2f3eb-115">No</span></span> |
| <span data-ttu-id="2f3eb-116">benannte brainpoolp384r1</span><span class="sxs-lookup"><span data-stu-id="2f3eb-116">brainpoolP384r1</span></span> | <span data-ttu-id="2f3eb-117">Nein</span><span class="sxs-lookup"><span data-stu-id="2f3eb-117">No</span></span> |
| <span data-ttu-id="2f3eb-118">benannte brainpoolp512r1</span><span class="sxs-lookup"><span data-stu-id="2f3eb-118">brainpoolP512r1</span></span> | <span data-ttu-id="2f3eb-119">Nein</span><span class="sxs-lookup"><span data-stu-id="2f3eb-119">No</span></span> |
| <span data-ttu-id="2f3eb-120">nistP192</span><span class="sxs-lookup"><span data-stu-id="2f3eb-120">nistP192</span></span> | <span data-ttu-id="2f3eb-121">Nein</span><span class="sxs-lookup"><span data-stu-id="2f3eb-121">No</span></span> |
| <span data-ttu-id="2f3eb-122">nistP224</span><span class="sxs-lookup"><span data-stu-id="2f3eb-122">nistP224</span></span> | <span data-ttu-id="2f3eb-123">Nein</span><span class="sxs-lookup"><span data-stu-id="2f3eb-123">No</span></span> |
| <span data-ttu-id="2f3eb-124">benannte nistp521</span><span class="sxs-lookup"><span data-stu-id="2f3eb-124">nistP521</span></span> | <span data-ttu-id="2f3eb-125">Ja</span><span class="sxs-lookup"><span data-stu-id="2f3eb-125">Yes</span></span> |
| <span data-ttu-id="2f3eb-126">secP160k1</span><span class="sxs-lookup"><span data-stu-id="2f3eb-126">secP160k1</span></span> | <span data-ttu-id="2f3eb-127">Nein</span><span class="sxs-lookup"><span data-stu-id="2f3eb-127">No</span></span> |
| <span data-ttu-id="2f3eb-128">secP160r1</span><span class="sxs-lookup"><span data-stu-id="2f3eb-128">secP160r1</span></span> | <span data-ttu-id="2f3eb-129">Nein</span><span class="sxs-lookup"><span data-stu-id="2f3eb-129">No</span></span> |
| <span data-ttu-id="2f3eb-130">secP160r2</span><span class="sxs-lookup"><span data-stu-id="2f3eb-130">secP160r2</span></span> | <span data-ttu-id="2f3eb-131">Nein</span><span class="sxs-lookup"><span data-stu-id="2f3eb-131">No</span></span> |
| <span data-ttu-id="2f3eb-132">secP192k1</span><span class="sxs-lookup"><span data-stu-id="2f3eb-132">secP192k1</span></span> | <span data-ttu-id="2f3eb-133">Nein</span><span class="sxs-lookup"><span data-stu-id="2f3eb-133">No</span></span> |
| <span data-ttu-id="2f3eb-134">secP192r1</span><span class="sxs-lookup"><span data-stu-id="2f3eb-134">secP192r1</span></span> | <span data-ttu-id="2f3eb-135">Nein</span><span class="sxs-lookup"><span data-stu-id="2f3eb-135">No</span></span> |
| <span data-ttu-id="2f3eb-136">secP224k1</span><span class="sxs-lookup"><span data-stu-id="2f3eb-136">secP224k1</span></span> | <span data-ttu-id="2f3eb-137">Nein</span><span class="sxs-lookup"><span data-stu-id="2f3eb-137">No</span></span> |
| <span data-ttu-id="2f3eb-138">secP224r1</span><span class="sxs-lookup"><span data-stu-id="2f3eb-138">secP224r1</span></span> | <span data-ttu-id="2f3eb-139">Nein</span><span class="sxs-lookup"><span data-stu-id="2f3eb-139">No</span></span> |
| <span data-ttu-id="2f3eb-140">secP256k1</span><span class="sxs-lookup"><span data-stu-id="2f3eb-140">secP256k1</span></span> | <span data-ttu-id="2f3eb-141">Nein</span><span class="sxs-lookup"><span data-stu-id="2f3eb-141">No</span></span> |
| <span data-ttu-id="2f3eb-142">secP256r1</span><span class="sxs-lookup"><span data-stu-id="2f3eb-142">secP256r1</span></span> | <span data-ttu-id="2f3eb-143">Nein</span><span class="sxs-lookup"><span data-stu-id="2f3eb-143">No</span></span> |
| <span data-ttu-id="2f3eb-144">secP384r1</span><span class="sxs-lookup"><span data-stu-id="2f3eb-144">secP384r1</span></span> | <span data-ttu-id="2f3eb-145">Nein</span><span class="sxs-lookup"><span data-stu-id="2f3eb-145">No</span></span> |
| <span data-ttu-id="2f3eb-146">secP521r1</span><span class="sxs-lookup"><span data-stu-id="2f3eb-146">secP521r1</span></span> | <span data-ttu-id="2f3eb-147">Nein</span><span class="sxs-lookup"><span data-stu-id="2f3eb-147">No</span></span> |

## <a name="enabling-elliptic-curves"></a><span data-ttu-id="2f3eb-148">Aktivieren von elliptischen Kurven</span><span class="sxs-lookup"><span data-stu-id="2f3eb-148">Enabling Elliptic Curves</span></span>

<span data-ttu-id="2f3eb-149">Um elliptische Kurven hinzuzufügen, stellen Sie entweder eine Gruppenrichtlinie bereit, oder verwenden Sie die TLS-Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="2f3eb-149">To add elliptic curves, either deploy a group policy or use the TLS cmdlets:</span></span>
- <span data-ttu-id="2f3eb-150">Um die Gruppenrichtlinie zu verwenden, konfigurieren Sie die [ECC-Kurven Reihenfolge](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) unter Computer Konfiguration > administrative Vorlagen > Netzwerk > SSL-Konfigurationseinstellungen mit der Prioritäts Liste für alle elliptischen Kurven, die Sie aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="2f3eb-150">To use group policy, [configure ECC Curve Order](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) under Computer Configuration > Administrative Templates > Network > SSL Configuration Settings with the priority list for all elliptic curves you want enabled.</span></span>

- <span data-ttu-id="2f3eb-151">Informationen zur Verwendung von PowerShell finden Sie unter [TLS-Cmdlets](/powershell/module/tls) für eine komplette Liste der TLS-Cmdlet-Syntax und Beschreibungen.</span><span class="sxs-lookup"><span data-stu-id="2f3eb-151">To use PowerShell, see [TLS cmdlets](/powershell/module/tls) for a complete list of TLS cmdlet syntax and descriptions.</span></span>


> [!NOTE]
> <span data-ttu-id="2f3eb-152">Vor Windows 10 wurden Chiffre Sammlungs Zeichenfolgen mit der elliptischen Kurve angehängt, um die Kurven Priorität zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="2f3eb-152">Prior to Windows 10, cipher suite strings were appended with the elliptic curve to determine the curve priority.</span></span> <span data-ttu-id="2f3eb-153">Windows 10 unterstützt eine Einstellung für die Prioritäts Reihenfolge der elliptischen Kurven, damit das elliptische Kurven Suffix nicht erforderlich ist und von der neuen Priorität der elliptischen Kurven Priorität außer Kraft gesetzt wird, um Organisationen die Verwendung von Gruppenrichtlinien zum Konfigurieren verschiedener Versionen von Windows mit denselben Verschlüsselungs Sammlungen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="2f3eb-153">Windows 10 supports an elliptic curve priority order setting so the elliptic curve suffix is not required and is overridden by the new elliptic curve priority order, when provided, to allow organizations to use group policy to configure different versions of Windows with the same cipher suites.</span></span>


## <a name="see-also"></a><span data-ttu-id="2f3eb-154">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2f3eb-154">See Also</span></span>

[<span data-ttu-id="2f3eb-155">Konfigurieren der TLS ECC-Kurven Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="2f3eb-155">Configuring TLS ECC Curve Order</span></span>](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[<span data-ttu-id="2f3eb-156">Verwalten der TLS ECC-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="2f3eb-156">Managing TLS ECC order</span></span>](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[<span data-ttu-id="2f3eb-157">Verwalten von Windows ECC-Kurven mithilfe von Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="2f3eb-157">Managing Windows ECC curves using Group Policy</span></span>](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[<span data-ttu-id="2f3eb-158">TLS-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="2f3eb-158">TLS cmdlets</span></span>](/powershell/module/tls)
