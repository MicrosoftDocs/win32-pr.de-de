---
description: Der Datenstrom für Zusammenfassungs Informationen enthält Informationen über das Paket, das über Microsoft Windows-Explorer angezeigt werden kann.
ms.assetid: b909955f-ddd6-4cf1-8e86-fcf89be80b41
title: Informationen zum Datenstrom für Zusammenfassungs Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ab931d7f9b6dd726fc6df3d7b805f4cc5c25caa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131509"
---
# <a name="about-the-summary-information-stream"></a><span data-ttu-id="5bb7c-103">Informationen zum Datenstrom für Zusammenfassungs Informationen</span><span class="sxs-lookup"><span data-stu-id="5bb7c-103">About the Summary Information Stream</span></span>

<span data-ttu-id="5bb7c-104">Der Datenstrom für Zusammenfassungs Informationen enthält Informationen über das Paket, das über Microsoft Windows-Explorer angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5bb7c-104">The summary information stream contains information about the package that can be viewed through Microsoft Windows Explorer.</span></span> <span data-ttu-id="5bb7c-105">Diese Informationen sind über die **IStream** -Schnittstelle zugänglich.</span><span class="sxs-lookup"><span data-stu-id="5bb7c-105">This information is accessible through the **IStream** interface.</span></span> <span data-ttu-id="5bb7c-106">Der Autor muss die Werte für jede dieser Eigenschaften angeben.</span><span class="sxs-lookup"><span data-stu-id="5bb7c-106">It is up to the author to provide the values for each of these properties.</span></span>

<span data-ttu-id="5bb7c-107">Der Zusammenfassungs Datenstrom verwendet com, um eine strukturierte Speicherung von Datenbanken bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="5bb7c-107">The summary information stream uses COM to provide structured storage of databases.</span></span> <span data-ttu-id="5bb7c-108">COM unterstützt das Konzept des strukturierten Speichers, der über die **IStream** -Schnittstelle zugänglich ist.</span><span class="sxs-lookup"><span data-stu-id="5bb7c-108">COM supports the concept of structured storage accessible through the **IStream** interface.</span></span> <span data-ttu-id="5bb7c-109">Die strukturierte Speicherung unterstützt wiederum das Konzept der Eigenschaften Sätze als flexible Methode für die Serialisierung von fast allen Informationen.</span><span class="sxs-lookup"><span data-stu-id="5bb7c-109">Structured storage, in turn, supports the concept of property sets as a flexible method for serializing almost any information.</span></span> <span data-ttu-id="5bb7c-110">Die com-Spezifikation definiert einen einzelnen Standardeigenschaften Satz, zusammenfassende Informationen, der verwendet wird, um die von Windows-Explorer sichtbaren Eigenschaften Blätter aufzufüllen.</span><span class="sxs-lookup"><span data-stu-id="5bb7c-110">The COM specification defines a single standard property set, summary information, which is used to populate property sheets viewable from Windows Explorer.</span></span> <span data-ttu-id="5bb7c-111">Daher können die im Zusammenfassungs Datenstrom gespeicherten Informationen von Benutzern angezeigt werden, wenn Sie mit der rechten Maustaste auf eine Installerdatenbank oder eine Transformation klicken und [Eigenschaften](about-properties.md)auswählen.</span><span class="sxs-lookup"><span data-stu-id="5bb7c-111">So, information stored in the summary information stream can be viewed by users when they right-click an installer database or transform and select [Properties](about-properties.md).</span></span>

<span data-ttu-id="5bb7c-112">Eine Liste der Zusammenfassungs Eigenschaften Satzes finden Sie unter [Summary Information Stream-Eigenschaften Satz](summary-information-stream-property-set.md).</span><span class="sxs-lookup"><span data-stu-id="5bb7c-112">For a list of the summary property set see [Summary Information Stream Property Set](summary-information-stream-property-set.md).</span></span>

<span data-ttu-id="5bb7c-113">Eine kurze Beschreibung der Eigenschaften der Zusammenfassungs Informationen, die mit Datenbanken, Transformationen und Patches verwendet werden, finden Sie unter [Summary Property-Beschreibungen](summary-property-descriptions.md).</span><span class="sxs-lookup"><span data-stu-id="5bb7c-113">For brief descriptions of the Summary Information properties used with databases, transforms, and patches, see [Summary Property Descriptions](summary-property-descriptions.md).</span></span>

 

 



