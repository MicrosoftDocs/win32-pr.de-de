---
title: Iagentcommandsex getglobalvoicecommandsenabled
description: Iagentcommandsex getglobalvoicecommandsenabled
ms.assetid: 9c8fa978-a02b-4dfc-8cf7-e066c5b75122
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea7275bfe28190e06782cb2564dbf4868dd2c096
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390238"
---
# <a name="iagentcommandsexgetglobalvoicecommandsenabled"></a><span data-ttu-id="73ebc-103">Iagentcommandsex:: getglobalvoicecommandsenabled</span><span class="sxs-lookup"><span data-stu-id="73ebc-103">IAgentCommandsEx::GetGlobalVoiceCommandsEnabled</span></span>

<span data-ttu-id="73ebc-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="73ebc-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetGlobalVoiceCommandsEnabled(
   long * pbEnabled  // address of the global voice command setting
);
```

<span data-ttu-id="73ebc-105">Ruft ab, ob die Sprachgrammatik für die globalen Befehle des Agents aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="73ebc-105">Retrieves whether the voice grammar for Agent's global commands is enabled.</span></span>

-   <span data-ttu-id="73ebc-106">Gibt S \_ OK zurück, um anzugeben, dass der Vorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="73ebc-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="73ebc-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbenabled*</span><span class="sxs-lookup"><span data-stu-id="73ebc-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="73ebc-108">Die Adresse, die **true** erhält, wenn die Sprachgrammatik für die globalen Befehle des Agents aktiviert ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="73ebc-108">The address that receives **True** if the voice grammar for Agent's global commands is enabled, **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="73ebc-109">Der Microsoft-Agent fügt automatisch sprach Parameter (Grammatik) zum Öffnen und Schließen des Sprachbefehle Fensters und zum ein-und Ausblenden des Zeichens hinzu.</span><span class="sxs-lookup"><span data-stu-id="73ebc-109">Microsoft Agent automatically adds voice parameters (grammar) for opening and closing the Voice Commands Window and for showing and hiding the character.</span></span> <span data-ttu-id="73ebc-110">Wenn diese Methode **false** zurückgibt, sind alle sprach Parameter für diese Befehle sowie die sprach Parameter für die [**Beschriftung**](caption-property.md) der [**Befehls**](/windows/desktop/lwef/the-command-object) Objekte anderer Clients nicht in der Grammatik enthalten.</span><span class="sxs-lookup"><span data-stu-id="73ebc-110">When this method returns **False**, any voice parameters for these commands as well as the voice parameters for the [**Caption**](caption-property.md) of other clients' [**Command**](/windows/desktop/lwef/the-command-object) objects are not included in the grammar.</span></span> <span data-ttu-id="73ebc-111">Dies ermöglicht es Ihnen, diese aus der aktuellen aktiven Grammatik Ihres Clients auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="73ebc-111">This enables you to eliminate these from your client's current active grammar.</span></span> <span data-ttu-id="73ebc-112">Diese Einstellung gibt jedoch nicht an, wie diese Befehle in das Popup Menü des Zeichens eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="73ebc-112">However, this setting does not reflect the inclusion of these commands in the character's pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="73ebc-113">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="73ebc-113">See Also</span></span>

[<span data-ttu-id="73ebc-114">**Iagentcommandsex:: setglobalvoicecommandsenabled**</span><span class="sxs-lookup"><span data-stu-id="73ebc-114">**IAgentCommandsEx::SetGlobalVoiceCommandsEnabled**</span></span>](iagentcommandsex--setglobalvoicecommandsenabled.md)


 

 