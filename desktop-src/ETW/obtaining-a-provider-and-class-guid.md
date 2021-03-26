---
description: Zum Abrufen einer Anbieter-GUID oder einer Klassen-GUIDs für die Ereignis Ablauf Verfolgung können Sie die Uuidgen.exe oder das Guidgen.exe Tool verwenden.
ms.assetid: 07483a78-ee67-4586-a75b-d376aa3351b7
title: Abrufen eines Anbieters und einer Klassen-GUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c12554cdb39459d824bf6622cd9d50e52f8c788d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980112"
---
# <a name="obtaining-a-provider-and-class-guid"></a><span data-ttu-id="75af0-103">Abrufen eines Anbieters und einer Klassen-GUID</span><span class="sxs-lookup"><span data-stu-id="75af0-103">Obtaining a Provider and Class GUID</span></span>

<span data-ttu-id="75af0-104">Zum Abrufen einer Anbieter-GUID oder einer Klassen-GUIDs für die Ereignis Ablauf Verfolgung können Sie die Uuidgen.exe oder das Guidgen.exe Tool verwenden.</span><span class="sxs-lookup"><span data-stu-id="75af0-104">To obtain a provider GUID or event trace class GUIDs, you can use the Uuidgen.exe or Guidgen.exe tool.</span></span>

<span data-ttu-id="75af0-105">Wenn Sie das Uuidgen.exe Tool verwenden, verwenden Sie die Option-d, um ein \_ GUID C-Makro zu definieren, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="75af0-105">If you use the Uuidgen.exe tool, use the -d option to create a DEFINE\_GUID C macro, as shown in the following example.</span></span> <span data-ttu-id="75af0-106">Wenn Sie Informationen zur Verwendung des Uuidgen.exe Tools verwenden, verwenden Sie das-?</span><span class="sxs-lookup"><span data-stu-id="75af0-106">For information about using the Uuidgen.exe tool, use the -?</span></span> <span data-ttu-id="75af0-107">(Neuen Branch erstellen und Pull Request starten).</span><span class="sxs-lookup"><span data-stu-id="75af0-107">option.</span></span> <span data-ttu-id="75af0-108">Wenn Sie das \_ Makro GUID C definieren verwenden, um Ihre GUID zu definieren, müssen Sie die \# Definition Initguid vor ihren GUID-Definitionen einschließen, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="75af0-108">If you use the DEFINE\_GUID C macro to define your GUID, you must include \#define INITGUID before your GUID definitions, as shown in the following example.</span></span>

``` syntax
#define INITGUID

DEFINE_GUID (
  ProviderGuid,
  0xf4dc272d, 
  0x88dd, 
  0x4472, 
  0xa3, 0xb1, 0xcb, 0x6d, 0xa4, 0x86, 0xf0, 0xbe
  );
```

<span data-ttu-id="75af0-109">Das Microsoft Windows Software Development Kit (SDK) und Microsoft Visual Studio enthalten das Guidgen.exe Tool.</span><span class="sxs-lookup"><span data-stu-id="75af0-109">The Microsoft Windows Software Development Kit (SDK) and Microsoft Visual Studio include the Guidgen.exe tool.</span></span> <span data-ttu-id="75af0-110">Das Guidgen.exe Tool verfügt über eine Benutzeroberfläche, über die Sie aus verschiedenen Formaten auswählen können.</span><span class="sxs-lookup"><span data-stu-id="75af0-110">The Guidgen.exe tool has a user interface that lets you select from several formats.</span></span> <span data-ttu-id="75af0-111">Sie sollten das Format verwenden, das eine statische Konstante GUID erstellt, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="75af0-111">You should use the format that creates a static constant GUID, as shown in the following example.</span></span>

``` syntax
// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };
```

 

 



