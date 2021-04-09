---
title: Aufhebung der Registrierung durch iagent
description: Aufhebung der Registrierung durch iagent
ms.assetid: d81cde72-f9ff-45aa-9dbf-faea9a478c3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 796e033ac823ee7c79fe5312fab2c57dec36e694
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858248"
---
# <a name="iagentunregister"></a><span data-ttu-id="bc034-103">Iagent:: Unregister</span><span class="sxs-lookup"><span data-stu-id="bc034-103">IAgent::Unregister</span></span>

<span data-ttu-id="bc034-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="bc034-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Unregister(
   long dwSinkID  //notification sink ID
);
```

<span data-ttu-id="bc034-105">Entlädt die Zeichendaten für das angegebene Zeichen aus der [**Zeichen**](/windows/desktop/lwef/the-characters-object) Auflistung.</span><span class="sxs-lookup"><span data-stu-id="bc034-105">Unloads the character data for the specified character from the [**Characters**](/windows/desktop/lwef/the-characters-object) collection.</span></span>

-   <span data-ttu-id="bc034-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="bc034-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="bc034-107"><span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*dwsink ID*</span><span class="sxs-lookup"><span data-stu-id="bc034-107"><span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*dwSinkID*</span></span>
</dt> <dd>

<span data-ttu-id="bc034-108">Die ID der Benachrichtigungs Senke.</span><span class="sxs-lookup"><span data-stu-id="bc034-108">The notification sink ID.</span></span>

</dd> </dl>

<span data-ttu-id="bc034-109">Verwenden Sie diese Methode, wenn Sie die Microsoft-Agent-Dienste nicht mehr benötigen, z. b. wenn die Anwendung heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="bc034-109">Use this method when you no longer need Microsoft Agent services, such as when your application shuts down.</span></span>

## <a name="see-also"></a><span data-ttu-id="bc034-110">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bc034-110">See Also</span></span>

[<span data-ttu-id="bc034-111">**Iagent:: Register**</span><span class="sxs-lookup"><span data-stu-id="bc034-111">**IAgent::Register**</span></span>](iagent--register.md)


 

 