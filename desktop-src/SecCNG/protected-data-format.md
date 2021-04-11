---
description: Geschützte Daten werden als ASN. 1-codiertes BLOB gespeichert.
ms.assetid: 8E287A1F-4EDF-4068-85F7-59A1D73F7BCD
title: Geschütztes Daten Format
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bafa230efd704536e9e30b946e5fbf2d403e664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131300"
---
# <a name="protected-data-format"></a><span data-ttu-id="321d7-103">Geschütztes Daten Format</span><span class="sxs-lookup"><span data-stu-id="321d7-103">Protected Data Format</span></span>

<span data-ttu-id="321d7-104">Geschützte Daten werden als ASN. 1-codiertes BLOB gespeichert.</span><span class="sxs-lookup"><span data-stu-id="321d7-104">Protected data is stored as an ASN.1 encoded BLOB.</span></span> <span data-ttu-id="321d7-105">Die Daten werden als CMS-Inhalte (Certificate Message Syntax) formatiert.</span><span class="sxs-lookup"><span data-stu-id="321d7-105">The data is formatted as CMS (certificate message syntax) enveloped content.</span></span> <span data-ttu-id="321d7-106">Der digitale Umschlag enthält verschlüsselte Inhalte, Empfängerinformationen, die einen verschlüsselten Inhalts Verschlüsselungsschlüssel (CEK) enthalten, und einen Header, der Informationen über den Inhalt enthält, einschließlich der unverschlüsselten Schutz Deskriptor-Regel Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="321d7-106">The digital envelope contains encrypted content, recipient information that contains an encrypted content encryption key (CEK), and a header that contains information about the content, including the unencrypted protection descriptor rule string.</span></span> <span data-ttu-id="321d7-107">Dies wird im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="321d7-107">This is shown by the following diagram.</span></span>

![geschützte eingehüllte Daten](images/protecteddatablob.png)

## <a name="related-topics"></a><span data-ttu-id="321d7-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="321d7-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="321d7-110">CNG-DPAPI</span><span class="sxs-lookup"><span data-stu-id="321d7-110">CNG DPAPI</span></span>](cng-dpapi.md)
</dt> <dt>

[<span data-ttu-id="321d7-111">Schutz Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="321d7-111">Protection Descriptors</span></span>](protection-descriptors.md)
</dt> <dt>

[<span data-ttu-id="321d7-112">Schutz Anbieter</span><span class="sxs-lookup"><span data-stu-id="321d7-112">Protection Providers</span></span>](protection-providers.md)
</dt> </dl>

 

 



