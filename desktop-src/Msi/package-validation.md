---
description: Es wird dringend empfohlen, die Validierung für jedes neue oder neu geänderte Installationspaket auszuführen, bevor Sie versuchen, das Paket zum ersten Mal zu installieren.
ms.assetid: 47168c0b-82ab-4f1b-84d7-98c8f64d6da0
title: Paketvalidierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 058fbd5bff08701f9603938a631de4e8a59857d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864080"
---
# <a name="package-validation"></a><span data-ttu-id="032a5-103">Paketvalidierung</span><span class="sxs-lookup"><span data-stu-id="032a5-103">Package Validation</span></span>

<span data-ttu-id="032a5-104">Es wird dringend empfohlen, die Validierung für jedes neue oder neu geänderte Installationspaket auszuführen, bevor Sie versuchen, das Paket zum ersten Mal zu installieren.</span><span class="sxs-lookup"><span data-stu-id="032a5-104">It is strongly recommended that you run validation on every new or newly modified installation package before attempting to install the package for the first time.</span></span>

<span data-ttu-id="032a5-105">Die Paket Validierung umfasst die folgenden drei Prozesse:</span><span class="sxs-lookup"><span data-stu-id="032a5-105">Package validation includes the following three processes:</span></span>

-   [<span data-ttu-id="032a5-106">Interne Validierung</span><span class="sxs-lookup"><span data-stu-id="032a5-106">Internal Validation</span></span>](internal-validation.md)
-   [<span data-ttu-id="032a5-107">Zeichen folgen-Pool-Validierung</span><span class="sxs-lookup"><span data-stu-id="032a5-107">String-Pool Validation</span></span>](string-pool-validation.md)
-   [<span data-ttu-id="032a5-108">Interne Konsistenz Auswertung-ICES</span><span class="sxs-lookup"><span data-stu-id="032a5-108">Internal Consistency Evaluators - ICEs</span></span>](internal-consistency-evaluators-ices.md)

<span data-ttu-id="032a5-109">Mergemodule sollten mithilfe der in [Validieren von Mergemodulen](validating-merge-modules.md)beschriebenen Methode überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="032a5-109">Merge modules should be validated by using the method described in [Validating Merge Modules](validating-merge-modules.md).</span></span>

<span data-ttu-id="032a5-110">Evalcom2.dll stellt ein COM-Objekt bereit, das Validierungs Vorgänge für Installationspakete und Mergemodule implementiert.</span><span class="sxs-lookup"><span data-stu-id="032a5-110">Evalcom2.dll provides a COM object that implements validation operations for installation packages and merge modules.</span></span> <span data-ttu-id="032a5-111">Das Hauptobjekt implementiert Schnittstellen für C/C++-Programme.</span><span class="sxs-lookup"><span data-stu-id="032a5-111">The main object implements interfaces for C/C++ programs.</span></span> <span data-ttu-id="032a5-112">Weitere Informationen finden Sie unter [Validation Automation](validation-automation.md).</span><span class="sxs-lookup"><span data-stu-id="032a5-112">For more information, see [Validation Automation](validation-automation.md).</span></span>

 

 



