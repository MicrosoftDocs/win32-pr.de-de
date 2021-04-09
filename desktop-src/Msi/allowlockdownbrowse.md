---
description: Das Festlegen des Werts für diese Computer spezifische System Richtlinie auf &\# 0034; 1&\# 0034; ermöglicht nicht Administratoren die Verwendung eines Dialog Felds zum Durchsuchen, um nach Quellen verwalteter Anwendungen zu suchen.
ms.assetid: 1cf83f77-75a4-48c3-961e-339c76ba4306
title: AllowLockdownBrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 187fe39a01e821b271050cdd8d6c8e96b6611d60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864499"
---
# <a name="allowlockdownbrowse"></a><span data-ttu-id="64f7e-103">AllowLockdownBrowse</span><span class="sxs-lookup"><span data-stu-id="64f7e-103">AllowLockdownBrowse</span></span>

<span data-ttu-id="64f7e-104">Wenn Sie den Wert dieser pro-Computer- [System Richtlinie](system-policy.md) auf "1" festlegen, können nicht Administratoren mit einem Dialog Feld " [Durchsuchen](browse-dialog.md) " nach Quellen [*verwalteter Anwendungen*](m-gly.md)suchen.</span><span class="sxs-lookup"><span data-stu-id="64f7e-104">Setting the value of this per-machine [system policy](system-policy.md) to "1" enables nonadministrative users to use a [Browse Dialog](browse-dialog.md) to locate sources of [*managed applications*](m-gly.md).</span></span> <span data-ttu-id="64f7e-105">Quellen können Medien wie z. b. CD-ROM, URLs und Netzwerk Orte enthalten.</span><span class="sxs-lookup"><span data-stu-id="64f7e-105">Sources may include media, such as CD-ROM, URLs, and network locations.</span></span> <span data-ttu-id="64f7e-106">Weitere Informationen finden Sie unter [Quellen Resilienz](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="64f7e-106">For more information, see [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="64f7e-107">Der Standardwert für Windows Installer ist, dass nicht-Administratoren nach neuen Quellen verwalteter Anwendungen suchen können.</span><span class="sxs-lookup"><span data-stu-id="64f7e-107">The default on Windows Installer is that nonadministrative users cannot browse for new sources of managed applications.</span></span> <span data-ttu-id="64f7e-108">Die einzigen verfügbaren Quellen sind die, die bereits in der Quell Liste des Produkts registriert sind.</span><span class="sxs-lookup"><span data-stu-id="64f7e-108">The only sources available are those that are already registered in the source list of the product.</span></span> <span data-ttu-id="64f7e-109">Wenn diese Richtlinie festgelegt ist, kann ein Benutzer, der nicht Administrator ist, nach neuen Quellen für zugewiesene oder veröffentlichte Anwendungen oder Anwendungen suchen, die für alle Benutzer installiert werden.</span><span class="sxs-lookup"><span data-stu-id="64f7e-109">If this policy is set, a nonadministrative user may browse for new sources of assigned or published applications or applications being installed for all users.</span></span> <span data-ttu-id="64f7e-110">Durch das Festlegen von AllowLockdownBrowse können auch nicht Administratoren Programme bei einer erweiterten Installation unter "LocalSystem"-Berechtigungen ausführen.</span><span class="sxs-lookup"><span data-stu-id="64f7e-110">Setting AllowLockdownBrowse also enables nonadministrative users to run programs at LocalSystem privileges during an elevated installation.</span></span>

<span data-ttu-id="64f7e-111">Die Standardeinstellung wird empfohlen, um eine sichere Umgebung sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="64f7e-111">The default setting is recommended to ensure a secure environment.</span></span>

## <a name="registry-key"></a><span data-ttu-id="64f7e-112">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="64f7e-112">Registry Key</span></span>

<span data-ttu-id="64f7e-113">**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="64f7e-113">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="64f7e-114">Datentyp</span><span class="sxs-lookup"><span data-stu-id="64f7e-114">Data Type</span></span>

<span data-ttu-id="64f7e-115">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="64f7e-115">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="64f7e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64f7e-116">Remarks</span></span>

<span data-ttu-id="64f7e-117">Durch Festlegen dieser Richtlinie können nicht Administratoren beliebige Programme unter "LocalSystem"-Berechtigungen ausführen, wenn Sie über ein Windows Installer Paket verfügen, mit dem diese Programme installiert oder gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="64f7e-117">Setting this policy also enables nonadministrative users to run arbitrary programs at LocalSystem privileges if they have a Windows Installer package that installs or launches those programs.</span></span>

<span data-ttu-id="64f7e-118">[Disablebrowse](disablebrowse.md) überschreibt AllowLockdownBrowse und verhindert das Durchsuchen, auch wenn AllowLockdownBrowse festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="64f7e-118">[DisableBrowse](disablebrowse.md) overrides AllowLockdownBrowse and prevents browsing even if AllowLockdownBrowse is set.</span></span>

<span data-ttu-id="64f7e-119">Informationen zur Interaktion dieser Richtlinie mit Installations Quellen finden Sie unter [Verwalten von Installations Quellen](managing-installation-sources.md).</span><span class="sxs-lookup"><span data-stu-id="64f7e-119">For information about the interaction of this policy with installation sources, see [Managing Installation Sources](managing-installation-sources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="64f7e-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="64f7e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64f7e-121">Quellen Resilienz</span><span class="sxs-lookup"><span data-stu-id="64f7e-121">Source Resiliency</span></span>](source-resiliency.md)
</dt> <dt>

[<span data-ttu-id="64f7e-122">AllowLockdownMedia</span><span class="sxs-lookup"><span data-stu-id="64f7e-122">AllowLockdownMedia</span></span>](allowlockdownmedia.md)
</dt> </dl>

 

 



