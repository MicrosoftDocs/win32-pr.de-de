---
description: Cert2SPC
ms.assetid: d05df388-c19d-47a5-9ede-11cf06c29fc8
title: Cert2SPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1680f8fe426c2e3a62cac0674928a1520b402357
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106363903"
---
# <a name="cert2spc"></a><span data-ttu-id="9b9da-103">Cert2SPC</span><span class="sxs-lookup"><span data-stu-id="9b9da-103">Cert2SPC</span></span>

<span data-ttu-id="9b9da-104">Das Cert2SPC-Tool erstellt ein Test [*Software Publisher-Zertifikat*](../secgloss/s-gly.md) (SPC) mithilfe vorhandener [*X. 509*](../secgloss/x-gly.md) - [*Zertifikate*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="9b9da-104">The Cert2SPC tool creates a test [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) by using existing [*X.509*](../secgloss/x-gly.md) [*certificates*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="9b9da-105">Cert2SPC kann mehrere X. 509-Zertifikate in ein mit [*PKCS \# 7*](../secgloss/p-gly.md) signiertes signiertes Datenobjekt umschließen.</span><span class="sxs-lookup"><span data-stu-id="9b9da-105">Cert2SPC can wrap multiple X.509 certificates into a [*PKCS \#7*](../secgloss/p-gly.md) signed-data object.</span></span> <span data-ttu-id="9b9da-106">Das Tool wird im \\ Ordner bin des Installations Pfads des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="9b9da-106">The tool is installed in the \\Bin folder of the Microsoft Windows Software Development Kit (SDK) installation path.</span></span>

<span data-ttu-id="9b9da-107">Cert2SPC ist als Teil des Windows SDK verfügbar, das Sie von herunterladen können <https://go.microsoft.com/fwlink/p/?linkid=84091> .</span><span class="sxs-lookup"><span data-stu-id="9b9da-107">Cert2SPC is available as part of the Windows SDK, which you can download from <https://go.microsoft.com/fwlink/p/?linkid=84091>.</span></span>

> [!Note]
> <span data-ttu-id="9b9da-108">Dieses Tool ist nur für Testzwecke vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="9b9da-108">This tool is for test purposes only.</span></span> <span data-ttu-id="9b9da-109">Ein gültiges SPC wird von einer [*Zertifizierungs*](../secgloss/c-gly.md)Stelle abgerufen.</span><span class="sxs-lookup"><span data-stu-id="9b9da-109">A valid SPC is obtained from a [*certification authority*](../secgloss/c-gly.md).</span></span>


<span data-ttu-id="9b9da-110">**Cert2SPC** *Cert1. CER Cert2. CER* ...</span><span class="sxs-lookup"><span data-stu-id="9b9da-110">**Cert2SPC** *Cert1.cer Cert2.cer* …</span></span> <span data-ttu-id="9b9da-111">*Ausgabe. SPC*</span><span class="sxs-lookup"><span data-stu-id="9b9da-111">*Output.spc*</span></span>

 



|                         |                                                                                                                                    |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9b9da-112">*Cert1. CER Cert2. CER* ...</span><span class="sxs-lookup"><span data-stu-id="9b9da-112">*Cert1.cer Cert2.cer* …</span></span> | <span data-ttu-id="9b9da-113">Namen der X. 509-Zertifikate, die in das SPC eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9b9da-113">Names of the X.509 certificates to include in the SPC.</span></span> <span data-ttu-id="9b9da-114">Jeder Zertifikat Name endet mit der Erweiterung ". cer".</span><span class="sxs-lookup"><span data-stu-id="9b9da-114">Each certificate name ends with the .cer extension.</span></span>                         |
| <span data-ttu-id="9b9da-115">*Ausgabe. SPC*</span><span class="sxs-lookup"><span data-stu-id="9b9da-115">*Output.spc*</span></span>            | <span data-ttu-id="9b9da-116">Der Name des PKCS \# 7-Objekts, das die zu erstellenden X. 509-Zertifikate enthält.</span><span class="sxs-lookup"><span data-stu-id="9b9da-116">Name of the PKCS \#7 object that contains the X.509 certificates to be created.</span></span> <span data-ttu-id="9b9da-117">Der Name der Ausgabedatei endet mit der Erweiterung. SPC.</span><span class="sxs-lookup"><span data-stu-id="9b9da-117">The output file name ends with the .spc extension.</span></span> |



 

 

 
