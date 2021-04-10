---
title: DefaultIcon
description: Stellt Standard Symbol Informationen für die ikonischen Präsentationen von Objekten bereit.
ms.assetid: 45a3289b-d9c4-4857-bf48-1fd664ce4430
keywords:
- DefaultIcon-Registrierungsschlüssel com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0079fb02f4429c1939f54d643e0a6b08fbc90eb
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039661"
---
# <a name="defaulticon"></a><span data-ttu-id="c49c5-104">DefaultIcon</span><span class="sxs-lookup"><span data-stu-id="c49c5-104">DefaultIcon</span></span>

<span data-ttu-id="c49c5-105">Stellt Standard Symbol Informationen für die ikonischen Präsentationen von Objekten bereit.</span><span class="sxs-lookup"><span data-stu-id="c49c5-105">Provides default icon information for iconic presentations of objects.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="c49c5-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="c49c5-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      DefaultIcon = path, resourceID
```

## <a name="remarks"></a><span data-ttu-id="c49c5-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c49c5-107">Remarks</span></span>

<span data-ttu-id="c49c5-108">Dies ist ein **reg \_ SZ** -Wert, der den vollständigen Pfad zum Namen der Objekt Anwendung und den Ressourcen Index des Symbols in der ausführbaren Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="c49c5-108">This is a **REG\_SZ** value that specifies the full path to the executable name of the object application and the resource index of the icon within the executable.</span></span>

<span data-ttu-id="c49c5-109">**DefaultIcon** identifiziert das Symbol, das verwendet werden soll, wenn beispielsweise ein-Steuerelement auf ein Symbol minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="c49c5-109">**DefaultIcon** identifies the icon to use when, for example, a control is minimized to an icon.</span></span> <span data-ttu-id="c49c5-110">Dieser Eintrag enthält den vollständigen Pfad des ausführbaren namens der Serveranwendung und den Ressourcen Index des Symbols in der ausführbaren Datei.</span><span class="sxs-lookup"><span data-stu-id="c49c5-110">This entry contains the full path to the executable name of the server application and the resource index of the icon within the executable.</span></span> <span data-ttu-id="c49c5-111">Anwendungen können die von **DefaultIcon** bereitgestellten Informationen verwenden, um ein Symbol Handle mit [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona)abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c49c5-111">Applications can use the information provided by **DefaultIcon** to obtain an icon handle with [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona).</span></span>

 

 