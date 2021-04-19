---
description: Wenn Sie den Wert dieser pro-Computer-System Richtlinie auf &\# 0034; 1&0034 festlegen, \# wird verhindert, dass nicht Administratoren mithilfe eines Dialog Felds zum Durchsuchen nach Quellen verwalteter Anwendungen suchen, die auf Medien wie CD-ROM gespeichert sind.
ms.assetid: 51806a4c-4ae5-42e9-9d58-8032108164cb
title: Disablebrowse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 014d71993f05d52783aafbd1cfc73a986ade62e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106342824"
---
# <a name="disablebrowse"></a><span data-ttu-id="e7966-103">Disablebrowse</span><span class="sxs-lookup"><span data-stu-id="e7966-103">DisableBrowse</span></span>

<span data-ttu-id="e7966-104">Wenn Sie den Wert dieser pro-Computer- [System Richtlinie](system-policy.md) auf "1" festlegen, wird verhindert, dass nicht Administratoren mithilfe eines Dialog Felds zum [Durchsuchen](browse-dialog.md) nach Quellen [*verwalteter Anwendungen*](m-gly.md) suchen, die auf Medien wie CD-ROM gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="e7966-104">Setting the value of this per-machine [system policy](system-policy.md) to "1" prevents nonadministrative users from using a [Browse Dialog](browse-dialog.md) to locate sources of [*managed applications*](m-gly.md) stored on media, such as CD-ROM.</span></span> <span data-ttu-id="e7966-105">Das Kombinations Feld "Funktion von: verwenden" für die direkte Eingabe ist gesperrt, und das "Durchsuchen..." die Schaltfläche ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e7966-105">The "Use feature from:" combo box for direct input is locked and the "Browse..." button is disabled.</span></span> <span data-ttu-id="e7966-106">Weitere Informationen zum Durchsuchen von Quellen finden Sie unter [Quellen Resilienz](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="e7966-106">For more details on source browsing, see [source resiliency](source-resiliency.md).</span></span>

<span data-ttu-id="e7966-107">Disablebrowse überschreibt AllowLockdownBrowse und verhindert das Durchsuchen, auch wenn AllowLockdownBrowse festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e7966-107">DisableBrowse overrides AllowLockdownBrowse and prevents browsing even if AllowLockdownBrowse is set.</span></span>

## <a name="registry-key"></a><span data-ttu-id="e7966-108">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="e7966-108">Registry Key</span></span>

<span data-ttu-id="e7966-109">**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="e7966-109">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="e7966-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e7966-110">Data Type</span></span>

<span data-ttu-id="e7966-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="e7966-111">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="e7966-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7966-112">Remarks</span></span>

<span data-ttu-id="e7966-113">In einigen Fällen, in denen "disablebrowse" festgelegt ist, kann ein nicht administrativer Benutzer weiterhin verwaltete Anwendungen aus Quellen auf ordnungsgemäß gekennzeichneten Medien installieren.</span><span class="sxs-lookup"><span data-stu-id="e7966-113">In some cases with DisableBrowse set, a nonadministrative user may still be capable of installing managed applications from sources on correctly labeled media.</span></span> <span data-ttu-id="e7966-114">Durch das Festlegen der disablebrowse-Richtlinie wird nur die Funktion zum Durchsuchen der Quellen deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="e7966-114">Setting the DisableBrowse policy only disables the capability to browse to sources.</span></span> <span data-ttu-id="e7966-115">Sie kann verwendet werden, um zu verhindern, dass ein Benutzer, der nicht Administrator ist, während einer Installation auf Abruf, Neuinstallation oder Reparatur eine neue Quelle durchsucht.</span><span class="sxs-lookup"><span data-stu-id="e7966-115">It can be used to prevent a nonadministrative user from browsing to a new source during an install-on-demand installation, reinstallation, or repair.</span></span> <span data-ttu-id="e7966-116">Wenn [AllowLockdownMedia](allowlockdownmedia.md) festgelegt ist, kann der nicht administrative Benutzer dennoch eine verwaltete Anwendung von einem ordnungsgemäß gekennzeichneten Medium installieren.</span><span class="sxs-lookup"><span data-stu-id="e7966-116">If [AllowLockdownMedia](allowlockdownmedia.md) is set, the nonadministrative user could still install a managed application from correctly labeled media.</span></span>

<span data-ttu-id="e7966-117">Disablebrowse hindert den nicht Administrator daran, zu einem neuen Medien Speicherort oder einem anderen Quell Speicherort zu navigieren.</span><span class="sxs-lookup"><span data-stu-id="e7966-117">DisableBrowse prevents the nonadministrative user from browsing to a new media location or any other source location.</span></span> <span data-ttu-id="e7966-118">Ausführliche Informationen zum Sichern von Medienquellen verwalteter Anwendungen finden Sie unter [Resilienz der Quelle](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="e7966-118">For details of how to secure media sources of managed applications see [Source Resiliency](source-resiliency.md).</span></span>

<span data-ttu-id="e7966-119">Informationen zur Interaktion dieser Richtlinie mit Installations Quellen finden Sie unter [Verwalten von Installations Quellen](managing-installation-sources.md).</span><span class="sxs-lookup"><span data-stu-id="e7966-119">For information about the interaction of this policy with installation sources, see [Managing Installation Sources](managing-installation-sources.md).</span></span>

 

 



