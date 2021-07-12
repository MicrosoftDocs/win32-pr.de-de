---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 419f0e6dc6f1183252f138029dadc7817ac3b5ed
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581978"
---
# <a name="cert2spc"></a><span data-ttu-id="62ad7-103">Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="62ad7-103">Cert2SPC</span></span>

<span data-ttu-id="62ad7-104">Das Cert2SPC-Tool erstellt mithilfe vorhandener [*X.509-Zertifikate*](../secgloss/x-gly.md) [](../secgloss/c-gly.md)ein [*Test-SPC (Software Publisher Certificate).*](../secgloss/s-gly.md)</span><span class="sxs-lookup"><span data-stu-id="62ad7-104">The Cert2SPC tool creates a test [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) by using existing [*X.509*](../secgloss/x-gly.md) [*certificates*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="62ad7-105">Cert2SPC kann mehrere X.509-Zertifikate in ein [*PKCS \# 7-Datenobjekt*](../secgloss/p-gly.md) mit Vorzeichen umschließen.</span><span class="sxs-lookup"><span data-stu-id="62ad7-105">Cert2SPC can wrap multiple X.509 certificates into a [*PKCS \#7*](../secgloss/p-gly.md) signed-data object.</span></span> <span data-ttu-id="62ad7-106">Das Tool wird im \\ Ordner Bin des Installationspfads des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="62ad7-106">The tool is installed in the \\Bin folder of the Microsoft Windows Software Development Kit (SDK) installation path.</span></span>

<span data-ttu-id="62ad7-107">Cert2SPC ist als Teil des Windows SDK verfügbar, das Sie unter herunterladen <https://go.microsoft.com/fwlink/p/?linkid=84091> können.</span><span class="sxs-lookup"><span data-stu-id="62ad7-107">Cert2SPC is available as part of the Windows SDK, which you can download from <https://go.microsoft.com/fwlink/p/?linkid=84091>.</span></span>

> [!Note]
> <span data-ttu-id="62ad7-108">Dieses Tool dient nur zu Testzwecken.</span><span class="sxs-lookup"><span data-stu-id="62ad7-108">This tool is for test purposes only.</span></span> <span data-ttu-id="62ad7-109">Ein gültiges SPC wird von einer [*Zertifizierungsstelle*](../secgloss/c-gly.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="62ad7-109">A valid SPC is obtained from a [*certification authority*](../secgloss/c-gly.md).</span></span>


<span data-ttu-id="62ad7-110">**Cert2SPC** *Cert1.cer Cert2.cer* ...</span><span class="sxs-lookup"><span data-stu-id="62ad7-110">**Cert2SPC** *Cert1.cer Cert2.cer* …</span></span> <span data-ttu-id="62ad7-111">*Output.spc*</span><span class="sxs-lookup"><span data-stu-id="62ad7-111">*Output.spc*</span></span>

 



| <span data-ttu-id="62ad7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="62ad7-112">Parameters</span></span>              | <span data-ttu-id="62ad7-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62ad7-113">Description</span></span>                                                                                                                        |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62ad7-114">*Cert1.cer Cert2.cer* ...</span><span class="sxs-lookup"><span data-stu-id="62ad7-114">*Cert1.cer Cert2.cer* …</span></span> | <span data-ttu-id="62ad7-115">Namen der X.509-Zertifikate, die in das SPC aufgenommen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="62ad7-115">Names of the X.509 certificates to include in the SPC.</span></span> <span data-ttu-id="62ad7-116">Jeder Zertifikatname endet mit der ERWEITERUNG CER.</span><span class="sxs-lookup"><span data-stu-id="62ad7-116">Each certificate name ends with the .cer extension.</span></span>                         |
| <span data-ttu-id="62ad7-117">*Output.spc*</span><span class="sxs-lookup"><span data-stu-id="62ad7-117">*Output.spc*</span></span>            | <span data-ttu-id="62ad7-118">Name des PKCS \# 7-Objekts, das die zu erstellenden X.509-Zertifikate enthält.</span><span class="sxs-lookup"><span data-stu-id="62ad7-118">Name of the PKCS \#7 object that contains the X.509 certificates to be created.</span></span> <span data-ttu-id="62ad7-119">Der Name der Ausgabedatei endet mit der Erweiterung .spc.</span><span class="sxs-lookup"><span data-stu-id="62ad7-119">The output file name ends with the .spc extension.</span></span> |



 

 

 
