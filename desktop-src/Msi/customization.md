---
description: Da der Windows Installer alle Informationen zur Installation in einer relationalen Datenbank beibehält, kann die Installation einer Anwendung oder eines Produkts für bestimmte Benutzergruppen angepasst werden, indem Transformations Vorgänge auf das Paket angewendet werden.
ms.assetid: 98c5cda2-a01a-4bdd-840f-76c0ffacd194
title: Anpassung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5238cc145bc4a47bff459cb6caa30be37e1ca6ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346976"
---
# <a name="customization"></a><span data-ttu-id="5f5bb-103">Anpassung</span><span class="sxs-lookup"><span data-stu-id="5f5bb-103">Customization</span></span>

<span data-ttu-id="5f5bb-104">Da der Windows Installer alle Informationen zur Installation in einer relationalen Datenbank beibehält, kann die Installation einer Anwendung oder eines Produkts für bestimmte Benutzergruppen angepasst werden, indem Transformations Vorgänge auf das Paket angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f5bb-104">Because the Windows Installer keeps all information about the installation in a relational database, the installation of an application or product can be customized for particular user groups by applying transform operations to the package.</span></span> <span data-ttu-id="5f5bb-105">Transformationen können verwendet werden, um die verschiedenen Anpassungen eines Basispakets zu kapseln, das von unterschiedlichen Arbeitsgruppen benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="5f5bb-105">Transforms can be used to encapsulate the various customizations of a base package required by different workgroups.</span></span> <span data-ttu-id="5f5bb-106">Weitere Informationen finden Sie unter Zusammenführungen [und Transformationen](merges-and-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="5f5bb-106">For more information, see [Merges and Transforms](merges-and-transforms.md).</span></span>

<span data-ttu-id="5f5bb-107">Mehrere Transformationen eines Basispakets können während der Installation dynamisch angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="5f5bb-107">Multiple transforms of a base package can be applied on-the-fly during installation.</span></span> <span data-ttu-id="5f5bb-108">Dies bietet einen Mechanismus, mit dem benutzerdefinierte Installationen unterschiedlichen Benutzergruppen effizient zugewiesen werden können.</span><span class="sxs-lookup"><span data-stu-id="5f5bb-108">This provides a mechanism for efficiently assigning customized installations to different groups of users.</span></span> <span data-ttu-id="5f5bb-109">Dies wäre z. b. in Organisationen hilfreich, in denen die Support Abteilungen für Finanzabteilung und Personal verschiedene Installationen eines bestimmten Produkts benötigen.</span><span class="sxs-lookup"><span data-stu-id="5f5bb-109">For example, this would be useful in organizations where the finance and staff support departments require different installations of a particular product.</span></span> <span data-ttu-id="5f5bb-110">Das Produkt kann allen Benutzern in der Organisation durch eine [Administrative Installation](administrative-installation.md) des Basispakets an einen einzelnen administrativen Installations Punkt zur Verfügung gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5f5bb-110">The product can be made available to everyone in the organization by an [administrative installation](administrative-installation.md) of the base package to a single administrative installation point.</span></span> <span data-ttu-id="5f5bb-111">Jede Arbeitsgruppe kann dann automatisch Ihre geeignete Anpassung über eine dynamische Transformation erhalten, wenn Sie das Produkt installieren.</span><span class="sxs-lookup"><span data-stu-id="5f5bb-111">Each work group can then automatically receive their appropriate customization by means of an on-the-fly transform when they install the product.</span></span>

 

 



