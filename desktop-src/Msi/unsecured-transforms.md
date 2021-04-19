---
description: Bei Transformationen, die nicht gesichert wurden, wie in gesicherte Transformationen beschrieben, handelt es sich standardmäßig um unsichere Transformationen.
ms.assetid: feace6c3-7828-44d0-8d2b-482a02e8e0c0
title: Unsichere Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6743898142197d87d4e3fef5d0f48778f6261ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352790"
---
# <a name="unsecured-transforms"></a><span data-ttu-id="5a5a8-103">Unsichere Transformationen</span><span class="sxs-lookup"><span data-stu-id="5a5a8-103">Unsecured Transforms</span></span>

<span data-ttu-id="5a5a8-104">Bei Transformationen, die nicht gesichert wurden, wie in [gesicherte Transformationen](secured-transforms.md) beschrieben, handelt es sich standardmäßig um unsichere Transformationen.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-104">Transforms that have not been secured as described in [Secured Transforms](secured-transforms.md) are unsecured transforms by default.</span></span>

<span data-ttu-id="5a5a8-105">Wenn Sie bei der Installation eines Pakets eine unsichere Transformation anwenden möchten, übergeben Sie die Transformations Dateinamen in der [**Transformationen**](transforms.md) -Eigenschaft oder der Befehlszeilen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-105">To apply an unsecured transform when installing a package, pass the transform file names in the [**TRANSFORMS**](transforms.md) property or command line string.</span></span> <span data-ttu-id="5a5a8-106">Beginnen Sie die Zeichenfolge nicht mit @ oder \| Zeichen, oder legen Sie die [transformssecure-Richtlinie](transformssecure-policy.md) oder die [**transformssecure**](transformssecure.md) -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-106">Do not begin the string with the @ or \| characters or set the [TransformsSecure policy](transformssecure-policy.md) or the [**TRANSFORMSSECURE**](transformssecure.md) property.</span></span> <span data-ttu-id="5a5a8-107">Beachten Sie, dass Sie unsichere Transformationen und [gesicherte Transformationen](secured-transforms.md) nicht in derselben Transformations Liste kombinieren können.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-107">Note that you cannot combine unsecured transforms and [secured transforms](secured-transforms.md) in the same transforms list.</span></span>

<span data-ttu-id="5a5a8-108">Wenn das Paket im [Installations Kontext](installation-context.md)pro Benutzer installiert oder angekündigt wird und ungesicherte Transformationen aufweist, speichert das Installationsprogramm die Transformations Quelle im Ordner Anwendungsdaten im Profil des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-108">If the package is installed or advertised in the per-user [installation context](installation-context.md), and has unsecured transforms, the installer saves the transform source in the Application Data folder in the user's profile.</span></span> <span data-ttu-id="5a5a8-109">Dadurch kann ein Benutzer seine Anpassung eines Produkts während der Umstellung zwischen Computern beibehalten.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-109">This enables a user to maintain their customization of a product while moving between computers.</span></span>

<span data-ttu-id="5a5a8-110">Wenn das Paket im [Installations Kontext](installation-context.md)pro Computer installiert oder angekündigt wird und ungesicherte Transformationen verwendet, speichert das Installationsprogramm die Transformations Quelle im Ordner "% windir% \\ Installer".</span><span class="sxs-lookup"><span data-stu-id="5a5a8-110">If the package is installed or advertised in the per-machine [installation context](installation-context.md), and uses unsecured transforms, the installer saves the transform source in the %windir%\\Installer folder.</span></span>

<span data-ttu-id="5a5a8-111">Während der erstmaligen Installation des Pakets sucht der Installer zuerst nach der Transformation an der Quelle, die von der [**Transformationen**](transforms.md) -Eigenschaft oder der Befehlszeilen Zeichenfolge bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-111">During a first-time installation of the package, the installer first searches for the transform at the source supplied by the [**TRANSFORMS**](transforms.md) property or command line string.</span></span> <span data-ttu-id="5a5a8-112">Wenn diese Quelle nicht verfügbar ist, sucht das Installationsprogramm an der Quelle des Pakets neben der MSI-Datei nach der Transformation.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-112">If this source is unavailable, the installer then searches for the transform at the source of the package next to the .msi file.</span></span>

<span data-ttu-id="5a5a8-113">Während einer [Wartungs Installation](maintenance-installation.md)sucht das Installationsprogramm am Cache Speicherort nach der Transformation.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-113">During a [maintenance installation](maintenance-installation.md), the installer searches for the transform at the cache location.</span></span> <span data-ttu-id="5a5a8-114">Wenn die zwischengespeicherte Kopie der Transformation nicht verfügbar ist, sucht das Installationsprogramm an der Quelle des Pakets neben der MSI-Datei nach der Transformation.</span><span class="sxs-lookup"><span data-stu-id="5a5a8-114">If the cached copy of the transform becomes unavailable, the installer searches for the transform at the source of the package next to the .msi file.</span></span>

<span data-ttu-id="5a5a8-115">Weitere Informationen finden Sie unter [Anwenden von Transformationen](applying-transforms.md) und [Quellen Resilienz](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="5a5a8-115">For more information, see [Applying Transforms](applying-transforms.md) and [Source Resiliency](source-resiliency.md).</span></span>

 

 



