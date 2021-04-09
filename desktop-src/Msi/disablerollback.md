---
description: Wenn diese System Richtlinie auf 1 festgelegt ist, speichert das Installationsprogramm während der Installation keine Rollback-Dateien und deaktiviert das Installations Rollback.
ms.assetid: 01747de6-7478-4403-ba36-8ff1abc2b70f
title: DISABLEROLLBACK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7f0ce15e618880f021e04adf7d2146a97f6ed65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959081"
---
# <a name="disablerollback"></a><span data-ttu-id="976f2-103">DISABLEROLLBACK</span><span class="sxs-lookup"><span data-stu-id="976f2-103">DisableRollback</span></span>

<span data-ttu-id="976f2-104">Wenn diese [System Richtlinie](system-policy.md) auf 1 festgelegt ist, speichert das Installationsprogramm während der Installation keine Rollback-Dateien und deaktiviert das Installations Rollback.</span><span class="sxs-lookup"><span data-stu-id="976f2-104">If this [system policy](system-policy.md) is set to 1, the installer does not store rollback files during installation and disables installation rollback.</span></span> <span data-ttu-id="976f2-105">Standardmäßig ist das Rollback aktiviert.</span><span class="sxs-lookup"><span data-stu-id="976f2-105">By default, rollback is enabled.</span></span> <span data-ttu-id="976f2-106">Administratoren wird empfohlen, diese Richtlinie nicht zu verwenden, es sei denn, Sie ist unbedingt erforderlich.</span><span class="sxs-lookup"><span data-stu-id="976f2-106">Administrators are advised to not use this policy unless it is absolutely essential.</span></span> <span data-ttu-id="976f2-107">Weitere Informationen finden Sie unter [Rollback-Installation](rollback-installation.md).</span><span class="sxs-lookup"><span data-stu-id="976f2-107">For more information, see [Rollback Installation](rollback-installation.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="976f2-108">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="976f2-108">Registry Key</span></span>

<span data-ttu-id="976f2-109">Um das Rollback für Installationen pro Benutzer zu deaktivieren, legen Sie **DISABLEROLLBACK** unter dem folgenden Registrierungsschlüssel auf 1 fest:</span><span class="sxs-lookup"><span data-stu-id="976f2-109">To disable rollback for per-user installations, set **DisableRollback** to 1 under the following registry key:</span></span>

<span data-ttu-id="976f2-110">**HKEY \_ Aktuelle \_** Richtlinien für Benutzer \\ **Software** \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="976f2-110">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

<span data-ttu-id="976f2-111">Um das Rollback für Installationen pro Computer zu deaktivieren, legen Sie **DISABLEROLLBACK** unter dem folgenden Registrierungsschlüssel auf 1 fest.</span><span class="sxs-lookup"><span data-stu-id="976f2-111">To disable rollback for per-computer installations, set **DisableRollback** to 1 under the following registry key.</span></span>

<span data-ttu-id="976f2-112">**HKEY \_ Software Richtlinien für lokale \_ Computer** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="976f2-112">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="976f2-113">Datentyp</span><span class="sxs-lookup"><span data-stu-id="976f2-113">Data Type</span></span>

<span data-ttu-id="976f2-114">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="976f2-114">**REG\_DWORD**</span></span>

 

 



