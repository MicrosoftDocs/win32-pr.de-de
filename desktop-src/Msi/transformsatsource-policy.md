---
description: Wenn diese System Richtlinie pro Benutzer auf &\# 0034; 1&0034; festgelegt ist \# , sucht das Installationsprogramm im Stammverzeichnis von Netzwerk Quellen in der Quell Liste für das Produkt nach Transformations Dateien. Standardmäßig werden Transformationen im Ordner Anwendungsdaten des Profils eines Benutzers gespeichert.
ms.assetid: 24881078-1610-4a37-a52d-fcabd78e1738
title: Transformsatsource-Richtlinie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91be9c56f2e68a27d904acf98088204dc4012b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128108"
---
# <a name="transformsatsource-policy"></a><span data-ttu-id="f4f06-104">Transformsatsource-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="f4f06-104">TransformsAtSource Policy</span></span>

<span data-ttu-id="f4f06-105">Wenn diese [System Richtlinie](system-policy.md) pro Benutzer auf "1" festgelegt ist; Das Installationsprogramm sucht im Stammverzeichnis von Netzwerk Quellen in der Quell Liste für das Produkt nach Transformations Dateien.</span><span class="sxs-lookup"><span data-stu-id="f4f06-105">If this per-user [system policy](system-policy.md) is set to "1"; the installer searches for transform files in the root of any network sources in the source list for the product.</span></span> <span data-ttu-id="f4f06-106">Standardmäßig werden Transformationen im Ordner Anwendungsdaten des Profils eines Benutzers gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f4f06-106">By default, transforms are stored in the Application Data folder of a user's profile.</span></span>

<span data-ttu-id="f4f06-107">Windows Installer interpretiert die transformsatsource-Richtlinie so, dass Sie mit der [transformssecure-Richtlinie](transformssecure-policy.md)identisch ist.</span><span class="sxs-lookup"><span data-stu-id="f4f06-107">Windows Installer interprets the TransformsAtSource policy to be the same as the [TransformsSecure policy](transformssecure-policy.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="f4f06-108">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="f4f06-108">Registry Key</span></span>

<span data-ttu-id="f4f06-109">**HKEY \_ Aktuelle \_** Richtlinien für Benutzer \\ **Software** \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="f4f06-109">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="f4f06-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f4f06-110">Data Type</span></span>

<span data-ttu-id="f4f06-111">**REG- \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="f4f06-111">**REG\_SZ**</span></span>

 

 



