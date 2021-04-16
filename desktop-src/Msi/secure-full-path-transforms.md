---
description: Bei Secure-Full-Path-Transformationen muss sich eine Quelle unter dem vollständigen Pfad befinden, der in der Transformationen-Eigenschaft angegeben ist.
ms.assetid: 9c1cd6c5-d246-49d8-a632-991274bb4511
title: Sichere vollständige Pfad Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8a60cf30beffe3831ed6489ea3827124ae319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530302"
---
# <a name="secure-full-path-transforms"></a><span data-ttu-id="7ee00-103">Sichere vollständige Pfad Transformationen</span><span class="sxs-lookup"><span data-stu-id="7ee00-103">Secure-Full-Path Transforms</span></span>

<span data-ttu-id="7ee00-104">Bei Secure-Full-Path-Transformationen muss sich eine Quelle unter dem vollständigen Pfad befinden, der in der [**Transformationen**](transforms.md) -Eigenschaft angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="7ee00-104">Secure-full-path transforms must have a source located at the full path specified in the [**TRANSFORMS**](transforms.md) property.</span></span> <span data-ttu-id="7ee00-105">Wenn das Paket installiert oder angekündigt wird, speichert das Installationsprogramm die Transformationen in einem Cache, in dem der Benutzer in einem sicheren Dateisystem keinen Schreibzugriff hat.</span><span class="sxs-lookup"><span data-stu-id="7ee00-105">When the package is installed or advertised, the installer saves the transforms in a cache where, on a secure file system, the user does not have write access.</span></span> <span data-ttu-id="7ee00-106">Wenn die lokale Kopie der Transformation nicht verfügbar ist, kann der Cache nur unter Verwendung des angegebenen Pfads wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7ee00-106">If the local copy of the transform becomes unavailable, it may only restore the cache using the specified path.</span></span> <span data-ttu-id="7ee00-107">Durch das Entfernen eines Produkts durch einen beliebigen Benutzer werden alle sicheren Transformationen für das Produkt auf dem Computer des Benutzers entfernt.</span><span class="sxs-lookup"><span data-stu-id="7ee00-107">The removal of a product by any user removes all secure transforms for that product from the user's computer.</span></span>

<span data-ttu-id="7ee00-108">Zum Anwenden von Transformationen für sichere vollständige Pfade bei der Installation eines Pakets legen Sie die [transformssecure-Richtlinie](transformssecure-policy.md) oder die [**transformssecure**](transformssecure.md) -Eigenschaft fest, oder legen Sie \| das erste Zeichen in der Transformations Liste an.</span><span class="sxs-lookup"><span data-stu-id="7ee00-108">To apply secure-full-paths transforms at the installation of a package, set the [TransformsSecure policy](transformssecure-policy.md) or the [**TRANSFORMSSECURE**](transformssecure.md) property or make \| the first character passed in the transform list.</span></span> <span data-ttu-id="7ee00-109">Die vollständigen Pfade zur Quelle der einzelnen Transformationen müssen in der Transformations Zeichenfolge übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="7ee00-109">The full paths to the source of each transform must be passed in the transforms string.</span></span> <span data-ttu-id="7ee00-110">Wenn in der Liste relative Pfade vorhanden sind, tritt bei der Installation ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="7ee00-110">If any relative paths are in the list, the installation fails.</span></span> <span data-ttu-id="7ee00-111">Die Transformations Quelle muss sich nicht mit der Quelle des Pakets befinden.</span><span class="sxs-lookup"><span data-stu-id="7ee00-111">The transform source does not have to be located with the source of the package.</span></span>

 

 



