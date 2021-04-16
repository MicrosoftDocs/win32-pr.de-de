---
description: Mit dem folgenden Befehl wird ein X. 509-Zertifikat mycert. CER in ein Test-PKCS \# 7-Software Herausgeber Zertifikat (SPC) mit dem Namen mycert. SPC umschlossen.
ms.assetid: c3287289-d2bf-4d1d-80f0-e7dd41a3cbe3
title: Verwenden von Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fca10b0ab121e283a181c84b056b63ce10ece385
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527620"
---
# <a name="using-cert2spc"></a><span data-ttu-id="d77fc-103">Verwenden von Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="d77fc-103">Using Cert2SPC</span></span>

<span data-ttu-id="d77fc-104">Mit dem folgenden Befehl wird ein [*X. 509*](../secgloss/x-gly.md) -Zertifikat *MyCert*. CER in ein Test-PKCS \# 7-Software Herausgeber [*Zertifikat*](../secgloss/s-gly.md) (SPC) mit dem Namen *MyCert*. SPC umschlossen.</span><span class="sxs-lookup"><span data-stu-id="d77fc-104">The following command wraps an [*X.509*](../secgloss/x-gly.md) certificate, *MyCert*.cer, into a test PKCS \#7 [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC), called *MyCert*.spc.</span></span> <span data-ttu-id="d77fc-105">Das erstellte SPC soll nur zu Testzwecken verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d77fc-105">The SPC created is to be used for test purposes only.</span></span> <span data-ttu-id="d77fc-106">Ein SPC, das verwendet wird, um den Code, der an die öffentliche Verteilung verteilt werden soll, tatsächlich zu signieren, muss von GTE, VeriSign, Inc. oder einer anderen vertrauenswürdigen [*Zertifizierungs*](../secgloss/c-gly.md) Stelle abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d77fc-106">An SPC used to actually sign code to be distributed to the public must be obtained from GTE, VeriSign, Inc., or another trusted [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="d77fc-107">**Cert2SPC** \*mycert \* \* *. CER* \*  *mycert \* \* *. SPC**</span><span class="sxs-lookup"><span data-stu-id="d77fc-107">**Cert2SPC** *MyCert\*\*\*.cer*\* *MyCert\*\*\*.spc*\*</span></span>

 

 
