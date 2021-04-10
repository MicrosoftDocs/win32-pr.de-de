---
description: Bei der Transformation für sichere Quellen muss sich eine Quelle im Stammverzeichnis der Quelle für das Paket befinden.
ms.assetid: b5355053-9922-444f-a117-f6af461ef9e9
title: Secure-at-Source-Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec59d551489fa1699c20c24d09b7ecbff99f8ca4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869043"
---
# <a name="secure-at-source-transforms"></a><span data-ttu-id="2f6ac-103">Secure-at-Source-Transformationen</span><span class="sxs-lookup"><span data-stu-id="2f6ac-103">Secure-At-Source Transforms</span></span>

<span data-ttu-id="2f6ac-104">Bei der Transformation für sichere Quellen muss sich eine Quelle im Stammverzeichnis der Quelle für das Paket befinden.</span><span class="sxs-lookup"><span data-stu-id="2f6ac-104">Secure-at-source transforms must have a source located at the root of the source for the package.</span></span> <span data-ttu-id="2f6ac-105">Wenn das Paket installiert oder angekündigt wird, speichert das Installationsprogramm die Transformationen in einem Cache, in dem der Benutzer in einem sicheren Dateisystem keinen Schreibzugriff hat.</span><span class="sxs-lookup"><span data-stu-id="2f6ac-105">When the package is installed or advertised, the installer saves the transforms in a cache where, on a secure file system, the user does not have write access.</span></span> <span data-ttu-id="2f6ac-106">Wenn die lokale Kopie der Transformation nicht verfügbar ist, sucht der Installer nach einer Quelle, um den Cache wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="2f6ac-106">If the local copy of the transform becomes unavailable, the installer searches for a source to restore the cache.</span></span> <span data-ttu-id="2f6ac-107">Die-Methode ist identisch mit dem Durchsuchen der Quell Liste nach einer MSI-Datei.</span><span class="sxs-lookup"><span data-stu-id="2f6ac-107">The method is the same as searching the source list for an .msi file.</span></span> <span data-ttu-id="2f6ac-108">Weitere Informationen finden Sie unter [Quellen Resilienz](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="2f6ac-108">For more information, see [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="2f6ac-109">Durch das Entfernen eines Produkts durch einen beliebigen Benutzer werden alle sicheren Transformationen für das Produkt auf dem Computer des Benutzers entfernt.</span><span class="sxs-lookup"><span data-stu-id="2f6ac-109">The removal of a product by any user removes all secure transforms for that product from the user's computer.</span></span>

<span data-ttu-id="2f6ac-110">Wenn Sie bei der Installation eines Pakets sichere at-Source-Transformationen anwenden möchten, legen Sie die [transformssecure-Richtlinie](transformssecure-policy.md) oder die [**transformssecure**](transformssecure.md) -Eigenschaft fest, oder geben Sie @ das erste Zeichen an, das in der Transformations Liste übergangen wird.</span><span class="sxs-lookup"><span data-stu-id="2f6ac-110">To apply secure-at-source transforms at the installation of a package, set the [TransformsSecure policy](transformssecure-policy.md) or the [**TRANSFORMSSECURE**](transformssecure.md) property, or make @ the first character passed in the transform list.</span></span> <span data-ttu-id="2f6ac-111">Jede Transformation muss durch einen Dateinamen angegeben werden und muss sich im Stammverzeichnis der Quelle für das Paket befinden.</span><span class="sxs-lookup"><span data-stu-id="2f6ac-111">Each transform must be indicated by a file name and must be located at the root of the source for the package.</span></span> <span data-ttu-id="2f6ac-112">Wenn sich eine der Transformationen nicht im Stammverzeichnis der Paketquelle befindet, tritt bei der Installation ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="2f6ac-112">If any of the transforms are not located at the root of the package source, the installation fails.</span></span> <span data-ttu-id="2f6ac-113">Weitere Informationen finden Sie unter [Anwenden von Transformationen](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="2f6ac-113">For more information, see [Applying Transforms](applying-transforms.md).</span></span>

 

 



