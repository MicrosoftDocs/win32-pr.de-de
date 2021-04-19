---
title: Iagentspeechinputproperties getlisteningtip
description: Iagentspeechinputproperties getlisteningtip
ms.assetid: b0488a54-03f8-43ce-935c-dd49c6ed5dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91218fb7935edb68458d540a8f35fe5402b317ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339176"
---
# <a name="iagentspeechinputpropertiesgetlisteningtip"></a><span data-ttu-id="528dc-103">Iagentspeechinputproperties:: getlisteningtip</span><span class="sxs-lookup"><span data-stu-id="528dc-103">IAgentSpeechInputProperties::GetListeningTip</span></span>

<span data-ttu-id="528dc-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="528dc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetListeningTip(
long * pbListeningTip  // address of variable for listening tip flag
);                       
```

<span data-ttu-id="528dc-105">Ruft einen Wert ab, der angibt, ob der Abhör Tipp für die Anzeige aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="528dc-105">Retrieves a value indicating whether the Listening Tip is enabled for display.</span></span>

-   <span data-ttu-id="528dc-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="528dc-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="528dc-107"><span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*pblisteningtip*</span><span class="sxs-lookup"><span data-stu-id="528dc-107"><span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*pbListeningTip*</span></span>
</dt> <dd>

<span data-ttu-id="528dc-108">Die Adresse einer Variablen, die **true** empfängt, wenn der lausch Tipp für die Anzeige aktiviert ist, oder **false** , wenn der lauschyme deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="528dc-108">Address of a variable that receives **True** if the Listening Tip is enabled for display, or **False** if the Listening Tip is disabled.</span></span>

</dd> </dl>

<span data-ttu-id="528dc-109">Wenn [**GetEnabled**](iagentspeechinputproperties--getenabled.md) **false** zurückgibt, gibt die Abfrage von anderen Spracheingabe Eigenschaften einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="528dc-109">If [**GetEnabled**](iagentspeechinputproperties--getenabled.md) returns **False**, querying any other speech input properties returns an error.</span></span>

## <a name="see-also"></a><span data-ttu-id="528dc-110">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="528dc-110">See Also</span></span>

[<span data-ttu-id="528dc-111">**Iagentspeechinputproperties:: GetEnabled**</span><span class="sxs-lookup"><span data-stu-id="528dc-111">**IAgentSpeechInputProperties::GetEnabled**</span></span>](iagentspeechinputproperties--getenabled.md)


 

 




