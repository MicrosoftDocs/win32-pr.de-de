---
description: Die mit Windows bereitgestellten Authentifizierungs Pakete unterstützen die Anpassung mithilfe von unter Authentifizierungs Paketen.
ms.assetid: e1f202c2-8574-4193-a99a-3922a4446013
title: Unter Authentifizierungs Pakete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18f0d96a971c35d33002bdab8a23cb5e59207193
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372960"
---
# <a name="subauthentication-packages"></a><span data-ttu-id="964e8-103">Unter Authentifizierungs Pakete</span><span class="sxs-lookup"><span data-stu-id="964e8-103">Subauthentication Packages</span></span>

<span data-ttu-id="964e8-104">Die mit Windows bereitgestellten [*Authentifizierungs Pakete*](../secgloss/a-gly.md) unterstützen die Anpassung mithilfe von [*unter Authentifizierungs Paketen*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="964e8-104">The [*authentication packages*](../secgloss/a-gly.md) provided with Windows support customization using [*subauthentication packages*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="964e8-105">Ein unter Authentifizierungs Paket ist eine DLL, die einen Teil der Authentifizierungs-und Validierungs Kriterien, die vom Haupt Authentifizierungs Paket verwendet werden, ergänzt oder ersetzt.</span><span class="sxs-lookup"><span data-stu-id="964e8-105">A subauthentication package is a DLL that supplements or replaces part of the authentication and validation criteria used by the main authentication package.</span></span> <span data-ttu-id="964e8-106">Beispielsweise kann ein bestimmter Server ein unter Authentifizierungs Paket bereitstellen, das das Kennwort eines Benutzers mit einem anderen Algorithmus überprüft oder Arbeitsstations Einschränkungen in einem anderen Format angibt.</span><span class="sxs-lookup"><span data-stu-id="964e8-106">For example, a particular server might supply a subauthentication package that validates a user's password with a different algorithm or specifies workstation restrictions in a different format.</span></span>

<span data-ttu-id="964e8-107">Weitere Informationen zu unter Authentifizierungs Paketen finden Sie im subauth-Beispiel, das mit dem Platform Software Development Kit (SDK) installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="964e8-107">For more information about subauthentication packages, see the SubAuth sample installed with the Platform Software Development Kit (SDK).</span></span>

 

 
