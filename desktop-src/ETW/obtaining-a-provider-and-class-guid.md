---
description: Um eine Anbieter-GUID oder Ereignisablaufverfolgungsklassen-GUIDs abzurufen, können Sie das Uuidgen.exe- oder Guidgen.exe-Tool verwenden.
ms.assetid: 07483a78-ee67-4586-a75b-d376aa3351b7
title: Abrufen eines Anbieters und einer Klassen-GUID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c480a45a5a826d3f258ab267e39db87bc85fad799fef5d7397a7c900f4872f22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914350"
---
# <a name="obtaining-a-provider-and-class-guid"></a>Abrufen eines Anbieters und einer Klassen-GUID

Um eine Anbieter-GUID oder Ereignisablaufverfolgungsklassen-GUIDs abzurufen, können Sie das Uuidgen.exe- oder Guidgen.exe-Tool verwenden.

Wenn Sie das Uuidgen.exe-Tool verwenden, verwenden Sie die Option -d, um ein DEFINE \_ GUID C-Makro zu erstellen, wie im folgenden Beispiel gezeigt. Informationen zur Verwendung des Uuidgen.exe Tools finden Sie unter -? (Neuen Branch erstellen und Pull Request starten). Wenn Sie das \_ DEFINE GUID C-Makro verwenden, um Ihre GUID zu definieren, müssen Sie \# definieren INITGUID vor Ihren GUID-Definitionen einschließen, wie im folgenden Beispiel gezeigt.

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

Das Microsoft Windows Software Development Kit (SDK) und Microsoft Visual Studio das Guidgen.exe-Tool enthalten. Das Guidgen.exe-Tool verfügt über eine Benutzeroberfläche, über die Sie aus verschiedenen Formaten auswählen können. Sie sollten das Format verwenden, das eine statische Konstante-GUID erstellt, wie im folgenden Beispiel gezeigt.

``` syntax
// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };
```

 

 



