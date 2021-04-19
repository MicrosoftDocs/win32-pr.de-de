---
description: Der Entwurf von SSPI ermöglicht das Schreiben und Hinzufügen zusätzlicher SSPs zum System.
ms.assetid: 0d462340-e485-4746-b627-d823752462d9
title: Schreiben und Installieren eines Security Support Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19f827ddf2b0352acc889df3ed1d5b3dfff52c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106353552"
---
# <a name="writing-and-installing-a-security-support-provider"></a><span data-ttu-id="5271f-103">Schreiben und Installieren eines Security Support Provider</span><span class="sxs-lookup"><span data-stu-id="5271f-103">Writing and Installing a Security Support Provider</span></span>

<span data-ttu-id="5271f-104">Der Entwurf von SSPI ermöglicht das Schreiben und Hinzufügen zusätzlicher SSPs zum System.</span><span class="sxs-lookup"><span data-stu-id="5271f-104">The design of SSPI enables additional SSPs to be written and added to the system.</span></span> <span data-ttu-id="5271f-105">Ein [*SSP*](../secgloss/s-gly.md) , der für ein Sicherheitsmodell spezifisch ist, kann je nach Ebene der Integration mit dem Betriebssystem relativ einfach oder sehr komplex entwickelt werden.</span><span class="sxs-lookup"><span data-stu-id="5271f-105">An [*SSP*](../secgloss/s-gly.md) specific to a security model can be developed with relative ease or great complexity, depending on the level of integration with the operating system.</span></span> <span data-ttu-id="5271f-106">Ein Client-SSP, der Verbindungen mit einem neuen Servertyp zulässt, kann sehr schnell entwickelt werden, wohingegen ein vollständiger SSP, der einen lokalen Identitätswechsel bereitstellt, einen höheren Aufwand erfordert.</span><span class="sxs-lookup"><span data-stu-id="5271f-106">A client SSP that allows connections to a new type of server could be developed very quickly, whereas a full SSP that provides local impersonation would require more effort.</span></span>

<span data-ttu-id="5271f-107">SSPs werden durch Aktualisieren eines **reg \_ SZ** -Werts in der Registrierung installiert, der sich wie folgt befindet:</span><span class="sxs-lookup"><span data-stu-id="5271f-107">SSPs are installed by updating a **REG\_SZ** value in the registry, located as follows:</span></span>

<span data-ttu-id="5271f-108">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet**- \\ **Steuer** Element \\ **SecurityProviders**  =  *Provider1.dll, Provider2.dll*...    </span><span class="sxs-lookup"><span data-stu-id="5271f-108">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\    **SecurityProviders** = *Provider1.dll, Provider2.dll,*…</span></span><dl> <dt>

            Data type
</dt> <dd>            <span data-ttu-id="5271f-109">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="5271f-109">REG\_SZ</span></span></dd> </dl>

<span data-ttu-id="5271f-110">Eine einzelne DLL kann mehrere SSPs enthalten.</span><span class="sxs-lookup"><span data-stu-id="5271f-110">A single DLL can contain multiple SSPs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5271f-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5271f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5271f-112">Einschränkungen bei der Registrierung und Installation eines Sicherheitspakets</span><span class="sxs-lookup"><span data-stu-id="5271f-112">Restrictions around Registering and Installing a Security Package</span></span>](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
