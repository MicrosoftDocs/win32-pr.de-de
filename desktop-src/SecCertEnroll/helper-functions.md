---
description: In den folgenden Abschnitten wird eine Funktion erläutert, die von Xenroll.dll exportiert wird. Außerdem wird in jedem Abschnitt erläutert, wie CertEnroll.dll verwendet wird, um die Funktion zu ersetzen, oder es wird angegeben, dass keine Zuordnung zwischen den beiden Bibliotheken besteht.
ms.assetid: 06d8dd6f-7a8d-4da5-a99d-9c9d8fb90cfa
title: Hilfsfunktionen (Zertifikatregistrierungs-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ee272e7b11c3fccf7975c5356302a2961b32ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347748"
---
# <a name="helper-functions-certificate-enrollment-api"></a><span data-ttu-id="3b4c4-104">Hilfsfunktionen (Zertifikatregistrierungs-API)</span><span class="sxs-lookup"><span data-stu-id="3b4c4-104">Helper Functions (Certificate Enrollment API)</span></span>

<span data-ttu-id="3b4c4-105">In den folgenden Abschnitten wird eine Funktion erläutert, die von Xenroll.dll exportiert wird.</span><span class="sxs-lookup"><span data-stu-id="3b4c4-105">Each of the following sections discusses a function exported by Xenroll.dll.</span></span> <span data-ttu-id="3b4c4-106">Außerdem wird in jedem Abschnitt erläutert, wie CertEnroll.dll verwendet wird, um die Funktion zu ersetzen, oder es wird angegeben, dass keine Zuordnung zwischen den beiden Bibliotheken besteht.</span><span class="sxs-lookup"><span data-stu-id="3b4c4-106">Each section also discusses how to use CertEnroll.dll to replace the function or indicates that no mapping between the two libraries exists.</span></span>

## <a name="binaryblobtostring"></a><span data-ttu-id="3b4c4-107">binaryblobto String</span><span class="sxs-lookup"><span data-stu-id="3b4c4-107">binaryBlobToString</span></span>

<span data-ttu-id="3b4c4-108">Die [**binaryblobdestring**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-binaryblobtostring) -Funktion in Xenroll.dll konvertiert ein Bytearray in eine Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="3b4c4-108">The [**binaryBlobToString**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-binaryblobtostring) function in Xenroll.dll converts a byte array to a string.</span></span>

<span data-ttu-id="3b4c4-109">Mithilfe CertEnroll.dll können Sie die [**variantbytearrayto String**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-variantbytearraytostring) -Methode für die [**ibinaryconverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) -Schnittstelle aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3b4c4-109">Using CertEnroll.dll, you can call the [**VariantByteArrayToString**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-variantbytearraytostring) method on the [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) interface.</span></span>

## <a name="stringtobinaryblob"></a><span data-ttu-id="3b4c4-110">stringdebinaryblob</span><span class="sxs-lookup"><span data-stu-id="3b4c4-110">stringToBinaryBlob</span></span>

<span data-ttu-id="3b4c4-111">Die [**stringdebinaryblob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-stringtobinaryblob) -Funktion in Xenroll.dll konvertiert eine Zeichenfolge in ein Bytearray.</span><span class="sxs-lookup"><span data-stu-id="3b4c4-111">The [**stringToBinaryBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-stringtobinaryblob) function in Xenroll.dll converts a string to a byte array.</span></span>

<span data-ttu-id="3b4c4-112">Mithilfe CertEnroll.dll können Sie die [**stringdevariantbytearray**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-stringtovariantbytearray) -Methode für die [**ibinaryconverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) -Schnittstelle aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3b4c4-112">Using CertEnroll.dll, you can call the [**StringToVariantByteArray**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-stringtovariantbytearray) method on the [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b4c4-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3b4c4-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b4c4-114">Zuordnung von Xenroll.dll zu CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="3b4c4-114">Mapping Xenroll.dll to CertEnroll.dll</span></span>](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[<span data-ttu-id="3b4c4-115">**Ibinaryconverter**</span><span class="sxs-lookup"><span data-stu-id="3b4c4-115">**IBinaryConverter**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)
</dt> </dl>

 

 
