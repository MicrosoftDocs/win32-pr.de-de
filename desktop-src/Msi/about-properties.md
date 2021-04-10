---
description: Windows Installer können die Software Installation konfigurieren, indem Sie die Werte der Variablen verwenden, die in einem Installationspaket oder vom Benutzer definiert sind.
ms.assetid: b7b715e7-e92c-4b84-b60d-a0ff8412749b
title: Informationen zu Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dc5d8154533cfebf4163983a149a547372ef4a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215734"
---
# <a name="about-properties"></a><span data-ttu-id="1ecf4-103">Informationen zu Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ecf4-103">About Properties</span></span>

<span data-ttu-id="1ecf4-104">Windows Installer können die Software Installation konfigurieren, indem Sie die Werte der Variablen verwenden, die in einem Installationspaket oder vom Benutzer definiert sind.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-104">Windows Installer can configure software installation by using the values of variables defined in an installation package or by the user.</span></span>

<span data-ttu-id="1ecf4-105">Windows Installer verwendet während einer Installation drei Kategorien globaler Variablen:</span><span class="sxs-lookup"><span data-stu-id="1ecf4-105">Windows Installer uses three categories of global variables during an installation:</span></span>

-   <span data-ttu-id="1ecf4-106">Private Eigenschaften: das Installationsprogramm verwendet intern private Eigenschaften, und ihre Werte müssen in der Installations Datenbank erstellt oder auf von der Betriebsumgebung festgelegte Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-106">Private properties: The installer uses private properties internally and their values must be authored into the installation database or set to values determined by the operating environment.</span></span>
-   <span data-ttu-id="1ecf4-107">Öffentliche Eigenschaften: öffentliche Eigenschaften können in der Datenbank erstellt und durch einen Benutzer-oder Systemadministrator in der Befehlszeile geändert werden, durch Anwenden einer Transformation oder durch Interaktion mit einer erstellten Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-107">Public properties: Public properties can be authored into the database and changed by a user or system administrator on the command line, by applying a transform, or by interacting with an authored user interface.</span></span>
-   <span data-ttu-id="1ecf4-108">Eingeschränkte öffentliche Eigenschaften: aus Sicherheitsgründen kann der Autor eines Installationspakets die öffentlichen Eigenschaften einschränken, die ein Benutzer ändern kann.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-108">Restricted public properties: For security purposes, the author of an installation package can restrict the public properties a user can change.</span></span>

<span data-ttu-id="1ecf4-109">Nicht alle Eigenschaften müssen in jedem Paket definiert werden. es gibt einen kleinen Satz von erforderlichen Eigenschaften, die in jedem Paket definiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-109">Not all properties need to be defined in every package, there is a small set of required properties that must be defined in every package.</span></span> <span data-ttu-id="1ecf4-110">Der Installer legt die Werte von Eigenschaften in einer bestimmten Rangfolge fest.</span><span class="sxs-lookup"><span data-stu-id="1ecf4-110">The installer sets the values of properties in a particular order of precedence.</span></span>

[<span data-ttu-id="1ecf4-111">Private Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ecf4-111">Private Properties</span></span>](private-properties.md)

[<span data-ttu-id="1ecf4-112">Öffentliche Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ecf4-112">Public Properties</span></span>](public-properties.md)

[<span data-ttu-id="1ecf4-113">Eingeschränkte öffentliche Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ecf4-113">Restricted Public Properties</span></span>](restricted-public-properties.md)

[<span data-ttu-id="1ecf4-114">Erforderliche Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ecf4-114">Required Properties</span></span>](required-properties.md)

[<span data-ttu-id="1ecf4-115">Reihenfolge der Eigenschafts Rangfolge</span><span class="sxs-lookup"><span data-stu-id="1ecf4-115">Order of Property Precedence</span></span>](order-of-property-precedence.md)

## <a name="related-topics"></a><span data-ttu-id="1ecf4-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1ecf4-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ecf4-117">Verwenden von Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1ecf4-117">Using Properties</span></span>](using-properties.md)
</dt> <dt>

[<span data-ttu-id="1ecf4-118">Eigenschafts Verweis</span><span class="sxs-lookup"><span data-stu-id="1ecf4-118">Property Reference</span></span>](property-reference.md)
</dt> </dl>

 

 



