---
description: Elliptische Kurven in Windows 10, Version 1607 und höher aktiviert.
title: TLS-elliptische Kurven in Windows 10, Version 1607 und höher
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: 813a7c117f5f1e3fc1c6484fc57d1c9f14cf9567
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217449"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1607-and-later"></a><span data-ttu-id="49ac0-103">TLS-elliptische Kurven in Windows 10, Version 1607 und höher</span><span class="sxs-lookup"><span data-stu-id="49ac0-103">TLS Elliptic Curves in Windows 10 version 1607 and later</span></span>

<span data-ttu-id="49ac0-104">Für Windows 10, Version 1607 und höher, sind die folgenden elliptischen Kurven aktiviert, und in dieser Prioritäts Reihenfolge wird standardmäßig der Microsoft SChannel-Anbieter verwendet:</span><span class="sxs-lookup"><span data-stu-id="49ac0-104">For Windows 10, versions 1607 and later, the following elliptic curves are enabled and in this priority order by default using the Microsoft Schannel Provider:</span></span>

| <span data-ttu-id="49ac0-105">Zeichenfolge mit elliptischer Kurve</span><span class="sxs-lookup"><span data-stu-id="49ac0-105">Elliptic curve string</span></span> | <span data-ttu-id="49ac0-106">Verfügbar im PPS-Modus</span><span class="sxs-lookup"><span data-stu-id="49ac0-106">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="49ac0-107">curve25519</span><span class="sxs-lookup"><span data-stu-id="49ac0-107">curve25519</span></span> | <span data-ttu-id="49ac0-108">Nein</span><span class="sxs-lookup"><span data-stu-id="49ac0-108">No</span></span> |
| <span data-ttu-id="49ac0-109">Benannte nistp256</span><span class="sxs-lookup"><span data-stu-id="49ac0-109">NistP256</span></span> | <span data-ttu-id="49ac0-110">Ja</span><span class="sxs-lookup"><span data-stu-id="49ac0-110">Yes</span></span> |
| <span data-ttu-id="49ac0-111">Benannte nistp384</span><span class="sxs-lookup"><span data-stu-id="49ac0-111">NistP384</span></span> | <span data-ttu-id="49ac0-112">Ja</span><span class="sxs-lookup"><span data-stu-id="49ac0-112">Yes</span></span> |


<span data-ttu-id="49ac0-113">Die folgenden elliptischen Kurven werden vom Microsoft SChannel-Anbieter unterstützt, sind jedoch nicht standardmäßig aktiviert:</span><span class="sxs-lookup"><span data-stu-id="49ac0-113">The following elliptic curves are supported by the Microsoft Schannel Provider, but not enabled by default:</span></span>

