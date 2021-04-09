---
description: Aus Sicherheitsgründen sind sichere Transformationen manchmal notwendig.
ms.assetid: c6019b28-b0a7-4104-9d78-b4b4228635b8
title: Gesicherte Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e498d6049a2c913ca78f12b6a8700a104af37c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869040"
---
# <a name="secured-transforms"></a><span data-ttu-id="cc4d9-103">Gesicherte Transformationen</span><span class="sxs-lookup"><span data-stu-id="cc4d9-103">Secured Transforms</span></span>

<span data-ttu-id="cc4d9-104">Aus Sicherheitsgründen sind sichere Transformationen manchmal notwendig.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-104">Secured transforms are sometimes necessary for security reasons.</span></span> <span data-ttu-id="cc4d9-105">Gesicherte Transformationen werden lokal auf dem Computer des Benutzers an einem Speicherort gespeichert, an dem der Benutzer auf einem sicheren Dateisystem keinen Schreibzugriff hat.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-105">Secured transforms are stored locally on the user's computer in a location where, on a secure file system, the user does not have write access.</span></span> <span data-ttu-id="cc4d9-106">Solche Transformationen werden an diesem Speicherort während der Installation oder Ankündigung des Pakets zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-106">Such transforms are cached in this location during the installation or advertisement of the package.</span></span> <span data-ttu-id="cc4d9-107">Nur Administratoren und das lokale System verfügen über Schreibzugriff auf diesen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-107">Only administrators and local system have write access to this location.</span></span> <span data-ttu-id="cc4d9-108">Ein Benutzer ohne Administratorrechte kann die Transformations Datei nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-108">A non-admin user would not be able to modify the transform file.</span></span> <span data-ttu-id="cc4d9-109">Bei einer nachfolgenden [Installation](installation-on-demand.md) oder [Wartung](maintenance-installation.md) des Pakets verwendet das Installationsprogramm die zwischengespeicherten Transformationen.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-109">During subsequent [installation-on-demand](installation-on-demand.md) or [maintenance installations](maintenance-installation.md) of the package, the installer uses the cached transforms.</span></span>

<span data-ttu-id="cc4d9-110">Legen Sie zum Angeben von sicherem Transformations Speicher die [transformssecure-Richtlinie](transformssecure-policy.md)fest, legen Sie die [**transformssecure**](transformssecure.md) -Eigenschaft fest, oder übergeben Sie das Symbol @ oder \| in der Liste Transformationen.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-110">To specify secured transform storage, set the [TransformsSecure policy](transformssecure-policy.md), set the [**TRANSFORMSSECURE**](transformssecure.md) property, or pass the @ or \| symbol in the transforms list.</span></span> <span data-ttu-id="cc4d9-111">Beachten Sie, dass Sie keine gesicherten und ungesicherten Transformationen in dieselbe Transformations Liste einschließen können.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-111">Note that you cannot include secured and unsecured transforms in the same transforms list.</span></span> <span data-ttu-id="cc4d9-112">Siehe [Anwenden von Transformationen](applying-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="cc4d9-112">See [Applying Transforms](applying-transforms.md).</span></span>

<span data-ttu-id="cc4d9-113">Durch das Entfernen des Produkts durch einen beliebigen Benutzer werden alle gesicherten Transformationen für das Produkt auf dem Computer des Benutzers entfernt.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-113">The removal of the product by any user removes all secured transforms for that product from the user's computer.</span></span>

<span data-ttu-id="cc4d9-114">Wenn das Installationsprogramm feststellt, dass eine gesicherte Transformation nicht lokal verfügbar ist, wird versucht, den Transformations Cache aus einer Quelle wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-114">If the installer finds that a secured transform is not locally available, it then attempts to restore the transform cache from a source.</span></span> <span data-ttu-id="cc4d9-115">Sichere Transformationen können eine sichere Quelle oder ein sicherer vollständiger Pfad sein:</span><span class="sxs-lookup"><span data-stu-id="cc4d9-115">Secure transforms can be secure-at-source or secure-full-path:</span></span>

-   <span data-ttu-id="cc4d9-116">Aus dem lokalen Transformations Cache fehlende [Secure-at-Source-Transformationen](secure-at-source-transforms.md) werden aus dem Stamm der Quelle der MSI-Datei wieder hergestellt.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-116">[Secure-at-source transforms](secure-at-source-transforms.md) that are missing from the local transform cache are restored from the root of the source of the .msi file.</span></span>
-   <span data-ttu-id="cc4d9-117">[Sichere vollständige Pfad Transformationen](secure-full-path-transforms.md) , die im lokalen Transformations Cache fehlen, werden vom ursprünglichen vollständigen Pfad wieder hergestellt, der durch die Liste der Transformationen angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cc4d9-117">[Secure-full-path transforms](secure-full-path-transforms.md) that are missing from the local transform cache are restored from the original full path specified by the transforms list.</span></span>

 

 



