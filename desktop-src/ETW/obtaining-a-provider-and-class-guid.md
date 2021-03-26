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
# <a name="obtaining-a-provider-and-class-guid"></a>Abrufen eines Anbieters und einer Klassen-GUID

Zum Abrufen einer Anbieter-GUID oder einer Klassen-GUIDs für die Ereignis Ablauf Verfolgung können Sie die Uuidgen.exe oder das Guidgen.exe Tool verwenden.

Wenn Sie das Uuidgen.exe Tool verwenden, verwenden Sie die Option-d, um ein \_ GUID C-Makro zu definieren, wie im folgenden Beispiel gezeigt. Wenn Sie Informationen zur Verwendung des Uuidgen.exe Tools verwenden, verwenden Sie das-? (Neuen Branch erstellen und Pull Request starten). Wenn Sie das \_ Makro GUID C definieren verwenden, um Ihre GUID zu definieren, müssen Sie die \# Definition Initguid vor ihren GUID-Definitionen einschließen, wie im folgenden Beispiel gezeigt.

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

Das Microsoft Windows Software Development Kit (SDK) und Microsoft Visual Studio enthalten das Guidgen.exe Tool. Das Guidgen.exe Tool verfügt über eine Benutzeroberfläche, über die Sie aus verschiedenen Formaten auswählen können. Sie sollten das Format verwenden, das eine statische Konstante GUID erstellt, wie im folgenden Beispiel gezeigt.

``` syntax
// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };
```

 

 