| <span data-ttu-id="49ac0-114">Zeichenfolge mit elliptischer Kurve</span><span class="sxs-lookup"><span data-stu-id="49ac0-114">Elliptic curve string</span></span> | <span data-ttu-id="49ac0-115">Verfügbar im PPS-Modus</span><span class="sxs-lookup"><span data-stu-id="49ac0-115">Available in FIPS mode</span></span> |
|-------------|--------------|
| <span data-ttu-id="49ac0-116">benannte brainpoolp256r1</span><span class="sxs-lookup"><span data-stu-id="49ac0-116">brainpoolP256r1</span></span> | <span data-ttu-id="49ac0-117">Nein</span><span class="sxs-lookup"><span data-stu-id="49ac0-117">No</span></span> |
| <span data-ttu-id="49ac0-118">benannte brainpoolp384r1</span><span class="sxs-lookup"><span data-stu-id="49ac0-118">brainpoolP384r1</span></span> | <span data-ttu-id="49ac0-119">Nein</span><span class="sxs-lookup"><span data-stu-id="49ac0-119">No</span></span> |
| <span data-ttu-id="49ac0-120">benannte brainpoolp512r1</span><span class="sxs-lookup"><span data-stu-id="49ac0-120">brainpoolP512r1</span></span> | <span data-ttu-id="49ac0-121">Nein</span><span class="sxs-lookup"><span data-stu-id="49ac0-121">No</span></span> |
| <span data-ttu-id="49ac0-122">nistP192</span><span class="sxs-lookup"><span data-stu-id="49ac0-122">nistP192</span></span> | <span data-ttu-id="49ac0-123">Nein</span><span class="sxs-lookup"><span data-stu-id="49ac0-123">No</span></span> |
| <span data-ttu-id="49ac0-124">nistP224</span><span class="sxs-lookup"><span data-stu-id="49ac0-124">nistP224</span></span> | <span data-ttu-id="49ac0-125">Nein</span><span class="sxs-lookup"><span data-stu-id="49ac0-125">No</span></span> |
| <span data-ttu-id="49ac0-126">benannte nistp521</span><span class="sxs-lookup"><span data-stu-id="49ac0-126">nistP521</span></span> | <span data-ttu-id="49ac0-127">Ja</span><span class="sxs-lookup"><span data-stu-id="49ac0-127">Yes</span></span> |
| <span data-ttu-id="49ac0-128">secP160k1</span><span class="sxs-lookup"><span data-stu-id="49ac0-128">secP160k1</span></span> | <span data-ttu-id="49ac0-129">Nein</span><span class="sxs-lookup"><span data-stu-id="49ac0-129">No</span></span> |
| <span data-ttu-id="49ac0-130">secP160r1</span><span class="sxs-lookup"><span data-stu-id="49ac0-130">secP160r1</span></span> | <span data-ttu-id="49ac0-131">Nein</span><span class="sxs-lookup"><span data-stu-id="49ac0-131">No</span></span> |
| <span data-ttu-id="49ac0-132">secP160r2</span><span class="sxs-lookup"><span data-stu-id="49ac0-132">secP160r2</span></span> | <span data-ttu-id="49ac0-133">Nein</span><span class="sxs-lookup"><span data-stu-id="49ac0-133">No</span></span> |
| <span data-ttu-id="49ac0-134">secP192k1</span><span class="sxs-lookup"><span data-stu-id="49ac0-134">secP192k1</span></span> | <span data-ttu-id="49ac0-135">Nein</span><span class="sxs-lookup"><span data-stu-id="49ac0-135">No</span></span> |
| <span data-ttu-id="49ac0-136">secP192r1</span><span class="sxs-lookup"><span data-stu-id="49ac0-136">secP192r1</span></span> | <span data-ttu-id="49ac0-137">Nein</span><span class="sxs-lookup"><span data-stu-id="49ac0-137">No</span></span> |
| <span data-ttu-id="49ac0-138">secP224k1</span><span class="sxs-lookup"><span data-stu-id="49ac0-138">secP224k1</span></span> | <span data-ttu-id="49ac0-139">Nein</span><span class="sxs-lookup"><span data-stu-id="49ac0-139">No</span></span> |
| <span data-ttu-id="49ac0-140">secP224r1</span><span class="sxs-lookup"><span data-stu-id="49ac0-140">secP224r1</span></span> | <span data-ttu-id="49ac0-141">Nein</span><span class="sxs-lookup"><span data-stu-id="49ac0-141">No</span></span> |
| <span data-ttu-id="49ac0-142">secP256k1</span><span class="sxs-lookup"><span data-stu-id="49ac0-142">secP256k1</span></span> | <span data-ttu-id="49ac0-143">Nein</span><span class="sxs-lookup"><span data-stu-id="49ac0-143">No</span></span> |
| <span data-ttu-id="49ac0-144">secP256r1</span><span class="sxs-lookup"><span data-stu-id="49ac0-144">secP256r1</span></span> | <span data-ttu-id="49ac0-145">Nein</span><span class="sxs-lookup"><span data-stu-id="49ac0-145">No</span></span> |
| <span data-ttu-id="49ac0-146">secP384r1</span><span class="sxs-lookup"><span data-stu-id="49ac0-146">secP384r1</span></span> | <span data-ttu-id="49ac0-147">Nein</span><span class="sxs-lookup"><span data-stu-id="49ac0-147">No</span></span> |
| <span data-ttu-id="49ac0-148">secP521r1</span><span class="sxs-lookup"><span data-stu-id="49ac0-148">secP521r1</span></span> | <span data-ttu-id="49ac0-149">Nein</span><span class="sxs-lookup"><span data-stu-id="49ac0-149">No</span></span> |



