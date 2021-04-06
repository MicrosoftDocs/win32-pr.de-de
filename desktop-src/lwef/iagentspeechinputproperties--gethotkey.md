---
title: Iagentspeechinputproperties GetHotKey
description: Iagentspeechinputproperties GetHotKey
ms.assetid: b93e5b46-b8f8-4ca4-8417-7626b97d8928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e672b26f97cfbe92bc71d0ceab165e100c3ecf92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036227"
---
# <a name="iagentspeechinputpropertiesgethotkey"></a><span data-ttu-id="21f1f-103">Iagentspeechinputproperties:: GetHotKey</span><span class="sxs-lookup"><span data-stu-id="21f1f-103">IAgentSpeechInputProperties::GetHotKey</span></span>

<span data-ttu-id="21f1f-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="21f1f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHotKey(
BSTR * pbszHotCharKey  // address of variable for listening key 
);                        
```

<span data-ttu-id="21f1f-105">Ruft die aktuelle Tastatur Zuweisung für den Schlüssel für die Spracheingabe Überwachung ab.</span><span class="sxs-lookup"><span data-stu-id="21f1f-105">Retrieves the current keyboard assignment for the speech input Listening key.</span></span>

-   <span data-ttu-id="21f1f-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="21f1f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="21f1f-107"><span id="pbszHotCharKey"></span><span id="pbszhotcharkey"></span><span id="PBSZHOTCHARKEY"></span>*pbszhotcharkey*</span><span class="sxs-lookup"><span data-stu-id="21f1f-107"><span id="pbszHotCharKey"></span><span id="pbszhotcharkey"></span><span id="PBSZHOTCHARKEY"></span>*pbszHotCharKey*</span></span>
</dt> <dd>

<span data-ttu-id="21f1f-108">Adresse eines BSTR, das die aktuelle Hotkey-Einstellung empfängt, mit der der Audiokanal für die Spracheingabe geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="21f1f-108">Address of a BSTR that receives the current hotkey setting used to open the audio channel for speech input.</span></span>

</dd> </dl>

<span data-ttu-id="21f1f-109">Wenn [**GetEnabled**](iagentspeechinputproperties--getenabled.md) **false** zurückgibt, löst eine Abfrage dieser Einstellung einen Fehler aus.</span><span class="sxs-lookup"><span data-stu-id="21f1f-109">If [**GetEnabled**](iagentspeechinputproperties--getenabled.md) returns **False**, querying this setting raises an error.</span></span>

## <a name="see-also"></a><span data-ttu-id="21f1f-110">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="21f1f-110">See Also</span></span>

[<span data-ttu-id="21f1f-111">**Iagentspeechinputproperties:: GetEnabled**</span><span class="sxs-lookup"><span data-stu-id="21f1f-111">**IAgentSpeechInputProperties::GetEnabled**</span></span>](iagentspeechinputproperties--getenabled.md)


 

 




