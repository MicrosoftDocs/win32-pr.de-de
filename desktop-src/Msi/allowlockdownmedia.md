---
description: Wenn Sie den Wert dieser pro-Computer-System Richtlinie auf &\# 0034; 1&\# 0034; festlegen, können nicht Administratoren verwaltete Anwendungen von auf Medien gespeicherten Quellen, z. b. einer CD-ROM, installieren.
ms.assetid: 9eac7520-0ba3-4529-a80b-010447a5b5e7
title: AllowLockdownMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be1a5ba06db0a484a55a6e18e5419dee951fc38
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869604"
---
# <a name="allowlockdownmedia"></a><span data-ttu-id="26daa-103">AllowLockdownMedia</span><span class="sxs-lookup"><span data-stu-id="26daa-103">AllowLockdownMedia</span></span>

<span data-ttu-id="26daa-104">Wenn Sie den Wert dieser pro-Computer- [System Richtlinie](system-policy.md) auf "1" festlegen, können nicht Administratoren [*verwaltete Anwendungen*](m-gly.md) von auf Medien gespeicherten Quellen, z. b. einer CD-ROM, installieren.</span><span class="sxs-lookup"><span data-stu-id="26daa-104">Setting the value of this per-machine [system policy](system-policy.md) to "1", enables nonadministrative users to install [*managed applications*](m-gly.md) from sources stored on media, such as a CD-ROM.</span></span> <span data-ttu-id="26daa-105">Siehe [quellresilienz](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="26daa-105">See [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="26daa-106">Wenn diese Richtlinie beispielsweise festgelegt ist, kann ein Benutzer, der nicht Administrator ist, eine Medienquelle verwenden, um zugewiesene oder veröffentlichte Anwendungen oder Anwendungen zu installieren, die für alle Benutzer installiert werden.</span><span class="sxs-lookup"><span data-stu-id="26daa-106">For example, if this policy is set, a nonadministrative user may use a media source to install assigned or published applications or applications being installed for all users.</span></span> <span data-ttu-id="26daa-107">Wenn Sie diese Richtlinie festlegen, können Benutzer, die nicht Administratoren sind, auch bei einer erweiterten Installation Programme mit LocalSystem-Berechtigungen ausführen.</span><span class="sxs-lookup"><span data-stu-id="26daa-107">Setting this policy also enables nonadministrative users to run programs at LocalSystem privileges during an elevated installation.</span></span>

<span data-ttu-id="26daa-108">Der Standardwert dieser Richtlinie ist 1 nur auf Computern, auf denen Windows Vista ausgeführt wird und die keiner Domäne hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="26daa-108">The default value of this policy is 1 only on computers running Windows Vista and that are not joined to a domain.</span></span> <span data-ttu-id="26daa-109">Die Standardeinstellung auf anderen Computern besteht darin, dass nicht-Administratoren verwaltete Anwendungen nicht über eine Quelle installieren können, die sich auf dem Medium befindet.</span><span class="sxs-lookup"><span data-stu-id="26daa-109">The default on other computers is that nonadministrative users cannot install managed applications from a source located on media.</span></span>

<span data-ttu-id="26daa-110">Da diese Richtlinie Benutzern, die kein Administrator sind, die Installation mit Berechtigungen ermöglicht, die Sie nicht standardmäßig haben, bevor Sie diese Richtlinie festlegen, sollten Sie berücksichtigen, ob Sie ein geeignetes Maß an Sicherheit für den Benutzer bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="26daa-110">Because this policy enables users that are not an administrator to install with privileges they do not have by default, before setting this policy you should consider whether it provides an appropriate level of security for your user.</span></span> <span data-ttu-id="26daa-111">Die Standardeinstellung wird empfohlen, um eine sichere Umgebung sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="26daa-111">The default setting is recommended to ensure a secure environment.</span></span>

<span data-ttu-id="26daa-112">Weitere Informationen zum Sichern von Installationen und zum Verwenden digitaler Zertifikate finden Sie unter [Richtlinien zum Erstellen sicherer Installationen](guidelines-for-authoring-secure-installations.md) und [digitaler Signaturen und Windows Installer](digital-signatures-and-windows-installer.md) und [Herunterladen einer-Installation aus dem Internet](downloading-an-installation-from-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="26daa-112">For more information about securing installations and using digital certificates see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md) and [Downloading an Installation from the Internet](downloading-an-installation-from-the-internet.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="26daa-113">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="26daa-113">Registry Key</span></span>

<span data-ttu-id="26daa-114">**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="26daa-114">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="26daa-115">Datentyp</span><span class="sxs-lookup"><span data-stu-id="26daa-115">Data Type</span></span>

<span data-ttu-id="26daa-116">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="26daa-116">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="26daa-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26daa-117">Remarks</span></span>

<span data-ttu-id="26daa-118">Durch Festlegen dieser Richtlinie können nicht Administratoren beliebige Programme unter "LocalSystem"-Berechtigungen ausführen, wenn Sie über ein Windows Installer Paket verfügen, mit dem diese Programme installiert oder gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="26daa-118">Setting this policy also enables nonadministrative users to run arbitrary programs at LocalSystem privileges if they have a Windows Installer package that installs or launches those programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26daa-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="26daa-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26daa-120">Quellen Resilienz</span><span class="sxs-lookup"><span data-stu-id="26daa-120">Source Resiliency</span></span>](source-resiliency.md)
</dt> <dt>

[<span data-ttu-id="26daa-121">AllowLockdownBrowse</span><span class="sxs-lookup"><span data-stu-id="26daa-121">AllowLockdownBrowse</span></span>](allowlockdownbrowse.md)
</dt> </dl>

 

 