## <a name="enabling-elliptic-curves"></a><span data-ttu-id="49ac0-150">Aktivieren von elliptischen Kurven</span><span class="sxs-lookup"><span data-stu-id="49ac0-150">Enabling Elliptic Curves</span></span>

<span data-ttu-id="49ac0-151">Um elliptische Kurven hinzuzufügen, stellen Sie entweder eine Gruppenrichtlinie bereit, oder verwenden Sie die TLS-Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="49ac0-151">To add elliptic curves, either deploy a group policy or use the TLS cmdlets:</span></span>
- <span data-ttu-id="49ac0-152">Um die Gruppenrichtlinie zu verwenden, konfigurieren Sie die [ECC-Kurven Reihenfolge](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) unter Computer Konfiguration > administrative Vorlagen > Netzwerk > SSL-Konfigurationseinstellungen mit der Prioritäts Liste für alle elliptischen Kurven, die Sie aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="49ac0-152">To use group policy, [configure ECC Curve Order](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) under Computer Configuration > Administrative Templates > Network > SSL Configuration Settings with the priority list for all elliptic curves you want enabled.</span></span>

- <span data-ttu-id="49ac0-153">Informationen zur Verwendung von PowerShell finden Sie unter [TLS-Cmdlets](/powershell/module/tls) für eine komplette Liste der TLS-Cmdlet-Syntax und Beschreibungen.</span><span class="sxs-lookup"><span data-stu-id="49ac0-153">To use PowerShell, see [TLS cmdlets](/powershell/module/tls) for a complete list of TLS cmdlet syntax and descriptions.</span></span>


> [!NOTE]
> <span data-ttu-id="49ac0-154">Vor Windows 10 wurden Chiffre Sammlungs Zeichenfolgen mit der elliptischen Kurve angehängt, um die Kurven Priorität zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="49ac0-154">Prior to Windows 10, cipher suite strings were appended with the elliptic curve to determine the curve priority.</span></span> <span data-ttu-id="49ac0-155">Windows 10 unterstützt eine Einstellung für die Prioritäts Reihenfolge der elliptischen Kurven, damit das elliptische Kurven Suffix nicht erforderlich ist und von der neuen Priorität der elliptischen Kurven Priorität außer Kraft gesetzt wird, um Organisationen die Verwendung von Gruppenrichtlinien zum Konfigurieren verschiedener Versionen von Windows mit denselben Verschlüsselungs Sammlungen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="49ac0-155">Windows 10 supports an elliptic curve priority order setting so the elliptic curve suffix is not required and is overridden by the new elliptic curve priority order, when provided, to allow organizations to use group policy to configure different versions of Windows with the same cipher suites.</span></span>


## <a name="see-also"></a><span data-ttu-id="49ac0-156">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="49ac0-156">See Also</span></span>

[<span data-ttu-id="49ac0-157">Konfigurieren der TLS ECC-Kurven Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="49ac0-157">Configuring TLS ECC Curve Order</span></span>](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[<span data-ttu-id="49ac0-158">Verwalten der TLS ECC-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="49ac0-158">Managing TLS ECC order</span></span>](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[<span data-ttu-id="49ac0-159">Verwalten von Windows ECC-Kurven mithilfe von Gruppenrichtlinie</span><span class="sxs-lookup"><span data-stu-id="49ac0-159">Managing Windows ECC curves using Group Policy</span></span>](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[<span data-ttu-id="49ac0-160">TLS-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="49ac0-160">TLS cmdlets</span></span>](/powershell/module/tls)
