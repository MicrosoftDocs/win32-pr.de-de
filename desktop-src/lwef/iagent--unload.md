---
title: Iagent entladen
description: Iagent entladen
ms.assetid: 560301b3-c038-4c6e-b3f1-1203b618b67d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc30d6c4c06c1d292a26a2f503477dcca651dd18
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104315050"
---
# <a name="iagentunload"></a><span data-ttu-id="93a74-103">Iagent:: entladen</span><span class="sxs-lookup"><span data-stu-id="93a74-103">IAgent::UnLoad</span></span>

<span data-ttu-id="93a74-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="93a74-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT UnLoad(
   long * dwCharID  //character ID
);
```

<span data-ttu-id="93a74-105">Entlädt die Zeichendaten für das angegebene Zeichen aus der [**Zeichen**](/windows/desktop/lwef/the-characters-object) Auflistung.</span><span class="sxs-lookup"><span data-stu-id="93a74-105">Unloads the character data for the specified character from the [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span>

-   <span data-ttu-id="93a74-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="93a74-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="93a74-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwcharid*</span><span class="sxs-lookup"><span data-stu-id="93a74-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="93a74-108">Die ID des Zeichens.</span><span class="sxs-lookup"><span data-stu-id="93a74-108">The character's ID.</span></span>

</dd> </dl>

<span data-ttu-id="93a74-109">Verwenden Sie diese Methode, wenn Sie kein Zeichen mehr benötigen, um Arbeitsspeicher freizugeben, der zum Speichern von Informationen über das Zeichen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="93a74-109">Use this method when you no longer need a character, to free up memory used to store information about the character.</span></span> <span data-ttu-id="93a74-110">Wenn Sie erneut auf das Zeichen zugreifen, verwenden Sie die [**Load**](load-method.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="93a74-110">If you access the character again, use the [**Load**](load-method.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="93a74-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="93a74-111">See Also</span></span>

[<span data-ttu-id="93a74-112">**Iagent:: Load**</span><span class="sxs-lookup"><span data-stu-id="93a74-112">**IAgent::Load**</span></span>](iagent--load.md)


 

 