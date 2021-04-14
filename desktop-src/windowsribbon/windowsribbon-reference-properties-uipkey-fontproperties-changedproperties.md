---
title: UI_PKEY_FontProperties_ChangedProperties
description: Gibt die Benutzeroberflächen- \_ pkey \_ fontproperties \_ changedproperties-Eigenschaft an.
ms.assetid: d96b89b5-af30-4e76-b6ec-03fbb8d28ab3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124b36d5e24f4e0c0122cffdbbed11669a4ea510
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390769"
---
# <a name="ui_pkey_fontproperties_changedproperties"></a><span data-ttu-id="6b6b6-103">UI \_ pkey \_ fontproperties \_ changedproperties</span><span class="sxs-lookup"><span data-stu-id="6b6b6-103">UI\_PKEY\_FontProperties\_ChangedProperties</span></span>

<span data-ttu-id="6b6b6-104">Gibt die Benutzeroberflächen- \_ pkey \_ fontproperties \_ changedproperties-Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="6b6b6-104">Identifies the UI\_PKEY\_FontProperties\_ChangedProperties property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_ChangedProperties
   shellPKey = UI_PKEY_FontProperties_ChangedProperties
   formatID = 00000312-7363-696e-8441798acf5aebb7
   propID = 13
   typeInfo
      type = IUISimplePropertySet
```

## <a name="remarks"></a><span data-ttu-id="6b6b6-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b6b6-105">Remarks</span></span>

<span data-ttu-id="6b6b6-106">UI \_ pkey \_ fontproperties \_ changedproperties wird von einer Anwendung verwendet, um nur geänderte Eigenschaften aus [UI \_ pkey \_ fontproperties](windowsribbon-reference-properties-uipkey-fontproperties.md)abzufragen.</span><span class="sxs-lookup"><span data-stu-id="6b6b6-106">UI\_PKEY\_FontProperties\_ChangedProperties is used by an application to query only changed properties from [UI\_PKEY\_FontProperties](windowsribbon-reference-properties-uipkey-fontproperties.md).</span></span>

<span data-ttu-id="6b6b6-107">Beim Aufrufen der [**iuisimplepropertyset:: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) -Methode für dieses [**iuisimplepropertyset**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) -Objekt wird ein [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6b6b6-107">Calling the [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) method on this [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object returns an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

<span data-ttu-id="6b6b6-108">UI \_ pkey \_ fontproperties \_ changedproperties wird als letzter Parameter des [**iuicommandhandler:: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) -Aufrufes an die Menüband-Host Anwendung übergeben.</span><span class="sxs-lookup"><span data-stu-id="6b6b6-108">UI\_PKEY\_FontProperties\_ChangedProperties is passed as the last parameter of the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) call to the Ribbon host application.</span></span>

<span data-ttu-id="6b6b6-109">Dieser Eigenschafts Schlüssel ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6b6b6-109">This property key is read-only.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b6b6-110">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6b6b6-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b6b6-111">Schriftart Steuerelement-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6b6b6-111">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="6b6b6-112">**Iuisimplepropertyset**</span><span class="sxs-lookup"><span data-stu-id="6b6b6-112">**IUISimplePropertySet**</span></span>](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)
</dt> <dt>

[<span data-ttu-id="6b6b6-113">Schriftart-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="6b6b6-113">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 